<template>
    <div class="sidebar-container">
        <div class="elephant-logo">
            <img src="~/assets/images/elephant-logo.svg" alt="logo">
        </div>
        <div class="link-div">
            <div class="links">
                <NuxtLink to="/"><p class="link-tags">Home</p></NuxtLink>
                <NuxtLink to="/elephant"><p class="link-tags">Elephant</p></NuxtLink>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        
    }
</script>

<style lang="css" scoped>
    .sidebar-container {
        width: 25vw;
        height: 100%;
        left: 0px;
        top: 0px;
        background: #DDDDFF;
        display: flex;
        justify-content: flex-start;
        flex-direction: column;
        align-items: center;
        padding-top: 56px;
        overflow-y: hidden;
        position: fixed;
    }
    a {
        text-decoration: none;
        font-style: normal;
        font-weight: normal;
        font-size: 18px;
        line-height: 28px;
        color: #30425A;
    }
    .link-tags:hover {
        background: #B9B9FF;
        width: 25vw;
        color: #ffffff;
        text-align: left;
        margin: 0;
        padding: 2.5vh 4vw;
    }
    a .link-tags:active {
        background: #B9B9FF;
        width: 25vw;
        color: #ffffff;
        text-align: left;
        margin: 0;
        padding: 2.5vh 4vw;
    }
    a .link-tags:focus {
        background: #B9B9FF;
        width: 25vw;
        color: #ffffff;
        text-align: left;
        margin: 0;
        padding: 2.5vh 4vw;
    }
    .link-tags {
        width: 25vw;
        text-align: left;
        margin: 0;
        padding: 2.5vh 4vw;
    }
    .link-div {
        margin-top: 3vh;
    }
</style>