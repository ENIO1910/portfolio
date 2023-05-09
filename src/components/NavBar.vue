<template>
    <v-app-bar app color="black" dark flat class="px-12">
        <v-btn class="d-flex ">
            <div class="d-flex align-baseline">
                <v-icon color="warning" left class="mr-2">fa-solid fa-robot</v-icon>
                <p class="ml-2" style="font-size:14px;">Patryk Staniewski</p>
            </div>
        </v-btn>
        <v-spacer></v-spacer>
        <v-btn text @click="scroll('home')" class="text-orange">Home</v-btn>
        <v-btn text @click="scroll('About')" class="text-white">About</v-btn>
        <v-btn text @click="scroll('portfolio')" class="text-white">portfolio</v-btn>
        <v-btn text @click="scroll('services')" class="text-white">services</v-btn>
        <v-btn text @click="scroll('page')" class="text-white">page</v-btn>
        <v-btn text @click="scroll('contact')" class="text-white">contact</v-btn>
    </v-app-bar>
</template>

<script>
  export default {
      methods: {
          scroll(refName) {
              const element = document.getElementById(refName);
              element.scrollIntoView({behavior: "smooth"});

          }
      }
  }
</script>

<style>

</style>