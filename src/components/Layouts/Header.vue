<script setup>

</script>

<template>
    <v-app-bar title="MY APP" :elevation="1">
            <template v-slot:append>
                <v-menu transition="slide-y-reverse-transition" width="180">
                    <template v-slot:activator="{props}">
                        <v-avatar v-bind="props" class="mr-3" image="https://randomuser.me/api/portraits/men/85.jpg"></v-avatar>
                    </template>

                    <v-list>
                        <v-list-item>
                        <v-list-item-title>Click Me1</v-list-item-title>
                        </v-list-item>

                        <v-list-item>
                        <v-list-item-title>Click Me1</v-list-item-title>
                        </v-list-item>

                        <v-list-item>
                        <v-list-item-title>Click Me1</v-list-item-title>
                        </v-list-item>
                    </v-list>

                </v-menu>
            </template>
        </v-app-bar>
</template>

<style scoped>

</style>