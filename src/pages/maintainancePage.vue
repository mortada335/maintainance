<template>
  <div id="app">
    <v-responsive class="grid grid-cols-3 gap-3 px-5 py-5">
      <v-form>
        <v-row>
          <v-col cols="5">
            <span class="px-5 py-3 text-sm">Reference</span>
            <v-text-field :rules="rules" variant="outlined" required label="Enter Order Reference"
              type="input"></v-text-field>
          </v-col>
          <v-col cols="6">
            <span class="px-5 py-3 text-xs">Date Generated</span>
            <v-text-field :rules="rules" variant="outlined" clearable label="15/12/2021" append-icon="mdi-calendar"
              type="text"></v-text-field>
          </v-col>
        </v-row>
        <v-row>
          <v-col cols="5">
            <span class="px-5 py-3 text-sm">Status</span>
            <v-select :rules="rules" variant="outlined" :items="items" label="Select status"></v-select>
          </v-col>
          <v-col cols="5">
            <span class="px-5 py-3 text-sm">Quantity</span>
            <v-text-field :rules="rules" variant="outlined" label="Enter Quantity" type="input"></v-text-field>
          </v-col>
        </v-row>
      </v-form>

    </v-responsive>

    <!-- 
       </div>
      <div>
        </div>} -->

    <v-card class="pa-1">
      <v-card-title>
        <v-row>
          <v-col cols="4">
            <h1 class="text-base text-blue-900">Manufacturing Orders</h1>
          </v-col>
          <v-spacer></v-spacer>
          <v-col cols="auto">
            <v-btn size="small" variant="outlined" link to="/newMaintainance" height="35" color="blue-lighten-3"
              class=" border-none mt-[-8px]">
              New Manufacturing Order
            </v-btn>
          </v-col>
        </v-row>


      </v-card-title>
      <v-data-table hide-default-footer="true" :headers="headers.text" :items="plants" density="compact"
        item-key="name"></v-data-table>
    </v-card>
  </div>
</template>

<script setup>
import "../assets/tailwind.css";
const rules = [
  value => {
    if (value) return true

    return 'You must enter a valid data to proceed.'
  },
]

const headers = [
  { text: "Plant", align: "start", sortable: false, value: "name" },
  { text: "Light", align: "end", value: "light" },
  { text: "Height", align: "end", value: "height" },
  { text: "Pet Friendly", align: "end", value: "petFriendly" },
  { text: "Price ($)", align: "end", value: "price" },
];

const plants = [
  { name: "Fern", light: "Low", height: "20cm", petFriendly: "Yes", price: 20 },
  { name: "Snake Plant", light: "Low", height: "50cm", petFriendly: "No", price: 35 },
  { name: "Monstera", light: "Medium", height: "60cm", petFriendly: "No", price: 50 },
  { name: "Pothos", light: "Low to medium", height: "40cm", petFriendly: "Yes", price: 25 },
  { name: "ZZ Plant", light: "Low to medium", height: "90cm", petFriendly: "Yes", price: 30 },
  { name: "Spider Plant", light: "Bright, indirect", height: "30cm", petFriendly: "Yes", price: 15 },
  { name: "Air Plant", light: "Bright, indirect", height: "15cm", petFriendly: "Yes", price: 10 },
  { name: "Peperomia", light: "Bright, indirect", height: "25cm", petFriendly: "Yes", price: 20 },
  { name: "Aloe Vera", light: "Bright, direct", height: "30cm", petFriendly: "Yes", price: 15 },
  { name: "Jade Plant", light: "Bright, direct", height: "40cm", petFriendly: "Yes", price: 25 },
];
const items = ['completed', 'waiting']
</script>

<style scoped></style>
