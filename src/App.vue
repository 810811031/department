<template>
    <app-layout v-if="useLayout">
        <router-view />
    </app-layout>

    <router-view v-else />
</template>

<script setup>
import AppLayout from "@/components/Layout";
import { computed } from "vue";
import { RouterView, useRoute } from 'vue-router';

const route = useRoute();

const useLayout = computed(() => {
    return typeof route?.meta?.useLayout === 'boolean' ? route?.meta?.useLayout : true;
});

</script>