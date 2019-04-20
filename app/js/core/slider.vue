<template>
    <section :class="cname">
        <swiper :options="swiperOption" :not-next-tick="swiperOption.notNextTick">
            <swiper-slide v-for="item in items" :key="item.href">
                <router-link :to="{name:item.href}">
                    <img :src="item.src">
                </router-link>
            </swiper-slide>
            <div class="swiper-pagination" slot="pagination" v-if="swiperOption.pagination"></div>
        </swiper>
    </section>
</template>

<script>
import { swiper, swiperSlide } from "vue-awesome-swiper";
export default {
    components: {
        swiper,
        swiperSlide
    },
    props: {
        cname: {
            type: String,
            default: ""
        },
        swiperOption: {
            type: Object,
            default() {
                return {
                    autoplay: true,
                    loop: true,
                    pagination: {
                        el: ".swiper-pagination"
                    },
                    notNextTick: false
                };
            }
        },
        items: {
            type: Array,
            default() {
                // [{href:"",src:""}]
                return [];
            }
        }
    }
};
</script>

<style  lang="scss">
@import "~swiper/dist/css/swiper.css";
</style>