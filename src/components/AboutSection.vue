<script setup>
import aboutImage from "../../public/images/about.svg"
const captionText = "About";
const headingTitle = "About Us" ;
const aboutDescription = "Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind texts. Separated they live in Bookmarksgrove right at the coast";
const descriptionHighlight = `Separated they <span class="highlight">live in Bookmarksgrove right at the coast of the Semantics</span>, a large language ocean. A small river named Duden flows by their place and supplies it with the necessary regelialia.`;
const listItems=[
                "There live the blind texts",
                "Far far away behind the word",
                "Their place and supplies"
            ];
</script>
<template>
     <div class="untree_co-section" id="about-section">
        <div class="container">
            <div class="row justify-content-between">
                <div class="col-lg-8" data-aos="fade-up" data-aos-delay="100">
                    <img :src="aboutImage" alt="Image" class="img-fluid">
                </div>
                <div class="col-lg-4">
                    <div class="mb-4" data-aos="fade-up" data-aos-delay="0">
                        <span class="caption">{{captionText}}</span>
                        <h2 class="heading">{{ headingTitle }}</h2>
                    </div>
                    <div class="mb-4" data-aos="fade-up" data-aos-delay="100">
                        <p>{{ aboutDescription }}</p>
                        <p v-html="descriptionHighlight"></p>
                    </div>
                    <ul class="list-unstyled ul-check primary mb-4" data-aos="fade-up" data-aos-delay="200">
                        <li v-for="(item ,index) in listItems" :key="index">{{ item }}</li>
                       
                    </ul>
                    <div class="row count-numbers">
                        <div class="col-lg-6" data-aos="fade-up" data-aos-delay="0">
                            <span class="counter d-block"><span data-number="59">0</span><span>M</span></span>
                            <span class="caption-2">Members</span>
                        </div>
                        <div class="col-lg-6" data-aos="fade-up" data-aos-delay="100">
                            <span class="counter d-block"><span data-number="14">0</span><span></span></span>
                            <span class="caption-2">Team</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<style scoped>
</style>