<template>
    <view style="padding: 25rpx 30rpx;">
        <button @click="open">文件选择</button>
    </view>

</template>

<script>
    var AfDocument = uni.requireNativePlugin("Aq-ChooseFile");
    export default {
        data() {
            return {
                data: ''
            }
        },
        onLoad() {

        },
        methods: {
            open(){
                AfDocument.openMode({
                    size: '10', //选择总数量
                    paths:['/storage/emulated/0/Download','/storage/emulated/0/A',],   //自定义选择目录
                    isDown:true,//是否下钻（true 筛选当前目录以下的所有文件，fales 只筛选当前目录文件） 
                    types:[{
                        name:'文档',
                        value:["doc","wps","docx","xls","xlsx","pdf"]
                    },{
                        name:'视频',
                        value:["mp4"] 
                    },{
                        name:'音乐',
                        value:['mp3','flac'] 
                    },{
                        name:'图片',
                        value:['jpg','png'] 
                    }]
                },(res)=>{
                    this.data = JSON.stringify(res);
                })
            }
        }
    }
</script>

<style>
    page{
        background: #fff;
    }
</style>