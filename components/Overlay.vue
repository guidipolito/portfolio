<template>
    <div>
        <div class="overlay fullScreen"
            ref="overlay"
        />
        <canvas ref="particles" class="fullScreen particles"></canvas>
    </div>
</template>

<script>
export default {
    name: 'Overlay',
    mounted(){
        let overlay = this.$refs.overlay
        let lock = false
        window.addEventListener('mousemove', e=>{
            if(lock == true)return true;
            lock = true
            let x = e.screenX / window.screen.availWidth * 100
            let y = e.screenY / window.screen.availHeight * 100
            overlay.style.backgroundPosition = `${x}% ${y}%`
            setTimeout(()=>lock = false, 100)
        })
        this.startBg()
    }, 
    methods: {
        startBg(){

            let canvas = this.$refs.particles
            let dimensions = document.body.getBoundingClientRect()
            let bodyHeight = dimensions.height
            let bodyWidth = dimensions.width
            const setCanvasSize = ()=>{
                canvas.width = window.innerWidth
                canvas.height = window.innerHeight
                let dimensions = document.body.getBoundingClientRect()
                bodyHeight = dimensions.height
                bodyWidth = dimensions.width
            }
            setCanvasSize()
            window.addEventListener('resize', setCanvasSize)

            const ctx = canvas.getContext('2d')

            const getRandomInt = (min, max)=>{
            min = Math.ceil(min);
            max = Math.floor(max);
            return Math.floor(Math.random() * (max - min) + min);
            }

            class dot{
            constructor(x=false, y=false){
                this.offsetOrigin = window.pageYOffset
                this.depth = getRandomInt(1,8)
                this.x = x === false ? getRandomInt(0, canvas.width) : x;
                this.y = y === false ? getRandomInt(0, window.mainSlider?.virtualSize ?? bodyHeight) : y;
                this.yv = -0.1 * this.depth
                //this.xv = 0.1 * this.depth
                this.color = '#fff'
            }
            drawCircle(){
                ctx.beginPath()
                ctx.arc(this.x, this.y - (window.mainSlider?.getTranslate()*-1 ?? 0)/8*this.depth, this.depth / 2, 0, 2 * Math.PI, false)
                ctx.fillStyle = this.color
                ctx.fill()
            }
            render(){
                this.y = this.y + this.yv
                if(this.y < 0 ){
                    this.y = document.body.getBoundingClientRect().height + 1
                }
                this.drawCircle()
            }
            }
            let dotsInScreen = 30
            let elements = []
            for(let i = 0; i<dotsInScreen; i++){
            elements.push(new dot)
            }

            const animate = () => {
                ctx.clearRect(0, 0, canvas.width, canvas.height)
                let lastOffset = window.pageYOffset
                for(let i = 0; i<elements.length; i++){
                    elements[i].render()
                }
            requestAnimationFrame(animate)
            }
        animate()
        }
    }
}
</script>

<style scoped>
.fullScreen{
    width: 100vw;
    height: 100vh;
    position: fixed;
    top: 0;
    left: 0;
    pointer-events: none;
}
.overlay{
    background-image: radial-gradient(transparent, rgba(0,0,0,.69));
    background-size: 200% 200%;
    z-index:5;
    transition: .2s;
}
.particles{
    filter: blur(1px)
}
</style>
