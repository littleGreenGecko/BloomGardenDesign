
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

<!-- About Info -->
<div class="container px-5 pt-16 mx-auto">
<div class="flex flex-col text-center w-full lg:mt-14">
      <h1 class="text-2xl font-medium title-font mb-4 text-gray-600">ABOUT US</h1>    
<div class="container-fluid mx-auto p-7 text-gray-700 bg-neutral-50 text-center mt-4 md:text-lg md:my-9 md:mx-5 md:px-0 md:leading-relaxed lg:mx-0">
<p class="md:px-3">We are a values-driven, award-winning landscape design practice. We work on a range of projects across the UK encompassing high-end residential, public, historic and commercial spaces. 
Understanding the spirit of the place is central to our approach, using vernacular materials, nearby nurseries and local craftspeople, so that the garden speaks of and is connected to its broader setting.</p>
</div>
</div>
</div>

<!-- Team Photos-->
<div>
 <section class="text-gray-600 body-font">
  <div class="container px-5 py-20 mx-auto">
    <div class="flex flex-col text-center w-full mb-20">
      <h1 class="text-2xl font-medium title-font mb-4 text-gray-600">OUR TEAM</h1>      
    </div>
    <div class="flex flex-wrap -m-4">
      <div class="p-4 lg:w-1/4 md:w-1/2">
        <div class="h-full flex flex-col items-center text-center">
          <img alt="team" class="flex-shrink-0 w-full h-100 object-cover object-center mb-4" src="images/teamPhotos/Caroline Damson-Managing Director.jpg">
          <div class="w-full">
            <h2 class="title-font font-medium text-lg text-gray-700">Caroline Damson</h2>
            <h3 class="text-gray-500 mb-3">Managing Director</h3>            
          </div>
        </div>
        </div>
        <div class="p-4 lg:w-1/4 md:w-1/2">
        <div class="h-full flex flex-col items-center text-center">
          <img alt="team" class="flex-shrink-0 w-full h-100 object-cover object-center mb-4" src="images/teamPhotos/Amy Concorde-Communications (2).jpg">
          <div class="w-full">
            <h2 class="title-font font-medium text-lg text-gray-700">Amy Concorde</h2>
            <h3 class="text-gray-500 mb-3">Communications</h3>            
          </div>
        </div>
        </div>      
      <div class="p-4 lg:w-1/4 md:w-1/2">
        <div class="h-full flex flex-col items-center text-center">
          <img alt="team" class="flex-shrink-0 w-full h-100 object-cover object-center mb-4" src="images/teamPhotos/Ivy Sunburst-Operations Manager (2).jpg">
          <div class="w-full">
            <h2 class="title-font font-medium text-lg text-gray-700">Ivy Sunburst</h2>
            <h3 class="text-gray-500 mb-3">Operations Manager</h3>            
          </div>
        </div>
        </div>
        <div class="p-4 lg:w-1/4 md:w-1/2">
        <div class="h-full flex flex-col items-center text-center">
          <img alt="team" class="flex-shrink-0 w-full h-100 object-cover object-center mb-4" src="images/teamPhotos/Sam Conference-Lead Designer.jpg">
          <div class="w-full">
            <h2 class="title-font font-medium text-lg text-gray-700">Sam Conference</h2>
            <h3 class="text-gray-500 mb-3">Lead Designer</h3>            
          </div>
        </div>
        </div>
        <div class="p-4 lg:w-1/4 md:w-1/2">
        <div class="h-full flex flex-col items-center text-center">
          <img alt="team" class="flex-shrink-0 w-full h-100 object-cover object-center mb-4" src="images/teamPhotos/Lisa Bramley-Senior Designer (2).jpg">
          <div class="w-full">
            <h2 class="title-font font-medium text-lg text-gray-700">Lisa Bramley</h2>
            <h3 class="text-gray-500 mb-3">Senior Designer</h3>            
          </div>
        </div>
        </div>
        <div class="p-4 lg:w-1/4 md:w-1/2">
        <div class="h-full flex flex-col items-center text-center">
          <img alt="team" class="flex-shrink-0 w-full h-100 object-cover object-center mb-4" src="images/teamPhotos/Luke Rochester-Studio Manager.jpg">
          <div class="w-full">
            <h2 class="title-font font-medium text-lg text-gray-700">Luke Rochester</h2>
            <h3 class="text-gray-500 mb-3">Studio Manager</h3>            
          </div>
        </div>
        </div>
        <div class="p-4 lg:w-1/4 md:w-1/2">
        <div class="h-full flex flex-col items-center text-center">
          <img alt="team" class="flex-shrink-0 w-full h-100 object-cover object-center mb-4" src="images/teamPhotos/Laura Morello-Landscape Architect (2).jpg">
          <div class="w-full">
            <h2 class="title-font font-medium text-lg text-gray-700">Laura Morello</h2>
            <h3 class="text-gray-500 mb-3">Landscape Architect</h3>            
          </div>
        </div>
        </div>
      <div class="p-4 lg:w-1/4 md:w-1/2">
        <div class="h-full flex flex-col items-center text-center">
          <img alt="team" class="flex-shrink-0 w-full h-100 object-cover object-center mb-4" src="images/teamPhotos/Katie Goldcot-Project Manager.jpg">
          <div class="w-full">
            <h2 class="title-font font-medium text-lg text-gray-700">Katie Goldcot</h2>
            <h3 class="text-gray-500 mb-3">Project Manager</h3>          
          </div>
        </div>
      </div>
      <div class="p-4 lg:w-1/4 md:w-1/2">
        <div class="h-full flex flex-col items-center text-center">
          <img alt="team" class="flex-shrink-0 w-full h-100 object-cover object-center mb-4" src="images/teamPhotos/Philip Williams-General Maintenance Manager.jpg">
          <div class="w-full">
            <h2 class="title-font font-medium text-lg text-gray-700">Philip Williams</h2>
            <h3 class="text-gray-500 mb-3">General Maintenance Manager</h3>           
          </div>
        </div>
      </div>
      <div class="p-4 lg:w-1/4 md:w-1/2">
        <div class="h-full flex flex-col items-center text-center">
          <img alt="team" class="flex-shrink-0 w-full h-100 object-cover object-center mb-4" src="images/teamPhotos/Paul Cox-Maintenance Manager.jpg">
          <div class="w-full">
            <h2 class="title-font font-medium text-lg text-gray-700">Paul Cox</h2>
            <h3 class="text-gray-500 mb-3">Maintenance Manager</h3>            
          </div>
        </div>
      </div>
    </div>
  </div>
</section> 
</div> 
<footer class="text-gray-500 body-font">
      <!-- Copyrights -->
  <div class="container-fluid mx-auto flex flex-wrap mt-5 pt-6 flex-col md:flex-row md:justify-between md:px-5 md:items-center md:mb-9">   
    <p class="mx-auto text-sm md:mx-0">© Copyright 2022 The Bloom      
    </p>
    
    <!-- Social Media Links -->
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







