<template>
    <div>
        <div class="crumbs">
            <el-breadcrumb separator="/">
                <el-breadcrumb-item><i class="el-icon-date"></i> 项目总览</el-breadcrumb-item>
            </el-breadcrumb>
        </div>
        <div class="container">
            
       
            <div class="schart-box">
            <div class="content-title">各产业项目使用情况一览</div>
            <schart class="schart" canvasId="line" :data="data1" type="line" :options="options2"></schart>
            </div>
            <div class="schart-box">
            <div class="content-title"></div>
            <schart class="schart" canvasId="pie" :data="data2" type="pie" :options="options3"></schart>
            </div>
        </div>
        <table>
        
        </table>
    </div>
    
</template>

<script>
    import Schart from 'vue-schart';
    export default {
        name: 'basecharts',
        components: {
            Schart
        },
        data: () => ({
            data1:[
                {name:'航旅',value:1141},
                {name:'实业',value:1499},
                {name:'物流',value:2260},
                {name:'科技',value:1170},
                {name:'资本',value:970},
               
            ],
            data2 : [
                {name:'航旅',value:1200},
                {name:'实业',value:1222},
                {name:'物流',value:1283},
                {name:'科技',value:1314},
                {name:'资本',value:2314}
            ],
            options1: {
                title: '各产业项目预算',
                autoWidth: true,   // 设置宽高自适应1
                showValue: false,
                bgColor: '#F9EFCC',
                fillColor: '#00887C',
                contentColor: 'rgba(46,199,201,0.3)',
                yEqual: 7
            },
            options2: {
                title: '各产业项目预算',
                bgColor: '#D5E4EB',
                titleColor: '#00887C',
                fillColor: 'red',
                contentColor: 'rgba(46,199,201,0.3)'
            },
            options3: {
                title: '各产业项目预算',
                bgColor: '#829dca',
                titleColor: '#ffffff',
                legendColor: '#ffffff',
                radius: 120
            },
            options4: {
                title: '某商店各商品年度销量',
                bgColor: '#829daa',
                titleColor: '#ffffff',
                legendColor: '#ffffff',
                radius: 120,
                innerRadius:80
            }
        })
    }
</script>

<style scoped>
.schart-box{
    display: inline-block;
    margin: 20px;
}
    .schart{
        width: 500px;
        height: 400px;
    }
    .content-title{
        clear: both;
        font-weight: 400;
        line-height: 50px;
        margin: 10px 0;
        font-size: 22px;
        color: #1f2f3d;
    }
    
</style>