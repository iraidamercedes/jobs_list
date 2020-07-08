<template>
    <div class="profile">
        <div class="profile-images-wrap">
            <img :src="profile.logo" class="image"/>
        </div>
        <div class="profile-inner">
            <div class="profile-text-wrapp">
                <h2 class="company-text">{{profile.company}}</h2>
                <h1 class="position-text">{{profile.position}}</h1>
            </div>
            <div class="position-info-text-wrapp">
                <a class="date-posted-info">{{profile.postedAt}}</a>
                <a> • </a>
                <a class="contract-text">{{profile.contract}}</a>
                <a> • </a>
                <a class="location-text">{{profile.location}}</a>
            </div>            
        </div>
        <div class="profile-tags">
            <div class="profile-tags-wrapp">
                <a class="tag-level-text">{{profile.level}}</a>
                <p class="tag-laguages-text" v-for="language in profile.languages">{{language}}</p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'profile',
    props: ['profile']
}
</script>