<template>
    <div class="container">
        <div class="heading heading-center mb-3">
            <h2 class="title">Top Selling Products</h2>
            <tabs class="nav-pills nav-pills justify-content-center" :data="tabsData" id="top"></tabs>
        </div>

        <div class="tab-content">
            <div class="tab-pane p-0 fade show active" id="top-all">
                <div class="products just-action-icons-sm">
                    <div class="row">
                        <div
                            class="col-6 col-md-4 col-lg-3 col-xl-5col"
                            v-for="(product, index) in products.slice(0, 10)"
                            :key="index"
                        >
                            <product-twelve :product="product"></product-twelve>
                        </div>
                    </div>
                </div>
            </div>
            <div class="tab-pane p-0 fade" id="top-women">
                <div class="products just-action-icons-sm">
                    <div class="row">
                        <div
                            class="col-6 col-md-4 col-lg-3 col-xl-5col"
                            v-for="(product, index) in womenProducts.slice(0, 6)"
                            :key="index"
                        >
                            <product-twelve :product="product"></product-twelve>
                        </div>
                    </div>
                </div>
            </div>

            <div class="tab-pane p-0 fade" id="top-men">
                <div class="products just-action-icons-sm">
                    <div class="row">
                        <div
                            class="col-6 col-md-4 col-lg-3 col-xl-5col"
                            v-for="(product, index) in menProducts.slice(0, 6)"
                            :key="index"
                        >
                            <product-twelve :product="product"></product-twelve>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="more-container text-center mt-5">
            <nuxt-link to="/shop/sidebar/list" class="btn btn-outline-lightgray btn-more btn-round">
                <span>View more products</span>
                <i class="icon-long-arrow-right"></i>
            </nuxt-link>
        </div>
    </div>
</template>
<script>
import Tabs from '~/components/elements/Tabs';
import ProductTwelve from '~/components/elements/products/ProductTwelve';

import { catFilter } from '~/utilities/common';

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
            ]
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
