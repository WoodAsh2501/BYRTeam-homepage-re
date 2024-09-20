<script>
export default {
    props: ['title']
}
</script>
<template>
    <div class="text-3xl w-fit">
        <h2>{{ title }}</h2>
        <div class="relative bottom-3 right-2 h-4 w-[calc(120%)] -skew-x-12 bg-gradient-to-r from-[#0067D1A6] to-[#D9D9D900]"></div>
    </div>

</template>