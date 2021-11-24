<template>
  <!-- header top -->
  <header>
    <div class="header-top-container">
      <div class="container">
        <div
          class="header-top d-flex justify-content-between align-items-center"
        >
          <div class="logo-container">
            <a href="#">
              <img src="../assets/dark-pet-logo.png" alt="" />
            </a>
          </div>
          <div class="search-bar">
            <input class="bg-grey-input" type="text" placeholder="Search..." />
          </div>
          <div>
            <h5 class="d-inline-block pe-2">Questions?</h5>
            <span>Call us: 1800123.4567</span>
          </div>
          <div>
            <a href="#" class="text-black">
              <i class="fa fa-shopping-bag" aria-hidden="true"></i>
            </a>
            <a href="#" class="text-black">
              <i class="ps-3 fa fa-user-o" aria-hidden="true"></i>
            </a>
          </div>
        </div>
      </div>
    </div>
    <div class="header-bottom-container">
      <div class="container">
        <nav>
          <ul class="d-flex justify-content-center mb-0">
            <li v-for="(el, i) in navPrincipale" :key="i">
              <a :href="el.link"
                >{{ el.title }}

                <i
                  v-if="el.type === 'drop'"
                  class="fa fa-chevron-down"
                  aria-hidden="true"
                ></i>
              </a>
            </li>
          </ul>
        </nav>
      </div>
    </div>
    <div class="promo-services">
      <div class="container">
        <ul class="d-flex justify-content-around align-items-center mb-0">
          <li>
            <i class="pe-2 fa fa-map-o" aria-hidden="true"></i
            ><strong>international</strong>
            Shipping Services
          </li>
          <li>
            <i class="pe-1 fa fa-clock-o" aria-hidden="true"></i> See our
            <strong>store houses</strong> and services
          </li>
          <li>
            <i class="pe-1 fa fa-check" aria-hidden="true"></i> We price match
            to give you the <strong>best deals</strong>
          </li>
        </ul>
      </div>
    </div>
  </header>
  <!-- header bottom -->
</template>

<script>
export default {
  data() {
    return {
      navPrincipale: [
        {
          title: "Home",
          link: "#",
          type: "drop",
        },
        {
          title: "Shop",
          link: "#",
          type: "drop",
        },
        {
          title: "About",
          link: "#",
          type: "normal",
        },
        {
          title: "Blog",
          link: "#",
          type: "normal",
        },
        {
          title: "Contact",
          link: "#",
          type: "normal",
        },
        {
          title: "Shop by brand",
          link: "#",
          type: "drop",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
@import "../styles/header.scss";
</style>