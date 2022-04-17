<template>


    <div class="row container container-form z-depth-5">

        <!-- FORM -->
        
        <form class="col s12 m6 l6">


                <!-- AVATAR -->
                    <div class="col s12 center container-avatar">
                        <img id="avatar" src="../assets/logo.png" alt="avatar">
                        
                        <label class="boton-avatar">
                            <input type="file" accept="image/png, image/jpeg" v-on:change="avatar">
                            Elegir un avatar
                        </label>
                    </div>


                <!-- NOMBRE -->
                    <div class="col s12 m6 l6">
                        <label>Nombre:</label>
                        <input  id="first_name" 
                                type="text" 
                                class="validate" 
                                maxlength=20
                                v-model="nombre"
                                required>        
                    </div>


                <!-- APELLIDO -->
                    <div class="col s12 m6 l6">
                        <label>Apellido:</label>
                        <input  id="last_name" 
                                type="text" 
                                class="validate"
                                maxlength=40
                                v-model="apellido"
                                required>
                    </div> 
                
                
                <!-- EMAIL -->
                    <div class="col s12">
                        <label>Email:</label>
                        <input  id="email" 
                                type="email" 
                                class="validate"
                                maxlength=60
                                v-model="email"
                                required>
                    </div>
                
                
                <!-- USUARIO -->
                    <div class="col s12 m6 l6">
                        <label>Usuario:</label>
                        <input  id="disabled" 
                                type="text" 
                                class="validate"
                                maxlength=30
                                v-model="usuario"
                                required>
                    </div>


                <!-- CONTRASE;A -->
                    <div class="col s12 m6 l6">
                        <label>Contraseña:</label>
                        <input  id="disabled" 
                                type="password" 
                                class="validate"
                                minlength="8"
                                maxlength=30
                                v-model="contraseña"
                                required>
                    </div>
                
            

                <!-- FECHA DE NACIMIENTO -->
                    <div class="col s4">
                        <label>Dia:</label>
                        <select v-model="dias">
                            <option v-for="dia in 31" v-bind:key="dia">{{ dia }}</option>
                        </select>
                    </div>
                    <div class="col s4">
                        <label>Mes:</label>
                        <select v-model="meses">
                            <option v-for="mes in 12" v-bind:key="mes">{{ mes }}</option>
                        </select>
                    </div>
                    <div class="col s4">
                        <label>Año:</label>
                        <select v-model="años">
                            <option v-for="año in 2022"  v-bind:key="año">{{ año }}</option>
                        </select>
                    </div>
                
                
                <!-- Sign UP --> 
                    <div class="col s12 sign-up">                        
                            <button type="button" name="action">
                                Sign Up
                            </button>                   
                    </div>

        </form>


        


        <!-- GOOGLE, FACEBOOK, ETC.-->
        <div class="col s12 m6 l6 google-form right">
            <div id="google-signin-button"></div>
        </div>
        
        
    </div>
    


</template>
<script>

export default {
    name: 'FormRedLyon',
    data() {
        return{
            nombre: '',
            apellido: '',
            email: '',
            usuario: '',
            contraseña: '',
            dias: '',
            meses: '',
            años: '',
            avatar: ''
            
        }
    },
    methods: {

    }

}

</script>

<style scoped>

    .container-form {
        background-color: rgb(255, 255, 255);
        border-radius: 1.5rem;
        width: 60rem; 
        height: 40rem;
        position: absolute;
        left: 50%;
        top: 50%; 
        transform: translate(-50%, -50%);
    }

    #avatar {
        width: 100px;
        border-radius: 50%;
        border: 2px solid black;
        margin-bottom: 10px;
    }
    .container-avatar {
        display: flex;
        flex-direction: column;
        align-content: center;
        align-items: center;
        margin-bottom: 20px;
    }
    .boton-avatar {
        border: 1px solid rgb(255, 0, 0);
        display: inline-block;
        padding: 3px 15px;
        cursor: pointer;
    }

    input[type="file"] {
        display: none;
    }

    form {
        background: rgb(187, 187, 187);
        text-align: left;
        padding: 40px;
        position: absolute;
        top: 50%;
        transform: translateY(-50%);
    }
    label {
        color: #aaa;
        display: inline-block;
        margin: 0;
        font-size: 0.7em;
        text-transform: uppercase;
        letter-spacing: 1px;
        font-weight: bold;
    }
    input, select {
        display: block;
        padding: 10px 6px;
        width: 100%;
        box-sizing: border-box;
        border: none;
        border-bottom: 1px solid #ddd;
        color: #555;
    }
    

    .sign-up {
        margin-top: 2.50rem !important;
    }
    .sign-up > button {
        color: white;
        background-color: red;
        border: none;
        border-radius: 5px;
        height: 30px;
        width: 100%;
        z-index: 1;
        transition: 500ms;
    }
    .sign-up > button:hover {
        background-color: #FF4545;
        border: 1px solid white;
    }
</style>