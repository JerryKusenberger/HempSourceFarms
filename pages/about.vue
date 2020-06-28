<template>
  <div id="about-page" class="page-wrapper about-page content-page">
    <site-hero
      title="About Us"
      subtitle=""
      image="/uploads/about-hero.jpg"
    ></site-hero>
    <main-section>
      <template v-slot:default>
        <div class="content">
          <h3>Our Products</h3>
          <p>
            Hemp Source Farms, LLC is a boutique farmer offering Oregon grown
            Deschutes & Umpqua flowers with F1 genetics grown from 100% organic
            seeds feminized for high CBD content. These sativa strains were
            outdoor farm cultivated and only fed with super-filtered natural
            Umpqua River water and grown without the use of any pesticide, spray
            or synthetic fertilizer to ensure a 100% organic product for our
            customers. Flowers were air dried, cured and stored in
            temperature-controlled environments to optimize bud integrity. Our
            flowers are rated “Top-Shelf”, due to their strains, care in
            cultivation, and attention to detail specialized processing. Our
            flowers are packed full of flavor and aroma, have a beautiful feel
            and aesthetic, plus the desirable cannabinoid content your customers
            are looking for. We are sure these flowers will add unique value to
            your assortment and bring customers back for more!
          </p>

          <h3>Umpqua</h3>
          <p>
            The Umpqua CBD hemp strain has a dense complex flower structure with
            a fragrance of gas, pine, and citrus. Umpqua is covered with complex
            trichomes, light green with orange pistols and light-yellow hues.
            Dominant Terpenes: Myrcene, β-Caryophyllene, a-Pinene, Limonene.
            Contains less than 0.3% delta-9 THC
          </p>
          <h3>Deschutes</h3>
          <p>
            Deschutes offers an earthy yet spicy peppery clove like taste with a
            floral aroma. This smooth smoke is packed with mutli-colored nuggets
            bursting with silvery trichomes. Dominant terpenes: B-caryophyllene,
            Elemene, Myrcene, Guaiol, Humelene Contains less than 0.3% delta-9
            THC
          </p>
        </div>
      </template>
    </main-section>
  </div>
</template>
<script>
// import QuoteCard from '~/components/cards/QuoteCard'
export default {
  head() {
    return {
      title: `About | ${this.$siteConfig.siteName}`
    }
  },
  components: {
    // QuoteCard
  }
}
</script>
