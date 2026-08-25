<script setup lang="ts">
interface propsAutobiography {
  label: string;
}

const props = withDefaults(defineProps<propsAutobiography>(), {
  label: '',
});
</script>

<template>
    <div class="identity-body">
        <div class="identity-headline">
          <!-- <div class="identity-image"> -->
            <img src="@/assets/images/FotoDiriNoBackground.png" alt="Under Construction" />
          <!-- </div> -->
          
          <div>
            <h1 class="text-align-left m-0-bottom m-0-top">{{ props.label }}</h1>
            <p class="text-align-left">The future is still under construction</p>
          </div>
        </div>
    </div>
</template>