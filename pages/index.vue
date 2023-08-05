<template>
    <div class="main home-page">
        <div class="container">
            <div class="intro-slider-container slider-container-ratio mb-2">
                <div class="swiper-carousel intro-slider swiper-1">
                    <div v-swiper:swiper1="carouselSetting1">
                        <div class="swiper-wrapper">
                            <div class="swiper-slide">
                                <div class="intro-slide">
                                    <figure class="slide-image mb-0">
                                        <picture>
                                            <source
                                                media="(max-width: 480px)"
                                                :srcset="'./images/home/sliders/slide-1-480w.jpg'"
                                            />
                                            <img
                                                v-lazy="'./images/home/sliders/slide-1.jpg'"
                                                alt="Image Desc"
                                            />
                                        </picture>
                                    </figure>

                                    <div class="intro-content">
                                        <h3 class="intro-subtitle">Deals and Promotions</h3>

                                        <h1 class="intro-title text-white">Sneakers & Athletic Shoes</h1>

                                        <div class="intro-price text-white">from $9.99</div>

                                        <nuxt-link
                                            to="/shop/sidebar/3cols"
                                            class="btn btn-white-primary btn-round"
                                        >
                                            <span>SHOP NOW</span>
                                            <i class="icon-long-arrow-right"></i>
                                        </nuxt-link>
                                    </div>
                                </div>
                            </div>
                            <div class="swiper-slide">
                                <div class="intro-slide">
                                    <figure class="slide-image mb-0">
                                        <picture>
                                            <source
                                                media="(max-width: 480px)"
                                                :srcset="'./images/home/sliders/slide-2-480w.jpg'"
                                            />
                                            <img
                                                v-lazy="'./images/home/sliders/slide-2.jpg'"
                                                alt="Image Desc"
                                            />
                                        </picture>
                                    </figure>

                                    <div class="intro-content">
                                        <h3 class="intro-subtitle">Trending Now</h3>

                                        <h1 class="intro-title text-white">This Week's Most Wanted</h1>

                                        <div class="intro-price text-white">from $49.99</div>

                                        <nuxt-link
                                            to="/shop/sidebar/3cols"
                                            class="btn btn-white-primary btn-round"
                                        >
                                            <span>SHOP NOW</span>
                                            <i class="icon-long-arrow-right"></i>
                                        </nuxt-link>
                                    </div>
                                </div>
                            </div>
                            <div class="swiper-slide">
                                <div class="intro-slide">
                                    <figure class="slide-image mb-0">
                                        <picture>
                                            <source
                                                media="(max-width: 480px)"
                                                :srcset="'./images/home/sliders/slide-3-480w.jpg'"
                                            />
                                            <img
                                                v-lazy="'./images/home/sliders/slide-3.jpg'"
                                                alt="Image Desc"
                                            />
                                        </picture>
                                    </figure>

                                    <div class="intro-content">
                                        <h3 class="intro-subtitle text-white">Deals and Promotions</h3>

                                        <h1 class="intro-title text-white">Can’t-miss Clearance:</h1>

                                        <div class="intro-price text-white">starting at 60% off</div>

                                        <nuxt-link
                                            to="/shop/sidebar/3cols"
                                            class="btn btn-white-primary btn-round"
                                        >
                                            <span>SHOP NOW</span>
                                            <i class="icon-long-arrow-right"></i>
                                        </nuxt-link>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="swiper-dots swiper-dots-inner"></div>
                </div>
            </div>
        </div>
        <div class="banner-group">
            <div class="container">
                <div class="row">
                    <div class="col-lg-8">
                        <div class="row">
                            <div class="col-sm-6">
                                <div class="banner banner-overlay">
                                    <nuxt-link to="/shop/sidebar/3cols">
                                        <img
                                            v-lazy="'./images/home/banners/banner-1.jpg'"
                                            width="376"
                                            height="250"
                                            alt="Banner"
                                        />
                                    </nuxt-link>

                                    <div class="banner-content banner-content-right">
                                        <h4 class="banner-subtitle">
                                            <a href="javascript:;">New Arrivals</a>
                                        </h4>

                                        <h3 class="banner-title text-white">
                                            <a href="javascript:;">
                                                Sneakers &
                                                <br />Athletic Shoes
                                            </a>
                                        </h3>

                                        <nuxt-link
                                            to="/shop/sidebar/3cols"
                                            class="btn btn-outline-white banner-link btn-round"
                                        >Discover Now</nuxt-link>
                                    </div>
                                </div>
                            </div>

                            <div class="col-sm-6">
                                <div class="banner banner-overlay banner-overlay-light">
                                    <nuxt-link to="/shop/sidebar/3cols">
                                        <img
                                            v-lazy="'./images/home/banners/banner-2.jpg'"
                                            width="376"
                                            height="250"
                                            alt="Banner"
                                        />
                                    </nuxt-link>

                                    <div class="banner-content">
                                        <h4 class="banner-subtitle bright-black">
                                            <a href="javascript:;">Clearance</a>
                                        </h4>

                                        <h3 class="banner-title">
                                            <a href="javascript:;">Sandals</a>
                                        </h3>

                                        <div class="banner-text">
                                            <a href="javascript:;">up to 70% off</a>
                                        </div>

                                        <nuxt-link
                                            to="/shop/sidebar/3cols"
                                            class="btn btn-outline-gray banner-link btn-round"
                                        >Shop Now</nuxt-link>
                                    </div>
                                </div>
                            </div>
                        </div>

                        <div class="banner banner-large banner-overlay d-none d-sm-block">
                            <nuxt-link to="/shop/sidebar/3cols">
                                <img
                                    v-lazy="'./images/home/banners/banner-3.jpg'"
                                    width="772"
                                    height="250"
                                    alt="Banner"
                                />
                            </nuxt-link>

                            <div class="banner-content">
                                <h4 class="banner-subtitle text-white">
                                    <a href="javascript:;">On Sale</a>
                                </h4>

                                <h3 class="banner-title text-white">
                                    <a href="javascript:;">Slip-On Loafers</a>
                                </h3>

                                <div class="banner-text text-white">
                                    <a href="javascript:;">up to 30% off</a>
                                </div>

                                <nuxt-link
                                    to="/shop/sidebar/list"
                                    class="btn btn-outline-white banner-link btn-round"
                                >Shop Now</nuxt-link>
                            </div>
                        </div>
                    </div>

                    <div class="col-lg-4 d-sm-none d-lg-block">
                        <div class="banner banner-middle banner-overlay">
                            <nuxt-link to="/shop/sidebar/3cols">
                                <img
                                    v-lazy="'./images/home/banners/banner-4.jpg'"
                                    width="376"
                                    height="520"
                                    alt="Banner"
                                />
                            </nuxt-link>

                            <div class="banner-content banner-content-bottom">
                                <h4 class="banner-subtitle text-white">
                                    <a href="javascript:;">On Sale</a>
                                </h4>

                                <h3 class="banner-title text-white">
                                    <a href="javascript:;">
                                        Amazing
                                        <br />Lace Up Boots
                                    </a>
                                </h3>

                                <div class="banner-text text-white">
                                    <a href="javascript:;">from $39.00</a>
                                </div>

                                <nuxt-link
                                    to="/shop/sidebar/list"
                                    class="btn btn-outline-white banner-link btn-round"
                                >Discover Now</nuxt-link>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <div class="icon-boxes-container icon-boxes-separator bg-transparent">
            <div class="container">
                <div class="row">
                    <div class="col-sm-6 col-lg-3">
                        <div class="icon-box icon-box-side">
                            <span class="icon-box-icon text-primary">
                                <i class="icon-rocket"></i>
                            </span>

                            <div class="icon-box-content">
                                <h3 class="icon-box-title">Free Shipping</h3>

                                <p>Orders $50 or more</p>
                            </div>
                        </div>
                    </div>

                    <div class="col-sm-6 col-lg-3">
                        <div class="icon-box icon-box-side">
                            <span class="icon-box-icon text-primary">
                                <i class="icon-rotate-left"></i>
                            </span>

                            <div class="icon-box-content">
                                <h3 class="icon-box-title">Free Returns</h3>

                                <p>Within 30 days</p>
                            </div>
                        </div>
                    </div>

                    <div class="col-sm-6 col-lg-3">
                        <div class="icon-box icon-box-side">
                            <span class="icon-box-icon text-primary">
                                <i class="icon-info-circle"></i>
                            </span>

                            <div class="icon-box-content">
                                <h3 class="icon-box-title">Get 20% Off 1 Item</h3>

                                <p>when you sign up</p>
                            </div>
                        </div>
                    </div>

                    <div class="col-sm-6 col-lg-3">
                        <div class="icon-box icon-box-side">
                            <span class="icon-box-icon text-primary">
                                <i class="icon-life-ring"></i>
                            </span>

                            <div class="icon-box-content">
                                <h3 class="icon-box-title">We Support</h3>

                                <p>24/7 amazing services</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <new-collection :products="products" v-if="loaded"></new-collection>

        <div class="container">
            <div class="row justify-content-center">
                <div class="col-sm-6 col-md-4">
                    <div class="banner banner-cat">
                        <nuxt-link to="/shop/sidebar/list">
                            <img
                                v-lazy="'./images/home/banners/banner-5.jpg'"
                                width="376"
                                height="280"
                                alt="Banner"
                            />
                        </nuxt-link>

                        <div class="banner-content banner-content-overlay text-center">
                            <h3 class="banner-title font-weight-normal">Women's</h3>

                            <h4 class="banner-subtitle">125 Products</h4>

                            <nuxt-link to="/shop/sidebar/3cols" class="banner-link">SHOP NOW</nuxt-link>
                        </div>
                    </div>
                </div>

                <div class="col-sm-6 col-md-4">
                    <div class="banner banner-cat">
                        <nuxt-link to="/shop/sidebar/list">
                            <img
                                v-lazy="'./images/home/banners/banner-6.jpg'"
                                width="376"
                                height="280"
                                alt="Banner"
                            />
                        </nuxt-link>

                        <div class="banner-content banner-content-overlay text-center">
                            <h3 class="banner-title font-weight-normal">Men's</h3>

                            <h4 class="banner-subtitle">97 Products</h4>

                            <nuxt-link to="/shop/sidebar/3cols" class="banner-link">SHOP NOW</nuxt-link>
                        </div>
                    </div>
                </div>

                <div class="col-sm-6 col-md-4">
                    <div class="banner banner-cat">
                        <nuxt-link to="/shop/sidebar/list">
                            <img
                                v-lazy="'./images/home/banners/banner-7.jpg'"
                                width="376"
                                height="280"
                                alt="Banner"
                            />
                        </nuxt-link>

                        <div class="banner-content banner-content-overlay text-center">
                            <h3 class="banner-title font-weight-normal">Kid's</h3>

                            <h4 class="banner-subtitle">48 Products</h4>

                            <nuxt-link to="/shop/sidebar/3cols" class="banner-link">SHOP NOW</nuxt-link>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <div class="mb-4"></div>

        <top-collection :products="products" v-if="loaded"></top-collection>

        <div class="mb-5"></div>

        <div class="container">
            <div
                class="cta cta-horizontal cta-horizontal-box bg-image mb-4 mb-lg-6"
                v-lazy:background-image="'./images/home/bg-1.jpg'"
            >
                <div class="row flex-column flex-lg-row align-items-lg-center">
                    <div class="col">
                        <h3 class="cta-title text-primary">New Deals! Start Daily at 12pm e.t.</h3>

                        <p class="cta-desc">
                            Get
                            <em class="font-weight-medium">FREE SHIPPING* & 5% rewards</em> on every order with Molla Theme rewards program
                        </p>
                    </div>

                    <div class="col-auto">
                        <a href="javascript:;" class="btn btn-white-primary btn-round">
                            <span>Add to Cart for $50.00/yr</span>
                            <i class="icon-long-arrow-right"></i>
                        </a>
                    </div>
                </div>
            </div>
        </div>

        <blog-section :blogs="blogs" v-if="loaded"></blog-section>

        <div
            class="cta bg-image bg-dark pt-4 pb-5 mb-0"
            v-lazy:background-image="'./images/home/bg-2.jpg'"
        >
            <div class="container">
                <div class="row justify-content-center">
                    <div class="col-sm-10 col-md-8 col-lg-6">
                        <div class="cta-heading text-center">
                            <h3 class="cta-title text-white">Subscribe for Our Newsletter</h3>

                            <p class="cta-desc text-white">
                                and receive
                                <span class="font-weight-normal">$20 coupon</span> for first shopping
                            </p>
                        </div>

                        <form action="#">
                            <div class="input-group input-group-round">
                                <input
                                    type="email"
                                    class="form-control form-control-white border-0"
                                    placeholder="Enter your Email Address"
                                    aria-label="Email Adress"
                                    required
                                />
                                <div class="input-group-append">
                                    <button class="btn btn-white" type="submit">
                                        <span>Subscribe</span>
                                        <i class="icon-long-arrow-right"></i>
                                    </button>
                                </div>
                            </div>
                        </form>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
