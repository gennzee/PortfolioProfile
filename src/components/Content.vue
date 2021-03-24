<template>
    <!-- Page Content-->
        <div class="container-fluid p-0">
            <!-- About-->
            <About/>
            <!-- Experience-->
            <Experience/>
            <!-- Education-->
            <Education/>
            <!-- Skills-->
            <Skill/>
            <!-- Interests-->
            <Interests/>
            <!-- Awards-->
            <Awards/>
        </div>
</template>

<script>
import About from '@/components/About.vue'
import Experience from '@/components/Experience.vue'
import Education from '@/components/Education.vue'
import Skill from '@/components/Skill.vue'
import Interests from '@/components/Interests.vue'
import Awards from '@/components/Awards.vue'

export default {
    name: 'Content',
    components: {
        About,
        Experience,
        Education,
        Skill,
        Interests,
        Awards
    }
}
</script>