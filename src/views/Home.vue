<template>

  <section class="bg-gradient-info "> 
        <div class="container">
            <article class="row justify-content-center">
                <div class="col-xl-10 col-lg-12 col-md-9">
                    <div class="card o-hidden border-0 shadow-lg my-5">
                        <div class="card-body p-0">
                            <div class="row">

                                <div class="col-lg-6 d-none d-lg-block">
                                    <img>
                                </div>

                                <div class="col-lg-6">
                                <div class="p-5">
                                    <div class="text-center">
                                        <h1 class="h4 text-gray-900 mb-4">Bienvenidos!</h1>
                                    </div>
                                            <form class="user" v-on:submit.prevent="login">
                                                <div class="form-group">
                                                    <input type="email" class="form-control form-control-user" id="exampleInputEmail" aria-describedby="emailHelp" placeholder="Emaill..." v-model="usuario">
                                                </div>

                                                <div class="form-group">
                                                    <input type="password" class="form-control form-control-user" id="exampleInputPassword" placeholder="Contraseña" v-model="password">
                                                </div>
                                            
                                                <button type="submit" class="btn btn-primary btn-user btn-block">  Iniciar </button>

                                                <hr />

                                                <a  class="btn btn-google btn-user btn-block">Iniciar con Gmail</a>
                                                <a  class="btn btn-facebook btn-user btn-block">

                                                <i class="fab fa-facebook-f fa-fw"></i> Iniciar con facebook</a>

                                            </form>

                                        <hr />

                                        <div class="text-center">
                                            <a class="small">Olvidaste Contraseña?</a>
                                        </div>

                                        <div class="text-center">
                                            <a class="small">Crear Cuenta!</a>
                                        </div>

                                        <div class="alert alert-danger" role="alert" v-if="error">
                                            {{ error_msg }}
                                        </div>

                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </article>
        </div>
  </section>
</template>

<script>

import axios from 'axios'

export default {
  name: "Home",

  data() {
    return{

      usuario :"",
      password:"",
      error:"",
      error_msg:"",

    }
  },

  methods:{
    login(){

      let json={
        usuario:  this.usuario,
        password: this.password,
      };

      axios
      .post('https://api.solodata.es/auth',json)
      .then( (datos) =>{
        console.log(datos);

        if(datos.data.status == "ok"){
          localStorage.token = datos.data.result.token;
          this.$router.push('about')
        }else{
          this.error = true
          this.error_msg = datos.data.result.error_msg
        }
      })



    }
  }
};
</script>



<style scoped src="@/css/estylo.css"> 


section{
height: 100vh;
}

</style>

