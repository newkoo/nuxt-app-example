<template>
    <div>
        <P_Details :product="product" />
    </div>
</template>

<script setup>
import P_Details from '~~/components/Product/P_Details.vue';


const { id } = useRoute().params;
definePageMeta({
    layout: 'products'
})

const uri = 'https://fakestoreapi.com/products/' + id;
const { data: product } = await useFetch(uri, { key: id });

</script>

<style scoped>

</style>