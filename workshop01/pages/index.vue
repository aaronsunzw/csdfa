<template>
  <v-card class="align-center">
    <v-container>
      <v-row class="align-center">
        <v-col cols="3"></v-col>
        <v-col cols="1">
          <v-img :src="require('../assets/slime.jpg')" alt="Slime" height="100px" width="100px" contain/>
        </v-col>
        <v-col>
          <p>{{ randomText }}</p>
        </v-col>
      </v-row>
      <v-row>
        <v-col class="d-flex justify-center align-center">
          Repository: 
          <a href="https://github.com/aaronsunzw/csdfa/tree/main/workshop01">https://github.com/aaronsunzw/csdfa/tree/main/workshop01</a>
        </v-col>
      </v-row>
    </v-container>
  </v-card>
</template>



<script>
export default {
  name: 'IndexPage',
  data() {
    return {
      randomText: '',
      textOptions: [
        "Logic will get you from A to B. Imagination will take you everywhere.",
        "There are 10 kinds of people. Those who know binary and those who don't.",
        "There are two ways of constructing a software design. One way is to make it so simple that there are obviously no deficiencies and the other is to make it so complicated that there are no obvious deficiencies.",
        "It's not that I'm so smart, it's just that I stay with problems longer.",
        "It is pitch dark. You are likely to be eaten by a grue.",
      ],
    };
  },
  created() {
    this.randomText = this.getRandomText();
  },
  methods: {
    getRandomText() {
      const randomIndex = Math.floor(Math.random() * this.textOptions.length);
      return this.textOptions[randomIndex];
    },
  },
}
</script>
