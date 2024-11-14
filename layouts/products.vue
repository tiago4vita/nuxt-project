<template>
    <div class="bg-gradient-to-r from-green-200 to-blue-200 h-full">
        <header class="shadow-sm bg-white">
            <nav class="container mx-auto p-4 flex justify-between">
                <NuxtLink to="/" class="font-bold">nuxt-project</NuxtLink>
                <ul class="flex gap-4 mt-2">
                    <li><NuxtLink to="/">Home</NuxtLink></li>
                    <li><NuxtLink to="/login">Login</NuxtLink></li>
                    <li><NuxtLink to="/products" class="btn bg-gradient-to-r from-green-400 to-blue-400">Products</NuxtLink></li>
                </ul>
            </nav>
        </header>
        <!-- output page -->
        <div class="py-10">
            <div class="container mx-auto py-4 px-6 bg-white rounded-lg shadow-md">
                <slot />
            </div>
        </div>
    </div>
</template>

<style scoped>
    .router-link-exact-active {
        font-weight: bold;
    }
</style>
