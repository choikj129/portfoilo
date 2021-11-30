<template>
    <div class="main">
        <link rel="preconnect" href="https://fonts.googleapis.com">
        <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
        <link href="https://fonts.googleapis.com/css2?family=Jua&display=swap" rel="stylesheet">
        <div id='intro' class="chapter">
            <div>신입 개발자 최경주의 포트폴리오입니다.</div>
        </div>
        <div id='explain' class="chapter">
            <div class="custom-shape-divider-top-1638253977">
                <svg data-name="Layer 1" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 120" preserveAspectRatio="none">
                    <path d="M1200 120L0 16.48 0 0 1200 0 1200 120z" class="shape-fill"></path>
                </svg>
            </div>
            <div class="head">『소개』</div>
            <div id='title'>
                안녕하십니까. 궁금함이 많은 신입 개발자 최경주입니다.
            </div>
            <div id='content'>
                궁금한 것이 생기면 검색하고 알아가는 것을 좋아하는 사람입니다.<br>
                전공 수업으로 프로그래밍을 들으며 개발자에 대해 궁금함이 생겨 개발자의 꿈을 키웠습니다.<br>
                2년간 빅데이터가 어떤 것인지 궁금해 학원을 다니고,<br>
                독학과 국비교육, 프로젝트를 통해 개발자에 대한 지식을 쌓았습니다.<br>
                더 깊은 개발의 세계에 대한 궁금함을 알아가며 성장하고 싶습니다.
            </div>
            <div :style="{height:'50px'}">
                <b-icon icon="github" class="icon" ></b-icon>
                <a href="https://github.com/choikj129" target="_blank">GitHub</a>
            </div>
            <div :style="{height:'50px'}">
                <b-icon icon="envelope" class="icon" ></b-icon>
                <span>ckj9829@naver.com</span>
            </div>
        </div>
        <div id='skill' class="chapter">
            <div class="custom-shape-divider-top-1638256438">
                <svg data-name="Layer 1" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 120" preserveAspectRatio="none">
                    <path d="M1200 0L0 0 598.97 114.72 1200 0z" class="shape-fill"></path>
                </svg>
            </div>
            <div class="head">『기술 스택』</div>
            <div>
                [백엔드]
            </div>
            <div class="skill_wrap backend">
                <div class="skill_img" :key="i" v-for="(b,i) in img.back">
                    <img :src="b.url">
                    <div>{{b.name}}</div>
                </div>
            </div>
            <div>
                [프론트엔드]
            </div>
            <div class="skill_wrap frontend" >
                <div class="skill_img" :key="i" v-for="(f,i) in img.front">
                    <img :src="f.url">
                    <div>{{f.name}}</div>
                </div>
            </div>
            <div>
                [기타]
            </div>
            <div class="skill_wrap etc" >
                <div class="skill_img" :key="i" v-for="(e,i) in img.etc">
                    <img :src="e.url">
                    <div>{{e.name}}</div>
                </div>
            </div>
            
        </div>
    </div>    
</template>

<script>
export default {
    name : "Main",
    data(){
        return{
            img : {
                back : [
                    {url : require("../assets/py.png"), name : "Python"},
                    {url : require("../assets/java.png"), name : "Java"},
                    {url : require("../assets/node-js.png"), name : "Nodejs"},
                ],
                front : [
                    {url : require("../assets/html.png"), name : "HTML"},
                    {url : require("../assets/css.png"), name : "CSS"},
                    {url : require("../assets/js.png"), name : "JavaScript"},
                    {url : require("../assets/jquery.png"), name : "Jquery"},
                    {url : require("../assets/vue.png"), name : "Vue"},
                ],
                etc : [
                    {url : require("../assets/github.png"), name : "GitHub"},
                    {url : require("../assets/mysql.png"), name : "MySQL"},
                    {url : require("../assets/aws.png"), name : "AWS"},
                ]
            }
            
        }
    }
}
</script>

<style>
    body{
        overflow-x: hidden;
        background-color : #E7ECEE;
        font-size: 30px;
        text-align: center;
    }
    .icon{
        width : 50px;
        height : auto;
        margin-right : 20px;
    }
    .chapter{
        width : 100vw;
        height: 100vh;
        font-family: 'Jua', sans-serif;
    }
    #intro{
        line-height: 100vh;
        font-weight: bold;
        font-size: 40px;
    }
    #intro::after{
        background-image : url('../assets/intro.png');
        width : 100%;
        height : 100%;
        content: "";
        position : absolute;
        top : 0;
        left : 0;
        z-index : -1;
        opacity : 0.5;
        background-size : 100% 100%;
        background-repeat: no-repeat;
    }
    #title{
        font-size: 35px;
        padding-top : 100px;
        padding-bottom : 40px;
    }
    #content{
        font-size : 25px;
        padding-bottom : 100px;
    }
    img{
        width: 130px;
    }
    .skill_wrap{
        width: 650px;
        height: 180px;
        margin : 0 auto
    }
    .skill_img{
        width: 130px;
        float: left;
    }
    .skill_img div{
        font-size: 18px;
    }
    .backend, .etc{
        width : 390px;
    }
    .head{
        font-size : 35px;
        padding-bottom: 20px;
    }




    .custom-shape-divider-top-1638253977 {
        position: inherit;
        top: 0;
        left: 0;
        width: 100%;
        overflow: hidden;
        line-height: 0;
    }
    .custom-shape-divider-top-1638253977 svg {
        position: relative;
        display: block;
        width: calc(100% + 1.3px);
        height: 177px;
    }
    .custom-shape-divider-top-1638253977 .shape-fill {
        fill: #C6CED6;
        z-index: -1;
    }
    .custom-shape-divider-top-1638256438 {
        position: inherit;
        top: 0;
        left: 0;
        width: 100%;
        height: 150px;
        overflow: hidden;
        line-height: 0;
    }
    .custom-shape-divider-top-1638256438 svg {
        position: relative;
        display: block;
        width: calc(100% + 1.3px);
        height: 100px;
    }
    .custom-shape-divider-top-1638256438 .shape-fill {
        fill: #9791A4;
    }
</style>