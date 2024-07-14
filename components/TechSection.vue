<script setup lang="ts"></script>

<template>
  <section id="tech">
    <div
      class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-green-border-green-600 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-green-border-green-600 py-4"
    >
      <h6 class="text-large sm:text-xl md:text-2xl">Technologies I use.</h6>
      <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">some of which I am really <span class="poppins text-primary">good</span> at.</h3>
    </div>

    <section class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14">
      <div class="text-center flex flex-col h-full poppins font-semibold text-balance mt-6 md:mt-0">
        <h4 class="text-2xl mb-4">Programming Languages</h4>
        <ul class="list-none grid grid-cols-1 sm:grid-cols-2 gap-4">
          <li class="flex flex-col items-center bg-gray-800 p-4 rounded-lg">
            <img src="/cpp.png" alt="JavaScript" class="w-20 h-20" />
            <span class="text-primary mt-2">C++</span>
          </li>
          <li class="flex flex-col items-center bg-gray-800 p-4 rounded-lg">
            <img src="/javascript-logo.png" alt="JavaScript" class="w-20 h-20" />
            <span class="text-primary mt-2">JavaScript</span>
          </li>
          <li class="flex flex-col items-center bg-gray-800 p-4 rounded-lg">
            <img src="https://cdn.iconscout.com/icon/free/png-256/free-java-60-1174953.png?f=webp&w=256" alt="TypeScript" class="w-20 h-20" />
            <span class="text-primary mt-2">Java</span>
          </li>
          <li class="flex flex-col items-center bg-gray-800 p-4 rounded-lg">
            <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/c/c3/Python-logo-notext.svg/935px-Python-logo-notext.svg.png" alt="Python" class="w-20 h-20" />
            <span class="text-primary mt-2">Python</span>
          </li>
          <li class="flex flex-col items-center bg-gray-800 p-4 rounded-lg">
            <img src="https://go.dev/blog/go-brand/Go-Logo/PNG/Go-Logo_Blue.png" alt="Go" class="w-20 h-20" />
            <span class="text-primary mt-2">Go</span>
          </li>
          <li class="flex flex-col items-center bg-gray-800 p-4 rounded-lg">
            <img src="https://static-00.iconduck.com/assets.00/php-icon-256x256-oq5bc0bt.png" alt="PHP" class="w-20 h-20" />
            <span class="text-primary mt-2">PHP</span>
          </li>
        </ul>
      </div>
      <div class="text-center flex flex-col h-full poppins font-semibold text-balance mt-6 md:mt-0">
        <h4 class="text-2xl mb-4">Libraries/Frameworks</h4>
        <ul class="list-none grid grid-cols-1 sm:grid-cols-2 gap-4">
          <li class="flex flex-col items-center bg-gray-800 p-4 rounded-lg">
            <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/9a/Laravel.svg/1969px-Laravel.svg.png" alt="Laravel" class="w-20 h-20" />
            <span class="text-primary mt-2">Laravel</span>
          </li>
          <li class="flex flex-col items-center bg-gray-800 p-4 rounded-lg">
            <img src="https://nuxt.com/assets/design-kit/icon-green.svg" alt="Laravel" class="w-20 h-20" />
            <span class="text-primary mt-2">Nuxt</span>
          </li>
          <li class="flex flex-col items-center bg-gray-800 p-4 rounded-lg">
            <img src="/vue.png" alt="Vue.js" class="w-20 h-20" />
            <span class="text-primary mt-2">Vue</span>
          </li>
          <li class="flex flex-col items-center bg-gray-800 p-4 rounded-lg">
            <img src="https://cdn.hashnode.com/res/hashnode/image/upload/v1632979765809/HTEigfQR-.png?auto=compress,format&format=webp" alt="React" class="w-20 h-20" />
            <span class="text-primary mt-2">Tailwind</span>
          </li>
          <li class="flex flex-col items-center bg-gray-800 p-4 rounded-lg">
            <img
              src="https://media.dev.to/cdn-cgi/image/width=800%2Cheight=%2Cfit=scale-down%2Cgravity=auto%2Cformat=auto/https%3A%2F%2Fdev-to-uploads.s3.amazonaws.com%2Fuploads%2Farticles%2Fm3l6zijyz7y7fcq6mc1j.png"
              alt="React"
              class="w-20 h-20"
            />
            <span class="text-primary mt-2">Elysia.js</span>
          </li>
        </ul>
      </div>
    </section>

    <div class="md:grid md:grid-cols gap-8 items-center py-8">
      <div class="text-center flex flex-col h-full poppins font-semibold text-balance mt-6 md:mt-0"></div>
    </div>
  </section>
</template>
