<template>

    <v-app-bar app color="#111111" dark flat class="px-8 ">
        <v-btn icon>
            <v-icon color="#FFD700">fas fa-diamond</v-icon>
        </v-btn>
        <v-spacer></v-spacer>
        <div class="navbar">
            <v-btn text @click="scroll('home')">Home</v-btn>
            <v-btn text @click="scroll('projects')">Projects</v-btn>
            <v-btn text @click="scroll('skills')">Skills</v-btn>
            <v-btn text @click="scroll('about')">About</v-btn>
            <v-btn text @click="scroll('contact')">Contact</v-btn>
        </div>
        <div class="mobileNavbar" style="position:relative;">
            <span class="menuIcon" @click="menu()">
                <i class="fa-solid fa-bars"></i>
            </span>
            <div class="mobileMenu" style="" v-if="mobileMenu">
                <v-row>
                    <v-col cols="12" class="menu">
                        <v-btn text @click="scroll('home')">Home</v-btn>
                    </v-col>
                    <v-col cols="12" class="menu">
                        <v-btn text @click="scroll('projects')">Projects</v-btn>
                    </v-col>
                    <v-col cols="12" class="menu">
                        <v-btn text @click="scroll('skills')">Skills</v-btn>
                    </v-col>
                    <v-col cols="12" class="menu">
                        <v-btn text @click="scroll('about')">About</v-btn>
                    </v-col>
                    <v-col cols="12" class="menu">
                        <v-btn text @click="scroll('contact')">Contact</v-btn>
                    </v-col>
                </v-row>
            </div>
        </div>
    </v-app-bar>

</template>

<script>
export default {
    methods: {
        scroll(refName) {
            const element = document.getElementById(refName);
            console.log(element)
            element.scrollIntoView({ behavior: "smooth" })
            this.mobileMenu = !this.mobileMenu; 
            
        },
        menu() {
            this.mobileMenu = !this.mobileMenu; 
        }
    },
    data() {
        return {
            mobileMenu: false,
        }
    },
}
</script>

<style>
</style>