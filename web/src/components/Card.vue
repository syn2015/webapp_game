<template>
    <div class="card bg-white p-3 mt-3 pb-3">
        <div class="card-header d-flex ai-center fs-lg "
         :class="{'border-bottom': !plain, 'pb-3': !plain}">
        <div class="border-bottom" v-if="!plain"></div>
            <i class="iconfont" :class="`icon-${icon}`"></i>
            <div class="fx-xl flex-1 px-2"><strong>{{title}}</strong></div>
            <i class="iconfont icon-menu1" v-if="!plain"></i>
        </div>
        <div class="card-body pt-3">
            <slot></slot>
        </div>
    </div>
</template>

<script >
export default {
    props:{
        title:{type:String,required:true},
        icon:{type:String,required:true},
        plain:{type:Boolean}
    }
}
</script>
<style lang="scss">
@import '../style.scss';
.card{
    border-bottom:1px solid $border-color;
}
</style>