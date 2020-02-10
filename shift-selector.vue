<template>
<div id="app">
  <v-app id="inspire">
    <v-row align="center" style="width: 50%;">
      <v-col class="text-center" cols="12" sm="4">
        <div class="my-2">
          <v-btn depressed :color="if1Chosen" @click="changeSelection(1)">Shift 1</v-btn>
        </div>
      </v-col>
      <v-col class="text-center" cols="12" sm="4">
        <div class="my-2">
          <v-btn depressed :color="if2Chosen" @click="changeSelection(2)">Shift 2</v-btn>
        </div>
      </v-col>
    </v-row>
    
  </v-app>
</div>
</template>

<script>
// import store mapping

export defaults {
  data() {
    return {
      if1Chosen: "primary",
      if2Chosen: "primary",
      
    }
  },
  methods: {
    changeSelection (num) {
      if(num == 1) {
        if(this.if1Chosen == "primary") {
          this.if1Chosen = "outlined";
          // remove this shift from the table
        }
        else {
          this.if1Chosen = "primary";
         // add this shift to table
        }
      }
      else {
        if(this.if2Chosen == "primary") {
          this.if2Chosen = "outlined";
          // remove this shift from the table
        }
        else {
          this.if2Chosen = "primary";
         // add this shift to table
        }
      }
    }
  }
}
</script>