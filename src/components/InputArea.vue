<script setup lang="ts">
//textarea高度自适应

import { ref } from 'vue';
let message = ref('')
 function sendMessage() {
    console.log("The sent message is " + message.value)
    message.value = ''
 }
 function resizeArea(){

 }


</script>

<template>
    <div class="footer">    
        <div class="">     
            <textarea v-model="message" @keydown.enter.prevent = "sendMessage" rows="1" @input="resizeArea" ref="textarea"></textarea>
        </div>

        <button @click="sendMessage" class="sendBtn">Send</button>
    </div>


</template>



<style>
.footer{
    display: flex;
    flex: auto;
    color: lightblue;
    margin: auto;
    border: 0.1rem solid red
    
}
textarea {
  color: #252424;
  border: 0.05rem solid black;
  border-radius: 1rem;
  border-color: #888;
  margin: 1rem;
  resize: none;
  font-size: 1rem;
  line-height: 1.2;

 

}
.expandingArea {
    position: relative;
    border: 1px solid #888;
    background: #fff;
    margin: 2rem;
  }

.sendBtn{
    
}

</style>
