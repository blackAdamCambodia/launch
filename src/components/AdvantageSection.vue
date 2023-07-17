<script setup>
const headingTitle = "Advantage of using our products";
const headingDescription = "Far from the countries Vokalia and Consonantia";
import imageIconOne from "../../public/images/app-indicator.svg";
import imageIconTwo from "../../public/images/arrow-repeat.svg";
import imageIconThree from "../../public/images/briefcase.svg";
import imageIconFour from "../../public/images/collection.svg";

const serviceItems =[
  {
    id: 1,
    color: 1,
    icon: imageIconOne,
    altText: 'App Indicator',
    title: 'Grow Your Business',
    description: 'Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind texts.',
    delay: 0
  },
  {
    id: 2,
    color: 2,
    icon: imageIconTwo,
    altText: 'Arrow Repeat',
    title: 'Build Products',
    description: 'Far far away, behind the word mountains, far from the countries Vokalia and Consonantia.',
    delay: 100
  },
  {
    id: 3,
    color: 3,
    icon: imageIconThree,
    altText:'Brief Case',
    title: 'Success Every Day',
    description: 'Far far away, behind the word mountains, far from the countries Vokalia and Consonantia.',
    delay: 200
  },
  {
    id: 4,
    color: 4,
    icon: imageIconFour,
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
</script>
<template>
    <div class="untree_co-section">
        <div class="container">
            <div class="row mb-4">
                <div class="col-12 text-center" data-aos="fade-up" data-aos-delay="0">
                    <h2 class="heading">{{ headingTitle }}</h2>
                    <p>{{ headingDescription }}</p>
                </div>
            </div>
            <div class="row">
                <div class="col-lg-6 mb-4" data-aos="fade-up" :data-aos-delay="item.delay" v-for="item in serviceItems" :key="item.id">
                    <div class="service horizontal d-flex">
                        <div class="service-icon mb-4" :class="`color-${item.color}`">
                            <img :src="item.icon" :alt="altText" :style="svgImgStyle">
                        </div>
                        <div class="service-contents">
                            <h3>{{ item.title }}</h3>
                            <p>{{ item.description }}</p>
                            <p><a href="#" class="read-more">Learn More</a></p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
</style>