<template>
  <v-container>
    <v-layout text-xs-left wrap>
      <v-flex mb-5 xs12>
        <h2 class="headline font-weight-bold mb-3">Company</h2>
        <h4 class="headline font-weight-light mb-3">Program Administrator</h4>
      </v-flex>
      
    </v-layout>


    <v-tabs v-model="tab" color="cyan" align-with-title>
      <v-tabs-slider color="blue"></v-tabs-slider>

      <v-tab v-for="item in items" :key="item">{{ item }}</v-tab>
    </v-tabs>

    <v-tabs-items v-model="tab">
      <v-tab-item>
        <v-card flat>
          <v-card-text>Under Construction</v-card-text>
        </v-card>
      </v-tab-item>
      <v-tab-item>
        <v-card flat>
          <v-card-text>Under Construction</v-card-text>
        </v-card>
      </v-tab-item>
      <v-tab-item>
        <v-card flat>
          <v-card-text>Under Construction</v-card-text>
        </v-card>
      </v-tab-item>
      <v-tab-item>
        <v-data-table
          v-model="selected"
          :headers="headers"
          :items="users"
          item-key="name"
          select-all
          class="elevation-1"
        >
          <template v-slot:items="props">
            <td>
              <v-checkbox v-model="props.selected" primary hide-details></v-checkbox>
            </td>
            <td>{{ props.item.name }}</td>
            <td class="text-xs-left">{{ props.item.email }}</td>
            <td class="text-xs-left">{{ props.item.role }}</td>
            <td class="text-xs-left">{{ props.item.client }}</td>
            <td class="text-xs-left">{{ props.item.status }}</td>
          </template>
        </v-data-table>
      </v-tab-item>
    </v-tabs-items>
  </v-container>
</template>
        </v-data-table>
      </v-tab-item>
    </v-tabs-items>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      tab: null,
      items: ["Reporting", "Monitoring", "Location Management", "Admin Tools"],
      text:
        "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.",
      selected: [],
      headers: [
        {
          text: "Name",
          align: "left",
          sortable: false,
          value: "name"
        },
        {
          text: "Email",
          value: "email"
        },
        {
          text: "Role",
          value: "role"
        },
        {
          text: "Client",
          value: "client"
        },
        {
          text: "Status",
          value: "status"
        }
      ],
      users: [
        {
          _id: 1,
          name: "Neeraj Vishwakarma",
          email: "neeraj.vishwakarma@synerzip.com",
          role: "Owner",
          client: "Burger Shop",
          status: "Active"
        },
        {
          _id: 2,
          name: "John Doe",
          email: "john.doe@synerzip.com",
          role: "Owner",
          client: "Morris Garrage",
          status: "Active"
        },
        {
          _id: 3,
          name: "Mary Stoy",
          email: "mary.stoy@synerzip.com",
          role: "Program Administrator",
          client: "Media Tek",
          status: "InActive"
        },
        {
          _id: 4,
          name: "Ryan Smith",
          email: "ryan.smith@synerzip.com",
          role: "Owner",
          client: "Burger Shop",
          status: "InActive"
        },
        {
          _id: 5,
          name: "Amey Potnis",
          email: "amey.potnis@synerzip.com",
          role: "Manager",
          client: "Lake School",
          status: "Active"
        }
      ]
    };
  }
};
</script>

<style>
</style>
