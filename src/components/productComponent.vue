<template>
<div class="row row-cols-1 row-cols-md-2 row-cols-lg-3 my-4 p-4 g-4">
    <div class="col" v-for="product in sortProducts " :key="product.id">
        <div class="card">
            <img :src="product.imageUrl"
                class="card-img-top" alt="">
            <div class="card-body">
                <h6 class="card-title">{{ product.title }}
                    <span class="float-end">$ {{ product.price }}</span>
                </h6>
                <a href="#" class="btn btn-outline-secondary w-100" @click.prevent="addToCart(product.id)">加入購物車</a>
            </div>
        </div>
    </div>
</div> 
</template>


<script>

import productsStore from "../stores/productsStore.js";
import cartStore from "../stores/cartStore.js";
import { mapState  , mapActions } from "pinia";

export default {
    computed: {
        ...mapState(productsStore, ['sortProducts'])
    },
    methods: {
        ...mapActions(cartStore, ['addToCart'])
    }
};
</script>