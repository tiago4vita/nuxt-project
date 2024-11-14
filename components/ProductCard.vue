<template>
    <div class="card text-center">
        <div class="fixed-height h-36 flex justify-center items-center">
            <img :src="product.image" alt="product thumb" class="thumb">
        </div>
        <div class="">
            <p class="font-bold text-gray-500 m-4 text-lg truncate">{{ product.title }}</p>
            <NuxtLink :to="`/products/${product.id}`">
                <p class="btn bg-gray-700 text-white my-4 w-1/2 mx-auto hover:bg-gradient-to-r hover:from-green-400 hover:to-blue-400 hover:animate-pulse">View Details</p>
            </NuxtLink>
        </div>
    </div>
</template>

<script setup>
    const { product } = defineProps(['product']);
</script>

<style scoped>
    .thumb {
        max-height: 120px;
        max-width: 70%;
        margin: 0 auto;
    }
</style>