<template>
  <v-app>
    <v-toolbar app>
      <v-toolbar-title class="headline text-uppercase">
        <span>PolyGraph Media</span>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <!-- <v-btn
        flat
        href="https://github.com/vuetifyjs/vuetify/releases/latest"
        target="_blank"
      >
        <span class="mr-2">
          <router-link to="/addUser">Add User</router-link>
          </span>
      </v-btn>-->
      <router-link to="/addUser">Add User</router-link>
    </v-toolbar>

    <v-content>
      <!-- <AddUser/> -->
              <ProgramAdmin/>

      <!-- <div v-show="showForm">
        
      </div>
      <div v-show="!showForm">
        <ProgramAdmin/>
      </div> -->
      <!--  -->
      <!-- <HelloWorld/> -->
    </v-content>
  </v-app>
</template>

<script>
import HelloWorld from "./components/HelloWorld";
import AddUser from "./components/AddUser";
import ProgramAdmin from "./components/ProgramAdmin";
export default {
  showForm: false,
  name: "App",
  components: {
    HelloWorld,
    AddUser,
    ProgramAdmin
  },
  data() {
    return {
      //
    };
  }
};
</script>
