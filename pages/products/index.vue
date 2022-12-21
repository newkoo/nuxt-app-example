<template>
    <div>
        <div class="grid grid-cols-4 gap-5">
            <div v-for="product in products" :key="product.id">
                <P_Card :product="product" />
            </div>
        </div>
    </div>
</template>

<script setup>
import P_Card from '~~/components/Product/P_Card.vue';

definePageMeta({
    layout: 'products'
})

//fetch the products
const { data: products } = await useFetch('https://fakestoreapi.com/products');
</script>

<style scoped>

</style>