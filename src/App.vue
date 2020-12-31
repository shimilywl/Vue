<template>
    <div id="appContainer">
        <h1>App 组件</h1>
        <button class="btn1">测试按钮1</button>
        <button>测试按钮2</button>
        <ul>
            <li :class="{active:navIndex === itmem}" @click="handler(itmem)"  v-for="itmem in 10" :key="itmem">{{itmem}}
            </li>
        </ul>
    </div>
</template>

<script>
    export default {
        name: 'app',
        data(){
            return{
                navIndex:1
            }
        },
        methods:{
            handler(itmem){
                this.navIndex = itmem

            }
        }
    }
</script>

<style lang="stylus">

    //定义函数
    add(a, b)
        padding a+b

    //定义变量
    btnStyle2(w, h, bgcolor)
        width  w
        height h
        background bgcolr

    $color = red
    btnStyle()
     width 100px
     height 100px
     background $color

    #appContainer
        .btn1
          btnStyle()

        h1
          font-size 40px
        ul
          li
            line-height 40px
            &.active
              color $color
</style>
