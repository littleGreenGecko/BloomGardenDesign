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
            <nav class="container-fluid mx-auto flex flex-wrap p-5 flex-col md:flex-row md:ml-auto md:mr-auto justify-center text-gray-100 bg-gray-700 items-center text-lg md:text-xl tracking-wide md:tracking-widest">                 
                <Link class="mx-auto lg:mx-14 hover:underline" href="/">home</Link>
                <Link class="mx-auto lg:mx-14 hover:underline" href="/about">about</Link>
                <Link class="mx-auto lg:mx-14 hover:underline" href="/portfolio">portfolio</Link>
                <Link class="mx-auto lg:mx-14 hover:underline" href="/contact">contact</Link>
            </nav>            

<!-- Project Photos and Info -->
            <section class="text-gray-600 body-font">
  <div class="container px-5 pt-16 mx-auto">
   <div class="flex flex-col text-center w-full">
      <h1 class="text-2xl font-medium title-font mb-4 text-gray-600">OUR PROJECTS</h1>    
<div class="container-fluid mx-auto p-7 text-gray-700 bg-neutral-50 text-center my-4 md:text-lg md:my-9 md:mx-5 md:px-0 md:leading-relaxed lg:mx-0">
<p class="md:px-3">We see our projects as creative collaborations between the homeowner, our team and nature itself. We’ll work to bring your vision to life, whether that’s to create an extension of your home, an outdoor adventure or a living work of art.</p>
</div>
</div>
    <div class="flex flex-wrap -m-4">
      <div class="lg:w-1/3 md:w-1/2 p-4">
        <div class="flex relative">
          <img alt="projects" class="absolute inset-0 w-full h-60 object-cover object-center" src="images/projectPhotos/portfolio-1.jpg">
          <div class="px-4 py-3 relative z-10 w-full h-60 border-4 border-gray-200 bg-white opacity-0 hover:opacity-100">
            <h2 class="tracking-widest text-sm title-font font-medium text-indigo-500 mb-1">Wimbledon</h2>
            <h1 class="title-font text-lg font-medium text-gray-900 mb-3">Luxury Garden</h1>
            <p class="leading-relaxed">This garden is a real feast for the eyes, where scale and colour make an instant impact.</p>
          </div>
        </div>
      </div>
      <div class="lg:w-1/3 md:w-1/2 p-4">
        <div class="flex relative">
          <img alt="projects" class="absolute inset-0 w-full h-60 object-cover object-center" src="images/projectPhotos/portfolio-2.jpg">
          <div class="px-4 py-3 relative z-10 w-full h-60 border-4 border-gray-200 bg-white opacity-0 hover:opacity-100">
            <h2 class="tracking-widest text-sm title-font font-medium text-indigo-500 mb-1">Kensington</h2>
            <h1 class="title-font text-lg font-medium text-gray-900 mb-3">Family Garden</h1>
            <p class="leading-relaxed">A large, family back garden in London, re-designed as part of an overall house redevelopment.</p>
          </div>
        </div>
      </div>
      <div class="lg:w-1/3 md:w-1/2 p-4">
        <div class="flex relative">
          <img alt="projects" class="absolute inset-0 w-full h-60 object-cover object-center" src="images/projectPhotos/portfolio-3.jpg">
          <div class="px-4 py-3 relative z-10 w-full h-60 border-4 border-gray-200 bg-white opacity-0 hover:opacity-100">
            <h2 class="tracking-widest text-sm title-font font-medium text-indigo-500 mb-1">Manchester</h2>
            <h1 class="title-font text-lg font-medium text-gray-900 mb-3">Back Garden</h1>
            <p class="leading-relaxed">Large specimen trees (craned into the garden, over the house) compliment the herbaceous planting.</p>
          </div>
        </div>
      </div>
      <div class="lg:w-1/3 md:w-1/2 p-4">
        <div class="flex relative">
          <img alt="projects" class="absolute inset-0 w-full h-60 object-cover object-center" src="images/projectPhotos/portfolio-4.jpg">
          <div class="px-4 py-3 relative z-10 w-full h-60 border-4 border-gray-200 bg-white opacity-0 hover:opacity-100">
            <h2 class="tracking-widest text-sm title-font font-medium text-indigo-500 mb-1">Bath</h2>
            <h1 class="title-font text-lg font-medium text-gray-900 mb-3">Terraced Garden</h1>
            <p class="leading-relaxed">The different levels in this garden provide an opportunity for split-level entertaining and relaxing.</p>
          </div>
        </div>
      </div>         
        <div class="lg:w-1/3 md:w-1/2 p-4">
        <div class="flex relative">
          <img alt="projects" class="absolute inset-0 w-full h-60 object-cover object-center" src="images/projectPhotos/portfolio-5.jpg">
          <div class="px-4 py-3 relative z-10 w-full h-60 border-4 border-gray-200 bg-white opacity-0 hover:opacity-100">
            <h2 class="tracking-widest text-sm title-font font-medium text-indigo-500 mb-1">Cheltenham</h2>
            <h1 class="title-font text-lg font-medium text-gray-900 mb-3">Entertaining Garden</h1>
            <p class="leading-relaxed">The design and landscaping of this garden coincided with the installation of a garden room.</p>
          </div>
        </div>
      </div>
      <div class="lg:w-1/3 md:w-1/2 p-4">
        <div class="flex relative">
          <img alt="projects" class="absolute inset-0 w-full h-60 object-cover object-center" src="images/projectPhotos/portfolio-6.jpg">
          <div class="px-4 py-3 relative z-10 w-full h-60 border-4 border-gray-200 bg-white opacity-0 hover:opacity-100">
            <h2 class="tracking-widest text-sm title-font font-medium text-indigo-500 mb-1">Cardiff</h2>
            <h1 class="title-font text-lg font-medium text-gray-900 mb-3">Sculpture Garden</h1>
            <p class="leading-relaxed">Two distinct Lucy Piper sculptures, surrounded by complementary planting adorn this large Cardiff Garden.</p>
          </div>
        </div>
      </div>
      <div class="lg:w-1/3 md:w-1/2 p-4">
        <div class="flex relative">
          <img alt="projects" class="absolute inset-0 w-full h-60 object-cover object-center" src="images/projectPhotos/portfolio-7.jpg">
          <div class="px-4 py-3 relative z-10 w-full h-60 border-4 border-gray-200 bg-white opacity-0 hover:opacity-100">
            <h2 class="tracking-widest text-sm title-font font-medium text-indigo-500 mb-1">Bristol</h2>
            <h1 class="title-font text-lg font-medium text-gray-900 mb-3">Town House</h1>
            <p class="leading-relaxed">Natural screening and incorporated water feature in the centre of the garden.</p>
          </div>
        </div>
      </div>
      <div class="lg:w-1/3 md:w-1/2 p-4">
        <div class="flex relative">
          <img alt="projects" class="absolute inset-0 w-full h-60 object-cover object-center" src="images/projectPhotos/portfolio-8.jpg">
          <div class="px-4 py-3 relative z-10 w-full h-60 border-4 border-gray-200 bg-white opacity-0 hover:opacity-100">
            <h2 class="tracking-widest text-sm title-font font-medium text-indigo-500 mb-1">St.Ives</h2>
            <h1 class="title-font text-lg font-medium text-gray-900 mb-3">Mediterranean Garden</h1>
            <p class="leading-relaxed">This large, family garden has costal elements being full of colour and textures.</p>
          </div>
        </div>
      </div>
      <div class="lg:w-1/3 md:w-1/2 p-4">
        <div class="flex relative">
          <img alt="projects" class="absolute inset-0 w-full h-60 object-cover object-center" src="images/projectPhotos/portfolio-9.jpg">
          <div class="px-4 py-3 relative z-10 w-full h-60 border-4 border-gray-200 bg-white opacity-0 hover:opacity-100">
            <h2 class="tracking-widest text-sm title-font font-medium text-indigo-500 mb-1">Winchester</h2>
            <h1 class="title-font text-lg font-medium text-gray-900 mb-3">High-End Large Garden</h1>
            <p class="leading-relaxed">The design incorporates modern hard landscaping and area of planting. </p>
          </div>
        </div>
      </div>       
      <div class="lg:w-1/3 md:w-1/2 p-4">
        <div class="flex relative">
          <img alt="projects" class="absolute inset-0 w-full h-60 object-cover object-center" src="images/projectPhotos/portfolio-10.jpg">
          <div class="px-4 py-3 relative z-10 w-full h-60 border-4 border-gray-200 bg-white opacity-0 hover:opacity-100">
            <h2 class="tracking-widest text-sm title-font font-medium text-indigo-500 mb-1">Cambridge</h2>
            <h1 class="title-font text-lg font-medium text-gray-900 mb-3">Water Feature Garden</h1>
            <p class="leading-relaxed">Sophisticated outdoor lighting ensures this luxury garden looks as stunning by night as it does by day.</p>
          </div>
        </div>
      </div>
      <div class="lg:w-1/3 md:w-1/2 p-4">
        <div class="flex relative">
          <img alt="projects" class="absolute inset-0 w-full h-60 object-cover object-center" src="images/projectPhotos/portfolio-11.jpg">
          <div class="px-4 py-3 relative z-10 w-full h-60 border-4 border-gray-200 bg-white opacity-0 hover:opacity-100">
            <h2 class="tracking-widest text-sm title-font font-medium text-indigo-500 mb-1">Oxford</h2>
            <h1 class="title-font text-lg font-medium text-gray-900 mb-3">Back Garden</h1>
            <p class="leading-relaxed">The design incorporates modern hard landscaping with a more traditional area of lawn and planting.</p>
          </div>
        </div>
      </div>
      <div class="lg:w-1/3 md:w-1/2 p-4">
        <div class="flex relative">
          <img alt="projects" class="absolute inset-0 w-full h-60 object-cover object-center" src="images/projectPhotos/portfolio-12.jpg">
          <div class="px-4 py-3 relative z-10 w-full h-60 border-4 border-gray-200 bg-white opacity-0 hover:opacity-100">
            <h2 class="tracking-widest text-sm title-font font-medium text-indigo-500 mb-1">Clapham</h2>
            <h1 class="title-font text-lg font-medium text-gray-900 mb-3">Modern House Garden</h1>
            <p class="leading-relaxed">A beautiful, unique garden in the heart of Clapham, that truly mirrors the client's house interior style.</p>
          </div>
        </div>
      </div>
    </div>
  </div>  
</section>

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
