<script>
export default {
    data() {
        return {
            isSelected: false,
        }
    },
    props: ["title", "icon"],
    computed: {
        iconUrl() {
            return `url(${this.icon})`;
        }
    }
}
</script>

<template>
    <div role="button"
        class="flex justify-center transition-colors flex-1 py-4 px-2 lg:grow-0 grow lg:px-6 lg:py-10 rounded-xl text-[#AAA]  relative groupButtonBackground"
        :style="{
            transition: 'background-color 0.5s ease, color 0.7s ease, opacity 5s ease',
            '--icon-url': this.iconUrl
        }" :class="{
                'groupButtonSelected': this.isSelected,
                'before:opacity-0': !this.isSelected,
                'before:opacity-15': this.isSelected
            }">
        <!-- <img :src="this.icon" class="absolute opacity-20"> -->
        <span class="relative whitespace-nowrap text-xl">
            {{ this.title }}
        </span>
    </div>
</template>

<style scoped>
.groupButtonSelected {
    @apply bg-white text-blue-500 font-bold;
}

.groupButtonBackground::before {
    @apply bg-center bg-no-repeat absolute w-full bg-[length:30%] lg:bg-[length:50%] h-full top-0 left-0 m-auto;
    transition: opacity 0.5s ease;
    aspect-ratio: 1;
    background-image: var(--icon-url);
    /* background-size: 50%; */
    content: '';
}
</style>