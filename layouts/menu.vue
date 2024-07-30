<template>
    <v-app>
        <v-tool-bar class="d-flex justify-space-between mx-16 my-6">
            <v-tool-bar-title class="ml-14">
                <NuxtLink to=""><img src="https://cdn.prod.website-files.com/63877b2a41191ed2e132006b/64dff2526c35b16f4ec9b74e_Component%209.png" loading="lazy" width="124" alt=""></NuxtLink>
            </v-tool-bar-title>
            <div class="mr-14">
                <v-btn text rounded large class="text-capitalize">Organizations</v-btn>
                <v-btn text rounded large class="text-capitalize">Workers</v-btn>
                <v-menu open-on-hover no-click-animation offset-y>
                    <template v-slot:activator="{ on, attrs }">
                        <v-btn text v-bind="attrs" v-on="on" rounded large class="text-capitalize">
                            <span>Resources</span>
                            <v-icon>mdi-chevron-down</v-icon>
                        </v-btn>
                    </template>
                    <v-card>
                        <v-list class="d-flex">
                            <div class="d-flex flex-column">
                                <v-list-subheader class="text-black text-bold font-weight-medium ml-8">Product</v-list-subheader>
                                <v-hover v-slot="{ hover }">
                                    <v-btn rounded text class="text-capitalize text-body-2"><v-list-item :class="hover ? 'deep-purple--text' : 'blue-grey--text'">FAQ</v-list-item></v-btn>
                                </v-hover>
                                <v-hover v-slot="{ hover }">
                                    <v-btn rounded text class="text-capitalize text-body-2"><v-list-item :class="hover ? 'deep-purple--text' : 'blue-grey--text'">Contact Us</v-list-item></v-btn>
                                </v-hover>
                            </div>
                            <v-divider class="mb-2"></v-divider>
                            <div class="d-flex flex-column">
                                <v-list-subheader class="text-black font-weight-medium ml-8">Other</v-list-subheader>
                                <v-hover v-slot="{ hover }">
                                    <v-btn rounded text class="text-capitalize text-body-2"><v-list-item :class="hover ? 'deep-purple--text' : 'blue-grey--text'">Terms & Conditions</v-list-item></v-btn>
                                </v-hover>
                                <v-hover v-slot="{ hover }">
                                    <v-btn rounded text class="text-capitalize text-body-2"><v-list-item :class="hover ? 'deep-purple--text' : 'blue-grey--text'">Privacy Policy</v-list-item></v-btn>
                                </v-hover>
                            </div>
                        </v-list>
                    </v-card>
                </v-menu>
                <v-hover v-slot="{ hover }">
                    <v-btn rounded :color="hover ? '#e4e6f1' : '#f89500'" depressed :dark="!hover" large class="text-capitalize">Get Started</v-btn>
                </v-hover>
            </div>
        </v-tool-bar>
    </v-app>
    
</template>

<script>
export default {
    name: 'Menu',
    data() {
        return {}
    }
}
</script>

<style scoped>
    
</style>

