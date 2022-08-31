<template>
<div>
    <div class="p-6 sm:px-20 bg-white text-green-700 border-gray-200">        
        <div class="mt-8 text-2xl">
            Hi {{ $page.props.user.name }}, welcome to your account!
         </div>
         <br>         
            <h2 class="text-gray-700">We will share with you some interesting tips and informations here.</h2>       
    </div>
    <!-- Content -->
    <div class="p-6 sm:px-20 bg-white text-gray-700 border-gray-200">
        <div class="mt-8 flex flex-wrap">
            <div class="h-full flex flex-col items-left">
                <h1 class="font-serif text-3xl font-semibold lg:text-4xl">Protect your garden</h1>
                    <p class="text-xl my-4 lg:text-2xl">With ever-increasing threats from pests and diseases, it's important for gardeners to be alert and try to prevent problems taking hold</p>
                        <img class="flex-shrink-0 w-full h-100 object-cover object-center my-4 md:w-auto lg:w-2/3" src="images/dashboardImg/plants_2.jpg" alt="plants" />               
                 <h2 class="text-2xl font-semibold lg:text-3xl">Watch out for new threats</h2>              
                    <p class="pt-3 pb-5 lg:text-lg">Keeping our gardens free of pests and diseases has always been high on gardeners’ agendas. With the frequent appearance of novel diseases and pests from abroad, planning for healthy gardens has become even more urgent.
                        The arrival of new pests and diseases in the UK is linked to the rise in the volume and diversity of plants being imported. Changes in climate, especially warmer winters, may also enable more pests and diseases to become established in our gardens</p>
                        <iframe class="w-fit h-80 md:w-full md:h-96 lg:w-2/3" src="https://www.youtube.com/embed/2xnsdASNvzQ" title="Xylella : How can we protect our plants?" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen>
                        </iframe> 
                 <h2 class="pt-5 text-2xl font-semibold lg:text-3xl">Source new plants carefully</h2> 
                    <p class="pt-3 lg:text-lg">One of the most common ways for pests and diseases to enter gardens is on new plants, or in associated soil.</p>   
                        <ul class="list-disc list-inside lg:text-lg">
                            <li>Propagate your own plants, from seed or local cuttings.</li>
                            <li>Where possible, purchase plants grown in the UK.</li>
                        </ul>
                 <h2 class="pt-5 pb-5 text-2xl font-semibold lg:text-3xl">Check plants coming into the garden</h2> 
                    <ul class="list-disc list-inside lg:text-lg">
                        <li>Check plants for signs of pests or diseases before purchase.</li>
                        <li>Keep new plants in an isolated part of the garden for a few weeks before planting out.</li>                    
                        <li>Monitor the health of new plants; if unusual symptoms are observed contact the supplier.</li>
                    </ul>
                 <h2 class="pt-5 text-2xl font-semibold lg:text-3xl">Keep your plants healthy</h2>
                    <p class="pt-3 pb-5 lg:text-lg">Good plant husbandry can reduce the impact of pests and diseases. Strong, healthy plants are more resilient and are less likely to be severely affected by pests and diseases. Mulching can not only feed plants to increase their vigour but may also prevent some pests and diseases leaving the soil and infecting the above-ground parts of your plants.</p>
                 <h2 class="pt-5 text-2xl font-semibold lg:text-3xl">Keep it clean</h2>
                    <p class="pt-3 pb-5 lg:text-lg">Keeping your garden clean and tidy helps to reduce pests and diseases. Cleaning garden tools, greenhouses and water butts also reduces the spread of pests and diseases and reduces the chances that they will threaten your garden in the next growing season.</p>
                 <h2 class="pt-5 text-2xl font-semibold lg:text-3xl">Monitor your plants</h2>
                    <p class="pt-3 pb-5 lg:text-lg">Keeping an eye out for pests and diseases means that problems are more likely to be noticed early and before they cause serious damage. Early detection is also likely to mean that the problem is easier to control.</p>
                 <h2 class="pt-5 text-2xl font-semibold lg:text-3xl">Deal with garden waste appropriately</h2>
                    <p class="pt-3 lg:text-lg">Garden waste affected by pests and diseases should be disposed appropriately.</p>
                        <ul class="list-disc list-inside lg:text-lg">
                            <li>Home composting can be used for most green waste; local green waste schemes compost at higher temperatures and therefore kill more pests and diseases</li>
                            <li>Burning or disposal at a council refuse site is best practice for woody plants, and material affected by persistent pests and diseases.</li>
                        </ul>
            </div>            
        </div>
    </div>
</div>                                 
</template>

<script>
    import { defineComponent } from 'vue'
    import JetApplicationLogo from '@/Jetstream/ApplicationLogo.vue'


    export default defineComponent({
        components: {
            JetApplicationLogo,
        },
    })
</script>
