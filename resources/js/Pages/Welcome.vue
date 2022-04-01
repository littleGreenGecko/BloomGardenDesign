<template>
    <Head title="Welcome" />

    <header class="text-gray-600 body-font">
        <div class="container-fluid mx-auto flex flex-wrap p-5 flex-col md:flex-row items-center"> 
            <div class="flex title-font items-center text-gray-900 mb-4 md:mb-0">                 
                <img src="images/bloom_tree.png" alt="" width="90" height="90" /> 
                <span class="ml-1 text-gray-700 text-4xl lg:text-5xl">BLOOM</span>                               
                <span class="ml-3 text-gray-700 text-sm md:text-xl">GARDEN DESIGN</span> 
            </div>     

            <div class="flex items-center text-base md:ml-auto md:mr-2">           
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

            <nav class="container-fluid mx-auto flex flex-wrap p-5 flex-row md:ml-auto md:mr-auto justify-center text-gray-100 bg-gray-700 items-center text-lg md:text-xl tarcking-wide md:tracking-widest">                 
                <Link class="mx-auto lg:mx-14 hover:underline" href="#">home</Link>
                <Link class="mx-auto lg:mx-14 hover:underline" href="#">about</Link>
                <Link class="mx-auto lg:mx-14 hover:underline" href="#">portfolio</Link>
                <Link class="mx-auto lg:mx-14 hover:underline" href="#">contact</Link>
            </nav> 
            <div class="container-fluid mx-auto items-center flex flex wrap flex-col md:flex-row md:justify-center lg:space-x-12">
                <img src="images/watercolour_1.jpg" alt="" class="img-fluid" width="500" height="400" />
                <img src="images/watercolour_2.jpg" alt="" class="img-fluid" width="500" height="400" />
                <img src="images/watercolour_3.jpg" alt="" class="img-fluid" width="500" height="400" />                 
            </div>
    
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
