<template>
    <div class="header-container">
        <p class="header-text">Acumen Digital Interview Task / Elephantom <span v-if="$route.name === 'elephant'">&gt; {{ $route.name.charAt(0).toUpperCase() + $route.name.slice(1) }}</span></p>
    </div>
</template>

<script>
    export default {
        
    }
</script>

<style lang="css" scoped>
    .header-container {
        width: 75vw;
        height: 13vh;
        background: #FFFFFF;
        box-shadow: 0px -7px 24px rgba(0, 0, 0, 0.25);
        padding: auto 2vw;
        display: flex;
        align-items: center;
        padding-left: 3vw;
    }
</style>