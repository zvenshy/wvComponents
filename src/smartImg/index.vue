<template>
    <img :src="imgUrl" 
        v-on:error.once="handleError($event)"
        :placeholder="defaultUrl"
        :alt="imgAlt">
</template>
    
<script>
    /**
     * 图片加载组件
     */
    export default {
        methods: {
            handleError(e) {
                e.currentTarget.src = this.defaultUrl;
            }
        },
        props: {
            //图片地址
            imgUrl: {
                type: String, 
                default: function () {
                    return ''
                }
            },
            //图片加载失败，则请求默认图片地址
            defaultUrl: {
                type: String, 
                default: function () {
                    return ''
                }
            },
            //图片加载失败，展示文案
            imgAlt: {
                type: String, 
                default: function () {
                    return ''
                }
            },
        }
    }
</script>