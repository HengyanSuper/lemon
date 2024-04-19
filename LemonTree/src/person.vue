<template>
    <div class="box">
        <h2>{{ number }}</h2>
        <h2>姓名：{{ name }}</h2>
        <h2>年龄：{{ age }}</h2>
        <button @click="changeName">修改名字</button>
        <button @click="addAge">年龄+1</button>
        <button @click="showTel"> 查看联系方式</button>
    </div>
</template>

<script lang="ts" setup name="PersonExcend">
import { ref } from 'vue';

//数据
let number = "设置"
let name = ref("陈晓晓")
let age = ref(22)
let tel = "021 - 88886666"
//方法
function changeName() {
    name.value = "方兮兮"
}

function addAge() {
    age.value += 1
}

function showTel() {
    alert(tel)
}
</script>





<style>
.box {
    background-color: aliceblue;
    border-radius: 20px;
    padding: 20px;
    width: 800px;

    h2 {
        color: black;
    }

    button{
        margin-left: 20px;
        border: solid 1px #000000 ;
    }

}
</style>