<template>
    <v-navigation-drawer location="right" expand-on-hover rail>

        <v-list density="compact">

            <v-list-item prepend-icon="mdi-folder" title="Drawer right" />
            <v-divider />
            <v-list-item title="Drawer right" />
            <v-divider />
            <v-card width="300px">
                <v-card-item v-card-title="'test'">
                    <v-img :src="'https://picsum.photos/200/300'" :lazy-src="'https://picsum.photos/id/237/200/300'"
                        style="margin-top: 20px;" />
                </v-card-item>
            </v-card>

        </v-list>

    </v-navigation-drawer>
</template>