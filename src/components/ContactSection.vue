<script setup>
    const headingTitle= "Get In Touch";
    const description="Far from the countries Vokalia and Consonantia";
    const contactInfoHeading="Contact Info";
    const contactInfo = {
        email: "blackadam2000kh@gmail.com",
        phone1: "+855968283659",
        phone2: "+855968283659",
        address: "Phnom phen , Cambodia",
        website: "http://blackadam.com"
    };
</script>
<template>
    <div class="untree_co-section" id="contact-section">
        <div class="container">
            <div class="row mb-4" data-aos="fade-up" data-aos-delay="0">
                <div class="col-12 text-center">
                    <h2 class="heading">{{ headingTitle }}</h2>
                    <p>{{ description }}</p>
                </div>
            </div>
            <div class="row">
                <div class="col-lg-7">
                    <form class="contact-form" data-aos="fade-up" data-aos-delay="100">
                        <div class="row">
                            <div class="col-6">
                                <div class="form-group">
                                    <label class="" for="fname">First name</label>
                                    <input type="text" class="form-control" id="fname">
                                </div>
                            </div>
                            <div class="col-6">
                                <div class="form-group">
                                    <label class="" for="lname">Last name</label>
                                    <input type="text" class="form-control" id="lname">
                                </div>
                            </div>
                        </div>
                        <div class="form-group">
                            <label class="" for="email">Email address</label>
                            <input type="email" class="form-control" id="email">
                        </div>
                        <div class="form-group">
                            <label class="" for="message">Message</label>
                            <textarea name="" class="form-control" id="message" cols="30" rows="5"></textarea>
                        </div>
                        <button type="submit" class="btn btn-primary">Send Message</button>
                    </form>
                </div>
                <div class="col-lg-4 ml-auto" data-aos="fade-up" data-aos-delay="200">
                    <h3 class="h5 mb-4">{{ contactInfoHeading }}</h3>
                    <address class="text-black d-flex"><span class="mt-1 icon-room mr-2"></span><span>{{contactInfo.address}}</span></address>
                    <ul class="list-unstyled ul-links mb-4">
                        <li><a :href="'tel://'+'contactInfo.phone1'" class="d-flex"><span class="mt-1 icon-phone mr-2"></span><span>{{ contactInfo.phone1 }}</span></a></li>
                        <li><a :href="'tel://'+'contactInfo.phone2'" class="d-flex"><span class="mt-1 icon-phone mr-2"></span><span>{{ contactInfo.phone2 }}</span></a></li>
                        <li><a :href="'mailto:'+'contactInfo.email'" class="d-flex"><span class="mt-1 icon-envelope mr-2"></span><span><span class="__cf_email__" data-cfemail="20494e464f604d59444f4d41494e0e434f4d">{{ contactInfo.email }}</span></span></a></li>
                        <li><a :href="[contactInfo.website]" target="_blank" class="d-flex"><span class="mt-1 icon-globe mr-2"></span><span>{{contactInfo.website}}</span></a></li>
                    </ul>
                </div>
            </div>
        </div>
    </div>
</template>
<style scoped>
</style>