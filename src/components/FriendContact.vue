<script setup lang="ts">
import { ref } from 'vue';
const detailsAreVisible = ref(false);
const friend = ref(
    {
    id: 'manuel',
    name: 'Manuel Lorenz',
    phone: '0123 45678 90',
    email: 'manuel@localhost.com'
    }
);

function toggleDetails() {
    detailsAreVisible.value = !detailsAreVisible.value;
}
</script>

<template>
    <li>
        <h2>{{ friend.name }}</h2>
        <button @click="toggleDetails">{{ detailsAreVisible ? 'Hide' : 'Show' }} Details</button>
        <ul v-if="detailsAreVisible">
            <li><strong>Phone:</strong> {{ friend.phone }}</li>
            <li><strong>Email:</strong> {{ friend.email }}</li>
        </ul>
    </li>
</template>

<style scoped></style>