import { mapGetters } from 'vuex';

import NewCollection from '~/components/partial/home/NewCollection';
import TopCollection from '~/components/partial/home/TopCollection';
import BlogSection from '~/components/partial/home/BlogSection';
import NewsletterModal from '~/components/elements/modals/NewsletterModal';

import Repository, { baseUrl } from '~/repositories/repository.js';
import { attrFilter } from '~/utilities/common';
import {
    carouselSettingSingle,
    carouselSettingDefault
} from '~/utilities/carousel';
import { homeData } from '~/utilities/data';

export default {
    components: {
        BlogSection,
        TopCollection,
        NewCollection
    },
    data: function() {
        return {
            loaded: false,
            products: [],
            blogs: [],
            carouselSetting1: {
                ...carouselSettingSingle,
                pagination: {
                    el: '.swiper-1 .swiper-dots',
                    clickable: true
                }
            },
            carouselSetting2: {
                ...carouselSettingDefault,
                slidesPerView: 7,
                spaceBetween: 0,
                breakpoints: {
                    992: {
                        slidesPerView: 6
                    },
                    768: {
                        slidesPerView: 5
                    },
                    576: {
                        slidesPerView: 3
                    },
                    480: {
                        slidesPerView: 2
                    }
                }
            },
            homeData: homeData
        };
    },
    computed: {
        ...mapGetters('demo', ['newsletterShow'])
    },
    created: function() {
        this.getProducts();
    },
    mounted: function() {
        if (this.newsletterShow) {
            setTimeout(() => {
                if (this.$route.path == '/' && this.newsletterShow) {
                    this.$modal.show(
                        NewsletterModal,
                        {},
                        { width: '970', height: 'auto', adaptive: true }
                    );
                }
            }, 8000);
        }
    },
    methods: {
        getProducts: async function() {
            this.loaded = false;
            await Repository.get(`${baseUrl}/demo10`)
                .then(response => {
                    this.products = response.data.products;
                    this.blogs = response.data.blogs;
                    this.loaded = true;
                })
                .catch(error => ({ error: JSON.stringify(error) }));
        }
    }
};
</script>