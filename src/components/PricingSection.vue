<script setup>
    const headingTitle = "Pricing";
    const description="Pricing for everyone. Choose your plan now!"
    const priceLists= [
        {
            id: 1,
            price: 0,
            priceType: 'Free',
            delay:100    
        },
        {
            id: 2,
            price: 19.99,
            priceType: 'Standard',
            delay:200    
        },
        {
            id: 1,
            price: 79.99,
            priceType: 'Premium',
            delay:300    
        },
        
    ];
    const listItems=[
                "There live the blind texts",
                "Far far away behind the word",
                "Far from the countries Vokalia and Consonantia"
            ];
</script>
<template>
    <div class="untree_co-section bg-light" id="pricing-section">
        <div class="container">
            <div class="row pricing-title">
                <div class="col-12 text-center" data-aos="fade-up" data-aos-delay="0">
                    <h2 class="heading">{{ headingTitle }}</h2>
                    <p>{{ description }}</p>
                </div>
            </div>
            <div class="row justify-content-center">
                <div class="col-lg-10">
                    <div class="row">
                        <div class="col-lg-4" data-aos="fade-up" data-aos-delay="100" v-for="priceList in priceLists" :key="priceList.id">
                            <div class="pricing">
                                <div class="body">
                                    <div class="price">
                                        <span class="d-block plan">{{priceList.priceType}}</span>
                                        <span class="price"><sup>$</sup><span>{{priceList.price}}</span></span>
                                    </div>
                                    <ul class="list-unstyled ul-check primary mb-5">
                                        <li v-for="(listItem,index) in listItems" :key="index">{{ listItem }}</li>
                                    </ul>
                                    <p class="text-center mb-0"><a href="#" class="btn btn-outline-primary">Get Started</a></p>
                                </div>
                            </div>
                        </div>
                       
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<style scoped></style>