<script>
import Card from './whyJoinUs/Card.vue';
import SectionTitle from './elements/SectionTItle.vue';

export default {
    data() {
        return {
            illu1: new URL("/assets/whyJoinUs/1.svg", import.meta.url),
            illu2: new URL("/assets/whyJoinUs/2.svg", import.meta.url),
            illu3: new URL("/assets/whyJoinUs/2.svg", import.meta.url),
        }
    },
    components: {
        SectionTitle,
        Card
    }
}
</script>

<template>
    <SectionTitle title="加入byrTeam的N个理由" />
    <div class="flex flex-col items-center md:flex-row mx-auto w-[96%] gap-4 justify-between">
        <Card title="开放自由" :img="illu1">
                自由开放的文化氛围让你的声音会被认真聆听，你可以与整个团队的同学进行思想碰撞，点燃创意的火花。在这里，你遇到的不只是学长学姐，更是并肩作战的伙伴。
        </Card>
        <Card title="收获满满" :img="illu2">
                无论你想提升自己的coding能力、产品思维能力还是交互设计能力，这里都有手握多个大厂offer的学长学姐手把手教学。从0到1带你做项目，成为你简历上最亮眼的一笔！
        </Card>
        <Card title="发挥价值" :img="illu3">
                这里有梦和追梦的勇气，我们为每一个有想法的同学搭建舞台，赋予把思考变为现实以满足用户需求的勇气和能力。好的内容，值得被更多人看见！
        </Card>
    </div>
</template>