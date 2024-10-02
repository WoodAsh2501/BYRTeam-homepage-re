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
            selectedGroup: 0
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
    }
}
</script>

<template>
    <SectionTitle title="部门介绍" />
    <div class="flex flex-col gap-3 rounded-2xl bg-white p-3 lg:flex-row h-min">
        <nav class="rounded-xl bg-[#F5F5F5] p-3 sm:p-3 lg:p-6">
            <GroupButton ref="groupButton0" @click="selectGroup(0)" title="技术组" />
            <GroupButton ref="groupButton1" @click="selectGroup(1)" title="设计组" />
            <GroupButton ref="groupButton2" @click="selectGroup(2)" title="新媒体组" />
            <GroupButton ref="groupButton3" @click="selectGroup(3)" title="产品运营组" />
        </nav>
        <main class="relative min-w-0 grow rounded-xl">
            <TechGroup v-if="selectedGroup === 0" />
            <DesignGroup v-if="selectedGroup === 1" />
            <MediaGroup v-if="selectedGroup === 2" />
            <ProductGroup v-if="selectedGroup === 3" />
        </main>
    </div>
</template>