<template>
    <div class="index">
        <!--        LOGO-->
        <div class="logo">
            <img src="../assets/zhangyu.png" style="width:136px;height: 55px">
            <img src="../assets/title.png" style="width: 153px;height: 55px">
        </div>
        <!--        menu-->
        <div class="menu">
            <div class="menu_item" v-for="(menu,index) in menubar" :class="{active:menu.isActive}" @mouseover="mouseOver(index)"
                 @mouseleave="mouseLeave(index)" @click="toMenu(index)">
                <img src="../assets/paopao.png" style="width: 40px;height: 40px;" v-show="menu.isActive">
                {{menu.name}}
            </div>
        </div>
        <!--        query-->
        <div class="query">
            <div class="check">
                <img src="../assets/search.png" style="width: 15px;height: 15px;margin-left: 10px;margin-right: 5px">
                <input type="text" v-model="userSearch">
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "index",
        data(){
            return{
                menubar:[
                    {name:'关于我们',isActive:true},
                    {name:'教学理念',isActive:false},
                    {name:'最新动态',isActive:false},
                    {name:'赢裕商学院',isActive:false},
                    {name:'国际亲自俱乐部',isActive:false},
                    {name:'企业大学',isActive:false},
                    {name:'加入月儿湾',isActive:false},
                    {name:'查询',isActive:false},
                ],
                userSearch:'',
            }
        },
        methods:{
            mouseOver(index){
                if(index !=0){
                    this.menubar[0].isActive = false
                    this.menubar[index].isActive = !this.menubar[index].isActive
                }else {
                    this.menubar[index].isActive = !this.menubar[index].isActive
                }
            },
            mouseLeave(index){
                this.menubar[index].isActive = !this.menubar[index].isActive
            },
            toMenu(index){
                this.menubar[index].isActive = true
            }

        }
    }
</script>

<style scoped>
    .index{
        width: 100%;
        height: 120px;
        background: #000000;
        display: flex;
        align-items: center;
        justify-content:  space-around;
        position: fixed;
        top: 0;
        left: 0;
        z-index: 99;
    }
    .menu{
        width: 60%;
        height: 100%;
        display: flex;
        align-items: center;
        justify-content: space-around;
        color: #ffffff;
    }
    .menu_item{
        display: flex;
        flex-direction: column;
        position: relative;
        font-size: 18px;
    }
    .menu_item>img{
        position: absolute;
        top: -40px;
        right: -35px;
    }
    .active{
        color: #94d7f5;
    }
    .logo,.query{
        width: 20%;
        display: flex;
        align-items: center;
        justify-content: space-around;
    }
    .check{
        width:156px;
        height: 23px;
        border-radius: 50px;
        border: 1px solid #ffffff;
        display: flex;
        align-items: center;
    }
    input{
        width: 100%;
        border: none;
        background: transparent;
        outline: none;
        color: #ffffff;
    }

</style>