<template>
    <div>
        <div class="grid grid-cols-4 gap-5">
            <div v-for="p in products" class="bg-white p-4 rounded-md">
                <NuxtLink :to="`/products/${p.id}`">{{ p.title }}</NuxtLink>
            </div>
        </div>
    </div>
</template>

<script setup>
    definePageMeta({
        layout: 'products'
    });

    const { data: products } = await useFetch('https://fakestoreapi.com/products/');
</script>

<style scoped>

</style>