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
            this.size = this.isSelected ? "100px" : "54px";
        },
    },
}
</script>

<template>
    <div role="button">
        <!-- <img :src="this.icon" :width="this.size" draggable="false"/> -->
        <img :src="this.icon" :style="{ width: this.size }" style="transition: width 0.3s ease;" draggable="false"/>
    </div>
</template>