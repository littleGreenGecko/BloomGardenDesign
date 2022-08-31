<template>
    <Link :href="'/'">
    <div class="flex flex-col md:flex-row title-font items-center text-gray-900 border-2 rounded-lg bg-white p-2 mb-4 md:mb-0">
     <img src="images/bloom_tree.png" alt="" width="90" height="90" />
     <span class="ml-1 text-gray-700 text-4xl lg:text-5xl">BLOOM</span>                               
     <span class="ml-3 text-gray-700 text-sm md:text-xl">GARDEN DESIGN</span> 
     </div>
    </Link>
</template>

<script>
    import { defineComponent } from 'vue'
    import { Link } from '@inertiajs/inertia-vue3';
    

    export default defineComponent({
        components: {
            Link,            
        },
    })
</script>
