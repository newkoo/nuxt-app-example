<template>
    <NuxtLoadingIndicator :height="7"></NuxtLoadingIndicator>
    <div>
        <header class="shadow-sm bg-white">
            <nav class="container mx-auto p-4">
                <NuxtLink to="/products" class="font-bold">Nuxt Dojo Merch</NuxtLink>
            </nav>
        </header>
    </div>

    <div class="container mx-auto p-4">
        <slot />
    </div>

    <footer class="container mx-auto p-4 flex justify-between border-t-2">
        <ul class="flex gap-4">
            <li>
                <NuxtLink to="/">Home</NuxtLink>
            </li>
            <li>
                <NuxtLink to="/about">About</NuxtLink>
            </li>
            <li>
                <NuxtLink to="/products">Products</NuxtLink>
            </li>
        </ul>
    </footer>
</template>

<script setup>
useHead({
    title: 'Mini Nuxt App | Merchant',
    meta:[
        {name:'description',content:'Nuxt 3 Merchant'}
    ]
})
</script>

<style scoped>

</style>