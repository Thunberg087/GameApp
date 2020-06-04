<template>
  <view class="container">
    <text class="text-color-primary">awd</text>
    <button
        :on-press="onPressLearnMore"
        title="Learn More"
        color="#841584"
        accessibility-label="Learn more about this purple button"
    />
  </view>
</template>

<script>
import axios from 'axios';

export default {
  methods: {
    onPressLearnMore() {

    axios.get('http://localhost:3000/')
        .then(res => {
          console.log(res);
          
        })
        .catch(error => {
          console.log(error.response);

        })
    }
  }
}
</script>

<style>
.container {
  background-color: green;
  align-items: center;
  justify-content: center;
  flex: 1;
}
.text-color-primary {
  color: blue;
}
</style>
