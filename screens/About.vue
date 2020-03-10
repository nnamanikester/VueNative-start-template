<template>
  <view class="container">
    <text>This is the App Details screen</text>
    <button title="Go to home screen" @press="goToHomeScreen('Home')"></button>
    <button title="GO BACK" @press="navigation.goBack()"></button>
    <text>Name: {{ navigation.getParam('name') }}</text>
    <text>Age: {{ navigation.getParam('age') }}</text>
  </view>
</template>

<script>
export default {
  props: {
    navigation: { type: Object }
  },
  methods: {
    goToHomeScreen(place) {
      this.navigation.navigate(place);
    },
    
  }
}
</script>

<style>
.container {
  align-items: center;
  justify-content: center;
  flex: 1;
}
</style>