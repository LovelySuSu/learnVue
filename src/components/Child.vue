<template>
    <div>
        <button @click="sendMsgToFather">点击发送信息给父组件</button>
    </div>
</template>

<script>
    export default {
        name: 'Child',
        data () {
            return {

            }
        },
        methods:{
            sendMsgToFather(){
                this.$emit('tell_dad','Msg From Child');
            }
        }
    }

</script>

<style scoped>
    button{
        border: 1px solid black;
    }
</style>
