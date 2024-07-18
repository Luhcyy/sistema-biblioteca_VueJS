<script setup lang="ts">
import { ref } from "vue";

const password =  ref('');
const confirmPassword = ref('');
const togglePassword =  ref(false);
const toggleConfirmPassword =  ref(false);
const phone = ref('')

const togglePasswordVisibility = () => {
    togglePassword.value = !togglePassword.value;
};

const toggleConfirmPasswordVisibility = () => {
    toggleConfirmPassword.value = !toggleConfirmPassword.value;
}
    
</script>


<template>
    <section class="custom-container">
    <img src="../assets/imgs/fundo-branco.jpg" alt="Slide 1" class="background-image">
<div class="container mt-2 mb-0">
    
    <div class="row">
        <div class="col-sm-12 col-md-6 image-container">
            <img src="../assets/imgs/Learning-pana.svg" alt="">
        </div>

        <div class="col form-container">
            <div class="form mt-2">
                <h1 class="mt-3 form-title">Cadastro</h1>
                <form action="" class=" mt-2">
                    <div class="input-container">
                        <img src="../assets/imgs/user-solid.svg" alt="">
                        <input type="name" placeholder="Nome Completo" class="text-box">
                    </div>
                    <div class="input-container">
                        <img src="../assets/imgs/phone-solid.svg" alt="">
                        <input type="text" placeholder="Telefone" class="text-box" v-model="phone" v-mask="'(##) #####-####'">
                    </div>
                    <div class="input-container">
                        <img src="../assets/imgs/at-solid.svg" alt="">
                        <input type="email" placeholder="E-mail" class="text-box">
                    </div>
                    <div class="input-container">
                        <img src="../assets/imgs/lock-solid.svg" alt="">
                        <input :type="togglePassword ? 'text' : 'password'" v-model="password" placeholder="Senha" class="text-box">
                        <i class="fas" :class="togglePassword ? 'fa-eye-slash' : 'fa-eye'" @click="togglePasswordVisibility" id="togglePassword"></i>
                    </div>
                    <div class="input-container">
                        <img src="../assets/imgs/lock-solid.svg" alt="">
                        <input :type="toggleConfirmPassword ? 'text' : 'password'" v-model="confirmPassword" placeholder="Confirmar Senha" class="text-box">
                        <i class="fas" :class="toggleConfirmPassword ? 'fa-eye-slash' : 'fa-eye'" @click="toggleConfirmPasswordVisibility" id="togglePassword" ></i>
                    </div>
                    <input type="button" value="Cadastrar" class="signup-btn">
                    <span class="login-text">Já tem uma conta? <router-link to="/login" class="login-link">faça login</router-link></span>
                </form>
            </div>
           
        </div>
    </div>
    
</div>
</section>
</template>


<style scoped>
.custom-container {
  position: relative;
  width: 100%;
  min-height: calc(100vh - 100px);  
  overflow: auto;
}

.custom-container .background-image {
  display: block;
  position: absolute;
  width: 100%;
  max-height: 400px;
  object-fit:fill;
  transform: scaleY(-1) scaleX(-1);
  top: -150px;
  clip-path: inset(50px 0 0 0);
  opacity: 0.20;
  z-index: -11;
}

.custom-container .image-container {
    display: flex;
    justify-content: center;
    align-items: center;
}

.image-container img {
    height: 78.247vh;
    width: 78.247vh;
    
}

.custom-container .form-container {
    display: flex;
    align-items: center;
    justify-content: center
    
}

.form-container .form-title {
    color: #a3130d;
}

.form-container .form {
    display: flex;
    align-items: center;
    flex-direction: column;
    height: 500px;
    width: 350px;
    border-radius: 14px;
    background-color: #ffffff;
    box-shadow: 0px 0px 14px 7px rgba(0,0,0,0.1);
}

.form form {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 15px;
}

.input-container {
    position: relative;
    
}

.input-container img {
    position: absolute;
    left: 10px;
    top: 55%;
    transform: translateY(-50%);
    height: 20px;
    width: 20px;
}

.form form .text-box {
    border: 1px #000 solid;
    border-radius: 5px;
    height: 45px;
    width: 230px;
    padding: 10px 10px 10px 40px;
    box-sizing: border-box;
}

.form form input::placeholder {
    color: #696565;
    font-weight: 500;
}

.form form .signup-btn {
    height: 50px;
    width: 150px;
    border: none;
    border-radius: 3px;
    background-color: #475d68;
    color: white;
    font-weight: 500;
    font-size: 20px;
}

.form form .signup-btn:hover {
    background-color: #5c7480;
}

#togglePassword {
    position: absolute;
    right: 10px;
    top: calc(50% - 7px);
    cursor: pointer;
}

.login-text {
    color: #000;
    font-weight: 400;
}

.login-link {
    font-size: 18px;
    color: #a3130d;
    text-decoration: none;
    font-weight: 500;
}

@media only screen and (max-width: 1000px) {
  .image-container img {
    display: none;
  }

  .form-container {
    margin-top: 20px;
  }

  .form-container .form {
    margin-top: 20px;
  }
}

</style>