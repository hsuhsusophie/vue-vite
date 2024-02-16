<template>
<nav class="navbar navbar-expand-md navbar-light bg-light fixed-top p-2 navbar-transparent">
    <div class="container-fluid">
        <a class="navbar-brand" href="#">©Caffice</a>
        <button type="button" class="btn btn-lighter">購物車
            <span class="badge bg-danger text-white"> {{ cart.length }} </span>
        </button>
    </div>
</nav>
</template>


<script>
import { mapState } from "pinia";
import cartStore from "../stores/cartStore.js";

export default {
    template: `<nav class="navbar navbar-expand-md navbar-light bg-light fixed-top p-2 navbar-transparent">
    <div class="container-fluid">
        <a class="navbar-brand" href="#">©Caffice</a>
        <button type="button" class="btn btn-lighter">購物車
            <span class="badge bg-danger text-white"> {{ cart.length }} </span>
        </button>
    </div>
</nav>`,
    computed: {
        ...mapState(cartStore, ['cart'])
    }
}
</script>