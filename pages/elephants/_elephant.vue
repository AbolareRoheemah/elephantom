<template>
    <div class="elephant-container">
        <div class="image-div">
            <img src="~assets/images/elephantPic.png" alt="elephant">
        </div>
        <div class="heading"><h2>{{ elephantName }}</h2><span>{{ elephantSex }}</span></div>
        <hr>
        <p class="text-body">{{ note }}</p>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                elephantName: '',
                elephantSex: '',
                note: '',
            }
        },
        props: ['elephant'],
        methods: {
            getElephants() {
            let baseUrl = 'https://elephantapimary3.herokuapp.com'
            let id = this.elephant
            fetch(baseUrl + '/elephants/id/' + id)
            .then(res => res.json())
            .then((data) => {
                let name = data.elephant.name
                this.elephantName = name.charAt(0).toUpperCase() + name.slice(1)
                this.elephantSex = data.elephant.sex
                this.note = data.elephant.note
            })
            }
        },
        created () {
        this.getElephants()
        },
    }
</script>

<style lang="css" scoped>
    .elephant-container {
        display: flex;
        flex-direction: column;
        justify-content: center;
        overflow-x: hidden
    }
    .heading {
        margin: 5vh;
        display: flex;
        flex-direction: row;
        justify-content: flex-start
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
    h2 {
        margin-right: 1vw;
    }
    span {
        margin-top: 1vh;
    }
    
</style>