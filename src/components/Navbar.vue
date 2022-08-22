<template>
    <ul>
        <li v-for="item in links" class="text-[10px] sm:text-base xl:text-lg 2xl:text-xl">
            <a> 
                {{item}}
            </a>
        </li>
        <li>
            <button type="button" class="text-white bg-[#3b5998] hover:bg-[#3b5998]/90 px-5 py-2.5 text-center inline-flex items-center dark:focus:ring-[#3b5998]/55 mr-2 mb-2 font-medium rounded-lg text-[10px] lg:text-sm 2xl:text-xl">
                Github
            </button>
            <button type="button" class="text-white bg-[#3b5998] hover:bg-[#3b5998]/90 px-5 py-2.5 text-center inline-flex items-center dark:focus:ring-[#3b5998]/55 mr-2 mb-2 font-medium rounded-lg text-[10px] lg:text-sm 2xl:text-xl">
                LinkedIn
            </button>
        </li>
    </ul>
</template>

<script lang="ts">
export default {
    data() {
        return {
            links: [
                "About",
                "Experience",
                "Project"
            ]
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
        width: 80%;
        display: flex;
        flex-direction: row;
        justify-content: right;
        align-items: baseline;
        flex-wrap: wrap;
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
</style>