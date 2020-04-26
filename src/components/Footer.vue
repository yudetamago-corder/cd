<template>
    <div class="apple">
        <input @click="showText" type="submit" placeholder="受け取る">
        <p>{{show}}</p>
    </div>
</template>
<script>
export default{
    data(){
        return{
            show:""
        }
    },
    props:["parentText"],
    methods:{
        showText(){
            this.show=this.parentText
        }
    }
}
</script>