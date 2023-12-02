<script setup>
    import '~/assets/css/topbar.css';
</script>

<template>
    <div class="navbar-top">
        <div class="search-container">
            <input type="text" class="navbar-search">
            <div class="search-icon">
                <svg width="35" height="35" viewBox="0 0 35 35" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M23.615 23.6401L32 32M27.1667 15.0833C27.1667 21.7567 21.7567 27.1667 15.0833 27.1667C8.40989 27.1667 3 21.7567 3 15.0833C3 8.40989 8.40989 3 15.0833 3C21.7567 3 27.1667 8.40989 27.1667 15.0833Z" stroke="#494949" stroke-width="5" stroke-linecap="round" stroke-linejoin="round"/></svg>
            </div>
        </div>
        <a href="/">Gallery</a>
        <a href="/forum">Forum</a>
        <button>Login</button>
    </div>
</template>