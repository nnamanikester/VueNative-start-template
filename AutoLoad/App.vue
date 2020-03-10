<template>
  <root>
    <app-navigator></app-navigator>
  </root>
</template>

<script>
import { Root } from 'native-base'

import {
  createAppContainer,
  createStackNavigator,
  createDrawerNavigator
} from "vue-native-router";

// Importing Pages
import Home from "./screens/Home.vue";
import About from "./screens/About.vue";

// Registering Routes
// Normal ROuting (DrawerNavigator)
const DrawerNavigator = createDrawerNavigator(
  {
    Home
  },
  {
    initialRouteName: 'Home',
    contentOptions: {
      activeTintColor: "#e91e63"
    },
  }
)

const StackNavigator = createStackNavigator(
  {
    // Register Drawer Navigation
    Drawer: DrawerNavigator,

    // Screens On top of each other navigation (StackNavigator)
    About
  },
  {
    headerMode: "none"
  }
)

const AppNavigator = createAppContainer(StackNavigator);

export default {
  components: { AppNavigator, Root }
}
</script>