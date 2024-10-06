<script>
import SectionTitle from './elements/SectionTItle.vue';
import Card from './membersTalk/Card.vue'
import SelectButton from './membersTalk/SelectButton.vue';
import Highlight from './elements/Highlight.vue';
export default {
    data() {
        return {
            selected: 0,
            avatarRed: new URL("/assets/membersTalk/red.svg", import.meta.url),
            avatarBlue: new URL("/assets/membersTalk/blue.svg", import.meta.url),
            avatarYellow: new URL("/assets/membersTalk/yellow.svg", import.meta.url),
        }
    },
    components: {
        SectionTitle,
        Card,
        SelectButton,
        Highlight
    },
    methods: {
        next() {
            if (this.selected < 5) this.selected++
        },
        prev() {
            if (this.selected > 0) this.selected--
        }
    },
    computed: {
        offset() {
            let i = this.selected
            return `calc(50% - 0.5 * 723px - ${i * 723}px)`
        }
    }

}
</script>

<template>
    <SectionTitle title="学长学姐说" />
    <div class="w-full h-fit">
        <div class="absolute w-screen left-1/2 -translate-x-1/2 h-[520px] z-10"
        style="background: linear-gradient(to right, #f5f5f5 0%, rgb(250 250 250 / 0) 33%,rgb(250 250 250 / 0) 67%, #f5f5f5 100%)">
        </div>
        <div class="flex w-fit relative" :style="{ left: offset }" style="transition: left 0.4s ease">
            <Card :img="avatarBlue">
                <template #name>
                    @zekin「技术组」
                </template>
                <template #info>
                    22级-计算机学院
                </template>
                <template #achievements>
                    <div class="flex gap-2">
                        <Highlight>北邮摸鱼硕士</Highlight>
                        <span>大厂实习</span>
                    </div>
                    <div class="flex gap-2">
                        <span>救火队长</span>
                        <Highlight>各类竞赛奖项</Highlight>
                    </div>
                </template>
                <template #content>
                    从构建处理器的第一个门电路开始……到串联起每一个北邮人的计算机网络……再到服务北邮人的各种服务，在这里你可以体验计算机的方方面面。现在，开启你最伟大的探索吧：从计算机体系结构到计算机网络技术实践。
                </template>
            </Card>

            <Card :img="avatarRed">
                <template #name>
                    @+1「新媒体组」
                </template>
                <template #info>
                    17级-数字媒体设计学院
                </template>
                <template #achievements>
                    <Highlight>北邮人产品设计新媒体前负责人</Highlight>
                    <span>活力研究生</span>
                    <Highlight>退休老干部(除了技术啥都干)</Highlight>
                </template>
                <template #content>
                    BYR
                    Team在北邮是一个响当当的名号，在这里确实认识了很多技术巨巨、设计大佬、运营鬼才。重要的是大家都有有趣而自由的灵魂，团队也有供大家自由创作和发挥才能的空间。可能有些组织退出了就不再联系，但加入BYR
                    Team，就会一直都是BYR Team的一员。我们有自己的传承，我们拥抱新人。
                </template>
            </Card>

            <Card :img="avatarBlue">
                <template #name>
                    @Makiras「技术组」
                </template>
                <template #info>
                    18级-计算机学院
                </template>
                <template #achievements>
                    <div class="flex gap-2"><span>前技术组划水负责人</span>
                        <Highlight>中科院在读博士</Highlight>
                    </div>
                    <div class="flex gap-2">
                        <Highlight>初创&大厂实习</Highlight>
                        <span>人工SMT&BGA平台</span>
                    </div>
                </template>
                <template #content>
                    在这里可以接触各路神仙，挑战各种问题，发展各式能力，探索各类可能。一个自驱的团队可以帮你能力与乐趣两开花，解决现实问题的同时丰富你的履历。如果你觉得 [这里忘了]
                    就去建设它，那这里就是最适合的地方，改变北邮的机会正触手可及！ It's now or never!
                </template>
            </Card>

            <Card :img="avatarYellow">
                <template #name>
                    @momo「新媒体组」
                </template>
                <template #info>
                    21级-网络空间安全学院
                </template>
                <template #achievements>
                    <Highlight>永远年轻的大三学姐^^</Highlight>
                    <span>可进可退可盐可甜</span>
                    <span>除了工科摄影遛狗插花啥都干</span>
                    <Highlight>国奖获得者</Highlight>
                </template>
                <template #content>
                    年级（纪）越大，BYR
                    Team越成为我的快乐老家，可可爱爱的学妹，温温柔柔的学弟，酷酷飒飒的老板老板娘以及一些可爱的小碎嘴子。成年人的生活太需要这样的轻松和志趣，我们是线上的好友和伙伴，也是线下的小姐妹、好朋友。如果一定要用一个词来形容我们，那便是松弛与理想并存吧。
                </template>
            </Card>

            <Card :img="avatarBlue">
                <template #name>
                    @好圆圆圆「产品组」
                </template>
                <template #info>
                    20级-数字媒体设计学院
                </template>
                <template #achievements>
                    <div class="flex gap-2">
                        <Highlight>国奖获得者</Highlight>
                        <span>支教团美术老师一枚</span>
                    </div>
                    <div class="flex gap-2">
                        <span>德艺双馨</span>
                        <Highlight>十余项设计竞赛获奖</Highlight>
                    </div>
                </template>
                <template #content>
                    在北邮人团队，你会收获亲自设计的项目上线服务全体北邮人的机会，你会收获为同一目标努力工作的好友，欢迎你加入北邮人团队大家庭，收获属于自己的未来！
                </template>
            </Card>

            <Card :img="avatarRed">
                <template #name>
                    @Sprr「设计组」
                </template>
                <template #info>
                    20级-数字媒体设计学院
                </template>
                <template #achievements>
                    <span>三好学生</span>
                    <Highlight>智育top1</Highlight>
                    <Highlight>没有滑板的铲屎官不是好设计师</Highlight>
                </template>
                <template #content>
                    这里有最自由和包容的土壤，有最可爱和有趣的灵魂。发现问题、设计构思、解决问题。在北邮人，让设计真正的落地，服务更多的人。
                </template>
            </Card>
        </div>
    </div>

    <div class="flex h-fit -mt-40 justify-end gap-4 [&>*]:z-50">
        <SelectButton :clickable="selected != 0" @click="prev"></SelectButton>
        <SelectButton :clickable="selected != 5" @click="next" class=" scale-x-[-1]"></SelectButton>
    </div>
</template>