<template>
    <header class="header header-8">
        <div class="header-top">
            <div class="container">
                <div class="header-left">
                    <div class="header-dropdown">
                        <a href="#">Usd</a>
                        <div class="header-menu">
                            <ul>
                                <li>
                                    <a href="#">Eur</a>
                                </li>
                                <li>
                                    <a href="#">Usd</a>
                                </li>
                            </ul>
                        </div>
                    </div>

                    <div class="header-dropdown">
                        <a href="#">Eng</a>
                        <div class="header-menu">
                            <ul>
                                <li>
                                    <a href="#">English</a>
                                </li>
                                <li>
                                    <a href="#">French</a>
                                </li>
                                <li>
                                    <a href="#">Spanish</a>
                                </li>
                            </ul>
                        </div>
                    </div>
                </div>

                <div class="header-right">
                    <ul class="top-menu">
                        <li>
                            <a href="#">Links</a>
                            <ul>
                                <li>
                                    <a href="tel:#">
                                        <i class="icon-phone"></i>Call: +0123 456 789
                                    </a>
                                </li>
                                <wishlist-menu></wishlist-menu>
                                <li>
                                    <nuxt-link to="/pages/about">About Us</nuxt-link>
                                </li>
                                <li>
                                    <nuxt-link to="/pages/about-us">Contact Us</nuxt-link>
                                </li>
                                <li>
                                    <a href="#signin-modal" @click.prevent="openSignInModal">
                                        <i class="icon-user"></i>Login
                                    </a>
                                </li>
                            </ul>
                        </li>
                    </ul>
                </div>
            </div>
        </div>

        <sticky-header>
            <div class="header-middle sticky-header">
                <div class="container">
                    <div class="header-left">
                        <button class="mobile-menu-toggler" @click="openMobileMenu">
                            <span class="sr-only">Toggle mobile menu</span>
                            <i class="icon-bars"></i>
                        </button>

                        <nuxt-link to="/" class="logo">
                            <img
                                v-lazy="'./images/home/logo.png'"
                                class="bg-white"
                                alt="Molla Logo"
                                width="105"
                                height="27"
                            />
                        </nuxt-link>
                    </div>

                    <div class="header-right">
                        <main-menu></main-menu>
                        <header-search></header-search>

                        <cart-menu></cart-menu>
                    </div>
                </div>
            </div>
        </sticky-header>
    </header>
</template>

<script>
import CartMenu from '~/components/partial/headers/shared/CartMenu';
import WishlistMenu from '~/components/partial/headers/shared/WishlistMenu';
import MainMenu from '~/components/partial/headers/shared/MainMenu';
import HeaderSearch from '~/components/partial/headers/shared/HeaderSearch';
import StickyHeader from '~/components/elements/StickyHeader';

export default {
    components: {
        CartMenu,
        WishlistMenu,
        MainMenu,
        HeaderSearch,
        StickyHeader
    },
    computed: {
        isFullwidth: function() {
            return this.$route.path.includes('fullwidth');
        }
    },
    methods: {
        openSignInModal: function() {
            this.$modal.show(
                () => import('~/components/elements/modals/SignInModal'),
                {},
                { width: '575', height: 'auto', adaptive: true }
            );
        },
        openMobileMenu: function() {
            document.querySelector('body').classList.add('mmenu-active');
        }
    }
};
</script>