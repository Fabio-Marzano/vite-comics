<script>
export default {
    name: 'AppHeader',
    data() {
        return {
            links: [
                { text: 'Characters', url: '#', current: false },
                { text: 'Comics', url: '#', current: true },
                { text: 'Movies', url: '#', current: false },
                { text: 'TV', url: '#', current: false },
                { text: 'Games', url: '#', current: false },
                { text: 'Collectibles', url: '#', current: false },
                { text: 'Videos', url: '#', current: false },
                { text: 'Fans', url: '#', current: false },
                { text: 'News', url: '#', current: false },
                { text: 'Shop', url: '#', current: false }
            ]
        }
    },

}

</script>

<template>

    <header class="container">
        <figure class="nav-logo">
            <img src="../assets/img/dc-logo.png" alt="">
        </figure>
        <ul class="nav-links">
            <li v-for="link in links" :key="link.text">
                <a :href="link.url" :class="{ 'active': link.current }">{{ link.text }}</a>
            </li>
        </ul>
    </header>


</template>


