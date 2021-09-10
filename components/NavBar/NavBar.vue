<template >

<nav class="bg-gray-100">

    <div class=" max-w-6xl mx-auto px-4">

        <div class="flex justify-between ">



              <div class="flex space-x-4">
                  <div >
                      <a href="#" class="flex items-center py-5 px-2 text-gray-700  hover:text-yellow-900">
                          <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 mr-1 text-yellow-900 " fill="none" viewBox="0 0 24 24" stroke="currentColor">
                            <path strokeLinecap="round" strokeLinejoin="round" strokeWidth={2} d="M12 19l9 2-9-18-9 18 9-2zm0 0v-8" />
                            </svg>

                            

                            <NuxtLink class="font-semibold" to="/">Djackets</NuxtLink>


                      </a>

                  </div>
            <div class=" hidden md:flex  items-center space-x-1">
               

            </div>
                  
                  </div>  

            
            <div class="hidden md:flex items-center space-x-1">
                <a href="" class="py-5 px-3 ">Login</a>
                <a href="" class="py-3 px-3 bg-yellow-400 text-yellow-900 rounded hover:bg-yellow-300 hover:text-yellow-800 transition duration-300">Sign Up</a>
            </div>



            <!---mobile button goes here--->

            <div class="md:hidden flex items-center">
                <button @click="shotask()" class="mobile-menu-button" >

                <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
                </svg>
            </button>

            </div>
        </div>
    </div>

    <div class="mobile-menu hidden md:hidden ">
        
       <a href="" class="block py-2 px-4 text-sm hover:bg-gray-200">Features</a>
       <a href="/about" class="block py-2 px-4 text-sm hover:bg-gray-200">Pricing</a> 
    </div>
</nav>


    
</template>
<script lang="ts">

export default{
    name:'NavBar',
    methods:{
        shotask():void{            
            const menu=document.querySelector(".mobile-menu");
            menu?.classList.toggle("hidden");
        }

    }

   

}


</script>



