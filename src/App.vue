<template>
    <div id="container"></div>
</template>
<script setup>
import * as zrender from "zrender";
import {nextTick, onMounted} from "vue";

onMounted(()=>{
    nextTick(()=>{
        const dom = document.getElementById('container')
        const zr = zrender.init(dom);
        const circle = new zrender.Circle({
            shape: {
                cx: 150,
                cy: 50,
                r: 40
            },
            style: {
                fill: 'none',
                stroke: '#F00'
            }
        });
        zr.add(circle);
    })

})
</script>



<style>
#container{
    width: 1000px;
    height: 1000px;
}
</style>
