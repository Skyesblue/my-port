<script setup lang="ts">
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome'
import { faFaceGrinWink } from '@fortawesome/free-regular-svg-icons'
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
            <!-- <img src="@/assets/images/FotoDiriNoBackground.png" alt="Under Construction" /> -->
          <!-- </div> -->
          <h1 class="text-align-left m-0-bottom m-0-top">{{ props.label }}</h1>
          <p class="text-align-left">Sometimes my code has its own character development <FontAwesomeIcon :icon="faFaceGrinWink" />. But anyway, I have experience in enhancing and maintaining enterprise applications. I'm skilled in C#, mySQL, and JavaScript. I have worked as a fullstack developer while working closely with tech teams and business stakeholders alike.</p>
        </div>
    </div>
</template>