
<template>
    <main>

        <div class="effects">
        </div>
        <div class="main-container">
            <router-view></router-view>
        </div>


        <div id="g-cursor" :class="['g-cursor', { 'g-cursor_hover': hover }, { 'g-cursor_hide': hideCursor }]">
            <div :style="cursorCircle" class="g-cursor__circle"></div>
            <div :style="cursorCircle2" class="g-cursor__circle2"></div>
            <div class="g-cursor__point" ref="point" :style="cursorPoint"></div>
        </div>
    </main>
</template>


<script>
export default {
    data() {
        return {
            xChild: 0,
            yChild: 0,
            xParent: 0,
            yParent: 0,
            yParentLarge: 0,
            xParentLarge: 0,
            hover: false,
            hideCursor: true
        }
    },
    computed: {
        cursorCircle() {
            return `transform: translateX(${this.xParent}px)
            translateY(${this.yParent}px)
            translateZ(0)
            translate3d(0, 0, 0)
            scale(0.5);
            `
        },
        cursorCircle2() {
            return `transform: translateX(${this.xParentLarge}px)
    translateY(${this.yParentLarge}px)
    translateZ(0)
    translate3d(0, 0, 0)
    scale(0.5);
    `
        },
        cursorPoint() {
            return `transform:
            translateX(${this.xChild - 3}px)
            translateY(${this.yChild - 3}px)
            translateZ(0)
            translate3d(0, 0, 0);`
        }
    },
    methods: {
        moveCursor(e) {
            this.xChild = e.clientX;
            this.yChild = e.clientY;
            setTimeout(() => {
                this.xParent = e.clientX - 14.5;
                this.yParent = e.clientY - 14.5;
            }, 50);
            setTimeout(() => {
                this.xParentLarge = e.clientX - 22;
                this.yParentLarge = e.clientY - 22;
            }, 100);
        }
    },
    mounted() {
        document.addEventListener("mousemove", this.moveCursor);
        document.addEventListener('mouseleave', e => {
            this.hideCursor = true;
        });
        document.addEventListener('mouseenter', e => {
            this.hideCursor = false;
        });
        const ahref = document.querySelectorAll('a')
        ahref.forEach(aa => {
            aa.addEventListener('mouseenter', () => {
                this.hover = true;
                this.hideCursor = true;
            })
        });
        ahref.forEach(aa => {
            aa.addEventListener('mouseleave', () => {
                this.hover = false;
                this.hideCursor = false;
            })
        })



    }
};

</script>


<style lang="scss">
.movearea {
    transition: 0.3s background-color ease;
}
</style>

