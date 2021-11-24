<template>
  <footer>
    <div class="bg-footer-top text-white">
      <div class="container">
        <div class="row footer-top">
          <div class="col-3">
            <div class="logo-footer">
              <img src="@/assets/mobile-light-pet-logo-2x-200x52.png" alt="" />
            </div>
            <ul class="ps-0">
              <li>1234 Avada Avadaville</li>
              <li>info@you-company.company</li>
              <li>Call us: (1) 234 5678</li>
            </ul>
          </div>
          <div class="col-3">
            <h3>Shop by brand</h3>
            <ul class="ps-0 list-footer">
              <li><a href="#">Bed</a></li>
              <li><a href="#">Food</a></li>
              <li><a href="#">Toys</a></li>
              <li><a href="#">Transport</a></li>
            </ul>
          </div>
          <div class="col-3">
            <h3>Useful links</h3>
            <ul class="ps-0 list-footer">
              <li><a href="#">My account</a></li>
              <li><a href="#">Orders</a></li>
              <li><a href="#">Checkout</a></li>
              <li><a href="#">Cart</a></li>
            </ul>
          </div>
          <div class="col-3">
            <div
              class="form-container d-flex flex-column justify-content-center"
            >
              <div>
                <h4>Subcribe to our newletter</h4>
              </div>

              <form action="" class="">
                <input type="text" placeholder="insert your email...*" />
                <br />
                <button>Submit</button>
              </form>
            </div>
          </div>
        </div>
      </div>
      <div class="container">
        <div class="row">
          <div class="col">
            <div>
              <ul class="footer-menu d-flex justify-content-center m-0">
                <li class="px-4"><a href="#">Home</a></li>
                <li class="px-4"><a href="#">About</a></li>
                <li class="px-4"><a href="#">Blog</a></li>
                <li class="px-4"><a href="#">Contact</a></li>
                <li class="px-4"><a href="#">Shop</a></li>
              </ul>
              <ul class="social d-flex justify-content-center m-0">
                <li class="px-2">
                  <a href="#">
                    <i class="fa fa-facebook" aria-hidden="true"></i>
                  </a>
                </li>
                <li class="px-2">
                  <a href="#">
                    <i class="fa fa-twitter" aria-hidden="true"></i>
                  </a>
                </li>
                <li class="px-2">
                  <a href="#">
                    <i class="fa fa-instagram" aria-hidden="true"></i>
                  </a>
                </li>
                <li class="px-2">
                  <a href="#">
                    <i class="fa fa-youtube-play" aria-hidden="true"></i>
                  </a>
                </li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="bg-footer-bottom text-white">
      <div class="container">
        <div class="row footer-bottom">
          <div class="col">
            <div
              class="
                footer-bottom-text-block
                d-flex
                justify-content-center
                align-items-center
              "
            >
              <button class="bnt-up-container">
                <i class="fa fa-chevron-up" aria-hidden="true"></i>
              </button>
              <a href="#">
                <i class="fa fa-copyright" aria-hidden="true"></i>
              </a>
              <span>
                Copyright 2012 - 2020 | avada Theme by ThemeFusion | All Rights
                Reserved | Powered by WordPress</span
              >
            </div>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "Footer",
};
</script>

<style lang="scss">
.bg-footer-top {
  background-color: #1e3120;
}
.footer-top {
  padding-top: 115px;
  padding-bottom: 60px;
  border-bottom: 1px solid white;
  a {
    text-decoration: none;
    color: white;
  }
  a:hover {
    color: white;
  }
}
.logo-footer {
  margin-bottom: 50px;
}
ul {
  list-style-type: none;
  li {
    line-height: 25px;
  }
}
ul.list-footer {
  list-style-type: none;
  li {
    line-height: 65px;
  }
}
.form-container {
  padding: 0 40px;
  border-radius: 10px;
  width: 100%;
  height: 100%;
  background-color: #264229;
  background-image: url("../assets/bg-transparent-3.png");
  h4 {
    padding-bottom: 40px;
  }
  input {
    border-radius: 30px;
    height: 45px;
    padding: 15px 20px;
  }
  button {
    margin-top: 30px;
    width: 100%;
    border-radius: 30px;
    height: 45px;
  }
}

.footer-menu {
  padding: 65px 0 50px;
  a {
    text-decoration: none;
    color: white;
  }
  a:hover {
    color: white;
  }
}
.social {
  padding-bottom: 120px;
  a {
    text-decoration: none;
    color: white;
  }
  a:hover {
    color: white;
  }
  i {
    font-size: 28px;
    padding: 0 10px;
  }
}
.bg-footer-bottom {
  background-color: black;

  .footer-bottom {
    height: 80px;
    position: relative;
    .footer-bottom-text-block {
      text-align: center;
      height: 100%;
      button {
        height: 30px;
        width: 50px;
        border-radius: 5px 10px 0 0;
        position: absolute;
        bottom: 0;
        right: 0;
      }
    }
  }
}
</style>