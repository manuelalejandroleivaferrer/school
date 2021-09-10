<template>


<div class="container px-5 py-24 mx-auto">
            <div class="text-center mb-12">
                <h5 class="text-base md:text-lg text-indigo-700">See our Recent News</h5>
                <h1 class="text-4xl md:text-6xl text-gray-700 font-semibold">Categories Responsive Card</h1>

            </div>

            <div  class="flex flex-wrap -m-6">
                <div class="p-4 sm:w/12 lg:w-1/3" v-for="categories in categories" :key="categories.id">
                <div class="h-full border-2 border-gray-200 border-opacity-60 rounded-lg overflow-hidden">
                    <NuxtLink :to="`/productos/${categories.id}`"><img :src="`${categories.image}`" alt="" class="lg:h-72 md:h-48 w-full object-cover object-center "></NuxtLink>
                    <div class="p-6 hover:bg-indigo-700 hover:text-white transition duration-300 ease-in">
                       <h2 class=" text-base font-medium text-indigo-300 mb-1"> {{categories.name}}</h2>     
                       <h1 class="text-2xl font-semibold mb-3">{{categories.slug}}</h1>
                       <p class="leading-relaxed mb-3">Data</p>
                       <div class="flex items-center flex-wrap">
                           <a href="#" class=" text-indigo-300 inline-flex item-center md:mb-2 lg:mb-0"> Read More</a>

                       </div>
                    </div>
                </div>

                </div>

            </div>
</div>

    
</template>

<script>

import axios from 'axios'
export default {


data(){
        return  {  
            categories:[]
        };
   },

   
   mounted(){
       this.listar()
   },
   methods: {
      listar(){      
            //returns the lastest products of the database
         const a =  axios.get('http://127.0.0.1:8000/api/v1/categories/').
          then(response =>{
              this.categories=response.data
          }).catch(error =>{
              console.log(error)
          })            
          
          return a
      }
   }
    
}
</script>