<template>
    <div class="wrap2">
        <div class="about">
            <div class="left">
                <div class="title">
                    <div style="display: inline-block;display:flex;flex-direction: column">服务
                        <span style="margin-top: 39px">服务</span>
                        <span style="margin: 16px 0px">服务</span>
                        <span>服务</span>
                    </div>
                    <div style="display: inline-block;display:flex;flex-direction: column">合作项目
                        <span style="margin-top: 39px">合作项目</span>
                        <span style="margin: 16px 0px">合作项目</span>
                        <span>合作项目</span>
                    </div>
                    <div style="display: inline-block;display:flex;flex-direction: column">其他
                        <span style="margin-top: 39px">相关政策</span>
                        <span style="margin: 16px 0px">想关网址</span>
                        <span>声明</span>
                    </div>
                </div>
            </div>
            <div class="right">
                <div style="display: flex;flex-direction: column">
                    <div><img src="../assets/title1.png" alt="" style="margin-bottom: 20px"></div>
                    <div><img src="../assets/title2.png" alt=""></div>
                    <div style="margin-top: 37px;display: flex;align-items: center">
                        <div style="border: 1px solid #ffffff;font-size: 25px;width: 143px;height: 37px;text-align: center;line-height: 37px;color: #ffffff">加入我们</div>
                        <img src="../assets/weibo.png" alt="" style="margin-left: 68px;margin-right: 20px">
                        <img src="../assets/info.png" alt="">
                    </div>
                </div>
                <div>
                    <img src="../assets/QRcode.png" style="width: 166px;height: 166px;margin-left: 44px">
                </div>
            </div>
        </div>
        <div class="line"></div>
        <div class="copyright">
            <div style="font-size: 19px">专利版权|联系我们|隐私条款|法务公告|认证教师查询</div>
            <div style="font-size: 17px">网站备案号 京ICP备16038030号-2 北京月儿湾文化发展有限公司</div>
            <div style="font-size: 17px">投资有风险，选择需谨慎</div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "bottom",
        data(){
            return{
                data(){
                    serveList:[
                        {name:'服务1',active:false},
                        {name:'服务2',active:false},
                        {name:'服务3',active:false},
                    ]
                    hezuoDemo:[
                        {name:'合作项目1',active:false},
                        {name:'合作项目2',active:false},
                        {name:'合作项目3',active:false},
                    ]
                    other:[
                        {name:'相关政策',active:false},
                        {name:'相关网址',active:false},
                        {name:'声明',active:false},
                    ]
                }
            }
        }
    }
</script>

<style scoped>
    .wrap2{
        position: relative;
        width: 100%;
        height:508px;
        background:#000000;
        /*position: absolute;*/
    }
    .about{
        width: 80%;
        height: 356px;
        margin: 0 auto;
        display: flex;
    }
    .left{
        width: 50%;
        height: 100%;
        display: flex;
        align-items: center;
        justify-content: space-around;
        color: #ffffff;
    }

    .right{
        width: 50%;
        height: 100%;
        display: flex;
        align-items: center;
    }
    .title{
        width:50%;
        height: 100%;
        font-size: 25px;
        display: flex;
        align-items: center;
        justify-content: space-around;
    }
    .title>div>span{
        font-size: 20px;
        color: #a5a5a5;
    }
    .line{
        width: 100%;
        height: 2px;
        background:linear-gradient(to left,#000000,#6f6f6f,#000000)
    }
    .copyright{
        width: 100%;
        height: 150px;
        /*border-top: 1px solid #6f6f6f;*/
        display: flex;
        flex-direction: column;
        justify-content: space-around;
        color: #6d6d6d;
    }
    .copyright>div{
        text-align: center;
    }
</style>