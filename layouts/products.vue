<template>
    <div class="bg-gradient-to-r from-green-200 to-blue-200">
        <header class="shadow-sm bg-white">
            <nav class="container mx-auto p-4 flex justify-between">
                <NuxtLink to="/" class="font-bold">nuxt-project</NuxtLink>
            </nav>
        </header>
        <!-- output page -->
        <div class="container mx-auto p-4">
            <slot />
        </div>
    </div>
</template>

<style scoped>
    .router-link-exact-active {
        color: #12b488;
    }
</style>
