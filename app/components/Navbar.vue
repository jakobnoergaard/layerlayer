<template>
    <nav class="navbar bg-base-100 fixed top-0 left-0 w-full z-50">
        <div class="flex-none">
            <button class="btn btn-square btn-ghost">
                <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24"
                    class="inline-block h-5 w-5 stroke-current">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16">
                    </path>
                </svg>
            </button>
        </div>
        <div class="flex-1">
            <a class="btn btn-ghost text-xl">daisyUI</a>
        </div>
        <div class="flex-none">
            <button @click="toggleDarkMode" class="btn btn-ghost">
                {{ colorMode.value === 'dark' ? '🌙' : '☀️' }}
            </button>
        </div>
    </nav>
</template>

<script setup lang="ts">
const colorMode = useColorMode()

// Initialize with system preference, fallback to light
colorMode.value = colorMode.value || 'light'

const toggleDarkMode = () => {
    colorMode.value = colorMode.value === 'light' ? 'dark' : 'light'
}
</script>

<style scoped>
/* Component-specific styles can be added here if needed */
</style>