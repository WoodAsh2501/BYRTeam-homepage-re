<script>
export default {
    props: ["id", "avatar", "time", "msg"]
}
</script>

<template>
    <div class="flex w-full px-4">
        <div class="flex max-sm:gap-2 sm:gap-4 self-end grow">
            <img :src="avatar" class="justify-start w-12 h-12" />
            <div class="flex flex-col gap-[6px]">
                <div class="flex items-baseline justify-start gap-4">
                    <div class="leading-[180%] text-[#393939] max-sm:text-sm sm:text-lg">{{ id }}</div>
                    <div class="leading-[180%] opacity-50 max-sm:text-xs sm:text-sm">{{ time }}</div>
                </div>
                <slot></slot>
            </div>
            
        </div>
    </div>
</template>

<style>
.receiveMsg {
    @apply text-black w-fit px-5 py-2 text-lg shadow-[0_0_4px_0] shadow-[#DEE6F2] bg-[#ffffff] rounded-r-[24px] rounded-l-[4px] max-w-[640px];
}

.receiveMsg:last-child {
    @apply rounded-bl-[24px]
}

</style>