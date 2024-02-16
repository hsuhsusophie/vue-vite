<script>
import NavbarComponent from './components/NavbarComponent.vue';
import ProductComponent from './components/productComponent.vue';
import CartComponent from './components/cartComponent.vue';

export default {
  components:{
    NavbarComponent,
    ProductComponent,
    CartComponent
  },
}
</script>

<template>
<div class="continer">
<NavbarComponent></NavbarComponent>
<CartComponent></CartComponent>
<ProductComponent></ProductComponent>

</div>
</template>

<style lang="scss">
@import "./assets/all.scss";
</style>
