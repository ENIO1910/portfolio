<template>
    <v-app id="home">
        <NavBar/>
        <v-container fluid>
            <div class="head">
                <v-row>
                    <v-col>
                        <div style="position:relative" class="mt-16">
                            <h1 class="text-white pt-16 pt-sm-0">Witaj,</h1>
                            <h1 class="text-grey">Nazywam się</h1>
                            <h1 class="text-white">Patryk Staniewski</h1>
                            <span class="text-grey">Web Designer & Developer</span><br/>
                            <v-btn title dark class="text-orange mt-8" variant="outlined">Contact me</v-btn>
                        </div>
                    </v-col>
                    <v-col cols="5" class="d-none d-md-block">
                        <div style="position:relative; z-index: 999;" class="mt-16 pr-16">
                            <v-img src="img/me.png" contain max-height="350"></v-img>
                        </div>

                    </v-col>
                </v-row>
            </div>
            <v-col cols="12" class="mt-16" id="about">
                <div>
                    <v-row>
                        <v-col cols="12" sm="6">
                            <div class="egg">
                                <v-img src="img/i2.png" max-height="300"></v-img>
                            </div>
                        </v-col>
                        <v-col cols="12" sm="6">
                            <h5 class="mt-16">About Me</h5>
                            <div style="width: 120px">
                                <v-slider v-model="slider2" color="orange"></v-slider>
                            </div>
                            <h4 class="mt-n4">I Am a backend developer</h4>
                            <h4 class="">And frontend developer</h4>
                            <p class="text-grey">
                                I am passionate about IT in the broadest sense.
                                I am a quick learner and try to make time every day to learn something new.
                            </p>
                            <br/>
                            <p class="text-grey">
                                Since 2018, I have been trying to gain vision towards PHP developer.
                                Since then, I have done small projects mostly for myself.
                                However, I gained my commercial experience when I worked in a software house.
                            </p>
                            <v-btn tile dark color="#ffa35b" class="mt-4">
                                Download Resume
                            </v-btn>
                        </v-col>
                    </v-row>
                </div>
                <v-divider class="mt-5"></v-divider>

            </v-col>
            <div class="text-center mt-5" id="portfolio">
                <h2>Co do tej pory poznałem 🤔</h2>
            </div>
            <div class="first" id="project">
                <div class="d-flex flex-column justify-center text-center mt-5">
                    <div>
                        <v-btn
                                icon="fas fa-laptop without-fas"
                                color="#ffa35b"
                                class="text-white"
                        ></v-btn>
                    </div>
                    <h3 class="ml-3 text-center mt-4">Website <br/> development</h3>
                    <div class="text-grey flex text-caption">
                        <div>
                            Laravel
                        </div>
                        <div>
                            PHP
                        </div>
                        <div>
                            Vue
                        </div>
                        <div>
                            JS
                        </div>
                    </div>
                </div>
                <div class="d-flex flex-column justify-center mt-10">
                    <div>

                        <v-btn
                                icon="fas fa-mobile-alt without-fas"
                                color="#ffa35b"
                                class="text-white"
                        ></v-btn>
                    </div>

                    <h3 class=" mt-4">Mobile application <br/> development</h3>
                    <div class="text-grey flex text-caption">
                        <div>
                            Dart
                        </div>
                        <div>
                            Flutter
                        </div>
                        <div>
                            Bloc
                        </div>
                    </div>
                </div>
                <v-divider class="mt-3"></v-divider>
            </div>
            <v-col cols="12" sm="12" id="pages">
                <div class="d-flex justify-center mb-6">
                    <v-btn color="#ffa35b" class="mr-2">All</v-btn>
                    <v-btn class="mr-2" variant="tonal">Laravel</v-btn>
                    <v-btn class="mr-2" variant="tonal">Vue</v-btn>
                </div>
            </v-col>
            <v-col cols="12" class="imgHover ">
                <v-row class="fill-height" align="center" justify="center">
                    <template v-for="(item, i) in items" :key="i">
                        <v-col cols="12" md="4">
                            <v-hover v-slot="{ isHovering, props }">
                                <v-card
                                        :elevation="isHovering ? 12 : 2"
                                        :class="{ 'on-hover': isHovering }"
                                        v-bind="props"
                                >
                                    <v-img :src="item.img" height="225px" cover></v-img>
                                </v-card>
                            </v-hover>
                        </v-col>
                    </template>
                </v-row>
            </v-col>
            <v-divider class="mt-15"></v-divider>
            <v-col cols="12" sm="12" class="px-16" id="contact">
                <v-row>
                    <v-col cols="12" sm="4">
                        <div class="child">
                            <h1>Contact info.</h1>
                            <v-btn
                                    icon="fas fa-map-marker-alt"
                                    color=""
                                    class="mt-10"
                                    variant="outlined"
                            ></v-btn
                            >
                            <br/>
                            <span class="text-caption">Polska, Radom 26-600 </span
                            ><br/>
                            <v-btn
                                    icon="fas fa-phone-alt"
                                    color=""
                                    class="mt-10"
                                    variant="outlined"
                            ></v-btn
                            >
                            <br/>
                            <span class="text-caption">+48 667-598-402 </span> <br/>
                            <v-btn
                                    icon="fas fa-envelope"
                                    color=""
                                    class="mt-10"
                                    variant="outlined"
                            ></v-btn
                            >
                            <br/>
                            <span class="text-caption">patrykstaniewski1910@gmail.com </span> <br/>
                        </div>
                    </v-col>
                    <v-col cols="12" sm="8">
                        <h1 class="mt-8">Send your message</h1>
                        <v-divider></v-divider>
                        <span class="text-caption"
                        >Do you have a proposal?
                              Do you have an idea for an application?
                              Would you like your site?
                              <b>Send me a message.</b></span
                        >
                        <v-row class="mt-10">
                            <v-col cols="12" sm="6">
                                <v-text-field
                                        label="Name"
                                        persistent-hint
                                        variant="outlined"
                                ></v-text-field>
                            </v-col>
                            <v-col cols="12" sm="6">
                                <v-text-field
                                        label="Phone No"
                                        persistent-hint
                                        variant="outlined"
                                ></v-text-field>
                            </v-col>
                        </v-row>
                        <v-textarea
                                label="Message"
                                persistent-hint
                                variant="outlined"
                        ></v-textarea>
                        <v-btn color="#FBDF7E" class="mt-2">Submit Now</v-btn>
                    </v-col>
                </v-row>
            </v-col>
        </v-container>
    </v-app>
