<template>
    <Head title="Welcome" />

    <header class="text-gray-600 body-font">
        <div class="container-fluid mx-auto flex flex-wrap p-5 flex-col md:flex-row items-center"> 

               <div class="flex title-font items-center text-gray-900 mb-4 pb-5 md:mb-0">                 
                <img src="bloom_tree.png" alt="" width="90" height="90" /> 
                 <span class="ml-1 text-gray-700 text-4xl lg:text-5xl">BLOOM</span>                               
                  <span class="ml-3 text-gray-700 text-sm md:text-xl">GARDEN DESIGN</span> 
                  </div>     

         <div class="flex items-center text-base md:ml-auto">           
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

            <div class="container-fluid mx-auto flex flex-wrap p-5 flex-col text-gray-100 bg-gray-700 md:flex-row items-center">     
            <nav class="md:ml-auto md:mr-auto flex flex-wrap items-center text-base justify-center">
                <Link class="mr-10 text-lg hover:underline" href="#">home</Link>
                <Link class="mr-10 text-lg hover:underline" href="#">about</Link>
                <Link class="mr-10 text-lg hover:underline" href="#">portfolio</Link>
                <Link class="mr-10 text-lg hover:underline" href="#">contact</Link>
            </nav>     
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
