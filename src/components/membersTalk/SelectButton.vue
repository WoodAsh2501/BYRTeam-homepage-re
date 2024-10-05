<script>
export default {
    props: ["clickable"],
    data() {
        return {
            isHover: false
        }
    },
    computed: {
        colorArray() {
            if (!this.clickable) return ["bg-[#DDD]", "#AAA"]
            if (this.isHover) {
                return ["bg-[#175DDC]", "#FFF"]
            } else {
                return ["bg-[#FFF]", "#888"]
            }
        }
    }
}
</script>
<template>
    <button class="flex rounded-full w-16 h-16 items-center"
        @mouseover="() => (this.isHover = this.clickable ? true : false)" @mouseleave="() => (this.isHover = false)"
        :class="colorArray[0]">
        <svg class="m-auto rotate-180" xmlns="http://www.w3.org/2000/svg" width="32" height="32" fill="none"
            viewBox="0 0 32 32">
            <path :stroke="colorArray[1]" stroke-linecap="round" stroke-linejoin="round" stroke-width="3"
                d="m11 7 10 9-10 9"></path>
        </svg>
    </button>
</template>