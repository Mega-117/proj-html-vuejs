<template>
  <main>
    <Hero :contentHero="HeroList[0]"></Hero>
    <div class="promo">
      <div class="container">
        <div class="d-flex justify-content-center align-items-center">
          <img src="../assets/food-transparent-5-200x112.png" alt="" />
          <span>
            Get $25 OFF your first purchase of our homemade pet food!</span
          >
          <a href="#">Visit the shop</a>
        </div>
      </div>
    </div>

    <!-- category-product -->
    <div>
      <div class="container">
        <section class="categoty-secion">
          <IntroSection :content="introSection[0]"></IntroSection>
          <CardProduct :products="productList"></CardProduct>
        </section>
      </div>
    </div>
    <!-- fine category-product -->

    <!-- food card -->
    <div>
      <div class="container">
        <section class="animal-food">
          <div class="row row-cols-3 gx-5">
            <div v-for="(el, i) in foodList" :key="i" class="col">
              <div
                class="
                  food-card
                  bg-dog
                  d-flex
                  flex-column
                  align-items-center
                  py-5
                "
              >
                <div class="text-box">
                  <h2>{{ el.title }}</h2>
                  <small>{{ el.subTitle }}</small>
                </div>
                <div class="product">
                  <img :src="el.src" alt="" />
                </div>
                <button class="btn-2">
                  <strong>{{ el.btnText }}</strong>
                </button>
              </div>
            </div>
          </div>
        </section>
      </div>
    </div>
    <!-- fine food card -->

    <!-- hero 2 -->
    <div>
      <div class="container">
        <Hero :contentHero="HeroList[1]"></Hero>
      </div>
    </div>
    <!-- fine hero 2 -->

    <!-- best sellers -->
    <div>
      <div class="container">
        <section class="categoty-secion">
          <IntroSection :content="introSection[1]"></IntroSection>
          <CardProduct
            :products="productBestSellerList"
            :columnNumber="col4"
          ></CardProduct>
        </section>
      </div>
    </div>
    <!-- finebest sellers -->

    <!-- testimonials -->

    <GreenBlock :content="testimonials"></GreenBlock>

    <!-- fine testimonials -->

    <!-- hero 3 -->
    <div>
      <div class="container">
        <div class="bg-newsletter d-flex align-items-center">
          <div class="newsletter-text">
            <h1>Join our newsletter</h1>
            <p>
              Volutpat vel turpis nulla lorem sed semper. Aliquam sagittis sem
              libero viverra vehicula nullam ut nisl.
            </p>
            <form action="">
              <input
                class="bg-grey-input"
                type="text"
                placeholder="insert your email...*"
              />
              <button class="btn-2"><strong>Subscribe</strong></button>
            </form>
          </div>
        </div>
      </div>
    </div>

    <!-- fine hero 3 -->

    <!-- tip e trick -->
    <div>
      <div class="container">
        <section class="categoty-secion">
          <IntroSection :content="introSection[2]"></IntroSection>
          <CardProduct :products="tipTrick" :columnNumber="col4"></CardProduct>
          <div class="text-center">
            <button class="btn-2">Read all article</button>
          </div>
        </section>
      </div>
    </div>
    <!-- fine tip e trick -->

    <!-- doble hero -->
    <div class="doble-hero">
      <div class="riga">
        <div class="colonna1">
          <!-- hero 1 -->
          <Hero :contentHero="HeroList[2]"></Hero>
        </div>
        <!-- hero 2 -->
        <div class="colonna2">
          <Hero :contentHero="HeroList[3]"></Hero>
        </div>
      </div>
    </div>
    <!-- fine doble hero -->

    <!-- promo service -->
    <GreenBlock :content="promeService"></GreenBlock>
    <!-- fine promo service -->

    <!-- new arrive -->
    <div>
      <div class="container">
        <section class="categoty-secion">
          <IntroSection :content="introSection[3]"></IntroSection>
          <CardProduct
            :products="productsNewArival"
            :columnNumber="col3"
          ></CardProduct>
        </section>
      </div>
    </div>
    <!-- fine new arrive -->
  </main>
