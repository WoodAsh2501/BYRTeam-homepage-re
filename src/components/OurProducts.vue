<script>
import ProductButton from './outProducts/ProductButton.vue';
import SectionTitle from './elements/SectionTItle.vue';
import productIntroduction from '../assets/productIntroduction.json';
export default {
    data() {
        return {
            selected: 0,
            introduction: productIntroduction,
            iconByrbbs: new URL("/assets/products/byrbbs.png", import.meta.url),
            iconDekt: new URL("/assets/products/dekt.png", import.meta.url),
            iconNeticu: new URL("/assets/products/neticu.png", import.meta.url),
            iconBitwarden: new URL("/assets/products/bitwarden.png", import.meta.url),
            iconByrio: new URL("/assets/products/byrio.png", import.meta.url),
            iconGitlab: new URL("/assets/products/gitlab.png", import.meta.url),
            iconMirrors: new URL("/assets/products/mirrors.png", import.meta.url),
            iconOverleaf: new URL("/assets/products/overleaf.png", import.meta.url),
            iconEfficiency: new URL("/assets/products/efficiency.png", import.meta.url),
        }
    },
    mounted() {
        this.switchSelected(0)
    },
    components: {
        SectionTitle,
        ProductButton
    },
    methods: {
        switchSelected(id) {
            this.selected = id;
            for (let i = 0; i < 9; i++) {
                this.$refs[`productButton${i}`].isSelected = i === id;
            }
        }
    }
}

</script>

<template>
    <SectionTitle title="我们的产品" />
    <div class="flex items-center justify-around h-[100px]">
        <ProductButton ref="productButton0" @click="switchSelected(0)" :icon="iconByrbbs" />
        <ProductButton ref="productButton1" @click="switchSelected(1)" :icon="iconDekt" />
        <ProductButton ref="productButton2" @click="switchSelected(2)" :icon="iconNeticu" />
        <ProductButton ref="productButton3" @click="switchSelected(3)" :icon="iconBitwarden" />
        <ProductButton ref="productButton4" @click="switchSelected(4)" :icon="iconByrio" />
        <ProductButton ref="productButton5" @click="switchSelected(5)" :icon="iconGitlab" />
        <ProductButton ref="productButton6" @click="switchSelected(6)" :icon="iconMirrors" />
        <ProductButton ref="productButton7" @click="switchSelected(7)" :icon="iconOverleaf" />
        <ProductButton ref="productButton8" @click="switchSelected(8)" :icon="iconEfficiency" />
    </div>
    <div class="rounded-[18px] bg-white px-6 py-4">
        <div class="flex flex-col gap-2">
            <div>
                <h3 class="text-2xl">
                    {{ introduction[selected].name }}
                </h3>
            </div>
            <p class="text-[#0067D1] opacity-80">
                {{ introduction[selected].note }}
            </p>
            <article class="text-lg leading-7 indent-[2em]">
                <p>
                    {{ introduction[selected].introduction }}
                </p>
            </article>

        </div>
    </div>
</template>