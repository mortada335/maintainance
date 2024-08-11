<template>
    <v-app id="inspire">
        <v-app-bar flat>
            <v-app-bar-title>
                <v-btn to="/secondMaintainance" class="text-blue-400 text-sm hover:bg-blue-400 hover:text-white">
                    <v-icon size="x-large">mdi-chevron-left</v-icon>
                    <span class="mx-1">Back</span>
                </v-btn>
                <v-spacer></v-spacer>
            </v-app-bar-title>
        </v-app-bar>

        <v-main class="bg-grey-lighten-3">
            <v-container>
                <v-row>
                    <v-col cols="12">
                        <v-card flat class="pa-3">
                            <v-card-title>
                                <v-row justify="space-between" align="center">
                                    <v-col cols="auto">
                                        <strong class="text-sm">Product Name:</strong>
                                    </v-col>
                                    <v-col cols="auto">
                                        <v-icon size="x-small" icon="mdi-star-outline"></v-icon>
                                        <strong class="text-2xl">{{ product }}</strong>
                                    </v-col>
                                    <v-col cols="auto">
                                        <v-btn flat tile size="x-large" icon="mdi-camera-plus-outline"></v-btn>
                                    </v-col>
                                </v-row>
                            </v-card-title>
                            <v-card-subtitle>
                                <v-row>
                                    <v-col cols="auto">
                                        <v-checkbox color="primary" label="Can be sold"></v-checkbox>
                                    </v-col>
                                    <v-col cols="auto">
                                        <v-checkbox color="primary" label="Can be purchased"></v-checkbox>
                                    </v-col>
                                </v-row>
                            </v-card-subtitle>
                            <v-card-text>
                                <v-tabs v-model="activeTab" align-tabs="start" background-color="white">
                                    <v-tab>General Information</v-tab>
                                    <v-tab>Inventory</v-tab>
                                </v-tabs>
                                <v-tabs-items v-model="activeTab">
                                    <v-tab-item>
                                        <v-row class="pa-5">
                                            <v-col cols="12" md="6">
                                                <strong>
                                                    Product Type
                                                    <v-icon size="x-small" class="ml-[-3px] mt-[-7px]" color="primary"
                                                        icon="mdi-help" />
                                                </strong>
                                                <strong class="text-gray-400 ml-2">Storable Product</strong>

                                            </v-col>
                                            <v-col cols="12" md="6">
                                                <v-row>
                                                    <i class="text-gray-400">
                                                        Storable products are physical items for which you manage the
                                                        inventory level.
                                                    </i>
                                                </v-row>
                                            </v-col>
                                            <v-col class="py-5" cols="12" md="6">
                                                <v-row justify="space-between">
                                                    <strong>
                                                        Sales Price
                                                        <v-icon size="x-small" class="ml-[-5px] mt-[-5px]"
                                                            color="primary" icon="mdi-help" />
                                                    </strong>
                                                    <span>1.00 ع.د</span>
                                                </v-row>
                                                <v-row justify="space-between">
                                                    <strong>
                                                        Cost
                                                        <v-icon size="x-small" class="ml-[-5px] mt-[-5px]"
                                                            color="primary" icon="mdi-help" />
                                                    </strong>
                                                    <span>0.00 ع.د</span>
                                                </v-row>
                                                <v-row>
                                                    <strong>Internal Reference</strong>
                                                </v-row>
                                                <v-row>
                                                    <strong>Barcode</strong>
                                                </v-row>
                                                <v-row>
                                                    <strong>Product Category</strong>
                                                </v-row>
                                                <v-row justify="space-between">
                                                    <strong>Product Template Tags</strong>
                                                    <span>All</span>
                                                </v-row>
                                                <v-row>
                                                    <strong>Additional Product Tags</strong>
                                                </v-row>
                                            </v-col>
                                            <v-divider></v-divider>
                                            <v-col cols="12">
                                                <strong>Internal Notes</strong>
                                                <hr>
                                                <p class="text-gray-400 py-4">This note is only for Internal Purposes
                                                </p>
                                            </v-col>
                                        </v-row>
                                    </v-tab-item>
                                    <v-tab-item>
                                        <!-- Inventory content here -->
                                    </v-tab-item>
                                </v-tabs-items>
                            </v-card-text>
                        </v-card>
                    </v-col>
                </v-row>
            </v-container>
        </v-main>
    </v-app>
</template>

<script setup>
import { ref } from 'vue';
import '../assets/tailwind.css';

const product = 'hello';
const activeTab = ref(null);
</script>