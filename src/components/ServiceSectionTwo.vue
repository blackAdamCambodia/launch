<script setup>
const serviceItems =[
  {
    id: 1,
    color: 1,
    icon: '../../public/images/app-indicator.svg',
    altText: 'App Indicator',
    title: 'Grow Your Business',
    description: 'Far far away, behind the word mountains, far from the countries Vokalia and Consonantia.',
    delay: 0
  },
  {
    id: 2,
    color: 2,
    icon: '../../public/images/arrow-repeat.svg',
    altText: 'Arrow Repeat',
    title: 'Build Products',
    description: 'Far far away, behind the word mountains, far from the countries Vokalia and Consonantia.',
    delay: 100
  },
  {
    id: 3,
    color: 3,
    icon: '../../public/images/briefcase.svg',
    altText:'Brief Case',
    title: 'Success Every Day',
    description: 'Far far away, behind the word mountains, far from the countries Vokalia and Consonantia.',
    delay: 200
  },
  {
    id: 4,
    color: 4,
    icon: '../../public/images/collection.svg',
    altText:'Collection',
    title: 'Bring Ideas to Life',
    description: 'Far far away, behind the word mountains, far from the countries Vokalia and Consonantia.',
    delay: 300
  }
];
const svgImgStyle= {
  position: "absolute",
  top: "50%",
  left: "50%",
  transform: "translate(-50%, -50%)",
  width: "24px"
};
const serviceImage = {
  src:"../../public/images/dashboard.jpg",
  alt:"Dashboard Image"
};
</script>
<template>
    <div class="untree_co-section bg-light">
        <div class="container">
            <div class="row justify-content-between">
                <div class="col-lg-5 order-lg-2 js-custom-dots">
                    <a href="#" class="service link horizontal d-flex active" v-for="item in serviceItems" :key="item" data-aos="fade-left" :data-aos-delay="item.delay">
                        <div class="service-icon color-1 mb-4" :class="` color-${item.color}`">
                             <img :src="item.icon" :alt="item.altText" :style="svgImgStyle">
                        </div>
                        <div class="service-contents">
                            <h3>{{ item.title }}</h3>
                            <p>{{item.description}}</p>
                        </div>
                    </a>
                </div>
                <div class="col-lg-7">
                    <div class="img-shadow">
                        <div class="owl-single no-dots owl-carousel">
                            <div class="item">
                                <span class="number">1/4</span>
                                <img v-bind="serviceImage" class="img-fluid">
                            </div>
                            <div class="item">
                                <span class="number">2/4</span>
                                <img v-bind="serviceImage" class="img-fluid">
                            </div>
                            <div class="item">
                                <span class="number">3/4</span>
                                <img v-bind="serviceImage" class="img-fluid">
                            </div>
                            <div class="item">
                                <span class="number">4/4</span>
                                <img v-bind="serviceImage" class="img-fluid">
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<style scoped></style>