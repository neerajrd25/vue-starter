<template>
    <v-app id="inspire">
        <v-toolbar color="blue-grey" dark fixed app clipped-right>
            <v-toolbar-side-icon></v-toolbar-side-icon>
            <v-toolbar-title>Polygraph Media</v-toolbar-title>
            <v-spacer></v-spacer>
            <v-toolbar-side-icon @click.stop="drawerRight = !drawerRight"></v-toolbar-side-icon>
        </v-toolbar>
    
        <v-navigation-drawer v-model="left" temporary fixed></v-navigation-drawer>
        <v-content>
            <v-btn color="primary" @click.stop="right = !right">Add User</v-btn>
            
        </v-content>
            
        <v-content>
            <v-container fluid fill-height>
                <ProgramAdmin/>
            </v-container>
        </v-content>
        <v-navigation-drawer v-model="right" v-bind:width="500" right temporary fixed>
                <AddUser/>
        </v-navigation-drawer>
        <v-footer color="blue-grey" class="white--text" app>
            <span>Vuetify</span>
            <v-spacer></v-spacer>
            <span>&copy; 2017</span>
        </v-footer>
    </v-app>
</template>

<script>
    import AddUser from "./AddUser";
    import ProgramAdmin from "./ProgramAdmin";
    
    export default {
    
        components: {
            AddUser,
            ProgramAdmin
        },
        data: () => ({
            drawer: null,
            drawerRight: null,
            right: false,
            left: false
        }),
        props: {
            source: String
        }
    };
</script>