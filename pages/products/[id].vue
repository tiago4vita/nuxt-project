<template>
    <div>
        <h2>{{ product.title }}</h2>
        <p class="description">{{ product.description }}</p>
        <div class="flex justify-center">
            <img :src="product.image" alt="product image" class="w-1/4 shadow-2xl rounded-lg transition-transform duration-300 ease-in-out hover:scale-105 hover:shadow-3xl border-4 border-[#12b488] p-2">
        </div>
        <p class="font-bold text-2xl mt-4">${{ product.price }}</p>
    </div>
</template>

<script setup>
    const { id } = useRoute().params;
    const uri = 'https://fakestoreapi.com/products/' + id;

    const { data: product } = await useFetch(uri);

        definePageMeta({
        layout: 'products'
    });
</script>

<style scoped>
    h2 {
    margin-bottom: 20px;
    font-size: 36px;
    font-weight: bold;
    color: #333;
}
</style>