<script setup lang="ts">
const isScrolled = ref(false)
const isMobileMenuOpen = ref(false)

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
  handleScroll()
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
            :class="{ 'navbar--scrolled': isScrolled }"
        >
            <div class="navbar__inner">

                <div class="navbar__links">
                    <a href="#products">Works</a>
                    <a href="#research">Research</a>
                </div>

                <a href="/" class="navbar__logo">
                    <div v-if="!isScrolled">Rachellia Ayu Herdani</div>
                    <div v-else>RH .</div>
                </a>

                <a href="#contact" class="navbar__button">
                    Get in touch
                </a>

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