<template>
<div class=" bg-gray-100">
    <section class="md:h-full flex items-center text-gray-600">
        <Categorias />
        
    </section>

</div>
</template>

<script >

import Categorias from "~/components/categorias/Categorias.vue";

export default{
  name:'Practica',
  components:{
      Categorias
  },
 
}
</script>
