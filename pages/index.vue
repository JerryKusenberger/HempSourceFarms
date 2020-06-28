<template>
  <div id="home-page" class="page-wrapper home-page">
    <site-hero :title="title" :subtitle="subtitle" :image="featureImage">
      <!-- <button
        v-if="$siteConfig.newsletter.on"
        class="button is-primary"
        @click="$eventBus.$emit('modal-triggered', 'newsletter-modal')"
      >
        Subscribe To Newsletter
      </button> -->
    </site-hero>
    <main-section theme="one-column">
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
        <!-- All Posts -->
        <!-- <posts-grid />  -->
        <div class="content">
          <h3>Lab Reports</h3>
        </div>
        <resource-grid
          v-bind="$props"
          :resource="$cms.post"
          :theme="$siteConfig.posts.theme || $siteConfig.cards.theme || null"
        >
          <template v-slot:default="{ item }">
            <post-card
              :title="item.title"
              :link="item.url"
              :image="item.featureImage"
              :author="item.author"
              :date="item.date"
            />
          </template>
        </resource-grid>
      </template>
      <!-- <template v-slot:sidebar>
        Nothing here
      </template>-->
    </main-section>
    <!-- <news-letter-form-modal /> -->
  </div>
</template>

<script>
import { mapState } from 'vuex'
import { setPageData } from '../helper'
import PostCard from '~/components/cards/PostCard'
// import NewsLetterFormModal from '~/components/NewsLetterFormModal'

export default {
  name: 'HomePage',
  head() {
    return {
      title: `Home | ${this.$siteConfig.siteName}`
    }
  },
  components: {
    // NewsLetterFormModal
    PostCard
  },
  computed: {
    ...mapState(['title', 'subtitle', 'featureImage'])
  },
  fetch({ store, params }) {
    setPageData(store, { slug: 'home' })
  }
}
</script>

<style>
.home-page .under-subtitle {
  border-top: none;
}
</style>
