<template>
    <n-dialog-provider>
        <n-message-provider>
            <app-layout v-if="useLayout">
                <router-view />
            </app-layout>

            <router-view v-else />
        </n-message-provider>
    </n-dialog-provider>
</template>

<script setup>
import { NMessageProvider, NDialogProvider } from "naive-ui";
import AppLayout from "@/components/Layout";
import { computed } from "vue";
import { RouterView, useRoute } from 'vue-router';

const route = useRoute();

const useLayout = computed(() => {
    return typeof route?.meta?.useLayout === 'boolean' ? route?.meta?.useLayout : true;
});

</script>