<template>
    <div class="tab-bar-item" @click="itemClick">
        <div v-if="!IsActive">
            <slot  name="item-icon"></slot>
        </div>
        <div v-else>
            <slot  name="item-icon-active"></slot>
        </div>
        <div :style="activeStyle"> 
            <slot  name="item-text"></slot>
        </div>
       
    </div>
</template>

<script>
export default {
    name:'TabBarItem',
    props: {
        path:String,
        activeColor:{
            type:String,
            default:'red'
        }
    },
    data () {
        return {
            // IsActive:true
        }
    },
    computed: {
        IsActive(){
            return this.$route.path.indexOf(this.path)!==-1
        },
        activeStyle(){
            console.log(this.IsActive)
            return this.IsActive?{color:this.activeColor}:{}
        }
    }
    ,methods: {
        itemClick(){
           this.$router.push(this.path);
        }
    }
}
</script>

<style>
    .tab-bar-item{
        flex: 1;
        text-align: center;
        height: 49px;
        font-size: 14pxx;
    }
    .tab-bar-item img{
      height: 24px;
      width: 24px;
      margin-top: 3px;
      vertical-align: middle;
    }
    /* .active{
        color: red;
    } */
</style>