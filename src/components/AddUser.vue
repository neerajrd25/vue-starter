<template>
    <v-container>
        <v-layout text-xs-left wrap>
            <v-toolbar color="blue" dark fixed app clipped-right>
                <v-toolbar-title>Add User</v-toolbar-title>
    
            </v-toolbar>
            <!-- <v-flex mb-5 xs12>
                    <h2 class="headline font-weight-bold mb-3">Add User</h2>
                </v-flex> -->
        </v-layout>
        <v-layout mt-5> 
            <v-flex xs12 mb-5>
                <v-form v-model="valid">
                    <v-container>
                        <v-layout>
                            <v-flex xs12>
                                <v-text-field v-model="firstname" :rules="nameRules" :counter="10" label="First name" required></v-text-field>
                            </v-flex>
                        </v-layout>
                        <v-layout>
                            <v-flex xs12>
                                <v-text-field v-model="lastname" :rules="nameRules" :counter="10" label="Last name" required></v-text-field>
                            </v-flex>
                        </v-layout>
                        <v-layout>
                            <v-flex xs12>
                                <v-text-field v-model="email" :rules="emailRules" label="E-mail" required></v-text-field>
                            </v-flex>
                        </v-layout>
                        <v-layout>
                            <v-flex xs12>
                                <v-text-field v-model="phonenumber" :counter="10" label="Phone Number" required></v-text-field>
                            </v-flex>
                        </v-layout>
                        <v-layout>
                            <v-flex xs12>
                                <v-select v-model="role" :items="roles" :rules="[v => !!v || 'Role is required']" label="Role" required></v-select>
                            </v-flex>
                        </v-layout>
                        <v-layout>
                            <v-flex xs12>
                                <v-select v-model="client" :items="clients" :rules="[v => !!v || 'Client is Required']" label="Client" required></v-select>
                            </v-flex>
                        </v-layout>
                    </v-container>
                </v-form>
            </v-flex>
        </v-layout>
        <v-layout text-xs-right>
            <v-flex mb-5 xs12>
                <div>
                    <v-btn>Cancel</v-btn>
                    <v-btn color="primary">Create</v-btn>
                </div>
    
            </v-flex>
        </v-layout>
    </v-container>
</template>

<script>
    export default {
        data: () => ({
            valid: false,
            firstname: "",
            lastname: "",
            phonenumber: "",
            role: "",
            client: "",
            nameRules: [
                v => !!v || "Name is required",
                v => v.length <= 10 || "Name must be less than 10 characters"
            ],
            email: "",
            emailRules: [
                v => !!v || "E-mail is required",
                v => /.+@.+/.test(v) || "E-mail must be valid"
            ],
            // phoneRules:[
            //     v => !!v || "Phone is required",
            //     v => v.length = 10 || "Phone should be 10 characters"
            // ]
    
            //
            roles: ["Owner", "Admin", "Program Administrator"],
            clients: ["Google ", "Facebook"]
        })
    };
</script>

<style>
    
</style>
