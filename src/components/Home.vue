<template>
    <div>
        <p class="text text-[10px] md:text-base lg:text-2xl xl:text-4xl 2xl:text-5xl bg-clip-text text-transparent bg-gradient-to-r from-pink-500 to-violet-500">Hi,</p>
        <p class="text text-[10px] md:text-base lg:text-2xl xl:text-4xl 2xl:text-5xl bg-clip-text text-transparent bg-gradient-to-r from-pink-500 to-violet-500">I'm Zámbó Krisztián,</p>
        <p class="text text-[10px] md:text-base lg:text-2xl xl:text-4xl 2xl:text-5xl bg-clip-text text-transparent bg-gradient-to-r from-pink-500 to-violet-500">software developer</p>
    </div>
</template>

<script>
import anime from 'animejs';

export default {
        
    data() {
        return {
            width:window.innerWidth
        }
    },
    
    methods: {
        anime() {
            anime({
                targets: '.text',
                translateX: (30),
                direction: 'alternate',
                loop: true,
                delay: function(el, i, l) {
                    return i * 100;
                },
                endDelay: function(el, i, l) {
                    return (l - i) * 100;
                    }
            });
        }
    },
    
    mounted() {
        this.anime();
    },

    unmounted() {
        this.anime();
    }
}
</script>
