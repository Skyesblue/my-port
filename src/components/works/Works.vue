<script setup lang="ts">
interface propsInterface {
//   label: string;
}

const props = withDefaults(defineProps<propsInterface>(), {
//   label: '',
});
</script>

<template>
    <div class="works-body">
        <p class="text-align-center">The future is still under construction</p>
    </div>
</template>