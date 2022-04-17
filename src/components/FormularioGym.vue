<template>
    <div class="row container container-form z-depth-5">

        <!-- FORM -->
        <div class="col s12 m6 l6 row data-form left">
            <form class="col s12 form-form ">

                <div class="row row-form">

                    <!-- NOMBRE -->
                    <div class="input-field col s12 m6 l6">
                        <input  id="first_name" 
                                type="text" 
                                class="validate" 
                                placeholder="Nombre" 
                                maxlength=20>        
                    </div>

                    <!-- APELLIDO -->
                    <div class="input-field col s12 m6 l6">
                        <input  id="last_name" 
                                type="text" 
                                class="validate" 
                                placeholder="Apellido"
                                maxlength=40>
                    </div>
                </div>


                <div class="row row-form">

                    <!-- EMAIL -->
                    <div class="input-field col s12">
                        <input  id="email" 
                                type="email" 
                                class="validate" 
                                placeholder="Email"
                                maxlength=60>
                    </div>
                </div>

                <div class="row row-form">

                    <!-- USUARIO -->
                    <div class="input-field col s12 m6 l6">
                        <input  id="disabled" 
                                type="text" 
                                class="validate" 
                                placeholder="Usuario"
                                maxlength=30>
                    </div>

                    <!-- CONTRASE;A -->
                    <div class="input-field col s12 m6 l6">
                        <input  id="disabled" 
                                type="password" 
                                class="validate" 
                                placeholder="Contraseña"
                                minlength="8"
                                maxlength=30>
                    </div>
                </div>
            

                <div class="row row-form">
                    <div class="input-field col s4">
                        <select v-model="dia">
            <option value="1">1</option>
            <option value="2">2</option>
        </select>
                    </div>

                    <div class="input-field col s4">
                        <input id="password" type="text" class="validate" placeholder="Mes">
                        
                    </div>
                    <div class="input-field col s4">
                        <input id="password" type="text" class="validate" placeholder="Año">
                        
                    </div>
                </div>
                
                <!-- Sign UP --> 
                <div class="row row-form sign-up">                        
                        <button class=" btn-sign-up" type="button" name="action">
                            Sign Up
                        </button>                   
                </div>

            </form>

        </div>


        <!-- GOOGLE, FACEBOOK, ETC.-->
        <div class="col s12 m6 l6 google-form right">
            <div id="google-signin-button"></div>
        </div>
        
        
    </div>
    
        <div id="separador" class="hide-on-small-only">
            <span class="separacion separacion-linea top"></span>
            <p class="separacion">O</p>
            <span class=" separacion separacion-linea bottom"></span>
        </div>


</template>
<script>

export default {
    name: 'FormularioGym'
}

</script>

<style scoped>


    /* PROBLEMAS y CONSULTAS :
    -ROOT 
    -INPUT FIELD COMPLETOS
    -GOOGLE FORM
    -D/M/Y DROPDOWN
    -SOBRE USO DE MATERIALIZE */

    :root {
        /* COLORES */
        --grey: #DFDFDF;
        --white: #FFF;
        --red: #FF0000;
    }
    
    

    ::placeholder { /* Chrome, Firefox, Opera, Safari 10.1+ */
        color: rgb(215, 213, 213); /* Firefox */
    }
    .row, .input-field, input {
        margin: 0 !important;
    }
    
    .container-form {
        background-color: rgb(255, 255, 255);
        border-radius: 1.5rem;
        width: 60rem; 
        height: 34rem;
        margin: 200px;
        position: absolute;
        left: 50%;
        top: 50%; 
        transform: translate(-50%, -50%);
    }

    @media screen and (max-width: 600px) {
        .container-form {
            display: flex;
            width: 25rem;
            height: 40rem;
            border-radius: 1rem;
        }
    }
    .data-form {
        position: absolute;
        height: 250px;
        padding: 0px 2rem 0px 2rem;
        top: 44%;
        transform: translateY(-50%);
    }

    input:focus {
        color: red;
        border-bottom: 1px solid #000 !important;
        box-shadow: 0 1px 0 0 #000;
        text-decoration: none;
        
    }

    .validate:focus {
        color: black !important;
        box-shadow: none !important;
        border-color:  rgb(0, 0, 0) !important;
    }
    .input-field {
        margin: 0.75rem 0px 0px 0px !important;
    }
    .sign-up {
        margin-top: 2.50rem !important;
    }

    .btn-sign-up {
        color: white;
        background-color: red;
        border: none;
        border-radius: 5px;
        height: 30px;
        width: 100%;
        z-index: 1;
        transition: 500ms;
    }
    .btn-sign-up:hover {
        background-color: #FF4545;
        border: 1px solid white;
    }

    #separador {
        display: flex;
        flex-direction: column;
        align-items: center;
        position:absolute;
        left: 50%;
        top: 50%; 
        transform: translate(-50%, -50%);
    }

    .separacion-linea {
        background-color: rgb(114, 114, 114);
        height: 110px;
        width: 1px;
    }
    
</style>