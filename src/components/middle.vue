<template>
    <div class="wrap">
<!--新闻-->
        <div class="content">
            <div class="news">
                <div class="news1_l">
                    <div class="news1_l_t">
                        <span style="display: block;font-weight:bold;font-size: 28px;color: #FFFFFF">品牌优势</span>
                        <span style="display: block;font-weight:bold;font-size: 24px;color: #FFFFFF">Moonbay Brand</span>
                        <span style="display: block;font-weight:bold;font-size: 24px;color: #FFFFFF">Advantage</span>
                    </div>
                    <div class="news1_l_b" @mouseenter="mouseEnter2" @mouseleave="mouseLeave2">
                        <span style="font-size: 18px;" :class="{active:news.isActive}" v-for="(news,index) in newsList"
                              @mouseenter="mouseEnter(index)"
                              @mouseleave="mouseLeave(index)"
                        >{{news.title}}</span>
                    </div>
                </div>
                <div class="news1_r" v-show="newsShow">
                    {{newsDetail}}
                </div>
            </div>
            <div class="news">
                <div class="news2_l" :class="{show:statusShow}">
                    <span>月儿湾国际亲子俱乐部</span>
                    <div style="box-sizing: border-box;margin: 20px 10px;background: #003363">
                        <span>官宣|月儿湾(国际)亲子俱乐部!我们来了！</span>
                        <img src="../assets/pic.png" style="width: 464px;height: 310px">
                    </div>
                </div>
                <div class="news2_r" >
                    <div class="new2_r_t">
                        <span style="display:block;font-weight:bold;font-size: 28px;color: #FFFFFF">最新动态</span>
                        <span style="display: block;font-weight:bold;font-size: 24px;color: #FFFFFF">Moonbay Dynamic</span>
                    </div>
                    <div class="new2_r_b" @mouseenter="mouseEnter4_2" @mouseleave="mouseLeave4_2">
                        <span  style="font-size: 18px;"v-for="(status,index) in statusList" :class="{active:status.isActive}"
                               @mouseenter="mouseEnter4(index)" @mouseleave="mouseLeave4(index)"
                        >{{status.title}}</span>
                    </div>
                </div>
            </div>
            <div class="news">
                <div class="news1_l">
                    <div class="news1_l_t">
                        <span style="display: block;font-weight:bold;font-size: 28px;color: #FFFFFF">课程体系</span>
                        <span style="display: block;font-weight:bold;font-size: 24px;color: #FFFFFF">Moonbay cueeiculum</span>
                        <span style="display: block;font-weight:bold;font-size: 24px;color: #FFFFFF">system</span>
                    </div>
                    <div class="news3_l_b" @mouseenter="mouseEnter3_2" @mouseleave="mouseLeave3_2">
                        <div style="margin-bottom: 20px" v-for="(course,index) in courseList">
                            <span style="font-size: 18px" :class="{active:course.isActive}" @mouseenter="mouseEnter3(index)" @mouseleave="mouseLeave3(index)">{{course.title}}</span>
                           <div style="font-size: 16px">{{course.content}}</div>
                        </div>
                    </div>
                </div>
                <div class="news3_r" v-show="courseShow">
                    {{courseDetail}}
                </div>
            </div>
        </div>
<!--弯弯&&章鱼-->
        <div class="wz">
            <img src="../assets/wanwan.gif" style="width: 350px;height: 350px;position:absolute;top: -100px;right: 400px">
            <img src="../assets/zhangyu.gif" style="width: 350px;height: 350px;position: absolute;top:100px;left: 300px">
        </div>
<!--珊瑚背景--最远层-->
        <div class="shanhu6">
            <img src="../assets/shanhu.png" style="width: 100%;height: 1300px">
        </div>
    </div>
</template>

