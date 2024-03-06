<template>
    <v-main class="pt-0">
      <v-carousel height="700">
        <v-carousel-item
          cover
          v-for="(item, index) in carouselItems"
          :src="item.imageUrl"
          :key="index"
        >
        </v-carousel-item>
      </v-carousel>
      <v-container>
        <h2>寵物服務</h2>
        <v-row>
          <v-col
            v-for="(service, index) in petServices"
            :key="index"
            cols="12"
            md="4"
          >
            <v-card height="380">
              <v-img cover :src="service.imageUrl" height="200"></v-img>
              <v-card-title>{{ service.name }}</v-card-title>
              <v-card-text>{{ service.description }}</v-card-text>
              <v-card-actions>
                <v-btn color="primary">了解更多</v-btn>
              </v-card-actions>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
      <v-container>
        <v-row>
          <v-col cols="12">
            <h2>精選商品</h2>
          </v-col>
          <v-col
            v-for="(product, index) in products"
            :key="index"
            cols="12"
            md="4"
          >
            <v-card height="350">
              <v-img cover :src="product.imageUrl" height="200"></v-img>
              <v-card-title>{{ product.name }}</v-card-title>
              <v-card-text>{{ product.description }}</v-card-text>
              <v-card-actions>
                <v-btn color="primary">購買</v-btn>
              </v-card-actions>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </v-main>
  </template>
  
  <script>
    export default {
      data() {
        return {
          petServices: [
            {
              name: '寵物美容',
              description: '專業的寵物美容服務，讓您的寵物看起來更加美麗和健康。',
              imageUrl:
                'https://d3nb97lilvchvx.cloudfront.net/category_page/pet_grooming.jpg',
            },
            {
              name: '寵物健康檢查',
              description: '定期的健康檢查，確保您的寵物身體狀況良好。',
              imageUrl:
                'https://pet-care.event2.tw/Content/upload/News/294a344a-540d-4802-b2f6-cc0f1953866e.jpg',
            },
            {
              name: '寵物培訓',
              description: '訓練您的寵物成為良好的伴侶，學習基本指令和行為。',
              imageUrl:
                'https://images.unsplash.com/photo-1658314756284-7a83b8729efb?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80',
            },
          ],
          carouselItems: [
            {
              imageUrl:
                'https://images.unsplash.com/photo-1563460716037-460a3ad24ba9?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1974&q=80',
            },
            {
              imageUrl:
                'https://images.unsplash.com/photo-1557495235-340eb888a9fb?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2013&q=80',
            },
            {
              imageUrl:
                'https://images.unsplash.com/photo-1531884070720-875c7622d4c6?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2071&q=80',
            },
            {
              imageUrl:
                'https://images.unsplash.com/photo-1581888227599-779811939961?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2148&q=80',
            },
            {
              imageUrl:
                'https://images.unsplash.com/photo-1494947665470-20322015e3a8?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80',
            },
            {
              imageUrl:
                'https://images.unsplash.com/photo-1497752531616-c3afd9760a11?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80',
            },
            {
              imageUrl:
                'https://images.unsplash.com/photo-1625794084867-8ddd239946b1?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80',
            },
          ],
          products: [
            {
              name: '寵物食品',
              description: '新鮮美味的寵物食品，讓您的寵物健康快樂。',
              imageUrl:
                'https://images.unsplash.com/photo-1548767797-d8c844163c4c?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2071&q=80',
            },
            {
              name: '寵物玩具',
              description: '各種有趣的寵物玩具，提供娛樂和活力。',
              imageUrl:
                'https://images.unsplash.com/photo-1585837575652-267c041d77d4?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2095&q=80',
            },
            {
              name: '寵物用品',
              description: '多種寵物用品，滿足您寵物的所有需求。',
              imageUrl:
                'https://images.unsplash.com/photo-1520087619250-584c0cbd35e8?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2094&q=80',
            },
          ],
        }
      },
    }
  </script>
  
  <style scoped>
    /* 在這裡添加自定義的CSS樣式 */
  </style>
  
  