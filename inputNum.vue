<template>
    <div class="inputNum">
        <input class="down" @click="down" type="button" value="-">
        <span class="num">{{num}}</span>
        <input class="up" @click="up" type="button" value="+">
    </div>
</template>
<script>
export default {
    name:'inputNum',
    props:{
        numUp:{
            type:Number,
            default:1
        },
        numDown:{
            type:Number,
            default:1
        }
    },
    data(){
        return({
            num:0,
          
        })
    },
    methods: {
        down(){
            if(this.num>0){
                this.num-=this.numDown
            }
        },
        up(){
            this.num+=this.numUp
        }
    },
}
</script>
<style>
    .inputNum {
        width: 150px;
        display: flex;
    }
    .down {
        width: 50px;
        height: 40px;
        text-align: center;
        line-height: 40px;
    }
    .up {
        width: 50px;
        height: 40px;
        text-align: center;
        line-height: 40px;
    }
    .num {
        height: 40px;
        line-height: 40px;
        padding: 0 15px;
        border:1px solid gray;
        box-sizing: border-box
    }
</style>
