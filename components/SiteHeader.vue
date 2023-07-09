<script setup>
const foods = useState("foods");
</script>

<template>
    <div class="flex items-center justify-between max-w-7xl mx-auto px-4 py-4">
        <div class="flex items-center space-x-4">
            <img src="/favicon.ico" alt="logo" class="mr-4">

            <NuxtLink to="/" class="hover:text-gray-100 hover:font-bold">Index</NuxtLink>
            <NuxtLink to="/about" class="hover:text-gray-100 hover:font-bold">About</NuxtLink>
            <NuxtLink to="/bio" class="hover:text-gray-100 hover:font-bold">Bio</NuxtLink>

            <template v-for="food in foods">
                <NuxtLink :to="`/foods/${food.id}`" class="hover:text-gray-100 hover:font-bold">
                    {{ food.name }}
                </NuxtLink>
            </template>
        </div>
        <div>controls</div>
    </div>
</template>