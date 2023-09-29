<template>
  <div>
    <div class="btn-senha" @click="modalAberto = true">Esqueci minha senha</div>
    <div v-if="modalAberto">
      <div class="background-modal" @click="modalAberto = false"></div>
      
      <div class="modal">
        <div class="modal-conteudo">
          <div class="form-container">
            <div class="logo-container">
              Recuperar senha
            </div>
            <form class="form">
              <div class="form-group">
                <label for="email" id="form-email" style="align-self: center; color: black; font-weight: bold;">Digite seu cadastrado</label>
                <input type="email" id="email" name="email" placeholder="Digite seu email">
              </div>  
              <button class="form-submit-btn" type="submit">Enviar Email</button>
            </form>
          </div>
        </div>
      </div>

    </div>
  </div>
</template>

<script>

export default {
  data() {
    return {
      modalAberto: false
    }
  }
}


</script>

<style>
.btn-senha {
  color: rgb(171, 44, 171); 
  font-weight: bold;
  width: fit-content;
  cursor: pointer; 
}
.modal {
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
  z-index: 2;
}

.background-modal {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.5);
  z-index: 1;
}
.form-container {
  width: 20vw;
  background-color: #fff;
  padding: 32px 24px;
  font-size: 14px;
  font-family: sans-serif;
  color: #212121;
  display: flex;
  flex-direction: column;
  gap: 10px;
  box-sizing: border-box;
  border-radius: 10px;
  box-shadow: 0px 0px 3px rgba(0, 0, 0, 0.084), 0px 2px 3px rgba(0, 0, 0, 0.168);
}
.form-container button:active {
  scale: 0.95;
}

.form-container .logo-container {
  text-align: center;
  font-weight: 600;
  font-size: 30px;
  font-family:sans-serif;
}

.form-container .form {
  display: flex;
  flex-direction: column;
}

.form-container .form-group {
  display: flex;
  flex-direction: column;
  gap: 2px;
}

.form-container .form-group label {
  display: flex;
  margin-bottom: 1vh;
}

.form-container .form-group input {
  width: auto;
  height: 100%;
  padding: 12px;
  border-radius: 6px;
  font-family: sans-serif;
  border: 1px solid black;
  margin-top: 1em;
  text-align: left;
}

.form-container .form-group input:focus {
  outline: none;
  border-color: red;
  transition: all 250ms ease;
  transform: scale(1.02);
}

.form-container .form-submit-btn {
  display: flex;
  justify-content: center;
  align-items: center;
  font-family: inherit;
  color: #fff;
  background-color: #212121;
  border: none;
  width: 100%;
  padding: 12px 16px;
  font-size: inherit;
  gap: 8px;
  margin-top: 2em;
  cursor: pointer;
  border-radius: 6px;
}

.form-container .form-submit-btn:hover {
  background-color: red;
  transform: scale(1.02);
  transition: all 250ms ease;
  
}

.form-container .link:hover {
  text-decoration: underline;
}

</style>
