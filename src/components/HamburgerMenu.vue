<template>
    <header>
        <nav id="navbar-provisorio">

            <div class="logo">
                <img src="../assets/logo.png" alt="Logo">
            </div>

            <ul v-show="!mobile" class="navigation">
                <li><router-link class="link" :to="{ name: '/' }">Profesor</router-link></li>
                <li><router-link class="link" :to="{ name: '' }">Planificacion</router-link></li>
                <li><router-link class="link" :to="{ name: '' }">Ejercicios de metodologia</router-link></li>
                <li><router-link class="link" :to="{ name: '' }">Entrevistas</router-link></li>
                <li><router-link class="link" :to="{ name: '' }">Donaciones</router-link></li>
                <li><router-link class="link" :to="{ name: '' }">Crear cuenta</router-link></li>
            </ul>
            <div class="icon">
                <fa id="hamburguesa" @click="toggleMobileNav" v-show="mobile" icon="bars" :class="{'icon-active' :mobileNav}"/>
            </div>

            <transition name="mobile-nav">
                <ul v-show="mobileNav" class="dropdown-nav">
                    <div class="logo">
                        <img src="../assets/logo.png" alt="Logo">
                    </div>
                    <li><router-link class="link" :to="{ name: '' }">Profesor</router-link></li>
                    <li><router-link class="link" :to="{ name: '' }">Planificacion</router-link></li>
                    <li><router-link class="link" :to="{ name: '' }">Ejercicios de metodologia</router-link></li>
                    <li><router-link class="link" :to="{ name: '' }">Entrevistas</router-link></li>
                    <li><router-link class="link" :to="{ name: '' }">Donaciones</router-link></li>
                    <li><router-link class="link" :to="{ name: '' }">Crear cuenta</router-link></li>
            </ul>
            </transition>
        </nav>
    </header>
</template>

<script>

export default {
    name: 'HamburgerMenu',
    data() {
        return {
            mobile: null,
            mobileNav: null,
            windowWidth: null
        };
    },
    created() {
        window.addEventListener('resize', this.checkScreen);
        this.checkScreen();
    },
    methods: {
        toggleMobileNav() {
            this.mobileNav = !this.mobileNav;
        },

        checkScreen() {
            this.windowWidth = window.innerWidth;
            if( this.windowWidth <= 600 ) {
                this.mobile = true;
                return;
            }
            this.mobile = false;
            this.mobileNav = false;
            return;
        }
    }
}

</script>

<style scoped>

    header {
        background-color: black;
        z-index: 99;
        width: 100%;
        position: fixed;
        transform: 0.5s ease all;
        color: white;
    }

    nav {
        position: relative;
        display: flex;
        flex-direction: row;
        padding: 12px 0;
        transition: 0.5s ease all;
        width: 100%;
        margin: 0 auto;
    }

    ul,
    .link {
        font-weight: 500;
        color: white;
        list-style: none;
        text-decoration: none;
    }

    .navigation {
        display: flex;
        align-items: center;
        flex: 1;
        justify-content: flex-end;
    }

    .navigation > li {
        text-transform: uppercase;
        padding: 16px;
        margin-left: 16px;
    }

    .navigation > li > .link {
        font-size: 14px;
        transition: .5s ease all;
        padding-bottom: 4px;
        border-bottom: 1px solid transparent;
    }

    .navigation > li > .link:hover {
        color: red;
        border-color: black;
    }

    .logo {
        display: flex;
        align-items: center;
    }

    img {
        width: 50px;
        transition: .5s ease all ;
    }

    .icon {
        display: flex;
        align-items: center;
        position: absolute;
        top: 0;
        right: 24px;
        height: 100%;
    }

    #hamburguesa {
        cursor: pointer;
        font-size: 24px;
        transition: .8s ease all;
    }

    .icon-active {
        transform: rotate(180deg);
    }

    .dropdown-nav {
        display: flex;
        flex-direction: column;
        position: fixed;
        width: 100%;
        max-width: 250px;
        height: 100%;
        background-color: white;
        top: 0;
        left: 0;
    }
    
    .dropdown-nav > li {
        margin-left: 0;
    }

    .dropdown-nav > li > .link {
        color: black;
    }

</style>
