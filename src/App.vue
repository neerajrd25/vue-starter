<template>
  <v-app id="inspire">
    <v-toolbar color="blue" dark fixed app clipped-right>
      <v-toolbar-side-icon></v-toolbar-side-icon>
      <v-toolbar-title>Ad Campaign Management by XYZ</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn color="primary" @click.stop="right = !right">Add User</v-btn>
      <!-- <v-toolbar-side-icon @click.stop="drawerRight = !drawerRight"></v-toolbar-side-icon> -->
    </v-toolbar>

    <v-navigation-drawer v-model="left" temporary fixed></v-navigation-drawer>
    <v-content>
              
        <ProgramAdmin/>
    </v-content>
    <v-navigation-drawer v-model="right" v-bind:width="500" right temporary fixed>
      <AddUser/>
    </v-navigation-drawer>
    <v-footer color="blue-grey" class="white--text" app>
      <span>Ad Campaign</span>
      <v-spacer></v-spacer>
      <span>&copy; 2017</span>
    </v-footer>
  </v-app>

  <!-- <v-app>
    <v-toolbar app>
      <v-toolbar-title class="headline text-uppercase">
        <span>PolyGraph Media</span>
      </v-toolbar-title>
      <v-spacer></v-spacer>
    
      <router-link to="/addUser">Add User</router-link>
    </v-toolbar>

    <v-content>
   
    </v-content>
  </v-app>-->
</template>

<script>
import AddUser from "./components/AddUser";
import ProgramAdmin from "./components/ProgramAdmin";
export default {
  name: "App",
  components: {
    AddUser,
    ProgramAdmin
  },
  data() {
    return {
      drawer: null,
      drawerRight: null,
      right: false,
      left: false

      //
    };
  }
};
</script>
