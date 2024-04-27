<template>
    <div>
        <div class="overscroll-none scale-105 pointer-events-none absolute top-0 left-0 z-50 h-screen w-screen bg-[url('/電車.png')] bg-cover bg-center bg-no-repeat shake-animation"></div>
        <div class="overscroll-none flex overflow-x-auto hide-scrollbar" ref="images">
            <img class="h-screen object-cover" src="/test.png" alt="">
            <img class="h-screen object-cover" src="/test.png" alt="">
            <img class="h-screen object-cover" src="/test.png" alt="">
            <img class="h-screen object-cover" src="/test.png" alt="">
            <img class="h-screen object-cover" src="/test.png" alt="">
            <img class="h-screen object-cover" src="/test.png" alt="">
            <img class="h-screen object-cover" src="/test.png" alt="">
            <!-- Repeat for other images -->
        </div>
    </div>
</template>

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
</style>
