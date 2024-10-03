<script>
import MyMsg from './MyMsg.vue';
import ReceivedMsg from './ReceivedMsg.vue';
export default {
    components: {
        MyMsg,
        ReceivedMsg
    }

}
</script>

<template>
    <div class="absolute w-full max-h-full overflow-y-scroll rounded-xl border-[0.5px] bg-[#F6F8FC]">
        <header
            class="sticky top-0 z-10 bg-[#F6F8FC] flex h-[75px] items-center justify-between border-b-[0.5px] px-4 text-[#333] max-sm:py-2 sm:py-4">
            <div class=" text-2xl leading-[180%] tracking-[4.8px]">
                🎉招新啦🎉
            </div>
        </header>
        <section class="flex flex-col gap-5 my-5 h-fill overflow-hidden">
            <MyMsg time="05:04 PM" id="You" avatar="src/assets/groupInfo/avatar1.svg">
                <span class="myMsg">新媒体组好酷啊！好想加！！❤</span>
            </MyMsg>

            <div class="text-center leading-[180%] opacity-60 max-sm:text-xs sm:text-base">
                北邮人团队 新媒体组 拍了拍 你，并发送了一条加群邀请
            </div>

            <ReceivedMsg time="05:06 PM" id="新媒体组某不知名成员壹" avatar="src/assets/groupInfo/avatar2.svg">
                <span class="receiveMsg">Hi，欢迎来到有趣灵魂聚集地新媒体组！ 我们是——</span>
                <span class="receiveMsg">＃生活观察员＃</span>
                <span class="receiveMsg">
                    <p>
                        在这里，与你同行，写你所想。
                    </p>
                    <p>
                        我们驻守在官方新媒体平台，捕捉校园生活中的小确幸、小美好，以图文定格北邮人的独家记忆。
                    </p>
                </span>
                <span class="receiveMsg">
                    <div
                        class="flex justify-between max-sm:flex-col [&amp;>div]:flex [&amp;>div]:flex-col [&amp;>div]:gap-[2px]">
                        <div>
                            <div class="relative block w-fit">
                                <div
                                    class="absolute bottom-0 box-content h-3/5 w-full pr-8 bg-gradient-to-r from-[#DAFF47] to-[#D9D9D900] opacity-40">
                                </div>
                                <div
                                    class="relative whitespace-nowrap text-center leading-[180%] max-sm:text-base sm:text-xl">
                                    #春日邮啊邮：</div>
                            </div>
                            <div class="flex items-start gap-1"><a
                                    class="leading-[180%] underline max-sm:text-sm sm:text-lg"
                                    href="https://mp.weixin.qq.com/s/vI0UQ144QMib4nX00E_mNw" rel="noreferrer noopener"
                                    target="_blank">藏在北三环里的小众宝藏打卡地 </a><svg xmlns="http://www.w3.org/2000/svg"
                                    width="24" height="25" fill="none" viewBox="0 0 24 25">

                                    <defs>
                                        <clipPath id="clip0_496_4187">
                                            <path fill="#fff" d="M0 .104h24v24H0z"></path>
                                        </clipPath>
                                    </defs>
                                </svg></div>
                            <div class="flex items-start gap-1"><a
                                    class="leading-[180%] underline max-sm:text-sm sm:text-lg"
                                    href="https://mp.weixin.qq.com/s/ADSExMLzODeZxSbGP_Lg2Q" rel="noreferrer noopener"
                                    target="_blank">北六环约会圣地，城区40min可达 </a><svg xmlns="http://www.w3.org/2000/svg"
                                    width="24" height="25" fill="none" viewBox="0 0 24 25">

                                    <defs>
                                        <clipPath id="clip0_496_4187">
                                            <path fill="#fff" d="M0 .104h24v24H0z"></path>
                                        </clipPath>
                                    </defs>
                                </svg></div>
                            <div class="flex items-start gap-1"><a
                                    class="leading-[180%] underline max-sm:text-sm sm:text-lg"
                                    href="https://mp.weixin.qq.com/s/lC57Iya44k2g7KoiVcjtMw" rel="noreferrer noopener"
                                    target="_blank">春日邮花图鉴</a><svg xmlns="http://www.w3.org/2000/svg" width="24"
                                    height="25" fill="none" viewBox="0 0 24 25">
                                    <defs>
                                        <clipPath id="clip0_496_4187">
                                            <path fill="#fff" d="M0 .104h24v24H0z"></path>
                                        </clipPath>
                                    </defs>
                                </svg></div>
                        </div>
                        <div>
                            <div class="relative block w-fit">
                                <div
                                    class="absolute bottom-0 box-content h-3/5 w-full pr-8 bg-gradient-to-r from-[#DAFF47] to-[#D9D9D900] opacity-40">
                                </div>
                                <div
                                    class="relative whitespace-nowrap text-center leading-[180%] max-sm:text-base sm:text-xl">
                                    #北邮爱情故事：</div>
                            </div>
                            <div class="flex items-start gap-1"><a
                                    class="leading-[180%] underline max-sm:text-sm sm:text-lg"
                                    href="https://mp.weixin.qq.com/s/Fg4ETkdX0Z1qlUBazAE7DA" rel="noreferrer noopener"
                                    target="_blank">BYR七夕不规则访谈</a><svg xmlns="http://www.w3.org/2000/svg" width="24"
                                    height="25" fill="none" viewBox="0 0 24 25">

                                    <defs>
                                        <clipPath id="clip0_496_4187">
                                            <path fill="#fff" d="M0 .104h24v24H0z"></path>
                                        </clipPath>
                                    </defs>
                                </svg></div>
                            <div class="flex items-start gap-1"><a
                                    class="leading-[180%] underline max-sm:text-sm sm:text-lg"
                                    href="https://mp.weixin.qq.com/s/oGQ9BGFT-Lt0YjMN4RoVGg" rel="noreferrer noopener"
                                    target="_blank">BYR520约会方式一览 </a><svg xmlns="http://www.w3.org/2000/svg" width="24"
                                    height="25" fill="none" viewBox="0 0 24 25">

                                    <defs>
                                        <clipPath id="clip0_496_4187">
                                            <path fill="#fff" d="M0 .104h24v24H0z"></path>
                                        </clipPath>
                                    </defs>
                                </svg></div>
                        </div>
                    </div>
                </span>
            </ReceivedMsg>

            <ReceivedMsg time="05:12 PM" id="新媒体组某不知名成员贰" avatar="src/assets/groupInfo/avatar3.svg">
                <span class="receiveMsg">我们也是——</span>
                <span class="receiveMsg">＃浪漫的幻想家＃</span>
                <span class="receiveMsg">
                    <p>在这里，梦境碰撞现实，一切皆有可能。</p>
                    <p>
                        我们点燃灵感的焰火，将天马行空的脑洞付诸笔下，摘星揽月、逐光织梦。</p>
                </span>
                <span class="receiveMsg">
                    <p>
                        <a class="leading-[180%] underline max-sm:text-sm sm:text-lg"
                            href="https://mp.weixin.qq.com/s/SPhbDiPZIETY8QqiC4rwSw" rel="noreferrer noopener"
                            target="_blank">世界破破烂烂，小动物缝缝补补</a>
                    </p>
                    <p>
                        <a class="leading-[180%] underline max-sm:text-sm sm:text-lg"
                            href="https://mp.weixin.qq.com/s/HCklNWP5T37ukMYtgPVYpg" rel="noreferrer noopener"
                            target="_blank">超能力与副作用的化学反应</a>
                    </p>
                </span>
            </ReceivedMsg>
        </section>
        <footer class="bg-white p-4 sticky bottom-0">
            <div
                class="flex items-center justify-between rounded-full bg-[#F6F8FC] text-[#333] max-md:px-6 max-md:py-[6px] md:px-11 md:py-3">
                <div
                    class="border-r-[2px] max-sm:pr-3 sm:pr-6 [&amp;>svg]:cursor-pointer [&amp;>svg]:max-sm:h-5 [&amp;>svg]:max-sm:w-5">
                    <img src="/src/assets/groupInfo/link.svg" fill="#fff">
                </div>
                <input
                    class="min-w-0 bg-transparent py-[3px] outline-none placeholder:tracking-[2.16px] max-sm:shrink max-sm:px-4 sm:grow sm:px-7"
                    placeholder="请输入..." type="text">
                <div
                    class="flex justify-between gap-7 ">
                    <img src="/src/assets/groupInfo/emoji.svg"/>
                    <img src="/src/assets/groupInfo/image.svg" />
                    <img src="/src/assets/groupInfo/location.svg" />
                    </div>
            </div>
        </footer>
    </div>
</template>
