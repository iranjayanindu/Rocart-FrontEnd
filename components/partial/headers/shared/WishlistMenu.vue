<template>
    <li>
        <nuxt-link to="/shop/wishlist" title="Wishlist">
            <i class="icon-heart-o"></i>My Wishlist
            <span>({{ wishlistQty }})</span>
        </nuxt-link>
    </li>
</template>

<script>
import { mapGetters } from 'vuex';
export default {
    computed: {
        ...mapGetters('wishlist', ['wishlistQty'])
    }
};
</script>