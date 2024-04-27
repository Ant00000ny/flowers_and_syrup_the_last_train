<template>
    <div>
        <div class="overscroll-none scale-105 pointer-events-none absolute top-0 left-0 z-50 h-screen w-screen bg-[url('/電車_no_title.png')] bg-cover bg-center bg-no-repeat shake-animation"></div>
        <div class="overscroll-none flex overflow-x-auto hide-scrollbar" ref="images">
            <img class="h-screen object-cover img-blur-to-white" src="/screenshots/1-もうじき夏が終わるから.png" alt="">
            <img class="h-screen object-cover img-blur-to-white" src="/screenshots/2-無人駅.png" alt="">
            <img class="h-screen object-cover img-blur-to-white" src="/screenshots/3-始発とカフカ.png" alt="">
            <img class="h-screen object-cover img-blur-to-white" src="/screenshots/4-ウミユリ海底譚.png" alt="">
            <img class="h-screen object-cover img-blur-to-white" src="/screenshots/5-背景、夏に溺れる.png" alt="">
            <img class="h-screen object-cover img-blur-to-white" src="/screenshots/6-ヒグレギ.png" alt="">
            <img class="h-screen object-cover img-blur-to-white" src="/screenshots/7-透明エレジ.png" alt="">
            <img class="h-screen object-cover img-blur-to-white" src="/screenshots/8-メリュー.png" alt="">
            <img class="h-screen object-cover img-blur-to-white" src="/screenshots/9-着火、カウントダウン.png" alt="">
            <img class="h-screen object-cover img-blur-to-white" src="/screenshots/10-ずっと空を見ていた.png" alt="">
            <img class="h-screen object-cover img-blur-to-white" src="/screenshots/11-夜明けと蛍.png" alt="">
        </div>
    </div>
    <div class="fixed top-0 right-0 z-50 transition-all translate-x-[93%] hover:translate-x-0">
        <iframe frameborder="no" border="0" marginwidth="0" marginheight="0" width=330 height=450 src="//music.163.com/outchain/player?type=1&id=3190774&auto=1&height=430"></iframe>
    </div>
</template>

<script setup>
import anime from "animejs";

let images = ref(null);

onMounted(() => {
    anime({
        targets: images.value,
        scrollLeft: images.value.scrollWidth,
        duration: 100000,
        easing: "linear",
        loop: true
    })
});
</script>

<style scoped>
.hide-scrollbar::-webkit-scrollbar {
    display: none;
}

.hide-scrollbar {
    -ms-overflow-style: none;
    scrollbar-width: none;
}

.shake-animation {
    animation: shake 3s both infinite;
}

@keyframes shake {
    0%, 100% {
        transform: translateX(-1px);
    }
    10%, 30%, 50%, 70%, 90% {
        transform: translateX(2px);
    }
    20%, 40%, 60%, 80% {
        transform: translateX(-2px);
    }
}

.img-blur-to-white {
    mask-image: linear-gradient(to right, rgba(0, 0, 0, 0) 0%, rgba(0, 0, 0, 0.5) 10%, rgba(0, 0, 0, 0.5) 90%, rgba(0, 0, 0, 0) 100%);
}
</style>
