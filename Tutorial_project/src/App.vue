<template>
    <div id="app">
        <div class="container" id="nav">
            <div class="jumbotron">
                <router-link class="btn btn-primary" to="/">Home</router-link>
                |
                <router-link class="btn btn-primary" to="/about">About</router-link>
                |
                <router-link class="btn btn-primary" to="/calculator">Calculator</router-link>
            </div>
        </div>
        <router-view/>
    </div>
</template>

<style>
    #app {
        font-family: 'Avenir', Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        text-align: center;
        color: #2c3e50;
        margin-top: 60px;
    }
</style>
