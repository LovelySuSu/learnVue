<template>
    <div>
        <h1>{{ tell_son }}</h1>
    </div>
</template>

<script>
    export default {
        name: 'Son',
        data () {
            return {

            }
        },
        props:['tell_son']
    }
</script>

<style scoped>
    h1, h2 {
        font-weight: normal;
    }
    ul {
        list-style-type: none;
        padding: 0;
    }
    li {
        display: inline-block;
        margin: 0 10px;
    }
    a {
        color: #42b983;
    }
</style>
