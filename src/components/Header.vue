<template>
    <header>
        <div class="header-nav container">
            <div class="logo">
                <img src="@/assets/img/dc-logo.png" alt="logo.png">
            </div>
            <div class="nav-menu">
                <ul class="nav-items">
                    <li v-for="(link, index) in links" :key="index" class="nav-item" :class="(link.current) ? 'active' : null">
                        <a :href="link.url">{{link.text.toUpperCase()}}</a>
                    </li>
                </ul>
            </div>
        </div>
    </header>
</template>

<script>
export default {
    name: "Header",

    data(){
        return{
            links:[
                {
                    text: "CHARACTERS",
                    url: "#",
                    current: false,
                },
                {
                    text: "COMICS",
                    url: "#",
                    current: true,
                },
                {
                    text: "MOVIES",
                    url: "#",
                    current: false,
                },
                {
                    text: "TV",
                    url: "#",
                    current: false,
                },
                {
                    text: "GAMES",
                    url: "#",
                    current: false,
                },
                {
                    text: "COLLECTIBLES",
                    url: "#",
                    current: false,
                },
                {
                    text: "VIDEOS",
                    url: "#",
                    current: false,
                },
                {
                    text: "FANS",
                    url: "#",
                    current: false,
                },
                {
                    text: "NEWS",
                    url: "#",
                    current: false,
                },
                {
                    text: "SHOP",
                    url: "#",
                    current: false,
                },
            ]
        }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "@/style/generals";

.header-nav{
    height: 100px;
    @include center(vertical); 
    justify-content: space-between;
}
.logo {
    width: 70px;
    padding: 20px 0px;
    img{
        width: 100%;
    }
}
.nav-items{
    list-style: none; 
    display: flex; 
    font-size: 12px;
    line-height: 95px;
}
.nav-item{
    padding: 0px 15px;
    color: black;
    cursor: pointer;
    a{
        text-decoration: none;
        color: inherit;
        font-weight: 600;
        &:hover{
        color: $primary-color;
    }
}
    &:hover{
        color: $primary-color;
        border-bottom: 5px solid $primary-color;
    }
    &.active{
        color: $primary-color;
        border-bottom: 5px solid $primary-color;
    }
}
</style>