</template>

<script>
import {defineComponent} from 'vue';

// Components
import NavBar from '../components/NavBar.vue';

export default defineComponent({
    name: 'HomeView',
    setup() {
        return {
            slider2: 50,
            items: [
                {
                    img: "img/webmein.png"
                },
                {
                    img: "img/spacer.png"
                },
            ],
        };
    },

    components: {
        NavBar,
    },
});
</script>
<style scoped>
.v-container {
    padding: 16px 0;
}

#pages{
    margin-top:10rem;
}

.head {
    position: relative;
    text-align: center;
    padding: 12px;
    margin-bottom: 6px;
    height: 400px;
    width: 100%;
    background-color: black;
}

@media (min-width: 960px) {
    .head:before {
        content: " ";
        position: absolute;
        top: 0;
        left: 0;
        height: 100%;
        width: 50%;
        background: black;
        transform: skew(0deg, 5deg);
    }

    .head:after {
        content: " ";
        position: absolute;
        top: 0;
        right: 0;
        height: 100%;
        width: 50%;
        background: black;
        transform: skew(0deg, -5deg);
    }
}

.egg {
    display: block;
    margin-left: 100px;
    margin-top: 50px;
    width: 356px;
    height: 300px;
    background-color: #ffa35b;
    border-radius: 50% 50% 50% 50% / 60% 60% 40% 40%;
}

.first {
    width: 100%;
    height: 280px;
    text-align: center;
}

.child {
    display: inline-block;
    padding: 2rem 1rem;
    vertical-align: middle;
    text-align: center;
    margin-right: 8px;
}

:deep(.without-fas) {
    display: flex;
}


</style>