</template>

<script>
import Hero from "../components/Hero.vue";
import CardProduct from "../components/CardProduct.vue";
import IntroSection from "../components/IntroSection.vue";
import GreenBlock from "../components/GreenBlock.vue";
export default {
  name: "Main",
  components: { Hero, CardProduct, IntroSection, GreenBlock },
  data() {
    return {
      col4: "row-cols-4",
      col3: "row-cols-3",
      productList: [
        {
          src: require("@/assets/product-9-400x400.jpg"),
          text: "Bed (1)",
          alignText: "text-center",
        },
        {
          src: require("@/assets/product-3-400x400.jpg"),
          text: "Food (6)",
          alignText: "text-center",
        },
        {
          src: require("@/assets/product-2-400x400.jpg"),
          text: "Toys (6)",
          alignText: "text-center",
        },
        {
          src: require("@/assets/product-4-400x400.jpg"),
          text: "Transport (6)",
          alignText: "text-center",
        },
      ],
      tipTrick: [
        {
          src: require("@/assets/blog-1-400x400.jpg"),
          text: "How to 'loose leash walk' your dog",
          dataText: "April 21st, 2020",
          textOverlay2: "Tip & Tricks",
        },
        {
          src: require("@/assets/blog-2-400x400.jpg"),
          text: "Stop cats from scratching furniture",
          dataText: "April 19th, 2020",
          textOverlay2: "Tip & Tricks",
        },
        {
          src: require("@/assets/blog-3-200x200.jpg"),
          text: "Where to buy the best pet food",
          dataText: "April 18th, 2020",
          textOverlay2: "Tip & Tricks",
        },
        {
          src: require("@/assets/blog-4-200x200.jpg"),
          text: "Proper care for your pet toys",
          dataText: "April 17th, 2020",
          textOverlay2: "Tip & Tricks",
        },
      ],
      productBestSellerList: [
        {
          src: require("@/assets/product-21-400x400.jpg"),
          text: "Transport cage",
          price: "$25.00",
          alignText: "text-center",
          textOverlay: "VIEW CART",
        },
        {
          src: require("@/assets/product-20-400x400.jpg"),
          text: "Dog leash",
          price: "$25.00",
          alignText: "text-center",
          textOverlay: "VIEW CART",
        },
        {
          src: require("@/assets/product-16-400x400.jpg"),
          text: "Animal transport cage",
          price: "$25.00",
          scount: "$35.00",
          alignText: "text-center",
          textOverlay: "VIEW CART",
        },
        {
          src: require("@/assets/product-11-400x400.jpg"),
          text: "Colorful cat leash",
          price: "$12.00",
          alignText: "text-center",
          textOverlay: "VIEW CART",
        },
      ],
      introSection: [
        {
          title: "Browse by category",
          text: "Augue purus et, tincidunt condimentus mauris. At nibh rutrum mi in. Nisi, vitae interdum eleifend dui, consequat nulla rhoncus dictum. Viverra.",
          align: "d-flex justify-content-center",
          alignText: "text-center",
        },
        {
          textUp: "All-time-best sellers",
          textSmall: "text-green",
          title: "Items everyone loves",
          text: "",
          align: "d-flex justify-content-between align-items-center",
          alignText: "text-left",
          btnText: "View all products",
        },
        {
          title: "Get the best tips & tricks",
          text: "Recent articles",
          align: "d-flex justify-content-center",
          alignText: "text-center",
        },
        {
          title: "New products arrival",
          text: "Last products",
          align: "d-flex justify-content-center",
          alignText: "text-center",
        },
      ],
      foodList: [
        {
          title: "Kibble",
          subTitle: "Dry dog food",
          src: require("@/assets/food-transparent-18-400x420.png"),
          btnText: "Shop dry food",
        },
        {
          title: "Moist",
          subTitle: "Canned dog food",
          src: require("@/assets/food-transparent-17-400x420.png"),
          btnText: "Shop moist food",
        },
        {
          title: "Frozen",
          subTitle: "Freeze-Dried dog food",
          src: require("@/assets/food-transparent-16-400x420.png"),
          btnText: "Shop frozen food",
        },
      ],
      HeroList: [
        {
          title:
            "We know animals are a part of yiur family, let us help take care of them.",
          subTitle: "find the best anima supplies",
          src: require("@/assets/food-transparent-18-400x420.png"),
          btnText: "Learn more about us",
          bgHero: "bg-hero",
          align: "hero-text-container",
          overlay: true,
        },
        {
          title: "New Arrivals weekly",
          subTitle: "find the best anima supplies",
          src: require("@/assets/food-transparent-18-400x420.png"),
          btnText: "Learn more about us",
          bgHero: "bg-hero-2",
          align: "hero-text-container-center",
          overlay: false,
        },
        {
          title: "Popular accessories",
          subTitle: "find the best anima supplies",
          src: require("@/assets/food-transparent-18-400x420.png"),
          btnText: "View all toys accessories",
          bgHero: "bg-hero-4",
          align: "hero-text-container-center",
          overlay: false,
        },
        {
          title: "New food arrival",
          subTitle: "find the best food",
          src: require("@/assets/food-transparent-18-400x420.png"),
          btnText: "View all food products",
          bgHero: "bg-hero-5",
          align: "hero-text-container-center",
          overlay: false,
        },
      ],
      testimonials: [
        {
          align: "testimonials",
          testimonials: true,
          src: require("@/assets/avatar-3-200x200.jpg"),
          text: " Auctor est habitasse amet nunc , interdum vel mattis sodales cras. Ut nulla quis nun,tincidunt eu. Eu.",
          name: "Lisa Smith, ThemeFusion",
        },
        {
          testimonials: true,
          src: require("@/assets/avatar-1-200x200.jpg"),
          text: "Donec sollicitudin molestie malesuada Vivamus suscipit tortor eget felis porttitor volutpat vestibulum ac diam sit.",
          name: "Melissa Green, ThemeFusion",
        },
        {
          testimonials: true,
          src: require("@/assets/avatar-4-200x200.jpg"),
          text: "Curabitur arcu erat, accumsan id imperdiet et, porttitor at sem. Proin eget tortor risus vestibulum ante ipsum",
          name: "Sam Lewis, ThemeFusion",
        },
      ],
      promeService: [
        {
          align: "servizzi",
          icon: "fa fa-truck",
          text: "",
          name: "Free worldwide deliveries",
        },
        {
          icon: "fa fa-map-o",
          text: "",
          name: "Find store near you",
        },
        {
          icon: "fa fa-usd",
          text: "",
          name: "Best price guarranteed",
        },
        {
          icon: "fa fa-credit-card",
          text: "",
          name: "All credit card accepted",
        },
      ],
      productsNewArival: [
        {
          src: require("@/assets/product-8-400x400.jpg"),
          text: "Colored pet bed",
          price: "$18.00",
          price2: "- $26.00",
          alignText: "text-center",
          textOverlay: "VIEW CART",
          sale: false,
        },
        {
          src: require("@/assets/product-2-400x400.jpg"),
          text: "Colorful ball set",
          price: "$29.00",
          alignText: "text-center",
          textOverlay: "VIEW CART",
          sale: false,
        },
        {
          src: require("@/assets/product-3-400x400.jpg"),
          text: "Dog bone",
          price: "$18.00",
          scount: "$29.00",
          alignText: "text-center",
          textOverlay: "VIEW CART",
          sale: true,
        },
        {
          src: require("@/assets/product-4-400x400.jpg"),
          text: "Animal transport bag",
          price: "$29.00",
          alignText: "text-center",
          textOverlay: "VIEW CART",
          sale: false,
        },
        {
          src: require("@/assets/product-5-400x400.jpg"),
          text: "Animal transport cage",
          price: "$35.00",
          alignText: "text-center",
          textOverlay: "VIEW CART",
          sale: false,
        },
        {
          src: require("@/assets/product-10-400x400.jpg"),
          text: "Animal transport cage",
          price: "$16.00",
          alignText: "text-center",
          textOverlay: "VIEW CART",
          sale: false,
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
@import "@/styles/main.scss";
</style>