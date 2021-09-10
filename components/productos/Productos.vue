<template>


<div  class="flex flex-wrap -m-6 " v-if="!loading && latestProducts.length">
                <div class="p-4 sm:w/12 lg:w-1/3" v-for="products in latestProducts" :key="products.id">
                <div class="h-full border-2 border-gray-200 border-opacity-60 rounded-lg overflow-hidden">
                    <img :src="`${products.image}`" alt="" class="lg:h-72 md:h-48 w-full object-cover object-center ">
                    <div class="p-6 hover:bg-indigo-700 hover:text-white transition duration-300 ease-in">
                       <h2 class=" text-base font-medium text-indigo-300 mb-1"> {{products.price}}</h2>     
                       <h1 class="text-2xl font-semibold mb-3">{{products.name}}</h1>
                       <p class="leading-relaxed mb-3">{{products.description}}</p>
                       <div class="flex items-center flex-wrap">
                           <a href="#" class=" text-indigo-300 inline-flex item-center md:mb-2 lg:mb-0"> Read More</a>

                       </div>
                    </div>

                </div>
                

                </div>
</div>
<div v-else class="flex items-center justify-center">
    <img src="~/~/static/logo/error.png" alt="">
    
</div>
            
</template>

<script>
import axios from 'axios'
export default {
     data(){
        return  {  
            latestProducts:[],
            id_category:this.$route.params.id,
            loading:true
        };
   },
   mounted(){
       this.listar()
   },
   methods: {
    listar(){      
            //returns the lastest products of the database
         const a =  axios.get('http://127.0.0.1:8000/api/v1/productsa/'+this.id_category).
          then(response =>{
              this.latestProducts=response.data

          }).catch(error =>{
              console.log(error)
          })
          this.loading=false
            
          
          return a
      }
   }
    
}
</script>