<template>
    <button @click="$emit('btn-click')" :style="{background:color}" class="btn">{{text}}</button>
</template>
<script>


export default ({
    name:"Button",
    props:{
        text: String,
        color: String,
    },
    // methods: {
    //     onClick(){
    //         console.log("Clicked!");
    //     }
    // },
    emits:['toggle-show']
})
</script>
<style scoped>

</style>
