<template>
    <div>
        {{hh('什么鬼东西')}}
        <a :href="website">baidu</a>
        <p @click="top">{{time}}</p>
        <div id="canvas" @mousemove.once="update">
            {{x}},{{y}}
        </div>
    </div>
</template>
<script>
export default {
    data() {
        return {
            x:0,
            y:0,
            time:0,
            ff: '秦俊',
            website:"https://www.baidu.com"
        }
    },
    methods:{
        update(event){
            this.x=event.clientX
            this.y=event.clientY
            console.log(event)
        },
        hh(arg){
            return `jjjj ${arg} ${this.ff}`;
        },
        top(event){
            console.log(event)
            return `${this.time++}`
        }
    }
}
</script>
<style scoped>
    #canvas{
        width:500px;
        padding: 10px;
        height:200px;
        border:1px solid red
    }
</style>