<script>
export default {
    props: ['img', 'title']
}
</script>

<template>
    <div class=" flex max-w-[344px] flex-col items-center">
        <img :src="img" class="-mb-16 z-10">
        <div class="flex flex-col gap-6 grow rounded-2xl bg-white text-center  px-12 pb-9 pt-[100px]">
            <h2 class="text-[28px] text-center">
                {{ title }}
            </h2>
            <span class="text-[#777] text-[0.96rem]">
                <slot></slot>
            </span>
        </div>
    </div>
</template>