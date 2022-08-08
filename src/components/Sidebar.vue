<template>
    <div class="sidenav">
        <a href="" >
            <img src="../assets/icons/github.png" alt="github icon">
        </a>
        <a href="#">
            <img src="../assets/icons/linkedin.png" alt="linkedin icon">
        </a>
    </div>
</template>

<style scoped>
    .sidenav {
        height: 100%; /* Full-height: remove this if you want "auto" height */
        /* change dynamic  */
        width: 10%; /* Set the width of the sidebar */
        position: fixed; /* Fixed Sidebar (stay in place on scroll) */
        z-index: 1; /* Stay on top */
        top: 60%; /* Stay at the top */
        left: 0px;
        overflow-x: hidden; /* Disable horizontal scroll */
        padding-top: 20px;
    }

    /* The navigation menu links */
    .sidenav a {
        padding: 6px 8px 6px 16px;
        text-decoration: none;
        font-size: 25px;
        display: block;
    }

    img {
        width: 50px
    }
</style>