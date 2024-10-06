<script>
export default {
    props: ["scrollIntoMain"]
}
</script>

<template>
    <div class="fixed z-50 text-white"
    :class="{'glassMorphismHeader': this.scrollIntoMain}">
        <div class="flex sticky top-0 w-screen px-12 py-3 items-center justify-between transition duration-500">
            <a>
                <img src="../assets/logo.svg" onload="SVGInject(this)"/>
            </a>
            <div class="flex gap-10">
                <a>北邮人论坛</a>
                <a>北邮人BT</a>
                <a>BYRIO技术社区</a>
            </div>
        </div>
    </div>
</template>

<style scoped>
    .glassMorphismHeader {
        @apply text-[#333] backdrop-blur-sm border-b border-white/50 bg-white/50;
    }
</style>