<script setup>
import dashboardImage from "../../public/images/dashboard.jpg";
import PersonImage from "../../public/images/person_1.jpg";
const serviceItems =[
  "There live the blind texts",
  "Far far away behind the word"
];
const serviceTitle= "Digital Services";
const serviceHeading="Selling Digital Services";
const serviceParagraph="Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind texts. Separated they live in Bookmarksgrove right at the coast";
const serviceImage = {
  src:dashboardImage,
  alt:"Dashboard Image"
};
const  authorImage = {
  src:PersonImage,                                                                                                                                                               
  alt:" Author Image"
};
const authorName = "James Anderson";
const authorPosition= "Facebook, Product Lead";
</script>
<template>
    <div class="untree_co-section" id="features-section">
        <div class="container">
            <div class="row justify-content-between">
                <div class="col-lg-4">
                    <span class="caption" data-aos="fade-up" data-aos-delay="0">{{serviceTitle}}</span>
                    <h3 class="heading mb-4" data-aos="fade-up" data-aos-delay="100">{{ serviceHeading }}</h3>
                    <div class="mb-4" data-aos="fade-up" data-aos-delay="200">
                        <p>{{ serviceParagraph }}</p>
                        <ul class="list-unstyled ul-check primary">
                            <li v-for="serviceItem in serviceItems" :key="serviceItem">{{ serviceItem }}</li>
                            <!-- <li>Far far away behind the word</li> -->
                        </ul>
                    </div>
                    <div class="mb-4" data-aos="fade-up" data-aos-delay="300">
                        <div class="untree_co-testimonial d-flex">
                            <div class="text">
                                <blockquote>
                                    &ldquo;Separated they <span class="highlight">live in Bookmarksgrove right at the coast of the Semantics</span>, a large language ocean. A small river named Duden flows by their place and supplies it with the necessary regelialia. &rdquo;
                                </blockquote>
                                <div class="author d-flex">
                                    <div class="pic mr-3">
                                        <img v-bind="authorImage" class="img-fluid">
                                    </div>
                                    <div>
                                        <strong class="d-block">{{authorName}}</strong><span class="d-block">{{ authorPosition }}</span>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="col-lg-7" data-aos="fade-up" data-aos-delay="400">
                    <a href="https://www.youtube.com/watch?v=mwtbEGNABWU&amp;t=9s" class="btn-video" data-fancybox>
                        <span class="wrap-icon-play">
                            <svg class="bi bi-play-fill" width="1em" height="1em" viewBox="0 0 16 16" fill="currentColor" xmlns="http://www.w3.org/2000/svg">
                                <path d="M11.596 8.697l-6.363 3.692c-.54.313-1.233-.066-1.233-.697V4.308c0-.63.692-1.01 1.233-.696l6.363 3.692a.802.802 0 0 1 0 1.393z" />
                            </svg>
                        </span>
                        <img v-bind="serviceImage" class="img-fluid img-shadow">
                    </a>
                </div>
            </div>
        </div>
    </div>
</template>
<style scoped></style>