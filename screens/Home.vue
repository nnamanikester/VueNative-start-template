<template>
  <!-- <view class="container">
  </view> -->
  <nb-container>
    <nb-header>
      <nb-left>

      </nb-left>
      <nb-body>
        <nb-title>AfriFOoD</nb-title>
      </nb-body>
      <nb-right>

      </nb-right>
    </nb-header>
    <nb-container class="container">
      <text>This is the Home screen</text>
      <button title="Go to the Details screen" @press="changeRoute"></button>
    </nb-container>
  </nb-container>
</template>

<script>
export default {
  props: {
    navigation: { type: Object }
  },
  methods: {
    changeRoute() {
      this.navigation.navigate('About', {
        age: 21,
        name: 'John Kester'
      });
    }
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