<script>
    export default {
        data() {
            return {
                isSelected: false
            }
        },
        props: ["title", "icon"]
    }
</script>

<template>
    <div role="button" class="flex justify-center px-6 py-10 rounded-xl" :class="{'bg-white': this.isSelected}">
        <span
              class="relative whitespace-nowrap text-2xl">
            {{this.title}}
        </span>
    </div>
</template>