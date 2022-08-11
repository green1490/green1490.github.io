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
        padding: 0;
    }

    ul {
        position: fixed;
        top: 3%;
        width: 80%;
    }

    li {
        display: inline;
        float: right;
        margin-right: 3%;
        font-family: 'Press Start 2P';
    }

    li a {
        display: block;
        color: white;
        text-align: center;
        text-decoration: none;
        float: left;
    }

    /* Change the link color to #111 (black) on hover */
    li a:hover {
        color: rgb(31, 168, 127);
    }
</style>