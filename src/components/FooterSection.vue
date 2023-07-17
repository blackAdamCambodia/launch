<script setup>
const footerTitle= "About Launch";
const footerDescription = "Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind texts.";
 const contactInfo = {
        email: "blackadam2000kh@gmail.com",
        phone1: "+855968283659",
        phone2: "+855968283659",
        address: "Phnom phen , Cambodia",
       
    };
    const socialItems = [
    {
        link: 'https://www.instagram.com/',
        icon: 'icon-instagram'
    },
    {
        link: 'https://www.twitter.com/',
        icon: 'icon-twitter'
    },
    {
        link: 'https://www.facebook.com/',
        icon: 'icon-facebook'
    },
    {
        link: 'https://www.linkedin.com/',
        icon: 'icon-linkedin'
    },
    {
        link: 'https://www.pinterest.com/',
        icon: 'icon-pinterest'
    }
]
</script>
<template>
    <div class="site-footer">
        <div class="footer-dots"></div>
        <div class="container">
            <div class="row">
                <div class="col-lg-4">
                    <div class="widget">
                        <h3>{{ footerTitle }}<span class="text-primary">.</span> </h3>
                        <p>{{ footerDescription }}</p>
                    </div>
                    <div class="widget">
                        <h3>Connect</h3>
                        <ul class="list-unstyled social">
                            <li v-for="(socialItem , index ) in socialItems" :key="index"><a :href="socialItem.link"><span :class="socialItem.icon"></span></a></li>
                           
                        </ul>
                    </div>
                </div>
                <div class="col-lg-2 ml-auto">
                    <div class="widget">
                        <h3>Projects</h3>
                        <ul class="list-unstyled float-left links">
                            <li><a href="#">La Lega Stadium</a></li>
                            <li><a href="#">France Building</a></li>
                            <li><a href="#">22 New Homes</a></li>
                            <li><a href="#">Manage Center</a></li>
                            <li><a href="#">Sports Hall</a></li>
                        </ul>
                    </div>
                </div>
                <div class="col-lg-2">
                    <div class="widget">
                        <h3>Services</h3>
                        <ul class="list-unstyled float-left links">
                            <li><a href="#">Architect</a></li>
                            <li><a href="#">Interior Design</a></li>
                            <li><a href="#">Landscape Design</a></li>
                            <li><a href="#">Consultancy</a></li>
                        </ul>
                    </div>
                </div>
                <div class="col-lg-3">
                    <div class="widget">
                        <h3>Contact</h3>
                        <address>{{contactInfo.address}}</address>
                        <ul class="list-unstyled links mb-4">
                            <li><a href="">{{ contactInfo.phone1 }}</a></li>
                            <li><a href="">{{ contactInfo.phone2 }}</a></li>
                            <li><a href=""><span class="__cf_email__" data-cfemail="94fdfaf2fbd4f9edf0fbf9f5fdfabaf7fbf9">{{ contactInfo.email }}</span></a></li>
                        </ul>
                    </div>
                </div>
            </div>
            <div class="row mt-5">
                <div class="col-12 text-center">
                    <p>
                        Copyright &copy; 2023 All rights reserved | This template is made with <i class="icon-heart text-danger" aria-hidden="true"></i> by <a href="https://www.blackadam.com/" target="_blank">Kazi IT Home</a>
                    </p>
                </div>
            </div>
        </div>
    </div>
</template>
<style scoped></style>