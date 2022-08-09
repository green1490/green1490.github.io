<template>
    <ul>
        <li v-for="item in links">
            <a> 
                {{item}}
            </a>
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
        list-style-type: none;
        margin-right: 0;
        padding: 0;
        overflow: hidden;
    }

    ul {
        position: fixed;
        top: 3%;
        width: 100%;
        margin-left: 60%;
    }

    li {
        display: inline;
        float: left;
        margin-right: 3%;
        font-family: 'Press Start 2P';
    }

    li a {
        display: block;
        color: white;
        text-align: center;
        text-decoration: none;
    }

    /* Change the link color to #111 (black) on hover */
    li a:hover {
        color: rgb(31, 168, 127);
    }
</style>