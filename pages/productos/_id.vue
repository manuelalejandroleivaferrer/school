<template>
<div class=" bg-gray-100">
    <section class="md:h-full flex items-center text-gray-600">
        <div class="container px-5 py-24 mx-auto">
            <div class="text-center mb-12">
                <h5 class="text-base md:text-lg text-indigo-700">See our Recent News</h5>
                <h1 class="text-4xl md:text-6xl text-gray-700 font-semibold">Products Responsive Card</h1>

            </div>


            <Productos />

            


        
    

            



            

        </div>
    </section>



    
</div>





    
</template>

<script >
import axios from 'axios'
import Productos from "~/components/productos/Productos.vue";
export default {
    name:'index',
     components:{
      Productos
  },


   





 
   

    
}

</script>