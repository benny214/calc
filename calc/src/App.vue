<template>
  <div class="calc">
    <input type="text" 
        v-model="display" 
        class="calc__display" 
        disabled>

        <div class="calc__btns-list">
          <button 
            v-for="button in buttons"
            :key="button.value"
            @click=""
            :class="'calc__btn' ">
            {{ button.value }}
          </button>
        </div>

  </div>
</template>

<script>
import { ref } from 'vue'

export default {
  setup() {
      const display = ref('0');
      const buttons = [
        {value: 'AC', type: 'clear'},
        {value: 'Del', type: 'delete'},
        {value: '.', type: 'operator'},
        {value: '/', type: 'operator'},

        {value: '7'},
        {value: '8'},
        {value: '9'},
        {value: '*', type: 'operator'},

        {value: '4'},
        {value: '5'},
        {value: '6'},
        {value: '-', type: 'operator'},

        {value: '1'},
        {value: '2'},
        {value: '3'},
        {value: '+', type: 'operator'},

        {value: '000'},
        {value: '00'},
        {value: '0'},
        {value: '=', type: 'equals'},
      ]
      return {
        display,
        buttons
      }
    }
  }
  
</script>


