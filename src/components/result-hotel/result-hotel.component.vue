<template>
  <div class="result-hotel">
    <div class="container">
      <div class="result-hotel__wrapper">
        <a href="#">
          <span class="result-hotel__suggest">Gợi ý cho bạn</span>
          <div class="result-hotel__content">
            <div class="result-hotel__content-img">
              <img
                src="//pix6.agoda.net/hotelImages/267/267398/267398_16032317580041022202.jpg?s=450x450"
                class="img-fluid"
                alt="Hanoi Merci Hotel"
              >
            </div>
            <div class="result-hotel__content-detail"></div>
            <div class="result-hotel__content-price"></div>
          </div>
        </a>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import "./result-hotel.component.scss";
import axios from "axios";
export default {
  name: "ResultHotel",
  data() {
    return {
      hotel: []
    };
  },
  created() {
    this.getData();
  },

  methods: {
    async getData() {
      const response = await axios.get("https://demo0535107.mockable.io/agoda");
      this.hotel = response.data.ResultList;
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->