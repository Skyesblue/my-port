<script setup lang="ts">
interface propsInterface {
//   label: string;
}

const props = withDefaults(defineProps<propsInterface>(), {
//   label: '',
});
</script>

<template>
    <div class="works-container">
        <div class="works-title">
            <h2>My Works</h2>
        </div>
    </div>
</template>