<script setup lang="ts">
const isScrolled: Ref<boolean | null> = ref(null);
const isMobileMenuOpen: Ref<boolean | null> = ref(false)

const handleScroll = () => {
  isScrolled.value = window.scrollY > 40
}

const toggleMobileMenu = () => {
  isMobileMenuOpen.value = !isMobileMenuOpen.value
}

const closeMobileMenu = () => {
  isMobileMenuOpen.value = false
}

onMounted(() => {
  window.addEventListener('scroll', handleScroll)
})

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll)
})
</script>

<template>
    <header>
        <nav 
            class="navbar"
        >
            <div class="navbar__inner">

                <!-- Logo -->
                <a href="/" class="navbar__logo">
                    Rachellia Ayu Herdani
                </a>

                <!-- Desktop navigation -->
                <nav class="navbar__links">
                    <a href="#products">Products</a>
                    <a href="#research">Research</a>
                    <a href="#experts">Experts</a>
                    <a href="#contact">Contact</a>
                </nav>

                <!-- Desktop button -->
                <a href="#contact" class="navbar__button">
                    Get in touch
                </a>

                <!-- Mobile hamburger -->
                <button
                    class="navbar__hamburger"
                    @click="toggleMobileMenu"
                    aria-label="Toggle navigation"
                >
                    <span></span>
                    <span></span>
                    <span></span>
                </button>

            </div>
        </nav>
    </header>
</template>