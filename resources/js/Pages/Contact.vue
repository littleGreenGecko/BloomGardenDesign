<template>

  <Head title="Welcome" />
<body>
    <header class="text-gray-600 body-font">
      <!-- Company Name and Logo -->
        <div class="container-fluid mx-auto flex flex-wrap p-5 flex-col md:flex-row items-center"> 
            <div class="flex flex-col md:flex-row title-font items-center text-gray-700">                 
                <img src="images/bloom_tree.png" alt="" width="90" height="90" /> 
                <span class="ml-1 text-gray-700 text-4xl lg:text-5xl">BLOOM</span>                               
                <span class="ml-3 text-gray-700 text-sm md:text-xl">GARDEN DESIGN</span> 
            </div>     
            <!-- Log In and Register Links -->
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

            <!-- Main Navigation Links -->
            <nav class="container-fluid mx-auto flex flex-wrap p-5 flex-col md:flex-row md:ml-auto md:mr-auto justify-center text-gray-100 bg-gray-700 items-center text-lg md:text-xl tracking-wide md:tracking-widest lg:justify-evenly lg:text-2xl">                 
                <Link class="mx-auto lg:mx-14 hover:underline" href="/">home</Link>
                <Link class="mx-auto lg:mx-14 hover:underline" href="/about">about</Link>
                <Link class="mx-auto lg:mx-14 hover:underline" href="/portfolio">portfolio</Link>
                <Link class="mx-auto lg:mx-14 hover:underline" href="/contact">contact</Link>
            </nav> 
            
            <!-- Contact Info-->
            <div class="container-fluid px-5 pt-16 mx-auto">
   <div class="flex flex-col grid grid-cols-1 justify-items-center text-center w-full md:grid-cols-2">
    <img src="images/contactImg/watercolour_4.jpg" alt="garden image" class="img-fluid" width="600" height="500" />        
<div class="container-fluid mx-auto p-7 text-gray-700 bg-neutral-50 text-center my-4 md:text-lg md:my-0 md:ml-5 md:mr-0 md:px-0 md:pt-0 md:leading-relaxed lg:mx-0 lg:w-3/4">    
    <h1 class="text-2xl font-medium title-font my-4 text-gray-600 md:mb-10 md:mt-16">CONTACT US</h1>  
<p class="md:px-3 lg:mx-6">If you would like to find out more, please phone or email us and our team will be delighted to respond to you as soon as possible.</p>
<br><br><br>
<p><strong>Telephone</strong></p>
<a href="#">020 7350 2318</a>
<br><br><br>
<p><strong>Email</strong></p>
<a href="mailto:info@blum.co.uk" target="_blank" class="text-green-700 hover:underline">info@blum.co.uk</a>
<br><br><br>
<p><strong>Address</strong></p>
<p>8 Happy Rd, Cardiff, CF10 3NQ</p>
<br><br>
<p><strong>Follow Us</strong></p>
<!-- Social Media Links -->
<span class="inline-flex space-x-3 justify-center md:mb-16">
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
</div>
  </div> 
                <footer class="text-gray-500 body-font md:mt-96">
                <!-- Copyrights -->
  <div class="container-fluid mx-auto flex flex-wrap mb-5 pt-6 flex-col md:flex-row md:justify-between md:px-5 md:items-center md:mb-9">   
    <p class="mx-auto text-sm md:mx-0">© Copyright 2022 The Bloom      
    </p>   
  </div>
</footer>
</body>
</template>

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