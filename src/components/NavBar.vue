<template>
    <v-app-bar app color="black" class="remove-height-style">
        <div class="d-sm-flex d-md-flex">
            <v-btn class="d-sm-flex d-md-flex">
                <div class="d-flex align-baseline">
                    <v-icon color="warning" left class="mr-2">fa-solid fa-robot</v-icon>
                    <p class="ml-2" style="font-size: 14px;">Patryk Staniewski</p>
                </div>
            </v-btn>
            <v-spacer></v-spacer>
            <v-btn text @click="scroll('home')" class="text-orange d-md-flex">Home</v-btn>
            <v-btn text @click="scroll('about')" class="text-white d-md-flex">About</v-btn>
            <v-btn text @click="scroll('portfolio')" class="text-white d-md-flex">Portfolio</v-btn>
            <v-btn text @click="scroll('pages')" class="text-white d-md-flex">Pages</v-btn>
            <v-btn text @click="scroll('contact')" class="text-white d-md-flex">Contact</v-btn>
        </div>

    </v-app-bar>
</template>

<script>
export default {
    methods: {
        scroll(refName) {
            const element = document.getElementById(refName);
            element.scrollIntoView({ behavior: "smooth" });
        },
    },
};
</script>

<style scoped>
.phones {
    display: flex;
    align-items: center;
    min-height: 500px;
}

.remove-height-style :deep(.v-toolbar__content) {
    text-align: center;
    width: 100%;
    height: auto !important;
    justify-content: space-evenly;
}
</style>
