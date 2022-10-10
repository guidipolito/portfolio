<template>
    <div class="bg-blue-900 bg-gradient-to-r from-blue-900 to-black">
        <Overlay />
        <main 
            ref="main"
            class="swiper text-white h-screen w-screen !z-10" 
        >
            <div class="swiper-wrapper">

                <section class="swiper-slide flex flex-col justify-center container mx-auto">
                    <h1 class="text-6xl font-bold mb-5">Guilherme <br/>D'Ipolito</h1>
                    <p>Laravel fullstack Web developer</p>
                </section>

                <section class="swiper-slide flex flex-col justify-center container mx-auto text-center relative">
                    <h2 class="text-4xl font-bold">What can I do for you</h2>
                    <div class="mt-14 flex justify-center">
                        <Card>
                            <svg class="mx-auto" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="54" height="54"><path fill="none" d="M0 0h24v24H0z"/><path d="M4 21a1 1 0 0 1-1-1V4a1 1 0 0 1 1-1h16a1 1 0 0 1 1 1v16a1 1 0 0 1-1 1H4zm4-11H5v9h3v-9zm11 0h-9v9h9v-9zm0-5H5v3h14V5z" fill="rgba(255,255,255,1)"/></svg>
                            <h3 class="text-2xl font-semibold">Front-end</h3>
                            <p>I can develop beautiful and fast web pages that are going to attract clients to your business and increase sells.</p>
                        </Card>
                        <Card>
                            <svg class="mx-auto" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="54" height="54"><path fill="none" d="M0 0h24v24H0z"/><path d="M5 12.5c0 .313.461.858 1.53 1.393C7.914 14.585 9.877 15 12 15c2.123 0 4.086-.415 5.47-1.107 1.069-.535 1.53-1.08 1.53-1.393v-2.171C17.35 11.349 14.827 12 12 12s-5.35-.652-7-1.671V12.5zm14 2.829C17.35 16.349 14.827 17 12 17s-5.35-.652-7-1.671V17.5c0 .313.461.858 1.53 1.393C7.914 19.585 9.877 20 12 20c2.123 0 4.086-.415 5.47-1.107 1.069-.535 1.53-1.08 1.53-1.393v-2.171zM3 17.5v-10C3 5.015 7.03 3 12 3s9 2.015 9 4.5v10c0 2.485-4.03 4.5-9 4.5s-9-2.015-9-4.5zm9-7.5c2.123 0 4.086-.415 5.47-1.107C18.539 8.358 19 7.813 19 7.5c0-.313-.461-.858-1.53-1.393C16.086 5.415 14.123 5 12 5c-2.123 0-4.086.415-5.47 1.107C5.461 6.642 5 7.187 5 7.5c0 .313.461.858 1.53 1.393C7.914 9.585 9.877 10 12 10z" fill="rgba(255,255,255,1)"/></svg>
                            <h3 class="text-2xl font-semibold">Back-end</h3>
                            <p>I'm able to deliver a expansive and robust back-end that can attend your customer and business needs.</p>
                        </Card>
                    </div>
                    <p>All with the best technologies available</p>
                    <div class="absolute bottom-12 text-center w-full">
                        <span class="cursor-pointer">Know the stack I use</span>
                    </div>
                </section>

                <MyWork />
            </div>
        </main>
    </div>
</template>

<script>
import Overlay from "../components/Overlay"
import Swiper from 'swiper/swiper-bundle.min';
import 'swiper/swiper-bundle.min.css';
import Card from '../components/Card';
import MyWork from '../components/home/MyWork';

export default {
    name: 'IndexPage',
    components: [ Overlay, Card, ListItem ],
    async mounted(){
        await this.$nextTick();
        this.slide = new Swiper(this.$refs.main, {
            direction: "vertical",
            slidesPerView: 1,
            mousewheel: true,
            spaceBetween: 30,
        })
        window.mainSlider = this.slide
    }
}
</script>

