<template>
    <NuxtLayout>
        <NuxtPage/>
    </NuxtLayout>
</template>
<script setup lang="ts">
const nuxtApp = useNuxtApp();
const loading = ref(false);

nuxtApp.hook("page:start", () => {
    loading.value = true;
});

nuxtApp.hook("page:finish", () => {
    loading.value = true;

});
</script>