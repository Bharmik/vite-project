<template>
  <h2>V2和V3生命周期对比</h2>
  <p>{{ msg }}</p>
  <button @click="updateMsg">更新</button>
</template>

<script lang="ts">
import { defineComponent, onBeforeMount, onBeforeUnmount, onBeforeUpdate, onMounted, onUnmounted, onUpdated, ref } from 'vue';
export default defineComponent({
    name: 'LifeDemo',
    beforeCreate(){
        console.log('V2---beforeCreate');
    },
    created(){
        console.log('V2---created');
    },
    beforeMount(){
        console.log('V2---beforeMount');
    },
    mounted(){
        console.log('V2---mounted');
    },
    beforeUpdate(){
        console.log('V2---beforeUpdate');
    },
    updated(){
        console.log('V2---updated');
    },
    beforeUnmount(){
        console.log('V2---unmount');
    },
    unmounted(){
        console.log('V2---unmounted');
    },
    setup(){
        console.log('V3---setup')
        const msg = ref("初始msg");
        const updateMsg = ()=>{
            msg.value += "_";
        };
        onBeforeMount(()=>{
            console.log('V3---onBeforeMount');
        })

        onMounted(()=>{
            console.log('V3---onMounted');
        })

        onBeforeUpdate(()=>{
            console.log('V3---onBeforeUpdate');
        })

        onUpdated(()=>{
            console.log('V3---onUpdated');
        })

        onBeforeUnmount(()=>{
            console.log('V3---onBeforeUnmount');
        })

        onUnmounted(()=>{
            console.log('V3---onUnmounted');
        })

        return {
            msg,
            updateMsg
        }
    }
});
</script>
