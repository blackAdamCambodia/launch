<script setup>
    import AvaterOne from "../../public/images/person_1.jpg";
    import AvaterTwo from "../../public/images/person_2.jpg";
    import AvaterThree from "../../public/images/person_3.jpg";
    const headingTitle ="Our News";
    const description="Far from the countries Vokalia and Consonantia";
    const blogCards = [
        {
            id: 1,
            image: AvaterOne,
            avaterName: "Posted by James",
            date: "Jun 14, 2020",
            category:"Digital Service",
            readingTime: "4 min read",
            blogTitle: "Far far away behind the word mountains far from the countries",
            delay:0
        },
        {
            id: 2,
            image: AvaterTwo,
            avaterName: "Posted by Khan",
            date: "Jun 14, 2020",
            category:"Digital Service",
            readingTime: "8 min read",
            blogTitle: "Far far away behind the word mountains far from the countries",
            delay:100
        },
        {
            id: 3,
            image: AvaterThree,
            avaterName: "Posted by Rob",
            date: "Jun 14, 2020",
            category:"Digital Service",
            readingTime: "6 min read",
            blogTitle: "Far far away behind the word mountains far from the countries",
            delay:300
        }
    ];
 
</script>
<template>
    <div class="untree_co-section bg-light">
        <div class="container">
            <div class="row mb-4">
                <div class="col-12 text-center" data-aos="fade-up" data-aos-delay="0">
                    <h2 class="heading">{{ headingTitle }}</h2>
                    <p>{{ description }}</p>
                </div>
            </div>
            <div class="row">
                <div class="col-sm-12 mb-4 mb-md-0 col-md-4" data-aos="fade-up" :data-aos-delay="delay" v-for="blogCard in blogCards" :key="blogCard.id">
                    <div class="news-item">
                        <div class="vcard d-flex align-items-center mb-4">
                            <div class="img-wrap">
                                <img :src="blogCard.image" alt="Image" class="img-fluid">
                            </div>
                            <div class="post-meta">
                                <strong>{{blogCard.avaterName}}</strong>
                                <span>{{blogCard.date}}</span>
                            </div>
                        </div>
                        <div class="news-contents mb-4">
                            <span class="post-meta-2">{{ blogCard.category}}, {{ blogCard.readingTime }}</span>
                            <h3><a href="#">{{ blogCard.blogTitle }}</a></h3>
                        </div>
                        <p class="mb-0">
                            <a href="#" class="read-more-arrow">
                                <svg class="bi bi-arrow-right" width="1em" height="1em" viewBox="0 0 16 16" fill="currentColor" xmlns="http://www.w3.org/2000/svg">
                                    <path fill-rule="evenodd" d="M10.146 4.646a.5.5 0 0 1 .708 0l3 3a.5.5 0 0 1 0 .708l-3 3a.5.5 0 0 1-.708-.708L12.793 8l-2.647-2.646a.5.5 0 0 1 0-.708z" />
                                    <path fill-rule="evenodd" d="M2 8a.5.5 0 0 1 .5-.5H13a.5.5 0 0 1 0 1H2.5A.5.5 0 0 1 2 8z" />
                                </svg>
                               
                            </a>
                        </p>
                    </div>
                </div>
               
            </div>
        </div>
    </div>
</template>
<style scoped>
</style>