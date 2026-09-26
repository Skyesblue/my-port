<script setup lang="ts">
interface propsInterface {
//   label: string;
}

const props = withDefaults(defineProps<propsInterface>(), {
//   label: '',
});
</script>

<template>
    <div class="coming-container">
        <div class="coming-title">
            <h1>Coming Soon</h1>
        </div>
    </div>
</template>