<template>
  <div id="diffy">
    <input type="text" v-model="name" />
    <button class="btn btn-success" @click="searchData()">Date</button>
    <div>Example YYYY-MM-DD</div>
    <b-card class="card bg-dark">
      <b-card
        v-for="data in resultData"
        :key="data.date"
        :title="data.title"
        :img-src="data.hdurl"
      >
        <div>{{ data.explanation }}</div>
      </b-card>
    </b-card>
  </div>
</template>

<script>
import axios from "axios";

export default {
  data() {
    return {
      resultData: null,
      name: "",
    };
  },

  methods: {
    searchData() {
      axios
        .get(
          "https://api.nasa.gov/planetary/apod?api_key=PjegsGGK7fmIKaCllSdF7lC4svqoD7mK0CTT24KR&date=" +
            this.name
        )
        .then((response) => {
          this.resultData = response;
        })
        .catch((err) => {
          console.log(err);
        });
    },
  },
};
</script>

<style>
#diffy {
  color: black;
  font-weight: 600;
  background: blanchedalmond;
}
</style>