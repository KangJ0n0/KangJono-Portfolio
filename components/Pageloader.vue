<template>
  <div v-if="isLoading" id="loading-page" :style="{ opacity: pageControl.opacity }">
    <div id="loading">
      <div id="loading-text">
        <div class="text">.</div>
        <div class="text">.</div>
        <div class="text">.</div>
      </div>
      <div id="loading-progress">
        <div class="progress">
          <div class="bar" :style="progressBar"></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, reactive, onMounted, defineProps, defineEmits } from "vue";

const props = defineProps({
  progressBarSpeed: {
    type: Number,
    default: 0.1,
  },
  progressBarColor: {
    type: String,
    default: "black",
  },
});
const emit = defineEmits(["closeHandler"]);
const isLoading = ref(true);

const progressBar = reactive({
  width: "0%",
  background: "black",
});

const pageControl = reactive({
  opacity: 1,
});

function startProgressBar() {
  let num = 0;
  let timer = setInterval(() => {
    num += 1;
    progressBar.width = num + "%";
    if (num > 100) {
      clearInterval(timer);
      closePage();
      emit("closeHandler");
    }
  }, props.progressBarSpeed);
}
function closePage() {
  pageControl.opacity = 0;
  setTimeout(() => {
    isLoading.value = false;
  }, 500); // Match this with the transition duration
}
onMounted(() => {
  progressBar.background = props.progressBarColor;
  startProgressBar();
});
</script>

<style lang="sass" scoped>
#loading-page
  position: fixed
  top: 0
  left: 0
  height: 100%
  width: 100%
  background-color: #eee
  display: flex
  justify-content: center
  align-items: center
  transition: opacity 0.5s
  z-index: 1
#loading-text
  font-family: sans-serif, Comic Sans MS
  display: flex
  justify-content: center
  align-items: center
  position: relative
  .text
    font-size: 90px
    animation: loading 0.9s infinite alternate
    &:nth-child(2)
      animation-delay: 0.1s
    &:nth-child(3)
      animation-delay: 0.2s
    &:nth-child(4)
      animation-delay: 0.3s

#loading-progress
  height: 30px
  width: 100%
  display: flex
  justify-content: center
  align-items: center
  .progress
    height: 10px
    border-radius: 5px
    box-shadow: 5px 2px 5px rgba(0,0,0,0.1)
    width: 80%
    position: relative
    .bar
      position: absolute
      width: 0%
      height: 100%
      border-radius: 5px
      background-color: black
@keyframes loading
  0%
    transform: translateY(0px)
  100%
    transform: translateY(-30px)
</style>
