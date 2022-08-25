<template>
    <ul class="flex flex-col lg:flex-row justify-end content-end flex-wrap lg:flex-nowrap gap-8 w-9/12 lg:10/12">
        <button @click="show = !show" class="self-end lg:hidden">
            <svg viewBox="0 0 100 80" width="30" height="30" style="fill:rgb(255,255,255)">
                <rect width="100" height="20"></rect>
                <rect y="30" width="100" height="20"></rect>
                <rect y="60" width="100" height="20"></rect>
            </svg>
        </button>
        <TransitionGroup name="fade">
            <li v-for="item in links" class="text-[10px] md:text-xl lg:text-sm xl:text-lg 2xl:text-xl" v-if="show || windowWidth >= 1024">
                <RouterLink :to="'/' + item.toLowerCase( )">
                    {{item}}
                </RouterLink>
            </li>
            <li class="text-[10px] md:text-xl lg:text-sm xl:text-lg 2xl:text-xl" v-if="show || windowWidth >= 1024">
                <a>Github</a>
            </li>
            <li class="text-[10px] md:text-xl lg:text-sm xl:text-lg 2xl:text-xl" v-if="show || windowWidth >= 1024">
                <a>LinkedIn</a>
            </li>
        </TransitionGroup>
    </ul>
</template>

<script lang="ts">
export default {
    data() {
        return {
            links: [
                "Home",
                "About",
                "Experience",
                "Project"
            ],
            show: false,
            windowWidth: window.innerWidth
        }
    }
}
</script>

<style scoped>
    ul {
        padding: 0;
    }

    ul {
        position: fixed;
        top: 3%;
        align-items: baseline;
    }

    li {
        margin-right: 3%;
        font-family: 'Press Start 2P';
    }

    li a {
        color: white;
        text-decoration: none;
    }

    /* Change the link color to #111 (black) on hover */
    li a:hover {
        color: rgb(31, 168, 127);
    }

    .fade-enter, .fade-leave-to {
        opacity: 0;
        transform: translateX(2em);
    }

    .fade-enter-active, .fade-leave-active {
        transition: all .3s ease;
    }
</style>