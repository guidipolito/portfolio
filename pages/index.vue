<template>
    <div class="bg-blue-900 bg-gradient-to-r from-blue-900 to-black">
        <Overlay />
        <main 
            ref="main"
            class="swiper text-white h-screen w-screen !z-10" 
        >
            <div class="swiper-wrapper">
                <section class="swiper-slide flex flex-col justify-center container mx-2 md:mx-auto">
                    <h1 class="text-6xl font-bold mb-5">Guilherme <br/>D'Ipolito</h1>
                    <p>Laravel fullstack Web developer</p>
                    <div class="flex gap-3">
                        <a class="transition-all hover:scale-125" href="https://www.linkedin.com/in/guilherme-pereira-d-ipolito-a529381a5/" target="_BLANK">
                            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="24" height="24"><path fill="none" d="M0 0h24v24H0z"/><path d="M18.335 18.339H15.67v-4.177c0-.996-.02-2.278-1.39-2.278-1.389 0-1.601 1.084-1.601 2.205v4.25h-2.666V9.75h2.56v1.17h.035c.358-.674 1.228-1.387 2.528-1.387 2.7 0 3.2 1.778 3.2 4.091v4.715zM7.003 8.575a1.546 1.546 0 0 1-1.548-1.549 1.548 1.548 0 1 1 1.547 1.549zm1.336 9.764H5.666V9.75H8.34v8.589zM19.67 3H4.329C3.593 3 3 3.58 3 4.297v15.406C3 20.42 3.594 21 4.328 21h15.338C20.4 21 21 20.42 21 19.703V4.297C21 3.58 20.4 3 19.666 3h.003z" fill="rgba(255,255,255,1)"/></svg>
                        </a>
                        <a class="transition-all hover:scale-125" href="mailto:guilhermepereiradipolito@hotmail.com" target="_BLANK">
                            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="24" height="24"><path fill="none" d="M0 0h24v24H0z"/><path d="M3 3h18a1 1 0 0 1 1 1v16a1 1 0 0 1-1 1H3a1 1 0 0 1-1-1V4a1 1 0 0 1 1-1zm9.06 8.683L5.648 6.238 4.353 7.762l7.72 6.555 7.581-6.56-1.308-1.513-6.285 5.439z" fill="rgba(255,255,255,1)"/></svg>
                        </a>
                        <a class="transition-all hover:scale-125" href="https://github.com/guidipolito" target="_BLANK">
                            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="24" height="24"><path fill="none" d="M0 0h24v24H0z"/><path d="M12 2C6.475 2 2 6.475 2 12a9.994 9.994 0 0 0 6.838 9.488c.5.087.687-.213.687-.476 0-.237-.013-1.024-.013-1.862-2.512.463-3.162-.612-3.362-1.175-.113-.288-.6-1.175-1.025-1.413-.35-.187-.85-.65-.013-.662.788-.013 1.35.725 1.538 1.025.9 1.512 2.338 1.087 2.912.825.088-.65.35-1.087.638-1.337-2.225-.25-4.55-1.113-4.55-4.938 0-1.088.387-1.987 1.025-2.688-.1-.25-.45-1.275.1-2.65 0 0 .837-.262 2.75 1.026a9.28 9.28 0 0 1 2.5-.338c.85 0 1.7.112 2.5.337 1.912-1.3 2.75-1.024 2.75-1.024.55 1.375.2 2.4.1 2.65.637.7 1.025 1.587 1.025 2.687 0 3.838-2.337 4.688-4.562 4.938.362.312.675.912.675 1.85 0 1.337-.013 2.412-.013 2.75 0 .262.188.574.688.474A10.016 10.016 0 0 0 22 12c0-5.525-4.475-10-10-10z" fill="rgba(255,255,255,1)"/></svg>
                        </a>
                    </div>
                </section>

                <section class="swiper-slide flex flex-col justify-center container mx-auto text-center relative">
                    <h2 class="text-3xl md:text-4xl font-bold">What I can do for you</h2>
                    <div class="mt-6 md:mt-14 flex justify-center flex-wrap">
                        <Card>
                            <svg class="mx-auto" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="54" height="54"><path fill="none" d="M0 0h24v24H0z"/><path d="M4 21a1 1 0 0 1-1-1V4a1 1 0 0 1 1-1h16a1 1 0 0 1 1 1v16a1 1 0 0 1-1 1H4zm4-11H5v9h3v-9zm11 0h-9v9h9v-9zm0-5H5v3h14V5z" fill="rgba(255,255,255,1)"/></svg>
                            <h3 class="text-2xl font-semibold">Front end</h3>
                            <p>I can develop beautiful and fast web pages that are going to attract clients to your business and increase sells.</p>
                        </Card>
                        <Card>
                            <svg class="mx-auto" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="54" height="54"><path fill="none" d="M0 0h24v24H0z"/><path d="M5 12.5c0 .313.461.858 1.53 1.393C7.914 14.585 9.877 15 12 15c2.123 0 4.086-.415 5.47-1.107 1.069-.535 1.53-1.08 1.53-1.393v-2.171C17.35 11.349 14.827 12 12 12s-5.35-.652-7-1.671V12.5zm14 2.829C17.35 16.349 14.827 17 12 17s-5.35-.652-7-1.671V17.5c0 .313.461.858 1.53 1.393C7.914 19.585 9.877 20 12 20c2.123 0 4.086-.415 5.47-1.107 1.069-.535 1.53-1.08 1.53-1.393v-2.171zM3 17.5v-10C3 5.015 7.03 3 12 3s9 2.015 9 4.5v10c0 2.485-4.03 4.5-9 4.5s-9-2.015-9-4.5zm9-7.5c2.123 0 4.086-.415 5.47-1.107C18.539 8.358 19 7.813 19 7.5c0-.313-.461-.858-1.53-1.393C16.086 5.415 14.123 5 12 5c-2.123 0-4.086.415-5.47 1.107C5.461 6.642 5 7.187 5 7.5c0 .313.461.858 1.53 1.393C7.914 9.585 9.877 10 12 10z" fill="rgba(255,255,255,1)"/></svg>
                            <h3 class="text-2xl font-semibold">Back end</h3>
                            <p>I'm able to deliver a expansive and robust back-end that can attend your customer and business needs.</p>
                        </Card>
                    </div>
                    <p>All with the best technologies available</p>
                </section>

                <section class="swiper-slide container flex flex-col justify-center mx-2 md:mx-auto text-center relative">
                    <h2 class="text-3xl md:text-4xl md:mb-12 font-bold">Technologies I usually work with</h2>
                    <h3 class="mt-5 font-semibold mb-1">Basic</h3>
                    <div class="flex justify-center flex-wrap gap-2">
                        <Badge>
                            <i class="devicon-html5-plain colored text-xl"></i>
                            HTML5
                        </Badge>
                        <Badge>
                            <i class="devicon-css3-plain colored text-xl"></i>
                            CSS3
                        </Badge>
                        <Badge>
                            <i class="devicon-javascript-plain colored text-xl"></i>
                            Javascript
                        </Badge>
                    </div>
                    <h3 class="mt-5 mb-1 font-semibold">Front end related</h3>
                    <div class="flex justify-center flex-wrap gap-2">
                        <Badge>
                            <i class="devicon-react-plain colored text-xl"></i>
                            React
                        </Badge>
                        <Badge>
                            <i class="devicon-vuejs-plain colored text-xl"></i>
                            Vue
                        </Badge>
                        <Badge>
                            <svg width="20" height="20" viewBox="0 0 45.116 22.806" xmlns="http://www.w3.org/2000/svg"><g opacity=".8"><path d="M33.71 0 11.207 22.693l.113.113h22.586l11.21-11.304z" fill="#d8dee9"/><path d="m11.405 0 22.578 22.769-.039.037H11.209L0 11.502z" fill="#8ac0cf"/></g></svg>
                            Alpine.js
                        </Badge>
                        <Badge>
                            <i class="devicon-tailwindcss-plain colored text-xl"></i>
                            Tailwind
                        </Badge>
                        <Badge>
                            <i class="devicon-sass-plain colored text-xl"></i>
                            SASS
                        </Badge>
                        <Badge>
                            <i class="devicon-jquery-plain colored text-xl"></i>
                            jQuery
                        </Badge>
                    </div>
                    <h3 class="mt-5 mb-1 font-semibold">Back end related</h3>
                    <div class="flex justify-center flex-wrap gap-2">
                        <Badge>
                            <i class="devicon-php-plain colored text-xl"></i>
                            PHP
                        </Badge>
                        <Badge>
                            <i class="devicon-mysql-plain colored text-xl"></i>
                            MySQL
                        </Badge>
                        <Badge>
                            <i class="devicon-laravel-plain colored text-xl"></i>
                            Laravel
                        </Badge>
                        <Badge>
                            <i class="devicon-wordpress-plain text-xl"></i>
                            Wordpress ( core )
                        </Badge>
                    </div>
                </section>

                <section 
                    class="swiper-slide flex flex-col justify-center items-center bg-gradient-to-b from-transparent to-black last-slide relative">
                    <h2 class="text-3xl font-bold mb-5">Get in contact</h2>
                    <div class="flex gap-5 items-center">
                        <a href="mailto:guilhermepereiradipolito@hotmail.com" target="_BLANK">
                            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="24" height="24"><path fill="none" d="M0 0h24v24H0z"/><path d="M22 20.007a1 1 0 0 1-.992.993H2.992A.993.993 0 0 1 2 20.007V19h18V7.3l-8 7.2-10-9V4a1 1 0 0 1 1-1h18a1 1 0 0 1 1 1v16.007zM4.434 5L12 11.81 19.566 5H4.434zM0 15h8v2H0v-2zm0-5h5v2H0v-2z" fill="rgba(249,249,249,1)"/></svg>
                        </a>
                        <CopyArea value="guilhermepereiradipolito@hotmail.com" />   
                    </div>
                    <div class="mt-5">
                        <a href="https://www.linkedin.com/in/guilherme-pereira-d-ipolito-a529381a5/" target="_BLANK">
                            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="54" height="54"><path fill="none" d="M0 0h24v24H0z"/><path d="M18.335 18.339H15.67v-4.177c0-.996-.02-2.278-1.39-2.278-1.389 0-1.601 1.084-1.601 2.205v4.25h-2.666V9.75h2.56v1.17h.035c.358-.674 1.228-1.387 2.528-1.387 2.7 0 3.2 1.778 3.2 4.091v4.715zM7.003 8.575a1.546 1.546 0 0 1-1.548-1.549 1.548 1.548 0 1 1 1.547 1.549zm1.336 9.764H5.666V9.75H8.34v8.589zM19.67 3H4.329C3.593 3 3 3.58 3 4.297v15.406C3 20.42 3.594 21 4.328 21h15.338C20.4 21 21 20.42 21 19.703V4.297C21 3.58 20.4 3 19.666 3h.003z" fill="rgba(255,255,255,1)"/></svg>
                        </a>
                    </div>
                </section>
            </div>
        </main>
    </div>
</template>

<script>
import Overlay from "../components/Overlay"
import Swiper from 'swiper/swiper-bundle.min';
import 'swiper/swiper-bundle.min.css';
import Card from '../components/Card';
import Badge from '../components/Badge';
import CopyArea from '../components/CopyArea';

export default {
    name: 'IndexPage',
    components: [ Overlay, Card, Badge, CopyArea ],
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

<style scoped>
.swiper:not(.swiper-initialized) .swiper-slide:not(:first-child){
    display: none;
}
.last-slide::after{
    content: '';
    background-color: black;
    width: 100vw;
    height: 500px;
    position: absolute;
    top:100%;
    left: 0;
}
</style>
