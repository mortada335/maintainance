<template>
    <v-app id="app">
        <v-app-bar flat>
            <v-app-bar-title>
                <v-btn link to="/newMaintainance" class="text-blue-400 text-sm hover:bg-blue-400 hover:text-white">
                    <v-icon size="x-large">mdi-chevron-left</v-icon>
                    <span class="mx-1">Back</span>
                </v-btn>
                <v-spacer></v-spacer>
            </v-app-bar-title>
        </v-app-bar>

        <v-container>
            <v-app-bar class="pa-3 " flat>
                <v-app-bar-title>
                    <v-responsive>
                        <v-row>
                            <v-col cols="8" class="">
                                <v-btn-group class="gap-1 pa-0">
                                    <!-- <v-spacer></v-spacer> -->

                                    <v-btn max-width="100" size="small" link to="/thirdMaintainance"
                                        class="bg-blue-300 text-white" variant="solo-filled" flat>
                                        <h1>Produce</h1>
                                        <h1 class="text-center">All</h1>
                                    </v-btn>
                                    <v-btn size="small" class="bg-gray-300 text-white" variant="solo-filled" flat
                                        hide-details>Cancel</v-btn>
                                    <v-btn class="bg-gray-300 text-white" hide-details size="small"
                                        variant="solo-filled">Print
                                        Labels</v-btn>
                                </v-btn-group>
                                <!-- <v-spacer></v-spacer> -->


                            </v-col>
                            <!-- <v-spacer></v-spacer> -->
                            <v-col cols="4">
                                <v-btn variant="solo-filled" size="x-small" disabled
                                    class="rounded-xl bg-slate-50 font-bold " dark>Draft</v-btn>
                                <v-btn variant="solo-filled" size="x-small" disabled
                                    class="rounded-xl font-bold bg-slate-50 " color="blue" dark>Confirmed</v-btn>
                                <v-btn variant="solo-filled" size="x-small" disabled
                                    class="rounded-xl font-bold bg-slate-50 " dark>Done</v-btn></v-col>


                        </v-row>
                        <!-- <v-row>  -->
                    </v-responsive>

                    <!-- </v-row> -->
                </v-app-bar-title>
                <!-- <v-spacer></v-spacer> -->

                <!-- <div class="flex flex-row space-x-2"> -->
                <!-- </div> -->
                <!-- <v-spacer></v-spacer> -->

                <!-- <div class="gap-3 flex flex-row"> -->
                <!-- </div> -->
            </v-app-bar>
        </v-container>

        <v-main>
            <v-container>
                <v-card class="pa-3">
                    <v-toolbar class="bg-white">
                        <v-toolbar-title>
                            <v-icon class="" size="x-large">mdi-star-outline</v-icon>
                            <span class="">WH/MO/0003</span>
                        </v-toolbar-title>
                    </v-toolbar>

                    <v-divider></v-divider>

                    <v-row>
                        <v-col>
                            <v-row class="pa-5">
                                <v-col cols="12">
                                    <v-row class="gap-10">
                                        <h4>Product</h4>
                                        <h4 class="text-green-300">name</h4>
                                    </v-row>
                                    <v-row class="py-5 gap-5">
                                        <h4>Quantity</h4>
                                        <h4 class="font-bold">0.00/1.00</h4>
                                    </v-row>
                                </v-col>
                                <v-col class="pa-0 py-2" cols="10">
                                    <h4>Bill of Material</h4>
                                </v-col>
                            </v-row>
                        </v-col>
                        <v-col>
                            <v-row>
                                <v-col cols="12">
                                    <v-row class="ma-0 gap-10">
                                        <h4 class="font-bold">
                                            Scheduled Date
                                            <v-icon size="x-small"
                                                class="text-blue-300 mx-[-7px] mt-[-8px]">mdi-help</v-icon>
                                        </h4>
                                        <h4 class="text-red-500">05/13/2024 22:59:56</h4>
                                    </v-row>
                                </v-col>
                                <v-col cols="12">
                                    <v-row class="ma-0 gap-10">
                                        <h4>
                                            Scheduled End
                                            <v-icon size="x-small"
                                                class="text-blue-300 mx-[-7px] mt-[-8px]">mdi-help</v-icon>
                                        </h4>
                                        <h4 class="mx-3">05/13/2024 22:59:56</h4>
                                    </v-row>
                                </v-col>
                                <v-col cols="12">
                                    <v-row class="ma-0 gap-5">
                                        <h4>
                                            Component Status
                                            <v-icon size="x-small"
                                                class="text-blue-300 mx-[-7px] mt-[-8px]">mdi-help</v-icon>
                                        </h4>
                                        <h4 class="text-green-500">Available</h4>
                                    </v-row>
                                </v-col>
                                <v-col cols="12">
                                    <v-chip color="red darken-1" variant="flat" rounded="sm" class="pa-0">
                                        <v-avatar>
                                            <span class="text-white">A</span>
                                        </v-avatar>
                                    </v-chip>
                                    hayder
                                </v-col>
                            </v-row>
                        </v-col>
                    </v-row>

                    <v-divider></v-divider>

                    <v-list-item>

                        <v-list-item-content>
                            <v-row>
                                <v-col cols="4"><strong>Product</strong></v-col>
                                <v-col cols="4"><strong>To Consume</strong></v-col>
                                <v-col cols="4"><strong>Action</strong></v-col>
                            </v-row>
                        </v-list-item-content>
                    </v-list-item>

                    <v-divider></v-divider>

                    <v-list-item>
                        <v-list-item-content>
                            <v-row>
                                <v-col cols="4">01</v-col>
                                <v-col cols="4">add a line</v-col>
                                <v-col cols="4">
                                    <v-btn flat><span class="text-red-500">Delete</span></v-btn>
                                </v-col>
                            </v-row>
                        </v-list-item-content>
                    </v-list-item>

                    <v-list-item>
                        <v-list-item-content>
                            <v-row>
                                <v-col cols="4">02</v-col>
                                <v-col cols="4">add a line</v-col>
                                <v-col cols="4">
                                    <v-btn flat><span class="text-red-500">Delete</span></v-btn>
                                </v-col>
                            </v-row>
                        </v-list-item-content>
                    </v-list-item>
                </v-card>
            </v-container>
        </v-main>

        <v-navigation-drawer location="right" class="pa-0 ma-2">
            <v-list>
                <v-list-item>
                    <v-list-item-title class="pb-4">
                        <v-btn class="bg-blue text-white" variant="solo-filled" size="small" flat hide-details>Send
                            Message</v-btn>
                        <v-btn class="bg-gray-300 text-white" size="small" variant="solo-filled" flat hide-details>Log
                            Note</v-btn>

                    </v-list-item-title>

                    <v-list-item-content>
                        <v-list-item-title class="flex flex-row gap-1 items-center">
                            <v-chip color="red darken-1" variant="flat" rounded="sm" class="pa-0">
                                <v-avatar>
                                    <span class="text-white">A</span>
                                </v-avatar>
                            </v-chip>
                            <span>hayder</span>
                            <span class="text-gray-400 text-xs"> - 1 hour ago</span>
                        </v-list-item-title>
                        <ul class="list-disc pl-4 text-sm">
                            <li>
                                None
                                <v-icon size="x-small">mdi-arrow-right</v-icon>
                                <span class="text-blue-500 mr-1">Ready </span>
                                <i> (MO Readiness)</i>
                            </li>
                            <li>
                                Draft
                                <v-icon size="x-small">mdi-arrow-right</v-icon>
                                <span class="text-blue-500 mr-1">Completed </span>
                                <i> (state)</i>
                            </li>
                        </ul>
                    </v-list-item-content>
                </v-list-item>

                <v-list-item>
                    <v-list-item-content>
                        <v-list-item-title class="flex flex-row gap-1">
                            <v-chip color="red darken-1" variant="flat" rounded="sm" class="pa-0">
                                <v-avatar>
                                    <span class="text-white">A</span>
                                </v-avatar>
                            </v-chip>
                            <span>hayder</span>
                            <span class="text-gray-400 text-xs my-1"> - 1 hour ago</span>
                        </v-list-item-title>
                        <v-list-item-subtitle class="absolute right-6 top-9">Production Order
                            Completed</v-list-item-subtitle>
                    </v-list-item-content>
                </v-list-item>
            </v-list>
        </v-navigation-drawer>
    </v-app>
</template>

<script setup>
import '../assets/tailwind.css'
</script>

<style scoped>
/* Add any custom styles here */
</style>