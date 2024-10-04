<script>
export default {
    props: ['img']
}
</script>

<template>
    <div class="flex flex-col grow min-w-0 w-[723px]">
        <div class="flex items-center h-[200px] ">
            <img :src="img" class="w-fit h-fit">
            <div class="flex flex-col">
                <div class="flex flex-col gap-4">
                    <div class="flex items-baseline">
                        <div class="text-2xl">
                            <slot name="name"></slot>
                        </div>
                        <div class="text-[#777] text-[0.8rem]">
                            <slot name="info"></slot>
                        </div>
                    </div>
                    <div class="flex flex-wrap max-w-[300px] content-between shrink-0 text-[0.8rem] text-nowrap gap-2">
                        <slot name="achievements"></slot>
                    </div>
                </div>
            </div>
        </div>
        <span class="bg-white -mt-8 -z-10 rounded-2xl mx-[4rem] px-10 h-[270px] text-justify flex items-center">
            <slot name="content"></slot>
        </span>
        <div class="flex flex-col items-end -my-8 mx-6">
            <img src="/src/assets/membersTalk/comma.svg" class="w-fit">
        </div>
    </div>
</template>