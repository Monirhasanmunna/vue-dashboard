<script setup>
import {ref} from 'vue'
import { VSkeletonLoader } from 'vuetify/labs/VSkeletonLoader'
import { createVuetify } from 'vuetify/lib/framework.mjs';

createVuetify({
    components : {
        createVuetify
    }
});

    const loading = ref(true);

    setTimeout(()=>{
        loading.value = false
    },1000);

</script>

<template>
    <v-card class="ma-5">
        <v-card-item>
            <v-row>
                <v-col>
                    <v-skeleton-loader
                    class="mx-auto border"
                    type="image"
                    v-if="loading"
                    >
                    </v-skeleton-loader>

                    <div class="bg-green pa-5" v-else>
                        One of three columns
                    </div>
                </v-col>

                <v-col>
                    <v-skeleton-loader
                    class="mx-auto border"
                    type="image"
                    v-if="loading"
                    >
                    </v-skeleton-loader>

                    <div class="bg-green pa-5" v-else>
                        One of three columns
                    </div>
                </v-col>
            </v-row>
        </v-card-item>
    </v-card>
</template>

<style scoped>

</style>