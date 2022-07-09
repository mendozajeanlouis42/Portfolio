<template>

    <div>
        <FsLightbox :toggler="toggler" :sources="loadedPhotos" />

        <div v-for='(featuredProject, index)  in featuredProjects' :key='featuredProject.projectName'>

            <div class="first" v-if="index % 2 == 0">
                <v-row>
                    <v-col md="6" lg="6">
                        <v-img :src="'/images/projects/' + featuredProject.image" contain max-height="400"
                            @click="showImage(index, '/images/projects/' + featuredProject.image)">
                        </v-img>
                    </v-col>

                    <v-col md="6" lg="6">
                        <v-row>
                            <v-col md="12" lg="8" offset-lg="2">
                                <div class="child bgColor1">
                                    <v-row>
                                        <!-- Project Title -->
                                        <v-col cols="12" style="text-align:center;">
                                            <v-icon color="#fe4652" x-large class="ml-3 mb-5" dark
                                                style="display: inline;">
                                                {{ featuredProject.icon }}
                                            </v-icon>
                                            <h3 class="white--text ml-3 mt-4" style="display: inline;">
                                                {{ featuredProject.projectName }}</h3>
                                        </v-col>
                                        <!-- Project Title -->

                                        <!-- Programming Languages Used -->
                                        <v-col class="progLanguage" cols="12">
                                            <v-row class="justify-center">
                                                <v-col md="2" v-for='(skills) in featuredProject.involved_languages'
                                                    :key='skills'>
                                                    <v-img :src="'images/skills/' + skills + '.svg'" contain
                                                        max-height="40" max-width="40">
                                                    </v-img>
                                                </v-col>
                                            </v-row>
                                        </v-col>
                                        <!-- Programming Languages Used -->

                                        <!-- Project Description -->
                                        <v-col cols="12">
                                            <span class="grey--text ml-3 mt-6">
                                                {{ featuredProject.description }}
                                            </span>
                                        </v-col>
                                        <!-- Project Description -->
                                    </v-row>
                                </div>
                            </v-col>
                        </v-row>
                    </v-col>
                </v-row>
            </div>

            <div class="first" v-if="index % 2 != 0">
                <v-row>
                    <v-col lg="5" md="6">
                        <v-row>
                            <v-col md="12" lg="10" offset-lg="2">
                                <div class="child bgColor1">
                                    <v-row>
                                        <!-- Project Title -->
                                        <v-col cols="12" style="text-align:center;">
                                            <v-icon color="#fe4652" x-large class="ml-3 mb-5" dark
                                                style="display: inline;">
                                                {{ featuredProject.icon }}
                                            </v-icon>
                                            <h3 class="white--text ml-3 mt-4" style="display: inline;">
                                                {{ featuredProject.projectName }}</h3>
                                        </v-col>
                                        <!-- Project Title -->

                                        <!-- Programming Languages Used -->
                                        <v-col class="progLanguage" cols="12">
                                            <v-row class="justify-center">
                                                <v-col md="2" v-for='(skills) in featuredProject.involved_languages'
                                                    :key='skills'>
                                                    <v-img :src="'images/skills/' + skills + '.svg'" contain
                                                        max-height="30" max-width="30">
                                                    </v-img>
                                                </v-col>
                                            </v-row>
                                        </v-col>
                                        <!-- Programming Languages Used -->

                                        <!-- Project Description -->
                                        <v-col cols="12">
                                            <span class="grey--text ml-3 mt-6">
                                                {{ featuredProject.description }}
                                            </span>
                                        </v-col>
                                        <!-- Project Description -->
                                    </v-row>
                                </div>
                            </v-col>
                        </v-row>
                    </v-col>

                    <v-col md="6" lg="6" offset-lg="1">
                        <v-img :src="'/images/projects/' + featuredProject.image" contain max-height="400"
                            @click="showImage(index, '/images/projects/' + featuredProject.image)">
                        </v-img>
                    </v-col>
                </v-row>
            </div>
        </div>
    </div>

</template>
<script>
import FsLightbox from "fslightbox-vue";

export default {
    props: ['featureProjects'],
    data() {
        return {
            featuredProjects: this.featureProjects,
            loadedPhotos: this.loadedPhotos,
            toggler: false,
        }
    },
    methods: {
        showImage: function (id, sources) {
            this.loadedPhotos = [sources]
            this.toggler = !this.toggler
        }
    },
    components: { FsLightbox },

}
</script>

<style scoped>
.top {
    margin-top: 180px;
}

.topInverse {
    margin-top: -250px;
}

.topTolbar {
    margin-top: 100px;
    text-align: center;
}

.first {
    width: 100%;
    height: 100%;
    background: linear-gradient(to right,
            #181818,
            #181818 50%,
            #111111 50%,
            #111111 50%);
    text-align: center;
    padding: 2rem 2rem;
}

.second {
    width: 100%;
    height: 400px;
    background: #181818;
    text-align: center;
    padding: 2rem 2rem;
}

.secondchild1 {
    display: inline-block;
    background-color: #1e1e1e;
    padding: 2rem 1rem;
    vertical-align: middle;
    text-align: left;
    margin-top: 250px;
}

.child {
    display: inline-block;
    padding: 2rem 1rem;
    vertical-align: middle;
    text-align: left;
    margin-right: 8px;
}
</style>