<template>
  <div class="result-hotel">
    <div class="container">
      <ul class="nav nav-tabs result-hotel__tabs" id="myTab" role="tablist">
        <li class="nav-item result-hotel__tabs-item">
          <a class="nav-link result-hotel__tabs-link active" id="all-tab" data-toggle="tab" href="#all">Mọi lựa chọn</a>
        </li>
        <li class="nav-item result-hotel__tabs-item">
          <a class="nav-link result-hotel__tabs-link" id="profile-tab" data-toggle="tab" href="#profile">Khách sạn</a>
        </li>
        <li class="nav-item result-hotel__tabs-item">
          <a class="nav-link result-hotel__tabs-link" id="contact-tab" data-toggle="tab" href="#contact">
            <i aria-hidden="true" class="fa fa-modx"></i> agoda home
          </a>
        </li>
      </ul>
      <div class="tab-content" id="myTabContent">
        <div class="tab-pane fade show active" id="all" role="tabpanel" aria-labelledby="all-tab">
          <div class="result-hotel__wrapper">
            <a href="#" class="result-hotel__wrapper-link">
              <span class="result-hotel__suggest">Gợi ý cho bạn</span>
              <div class="result-hotel__content">
                <div class="result-hotel__content-image">
                  <img src="//pix6.agoda.net/hotelImages/267/267398/267398_16032317580041022202.jpg?s=450x450" class="img-fluid"
                    alt="Hanoi Merci Hotel">
                  <div class="result-hotel__content-thumnail-list">
                    <div class="result-hotel__content-thumnail-item" style="background: red"></div>
                    <div class="result-hotel__content-thumnail-item" style="background: red"></div>
                    <div class="result-hotel__content-thumnail-item" style="background: red"></div>
                    <div class="result-hotel__content-thumnail-item" style="background: red"></div>
                    <div class="result-hotel__content-thumnail-item" style="background: red"></div>
                    <div class="result-hotel__content-thumnail-item" style="background: red"></div>
                    <div class="result-hotel__content-thumnail-item" style="background: red"></div>
                    <div class="result-hotel__content-thumnail-item" style="background: red"></div>
                    <div class="result-hotel__content-thumnail-item" style="background: red"></div>
                    <div class="result-hotel__content-thumnail-item" style="background: red"></div>
                  </div>
                </div>
                <div class="result-hotel__content-detail">
                  <h2 class="result-hotel__content-detail__name-hotel">
                    Khách sạn & Căn hộ Palmo 2 (Palmo Hotel &
                    Apartment 2)
                  </h2>
                  <div class="result-hotel__content-detail__location">
                    <div class="result-hotel__content-detail__location">
                      <span class="badge badge-primary result-hotel__content-detail__location-badge">Agoda Homes</span>
                      <span>Chung cư</span>
                    </div>
                    <div class="result-hotel__content-detail__star">
                      <span>
                        <i class="fa fa-star" aria-hidden="true"></i>
                        <i class="fa fa-star" aria-hidden="true"></i>
                        <i class="fa fa-star" aria-hidden="true"></i>
                        <i class="fa fa-star" aria-hidden="true"></i>
                      </span>
                      <span>
                        <i class="fa fa-street-view" aria-hidden="true"></i>Quận Ba Đình, Hà Nội - Xem trên bản đồ
                      </span>
                    </div>
                  </div>
                  <div class="result-hotel__content-detail__rate">
                    <span>vị trí tuyệt vời</span>
                  </div>
                  <div class="result-hotel__content-detail__service">
                    <span>Ăn sáng</span>
                    <span>Ăn sáng</span>
                    <span>Ăn sáng</span>
                  </div>
                  <div class="result-hotel__content-detail__card">
                    <i class="fa fa-credit-card" aria-hidden="true"></i>
                    <span>Không cần thẻ tín dụng</span>
                  </div>
                  <div class="result-hotel__content-detail__guest-recommnended">
                    <i class="fa fa-users" aria-hidden="true"></i>
                    <span>Được 69% người giới thiệu</span>
                  </div>
                  <div class="result-hotel__content-detail__selling">
                    <span class="badge badge-primary">Đang bán chạy</span>
                    <span>Lần đặt gần đây nhất là 6 giờ</span>
                  </div>
                  <div class="result-hotel__content-detail__discount-code">
                    <span class="badge badge-primary">WEEKENDSALE</span>
                    <span>Đã dùng coupon - GIẢM</span>
                    <span>112.208 ₫</span>
                  </div>
                </div>
                <div class="result-hotel__content-price">
                  <div class="result-hotel__content-price__review">
                    <div class="result-hotel__content-price__review-text">Xuất sắc
                      <br>107 nhận xét
                    </div>
                    <div class="result-hotel__content-price__review-score">8.4</div>
                  </div>
                  <div class="result-hotel__content-price__ribbon">Còn 1 phòng có giá này</div>
                  <div class="result-hotel__content-price__discount">
                    <i class="fa fa-line-chart" aria-hidden="true"></i>
                    <span>Giảm giá 28%</span>
                  </div>
                  <div class="result-hotel__content-price__room-rate">
                    <p>Giá mỗi đêm rẻ nhất từ</p>
                    <div class="old-price">100.000.000</div>
                    <div class="new-price">500000</div>
                  </div>
                  <div class="result-hotel__content-price__benefit">
                    <p>Hủy miễn phí</p>
                  </div>
                </div>
              </div>
            </a>
          </div>
        </div>
        <div class="tab-pane fade" id="profile" role="tabpanel" aria-labelledby="profile-tab">...</div>
        <div class="tab-pane fade" id="contact" role="tabpanel" aria-labelledby="contact-tab">...</div>
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