<script>
    export default {
        name: "middle",
        data(){
            return{
                newsShow:true,
                courseShow:false,
                statusShow:false,
                newsList:[
                    {title:'ERP门店管理系统支持',isActive:false,detail:'this is news1 detail'},
                    {title:'SOP运营标准化管理体系支持',isActive:false,detail:'this is news2 detail'},
                    {title:'品牌标准化管理体系支持',isActive:false,detail:'this is news3 detail'},
                    {title:'售后服务标准化支持',isActive:false,detail:'this is news4 detail'},
                    {title:'自主研发产品系列',isActive:false,detail:'this is news5 detail'},
                ],
                newsDetail:'this is news1 detail',
                courseDetail:'this is course1detail',
                courseList:[
                    {
                        title:'Power Up 优+课',
                        content:'根据0-6岁宝宝月龄特点，提供宝宝学习、提升和进阶的水育早教课程。让宝宝在年龄增长的同时不断提高自己的语言、认知' +
                            '、感知、人格、社交、思维、自救、游泳等各项技能，帮助宝宝在人生的最初几年内就能够取得比同龄宝宝更加优异的成绩',
                        detail:'this is Power Up 优﹢课 detail',
                        isActive:false
                    },
                    {
                        title: 'Family LOVE 爱+课',
                        content: '根据0-6岁宝宝亲子关系的需要，通过丰富多彩的水中主题运动,专业的成长游戏和亲子互动开启宝宝的启蒙认知，让宝宝和父母在水中' +
                            '有更多肌肤的接触，提升亲子间信任感，让宝宝感觉更安全，提高宝宝自救能力，延续及发展其与生俱来的亲水本能，让宝宝与父母一起亲近水、热爱水' +
                            '，循序渐进地学会一项终生收益的技能，同时让孩子的身体更加强壮，社交和情感意识方面的能力得到发展，从而更加自信，培养勇敢顽强的精神，促进宝宝认知、' +
                            '社会性和情商的全方面发展。让亲子沟通变得更轻松、更快乐、更有爱',
                        detail: 'this is Family LOVE 爱+课',
                        isActive:false
                    }
                ],
                statusList:[
                    {title:'月儿湾总部',isActive:false},
                    {title: '赢裕商学院',isActive:false},
                    {title: '月儿湾国际亲子俱乐部',isActive: false},
                    {title: '月儿湾加盟',isActive: false}
                ]
                // courseDetail:this.courseList[0].detail
            }
        },
        methods:{
            mouseEnter(index){
                // console.log(index);
                this.newsList[index].isActive = true
                this.newsDetail = this.newsList[index].detail
            },
            mouseLeave(index){
                // console.log(index);
                this.newsList[index].isActive = false
            },
            mouseEnter2(){
                this.newsShow = true
            },
            mouseLeave2(){
                this.newsShow = false
            },
            mouseEnter3(index){
                // console.log(index);
                this.courseList[index].isActive = true
                this.courseDetail = this.courseList[index].detail
            },
            mouseLeave3(index){
                // console.log(index);
                this.courseList[index].isActive = false
            },
            mouseEnter3_2(){
                this.courseShow  = true
            },
            mouseLeave3_2(){
                this.courseShow = false
            },
            mouseEnter4(index){
                this.statusList[index].isActive = true
            },
            mouseLeave4(index){
                this.statusList[index].isActive = false
            },
            mouseEnter4_2(){
                this.statusShow = true
            },
            mouseLeave4_2(){
                this.statusShow = false
            }
        },
        mounted() {
            // window.addEventListener('scroll',)
        }
    }
</script>

<style scoped>
    .wrap{
        width: 100%;
        height: 3220px;
        background: #FFFFFF;
        position: relative;
        background: url("../assets/bimg2.jpg");
        background-repeat: no-repeat;
        background-size: cover;
        background-attachment: fixed;
    }
    .content{
        position: absolute;
        top: 1000px;
        width: 100%;
        z-index: 10;
    }
    .wz{
        position: absolute;
        width: 100%;
        height: 400px;
        top: 200px;
        z-index: 10;
    }
    .shanhu6{
        position: absolute;
        width: 100%;
        height: 400px;
        top: 400px;
        left: 0;
    }
    .news{
        width: 1200px;
        height: 650px;
        margin: 0 auto 60px;
        z-index: 80;
        display: flex;
    }
    .news1_l{
        width: 50%;
        height: 100%;
        box-sizing: border-box;
        padding: 80px 40px;
        background: rgba(0,51,99,.3);
    }
    .news1_r{
        width: 50%;
        height: 100%;
        background: #FFFFFF;
        box-sizing: border-box;
        padding: 80px 40px;
        background: rgba(0,51,99,.3);
    }
    .news1_l_b{
        margin-top: 50px;
        height: 60%;
        display: flex;
        flex-direction: column;
        justify-content: space-around;
        color: #FFFFFF;
    }
    .news2_l{
        visibility: hidden;
        width: 50%;
        height: 100%;
        box-sizing: border-box;
        padding: 80px 40px;
        background: rgba(0,51,99,.3);
    }
    .show{
        visibility: visible;
        width: 50%;
        height: 100%;
        box-sizing: border-box;
        padding: 80px 40px;
        background: rgba(0,51,99,.3);
    }
    .news2_r{
        width: 50%;
        height: 100%;
        background: #FFFFFF;
        box-sizing: border-box;
        padding: 80px 40px;
        background: rgba(0,51,99,.3);
        box-sizing: border-box;
        padding: 80px 40px;
    }
    .new2_r_b{
        display: flex;
        flex-direction: column;
        justify-content: space-around;
        margin-top: 50px;
        height: 60%;
        color:#FFFFFF ;
    }
    .news3_r{
        width: 50%;
        height: 100%;
        background: #FFFFFF;
        box-sizing: border-box;
        padding: 80px 40px;
        background: rgba(0,51,99,.3);
    }
    .news3_l_b{
        margin-top: 50px;
        /*height: 60%;*/
        display: flex;
        flex-direction: column;
        justify-content: space-around;
        color: #FFFFFF;
    }
    .active{
        color: #f7ff22;
    }
</style>