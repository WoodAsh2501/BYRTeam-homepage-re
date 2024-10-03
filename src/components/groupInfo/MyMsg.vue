<script>
export default {
    props: ["id", "avatar", "time", "msg"]
}
</script>

<template>
    <div class="flex w-full px-4">
        <div class="flex max-sm:gap-2 sm:gap-4 self-end grow justify-end">
            <div class="flex flex-col gap-[6px]">
                <div class="flex items-baseline justify-end gap-4">
                    <div class="leading-[180%] opacity-50 max-sm:text-xs sm:text-sm">{{ time }}</div>
                    <div class="leading-[180%] text-[#393939] max-sm:text-sm sm:text-lg">{{ id }}</div>
                </div>
                <slot></slot>
            </div>
            <img :src="avatar" class="justify-start w-12 h-12" />
        </div>
    </div>
</template>

<style>
.myMsg {
    @apply text-white w-fit px-5 py-2 text-lg bg-[#4AA3FF] rounded-l-[24px] rounded-r-[4px] max-w-[640px] text-justify;
}

.myMsg:last-child {
    @apply rounded-br-[24px]
}

</style>