<template>
  <v-app id="app">
    <v-app-bar>
      <v-container class="d-flex align-center justify-center">
        <v-btn link to="/maintainance">
          <v-icon color="primary" size="x-large">mdi-chevron-left</v-icon>
          <span class="mx-1 text-blue-500">Back</span>
        </v-btn>
        <v-spacer></v-spacer>
      </v-container>
    </v-app-bar>

    <v-main class="bg-grey-lighten-2">
      <v-responsive>
        <v-container>
          <v-row>
            <v-col>
              <v-sheet min-height="70vh" rounded="lg" class="pa-2">
                <v-toolbar class="bg-white">
                  <v-toolbar-title>
                    <v-row>
                      <v-col cols="1">
                        <v-icon class="" size="x-large" icon="mdi-star-outline" />
                      </v-col>
                      <v-col cols="1">
                        <h1 class="ml-2 mt-2">New</h1>
                      </v-col>
                    </v-row>
                  </v-toolbar-title>
                </v-toolbar>

                <v-form @submit.prevent class="px-5 py-5">
                  <v-row>
                    <v-col cols="6">
                      <span class="px-5 py-3 text-sm">Product</span>
                      <v-text-field variant="outlined" required label="Enter Order Product" :rules="rules"
                        type="input"></v-text-field>
                    </v-col>
                    <v-col cols="6">
                      <span class="px-5 py-3 text-xs">Date Generated</span>
                      <v-text-field variant="outlined" clearable required :rules="rules" label="15/12/2021"
                        append-inner-icon="mdi-calendar" type="text"></v-text-field>
                    </v-col>
                  </v-row>
                  <v-row>
                    <v-col cols="6">
                      <span class="px-5 py-3 text-sm">Status</span>
                      <v-select required :rules="rules" variant="outlined" :items="options"
                        label="Select status"></v-select>
                    </v-col>
                    <v-col cols="6">
                      <span class="px-5 py-3 text-sm">Quantity</span>
                      <v-text-field :rules="rules" required variant="outlined" label="Enter Quantity"
                        type="input"></v-text-field>
                    </v-col>
                  </v-row>
                  <v-row>
                    <v-col cols="6">
                      <span class="px-5 py-3">Bill of Material</span>
                      <v-select required :rules="rules" :items="options" variant="outlined"
                        label="Enter the Bill of Material" rounded="lg"></v-select>
                    </v-col>
                    <v-col cols="6" class="flex justify-end">
                      <v-btn block type="submit" size="large" color="primary" class="mt-7" to='/secondMaintainance'>
                        Create
                      </v-btn>
                    </v-col>

                  </v-row>
                </v-form>

                <!-- Add your v-table here -->
                <v-data-table class="pa-0 ma-0" hide-default-footer hide-default- :headers="headers.text"
                  :items="items">
                  <template v-slot:top>
                    <v-toolbar class="bg-white" flat>
                      <v-toolbar-title>Orders</v-toolbar-title>
                      <v-divider class="mx-4" inset vertical></v-divider>
                      <v-spacer></v-spacer>
                    </v-toolbar>
                  </template>
                </v-data-table>
                <!-- End of v-table -->

                <!-- Add v-row and v-col for the Create button -->

              </v-sheet>
            </v-col>
          </v-row>
        </v-container>
      </v-responsive>
    </v-main>
  </v-app>
</template>
<script setup>
import "../assets/tailwind.css";
// import { ref } from "vue";
// // import { useRouter } from "vue-router";

// // const router = useRouter();
// // const goBack = () => {
// //   router.go(-1);
// // }
const rules = [
  value => {
    if (value) return true

    return 'You must enter a valid data to proceed.'
  },
]
const headers = [
  { text: "Reference", value: "reference" },
  { text: "Status", value: "status" },
  { text: "Date Generated", value: "date_generated" },
  { text: "Quantity", value: "quantity" },
];
const items = [
  {
    reference: "ORD123",
    status: "Pending",
    date_generated: "2023-07-01",
    quantity: 10,
  },
  {
    reference: "ORD124",
    status: "Completed",
    date_generated: "2023-07-02",
    quantity: 5,
  },
];
const options = ['Pending', 'Completed', 'Draft']
</script>

<style scoped></style>
