<template>
    <div>
        <Head>
            <Title>'Mini Nuxt App | {{ product.title }}</Title>
            <Meta name="description" :content="product.description" />
        </Head>
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

if (!product.value) {
    throw createError({ statusCode: 404, statusMessage: 'Product Not Found', fatal: true });
}

</script>

<style scoped>

</style>