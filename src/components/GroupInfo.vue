<script>
import SectionTitle from './elements/SectionTItle.vue';
import DesignGroup from './groupInfo/DesignGroup.vue';
import GroupButton from './groupInfo/GroupButton.vue'
import MediaGroup from './groupInfo/MediaGroup.vue';
import ProductGroup from './groupInfo/ProductGroup.vue';
import TechGroup from './groupInfo/TechGroup.vue';
export default {
    data() {
        return {
            selectedGroup: 0,
            iconTech: new URL("/assets/groupInfo/icon-tech.svg", import.meta.url),
            iconDesign: new URL("/assets/groupInfo/icon-design.svg", import.meta.url),
            iconMedia: new URL("/assets/groupInfo/icon-media.svg", import.meta.url),
            iconProduct: new URL("/assets/groupInfo/icon-product.svg", import.meta.url)
        }
    },
    components: {
        SectionTitle,
        GroupButton,
        TechGroup,
        DesignGroup,
        MediaGroup,
        ProductGroup
    },
    methods: {
        selectGroup(id) {
            this.selectedGroup = id;
            for (let i = 0; i < 4; i++) {
                this.$refs[`groupButton${i}`].isSelected = i === id;
            }
        }
    },
    mounted() {
        this.selectGroup(0);
    },
}
</script>

<template>
    <SectionTitle title="部门介绍" />
    <div class="flex flex-col gap-3 rounded-2xl bg-white p-3 lg:flex-row h-min">
        <nav class="flex flex-row justify-between rounded-xl bg-[#F5F5F5] p-3 lg:p-6 lg:flex-col">
            <GroupButton ref="groupButton0" :icon="iconTech" @click="selectGroup(0)" title="技术组" />
            <GroupButton ref="groupButton1" :icon="iconDesign" @click="selectGroup(1)" title="设计组" />
            <GroupButton ref="groupButton2" :icon="iconMedia" @click="selectGroup(2)" title="新媒体组" />
            <GroupButton ref="groupButton3" :icon="iconProduct" @click="selectGroup(3)" title="产品运营组" />
        </nav>
        <main class="relative min-w-0 grow h-[550px] rounded-xl">
            <TechGroup v-if="selectedGroup === 0" />
            <DesignGroup v-if="selectedGroup === 1" />
            <MediaGroup v-if="selectedGroup === 2" />
            <ProductGroup v-if="selectedGroup === 3" />
        </main>
    </div>
</template>