<script setup>
const serviceItems =[
  {
    id: 1,
    color: 1,
    icon: '../../public/images/app-indicator.svg',
    altText: 'App Indicator',
    title: 'Grow Your Business',
    description: 'Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind texts.',
    delay: 0
  },
  {
    id: 2,
    color: 2,
    icon: '../../public/images/arrow-repeat.svg',
    altText: 'Arrow Repeat',
    title: 'Build Products',
    description: 'Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind texts.',
    delay: 100
  },
  {
    id: 3,
    color: 3,
    icon: '../../public/images/briefcase.svg',
    altText:'Brief Case',
    title: 'Success Every Day',
    description: 'Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind texts.',
    delay: 200
  },
  {
    id: 4,
    color: 4,
    icon: '../../public/images/collection.svg',
    altText:'Collection',
    title: 'Bring Ideas to Life',
    description: 'Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind texts.',
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
            <div class="row">
                <div class="col-md-6 mb-4 mb-lg-0 col-lg-3" v-for="item in serviceItems" :key="item" data-aos="fade-up" :data-aos-delay="item.delay">
                    <div class="service">
                        <div class="service-icon  mb-4" :class="` color-${item.color}`">
                            <img :src="item.icon" :alt="item.altText" :style="svgImgStyle">
                        </div>
                        <div class="service-contents">
                            <h3>{{ item.title }}</h3>
                            <p>{{item.description}}</p>
                        </div>
                    </div>
                </div>
              
            </div>
        </div>
    </div>
</template>
<style scoped>
</style>