<script>
export default {
    data() {
        return {
            isSelected: false,
            size: "54px"
        }
    },
    props: ["icon","id"],
    watch: {
        isSelected() {
            this.size = this.isSelected ? "100px" : "50px";
        },
    },
}
</script>

<template>
    <div role="button">
        <img :src="this.icon" :width="this.size" draggable="false"/>
    </div>
</template>