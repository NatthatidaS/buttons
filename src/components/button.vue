<template>
<div>
    <div>
        <button v-on:click="$like" class="button-apple " id="blue">Like</button>
        <button v-on:click="$dislike" class="button-apple" id="green">Unlike</button>
        <button v-on:click="$love"  class="button-apple" id="red">Love</button>
        <button v-on:click="counter = 0" class="button-apple" id="black">Reset</button>
        <h1>{{counter}}</h1>
    </div>
</div>
</template>

<script>
export default {
    name: 'button',
    props: {
        label: String
    },
    data: function () {
        return {
            like: 0,
            love: 0,
            dislike: 0, 
            counter:0,
            
            
        };
    },
        methods:{
            $like:function(){
                this.counter +=1
                this.like +=1
                this.$emit('cc',this.counter)
            },
            $love:function(){
                this.counter +=5
                this.love +=1
                this.$emit('cc',this.counter)
            },
            $dislike:function(){
                this.counter -=10
                this.dislike += 1
                this.$emit('cc',this.counter)
            }
        }
        
    
}
</script>

<style>
    .button-apple{
    background-color: white;
    border: none;
    padding: 5px 5px 5px 5px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 16px;
    margin: 4px 2px;
    cursor: pointer;
    border-radius: 8px;
    border: 0.5px solid #ebebeb;
    width : 60px;
}
.button-apple-font-dd{
    background-color: white;
    border: none;
    color: #646363;
    padding: 5px 5px 5px 5px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 16px;
    margin: 4px 2px;
    cursor: pointer;
    border-radius: 8px;
    border: 0.5px solid #ebebeb;
    width : 60px;
}
button:hover#blue {
    color: blue;
}
button:hover#red {
    color: red;
}
button:hover#black {
    color: black;
}
button:hover#green {
    color: green;
}
</style>
