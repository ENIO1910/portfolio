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
        <v-btn text @click="scroll('about')" class="text-white">About</v-btn>
        <v-btn text @click="scroll('portfolio')" class="text-white">Portfolio</v-btn>
        <v-btn text @click="scroll('pages')" class="text-white">Pages</v-btn>
        <v-btn text @click="scroll('contact')" class="text-white">Contact</v-btn>
    </v-app-bar>
</template>

<script>
  export default {
      methods: {
          scroll(refName) {
              const element = document.getElementById(refName);
              element.scrollIntoView({behavior: "smooth"});
          },
      },
  };
</script>

<style>

</style>