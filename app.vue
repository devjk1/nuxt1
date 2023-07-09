<script setup>
const foods = useState("foods", () => {
    return [
        { id: 1, name: "steak", desc: "A piece of beef" },
        { id: 2, name: "pasta", desc: "A dish with noodles and sauce" },
        { id: 3, name: "burrito", desc: "Delicious ingredients wrapped in a tortilla" },
    ];
});
</script>

<template>
    <div class="min-h-screen bg-gray-600 text-gray-200">
        <div class="bg-gray-800 text-gray-300">
            <SiteHeader />
        </div>
        <main class="max-w-7xl mx-auto px-4 py-4">
            <NuxtPage />
        </main>
    </div>
</template>
