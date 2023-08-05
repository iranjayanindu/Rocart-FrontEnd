<template>
    <div class="bg-light pt-5 pb-6 mb-3 new">
        <div class="container">
            <div class="heading heading-center mb-3">
                <h2 class="title">New Arrivals</h2>
                <tabs class="nav-pills nav-pills justify-content-center" :data="tabsData" id="new"></tabs>
            </div>

            <div class="tab-content tab-content-carousel">
                <div class="tab-pane fade show active" id="new-all">
                    <div class="swiper-carousel swiper-1">
                        <div class="mb-0" v-swiper:swiper1="carouselSetting1">
                            <div class="swiper-wrapper">
                                <div
                                    class="swiper-slide"
                                    v-for="(product, index) in products.slice(0, 6)"
                                    :key="index"
                                >
                                    <product-twelve :product="product"></product-twelve>
                                </div>
                            </div>
                        </div>
                        <div class="swiper-dots pt-2"></div>
                    </div>
                </div>
                <div class="tab-pane fade" id="new-women">
                    <div class="swiper-carousel swiper-2">
                        <div class="mb-0" v-swiper:swiper2="carouselSetting2">
                            <div class="swiper-wrapper">
                                <div
                                    class="swiper-slide"
                                    v-for="(product, index) in womenProducts"
                                    :key="index"
                                >
                                    <product-twelve :product="product"></product-twelve>
                                </div>
                            </div>
                        </div>
                        <div class="swiper-dots pt-2"></div>
                    </div>
                </div>

                <div class="tab-pane fade" id="new-men">
                    <div class="swiper-carousel swiper-3">
                        <div class="mb-0" v-swiper:swiper3="carouselSetting3">
                            <div class="swiper-wrapper">
                                <div
                                    class="swiper-slide"
                                    v-for="(product, index) in menProducts"
                                    :key="index"
                                >
                                    <product-twelve :product="product"></product-twelve>
                                </div>
                            </div>
                        </div>
                        <div class="swiper-dots pt-2"></div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
import Tabs from '~/components/elements/Tabs';
import ProductTwelve from '~/components/elements/products/ProductTwelve';

import { catFilter } from '~/utilities/common';
import { carouselSetting1 } from '~/utilities/carousel';

export default {
    components: {
        Tabs,
        ProductTwelve
    },
    props: {
        products: Array
    },
    data: function() {
        return {
            tabsData: [
                {
                    id: 'all',
                    title: 'All',
                    active: true
                },
                {
                    id: 'women',
                    title: "Women's"
                },
                {
                    id: 'men',
                    title: "Men's"
                }
            ],
            carouselSetting1: {
                ...carouselSetting1,
                slidesPerView: 4,
                spaceBetween: 0,
                pagination: {
                    el: '.new .swiper-1 .swiper-dots',
                    clickable: true
                }
            },
            carouselSetting2: {
                ...carouselSetting1,
                slidesPerView: 4,
                spaceBetween: 0,
                pagination: {
                    el: '.new .swiper-2 .swiper-dots',
                    clickable: true
                }
            },
            carouselSetting3: {
                ...carouselSetting1,
                slidesPerView: 4,
                spaceBetween: 0,
                pagination: {
                    el: '.new .swiper-3 .swiper-dots',
                    clickable: true
                }
            }
        };
    },
    computed: {
        menProducts: function() {
            return catFilter(this.products, ['men']).slice(0, 5);
        },
        womenProducts: function() {
            return catFilter(this.products, ['women']).slice(0, 5);
        }
    }
};
</script>
