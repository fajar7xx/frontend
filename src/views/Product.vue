<template>
    <div>
        <Header />

        <!-- Breadcrumb Section Begin -->
        <div class="breacrumb-section">
            <div class="container">
                <div class="row">
                    <div class="col-lg-12">
                        <div class="breadcrumb-text product-more">
                            <router-link to="/"><i class="fa fa-home"></i> Home</router-link>
                            <span>Detail</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <!-- Breadcrumb Section Begin -->

        <!-- Product Shop Section Begin -->
        <section class="product-shop spad page-details">
            <div class="container">
                <div class="row">
                    <div class="col-lg-12">
                        <div class="row">
                            <div class="col-lg-6">
                                <div class="product-pic-zoom">
                                    <img class="product-big-img" :src="default_img"/>
                                </div>
                                <div class="product-thumbs">
                                    <carousel class="product-thumbs-track ps-slider" :items="3" :nav="false" :dots="false">
                                        <div class="pt mr-2" @click="changeImage(thumbs[0])" :class="thumbs[0] == default_img ? 'active' : ''">
                                            <img src="images/mickey1.jpg"/>
                                        </div>

                                        <div class="pt mr-2" @click="changeImage(thumbs[1])" :class="thumbs[1] == default_img ? 'active' : ''">
                                            <img src="images/mickey2.jpg"/>
                                        </div>

                                        <div class="pt mr-2" @click="changeImage(thumbs[2])" :class="thumbs[2] == default_img ? 'active' : ''">
                                            <img src="images/mickey3.jpg"/>
                                        </div>

                                        <div class="pt mr-2" @click="changeImage(thumbs[3])" :class="thumbs[3] == default_img ? 'active' : ''">
                                            <img src="images/mickey4.jpg"/>
                                        </div>
                                    </carousel>
                                </div>
                            </div>
                            <div class="col-lg-6">
                                <div class="product-details">
                                    <div class="pd-title">
                                        <span>oranges</span>
                                        <h3>Pure Pineapple</h3>
                                    </div>
                                    <div class="pd-desc text-justify">
                                        <p>
                                            Lorem ipsum dolor sit amet consectetur adipisicing elit. Corporis, error
                                            officia. Rem aperiam laborum voluptatum vel, pariatur modi hic provident eum
                                            iure natus quos non a sequi, id accusantium! Autem.
                                        </p>
                                        <p>
                                            Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quam possimus
                                            quisquam animi, commodi, nihil voluptate nostrum neque architecto illo
                                            officiis doloremque et corrupti cupiditate voluptatibus error illum. Commodi
                                            expedita animi nulla aspernatur.
                                            Id asperiores blanditiis, omnis repudiandae iste inventore cum, quam sint
                                            molestiae accusamus voluptates ex tempora illum sit perspiciatis. Nostrum
                                            dolor tenetur amet, illo natus magni veniam quia sit nihil dolores.
                                            Commodi ratione distinctio harum voluptatum velit facilis voluptas animi non
                                            laudantium, id dolorem atque perferendis enim ducimus? A exercitationem
                                            recusandae aliquam quod. Itaque inventore obcaecati, unde quam
                                            impedit praesentium veritatis quis beatae ea atque perferendis voluptates
                                            velit architecto?
                                        </p>
                                        <h4>$495.00</h4>
                                    </div>
                                    <div class="quantity">
                                        <router-link to="/cart">
                                            <span class="primary-btn pd-cart">
                                                Add To Cart
                                            </span>
                                        </router-link>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>
        <!-- Product Shop Section End -->

        <RelatedProducts/>
        <Footer />
    </div>
</template>

<script>
  // @ is an alias to /src
  import Header from '@/components/Header'
  import Footer from '@/components/Footer'
  import carousel from 'vue-owl-carousel'
  import RelatedProducts from '@/components/RelatedProducts'

  export default {
    name: 'Product',
    components: {
      Header,
      Footer,
      carousel,
      RelatedProducts
    },
    data(){
        return{
            default_img: "images/mickey1.jpg",
            thumbs: [
                "images/mickey1.jpg",
                "images/mickey2.jpg",
                "images/mickey3.jpg",
                "images/mickey4.jpg"
            ]
        }
    },
    methods: {
        changeImage(urlImage){
            this.default_img = urlImage
        }
    }
  }
</script>
