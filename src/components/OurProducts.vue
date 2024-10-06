<script>
import ProductButton from './outProducts/ProductButton.vue';
import SectionTitle from './elements/SectionTItle.vue';
import productIntroduction from '../assets/products/productIntroduction.json';
export default {
    data() {
        return {
            selected: 0,
            introduction: productIntroduction
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
        <ProductButton ref="productButton0" @click="switchSelected(0)" icon="src/assets/products/byrbbs.png" />
        <ProductButton ref="productButton1" @click="switchSelected(1)" icon="src/assets/products/dekt.png" />
        <ProductButton ref="productButton2" @click="switchSelected(2)" icon="src/assets/products/neticu.png" />
        <ProductButton ref="productButton3" @click="switchSelected(3)" icon="src/assets/products/bitwarden.png" />
        <ProductButton ref="productButton4" @click="switchSelected(4)" icon="src/assets/products/byrio.png" />
        <ProductButton ref="productButton5" @click="switchSelected(5)" icon="src/assets/products/gitlab.png" />
        <ProductButton ref="productButton6" @click="switchSelected(6)" icon="src/assets/products/mirrors.png" />
        <ProductButton ref="productButton7" @click="switchSelected(7)" icon="src/assets/products/overleaf.png" />
        <ProductButton ref="productButton8" @click="switchSelected(8)" icon="src/assets/products/efficiency.png" />
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