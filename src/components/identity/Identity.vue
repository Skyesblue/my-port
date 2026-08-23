<script setup lang="ts">
interface propsInterface {
  label: string;
}

const props = withDefaults(defineProps<propsInterface>(), {
  label: '',
});
</script>

<template>
    <div class="identity-body">
        <div class="identity-headline">
          <h1 class="text-align-center m-0-bottom">{{ props.label }}</h1>
          <p class="text-align-center">The future is still under construction</p>
        </div>
    </div>
</template>