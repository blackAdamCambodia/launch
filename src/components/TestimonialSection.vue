<script setup>
import leftArrow from "../../public/images/left-arrow.svg";
import rightArrow from "../../public/images/right-arrow.svg";
import AvaterOne from "../../public/images/person_1.jpg";
import AvaterTwo from "../../public/images/person_2.jpg";
import AvaterThree from "../../public/images/person_3.jpg";
const captionText = "Testimonials ";
const headingTitle ="Our Customers Feedbck";

const testimonials = [
    {
        id:1,
        quoteText:`&ldquo;Separated they <span class="highlight">live in Bookmarksgrove right at the coast of the Semantics</span>, a large language ocean. A small river named Duden flows by their place and supplies it with the necessary regelialia. &rdquo;`,
        avaterImage:AvaterOne,
        avaterName:"James Anderson",
        avaterDesignation:"Facebook, Product Lead"
    },
    {
        id:1,
        quoteText:`&ldquo;Separated they <span class="highlight">live in Bookmarksgrove right at the coast of the Semantics</span>, a large language ocean. A small river named Duden flows by their place and supplies it with the necessary regelialia. &rdquo;`,
        avaterImage:AvaterTwo,
        avaterName:"James Anderson",
        avaterDesignation:"Facebook, Product Lead"
    },
    {
        id:1,
        quoteText:`&ldquo;Separated they <span class="highlight">live in Bookmarksgrove right at the coast of the Semantics</span>, a large language ocean. A small river named Duden flows by their place and supplies it with the necessary regelialia. &rdquo;`,
        avaterImage:AvaterThree,
        avaterName:"James Anderson",
        avaterDesignation:"Facebook, Product Lead"
    }

];

</script>
<template>
    <div class="untree_co-section" id="testimonials-section">
        <div class="container">
            <div class="row">
                <div class="col-lg-4 mb-5 text-center text-lg-left mb-lg-0" data-aos="fade-up" data-aos-delay="0">
                    <div class="mb-4">
                        <span class="caption">{{ captionText }}</span>
                        <h2 class="heading">{{ headingTitle }}</h2>
                    </div>
                    <div>
                        <a href="#" class="js-custom-prev-v2 cusotm-slider-nav custom-prev">
                            <span>
                                <img :src="leftArrow" alt="Left arrow icon">
                            </span>
                        </a>
                        <a href="#" class="js-custom-next-v2 cusotm-slider-nav custom-next">
                            <span>
                                <img :src="rightArrow" alt="Right arrow icon">
                            </span>
                        </a>
                    </div>
                </div>
                <div class="col-lg-8" data-aos="fade" data-aos-delay="200">
                    <div class="owl-2-slider owl-carousel">
                        <div class="item" v-for="testimonial in testimonials" :key="testimonial.id">
                            <div class="untree_co-testimonial d-flex">
                                <div class="text">
                                    <blockquote v-html="testimonial.quoteText">
                                        
                                    </blockquote>
                                    <div class="author d-flex">
                                        <div class="pic mr-3">
                                            <img :src="testimonial.avaterImage" alt="Image" class="img-fluid">
                                        </div>
                                        <div>
                                            <strong class="d-block">{{testimonial.avaterName}}</strong><span class="d-block">{{ testimonial.avaterDesignation }}</span>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                       
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<style scoped>
</style>