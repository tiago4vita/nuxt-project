<template>
    <div>
        <h2 class="text-gray-900 text-4xl font-bold">{{ product.title }}</h2>
        <p class="text-gray-900 mt-4">{{ product.description }}</p>
        <div class="flex justify-center mt-8">
            <img :src="product.image" alt="product image" class="w-1/4 shadow-2xl rounded-lg transition-transform duration-300 ease-in-out hover:scale-105 hover:shadow-3xl border-4 border-gray-200 p-2">
        </div>
        <div class="flex gap-4 mt-2">
            <p class="font-bold text-2xl mt-4">${{ product.price }}</p>
            <button class="font-bold text-2xl mt-4 hover:animate-spin">Add to Cart</button>
        </div>
    </div>
</template>

<script setup>
    const { id } = useRoute().params;
    const uri = 'https://fakestoreapi.com/products/' + id;

    const { data: product } = await useFetch(uri);

    definePageMeta({
        layout: 'product'
    });
</script>

<style scoped>
</style>