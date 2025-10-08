<script setup>
const emit = defineEmits(["AddComponent"])
</script>
<template>
    <v-sheet rounded border="sm" class="text-white mx-auto" color="#141518">
        <v-container>
            <v-row align="start" no-gutters>
                <v-col cols="2" no-gutters>
                    <v-icon icon="fa:fas fa-user">
                    </v-icon>
                </v-col>
                <v-col cols="1" no-gutters>
                    <v-divider vertical></v-divider>
                </v-col>
                <v-col cols="9" no-gutters>
                    <p>Header</p>
                </v-col>
            </v-row>
        </v-container>
    </v-sheet>
</template>