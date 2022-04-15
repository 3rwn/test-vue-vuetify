<template>
  <v-app>
    <v-app-bar app color="primary" dark>
      <v-toolbar-title>{{ school }}</v-toolbar-title>
    </v-app-bar>

    <v-main>
      <div class="text-center pa-10">👋 Bonjour 👋</div>
      <v-btn v-bind="{ block: isblock }" @click='greet'>Clique ici</v-btn>    
      <v-card>
        <v-card-text>
          test
        </v-card-text>
      </v-card>
    </v-main>

  </v-app>
</template>

<script>
  export default {
    name: "App",
    data() {
      return { school: "MyDigitalSchool",
      isblock: false };
    },
    methods: {
    greet: function () {
      this.isblock= true,
      // `this` fait référence à l'instance de Vue à l'intérieur de `methods`
      alert('Bonjour !')
      // // `event` est l'évènement natif du DOM
      // if (event) {
      //   alert(event.target.tagName)
      // }
    }
  }
  }
</script>

sty