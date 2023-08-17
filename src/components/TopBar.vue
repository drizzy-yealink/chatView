
<script setup lang="ts">
import { onMounted, ref } from 'vue';

let nowTime = ref('');

function getTimes(now: Date) {
    let hour = now.getHours().toString();
    let minute = now.getMinutes() < 10 ? "0" + String(now.getMinutes()) : now.getMinutes().toString();
    let second = now.getSeconds() < 10 ? "0" + String(now.getSeconds()) : now.getSeconds().toString();

    nowTime.value = hour + " : " + minute + " : " + second;     
}

let nowTimes = () => {
    console.log("nowTimes recall");
    getTimes(new Date());
    setTimeout(nowTimes, 1000);
}

onMounted(() => {
    nowTimes();
});
</script>

<template> 
    <div>
        {{ nowTime }}
    </div>
</template>

<style scoped>
.topBar{
    outline: 1rem 

}

</style>