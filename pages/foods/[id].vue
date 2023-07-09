<script setup>
const foods = useState("foods");
const foodId = useRoute().params.id;
const food = foods.value[foodId - 1];
</script>

<template>
    <div>
        <table class="table-auto w-full mt-2">
            <thead>
            <tr>
                <th class="text-left">ID</th>
                <th class="text-left">Name</th>
                <th class="text-left">Description</th>
            </tr>
            </thead>
            <tbody>
            <tr>
                <td>{{ food.id }}</td>
                <td>{{ food.name }}</td>
                <td>{{ food.desc }}</td>
            </tr>
            </tbody>
        </table>
    </div>
</template>