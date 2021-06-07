<template>
    <div class="elephant-container">
        <div class="image-div">
            <img src="~assets/images/elephantPic.png" alt="elephant">
        </div>
        <div class="heading"><h2>Tuffi</h2><span>Female</span></div>
        <hr>
        <p class="text-body">A female circus elephant that became famous in Germany during 1950 when she accidentally fell into the River Wupper, and survived.</p>
    </div>
</template>

<script>
    export default {
        
    }
</script>

<style lang="css" scoped>
    .elephant-container {
        display: flex;
        flex-direction: column;
        justify-content: flex-start;
        overflow-x: hidden
    }
    .heading {
        margin: 5vh;
        display: flex;
        flex-direction: row;
    }
    .text-body {
        font-family: Overpass;
        font-style: normal;
        font-weight: normal;
        font-size: 24px;
        line-height: 37px;
        margin-top: 2vh;
        color: #30425A;
    }
    
</style>