<template>
    <div>
        <header class="shadow-sm bg-white">
            <nav class="container mx-auto p-4 flex justify-between">
                <NuxtLink to="/" class="font-bold">nuxt-project</NuxtLink>
            </nav>
        </header>

        <!-- output page -->

        <div class="container mx-auto p-4" >
            <slot />
        </div>

        <footer class="container mx-auto p-4 flex justify-between">
            <ul class="flex space-x-4 text-xl">
                <li><NuxtLink to="/">Home</NuxtLink></li>
                <li><NuxtLink to="/login">Login</NuxtLink></li>
                <li><NuxtLink to="/products">Products</NuxtLink></li>
            </ul>
        </footer>
    </div>
</template>

<style scoped>
    .router-link-exact-active {
        color: #12b488;
    }
</style>
