
<template>
    <Head title="Welcome" />
<body>
    <header class="text-gray-600 body-font">
        <div class="container-fluid mx-auto flex flex-wrap p-5 flex-col md:flex-row items-center"> 
            <div class="flex flex-col md:flex-row title-font items-center text-gray-900 mb-4 md:mb-0">                 
                <img src="images/bloom_tree.png" alt="" width="90" height="90" /> 
                <span class="ml-1 text-gray-700 text-4xl lg:text-5xl">BLOOM</span>                               
                <span class="ml-3 text-gray-700 text-sm md:text-xl">GARDEN DESIGN</span> 
            </div>     

            <div class="flex items-center text-base text-green-700 md:ml-auto md:mr-2">           
            <Link                
            v-if="$page.props.user"
                :href="route('dashboard')"
                class="hover:underline"
            >
                Dashboard
            </Link>

            <template v-else>
                <Link :href="route('login')" class="hover:underline">
                    Log in
                </Link>

                <Link
                    v-if="canRegister"
                    :href="route('register')"
                    class="ml-4 hover:underline"
                >
                    Register
                </Link>
            </template>
            </div>            
        </div> 
    </header>

            <nav class="container-fluid mx-auto flex flex-wrap p-5 flex-col md:flex-row md:ml-auto md:mr-auto justify-center text-gray-100 bg-gray-700 items-center text-lg md:text-xl tracking-wide md:tracking-widest">                 
                <Link class="mx-auto lg:mx-14 hover:underline" href="/">home</Link>
                <Link class="mx-auto lg:mx-14 hover:underline" href="/about">about</Link>
                <Link class="mx-auto lg:mx-14 hover:underline" href="/portfolio">portfolio</Link>
                <Link class="mx-auto lg:mx-14 hover:underline" href="/contact">contact</Link>
            </nav> 
            <div class="container-fluid mx-auto items-center flex flex wrap flex-col md:justify-center lg:flex-row lg:space-x-12 lg:mt-14 lg:justify-evenly">
                <img src="images/watercolour_1.jpg" alt="" class="img-fluid" width="500" height="400" />
                <img src="images/watercolour_2.jpg" alt="" class="img-fluid" width="500" height="400" />
                <img src="images/watercolour_3.jpg" alt="" class="img-fluid" width="500" height="400" />                 
            </div>

           <div class="container-fluid mx-auto p-7 text-gray-700  bg-neutral-50 text-lg text-center mt-4 md:text-xl md:my-9 md:mx-5 md:px-0 md:leading-relaxed">
            <p>AWARD-WINNING GARDEN DESIGN, BUILD AND MAINTENANCE. <br><br>
               We will bring experience, artistry and discipline to your projects across the UK, from country gardens and city refuges to ground-breaking commercial spaces.</p>
            </div>

    <footer class="text-gray-600 body-font">
  <div class="container-fluid mx-auto flex flex-wrap mt-5 pt-6 flex-col md:flex-row md:justify-between md:px-5 md:items-center md:mb-9">   
    <p class="mx-auto text-sm md:mx-0">© Copyright 2022 The Bloom      
    </p>
    <span class="inline-flex space-x-3 mt-4 mb-9 justify-center md:my-0">
      <a>
        <svg fill="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" class="w-5 h-5" viewBox="0 0 24 24">
          <path d="M18 2h-3a5 5 0 00-5 5v3H7v4h3v8h4v-8h3l1-4h-4V7a1 1 0 011-1h3z"></path>
        </svg>
      </a>
      <a>
        <svg fill="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" class="w-5 h-5" viewBox="0 0 24 24">
          <path d="M23 3a10.9 10.9 0 01-3.14 1.53 4.48 4.48 0 00-7.86 3v1A10.66 10.66 0 013 4s-4 9 5 13a11.64 11.64 0 01-7 2c9 5 20 0 20-11.5a4.5 4.5 0 00-.08-.83A7.72 7.72 0 0023 3z"></path>
        </svg>
      </a>
      <a>
        <svg fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" class="w-5 h-5" viewBox="0 0 24 24">
          <rect width="20" height="20" x="2" y="2" rx="5" ry="5"></rect>
          <path d="M16 11.37A4 4 0 1112.63 8 4 4 0 0116 11.37zm1.5-4.87h.01"></path>
        </svg>
      </a>
      <a>
        <svg fill="currentColor" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="0" class="w-5 h-5" viewBox="0 0 24 24">
          <path stroke="none" d="M16 8a6 6 0 016 6v7h-4v-7a2 2 0 00-2-2 2 2 0 00-2 2v7h-4v-7a6 6 0 016-6zM2 9h4v12H2z"></path>
          <circle cx="4" cy="4" r="2" stroke="none"></circle>
        </svg>
      </a>
    </span>
  </div>
</footer>
</body>
</template>

<style scoped>
.text-gray-600 {
  color: #718096;
  color: rgba(113, 128, 150, var(--tw-text-opacity));
}

.text-gray-700 {
  color: #4a5568;
  color: rgba(74, 85, 104, var(--tw-text-opacity));
}

.text-gray-900 {
  color: #1a202c;
  color: rgba(26, 32, 44, var(--tw-text-opacity));
}
</style>

<script>
import { defineComponent } from "vue";
import { Head, Link } from "@inertiajs/inertia-vue3";

export default defineComponent({
  components: {
    Head,
    Link,
  },

  props: {
    canLogin: Boolean,
    canRegister: Boolean,
    laravelVersion: String,
    phpVersion: String,
  },
});
</script>
