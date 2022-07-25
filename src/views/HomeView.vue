<template>
  <Banner/>
  <div class="main-container">
    <h1>Cadastrar Produto: </h1>
    <ProdutoForm/>
  </div>
</template>

<script>
import Banner from '@/components/Banner.vue';
import ProdutoForm from '@/components/ProdutoForm.vue';

  export default {
    name: "Home",
    components: {
    Banner,
    ProdutoForm
}
}
</script>