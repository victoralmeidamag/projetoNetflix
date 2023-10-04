<template>
  <div>
    <div class="btn-senha" @click="modalAberto = true">Esqueci minha senha</div>
    <div v-if="modalAberto">
      <div class="background-modal" @click="modalAberto = false"></div>

      <div class="modal">
        <div class="modal-conteudo">
          <div class="login-body">
            <div class="login-content">
              <div data-uia="password-reset-wrapper">
                <h1 data-uia="password-reset-header">Esqueci minha senha</h1>
                <p data-uia="password-reset-subheader">Digite o seu Email cadastrado</p>
                <div>
                  <p data-uia="email-description">Enviaremos um email com instruções de como redefinir sua senha.</p>
                  <div class="contact-input-wrapper">
                    <label class="contact-method-input ui-label ui-input-label" id="lbl-forgot_password_input">
                      <span class="ui-label-text"></span>
                      <input type="email" data-uia="forgot_password_input" class="ui-text-input"
                        name="forgot_password_input" id="forgot_password_input" value="" placeholder="nome@exemplo.com"
                        tabindex="0"></label>
                  </div>
                </div>
                <button class="btn forgot-password-action-button btn-blue btn-large" type="button" autocomplete="off"
                  tabindex="0" data-uia="action_forgot_password">Enviar por email</button>
              </div>
            </div>
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
  color: rgb(0, 0, 0);
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

@import url(https://fonts.googleapis.com/css?family=Roboto:100,regular,italic,500,700);

body {
  font-family: "Roboto";
  font-size: 16px;
}

.login-body {
  background-color: transparent;
  color: #333;
}

* {
  letter-spacing: 0 !important;
}

div {
  display: block;
}

.login-content {
  min-width: 380px;
  padding: 40px;
  background-color: #f3f3f3;
}

h1 {
  margin-bottom: 20px;
  margin: 0 0 10px;
  padding: 0;
  font-size: 2em;
  display: block;
  font-size: 2em;
  margin-block-start: 0.67em;
  margin-block-end: 0.67em;
  margin-inline-start: 0px;
  margin-inline-end: 0px;
  font-weight: bold;
  font-family: "Roboto";
}

b,
h1,
h2,
h3,
h4,
h5,
h6,
optgroup,
strong {
  font-weight: 500;
  font-family: "Roboto";
  font-weight: bold;
}

p {
  display: block;
  margin-block-start: 1em;
  margin-block-end: 1em;
  margin-inline-start: 0px;
  margin-inline-end: 0px;
  font-family: "Roboto";
}

.contact-method-input {
  margin-bottom: 10px;
  padding-bottom: 10px;
}

.ui-input-label {
  position: relative;
}

.ui-label,
.ui-label-no-margin {
  color: grey;
  display: block;
  font-size: 1em;
  font-weight: 400;
}

label {
  cursor: default;
}

.contact-method-input .ui-text-input {
  max-width: none;
  width: 100%;
}

.input-password-input,
.ui-text-input {
  -webkit-appearance: none;
  -moz-appearance: none;
  appearance: none;
  border: 1px solid #b3b3b3;
  border-radius: 2px;
  box-sizing: border-box;
  color: #000;
  display: block;
  font-size: 16px;
  height: 44px;
  max-width: 500px;
  padding: 10px 11px;
  width: 100%;
}

input {
  line-height: normal;
}

button,
input,
optgroup,
select,
textarea {
  color: inherit;
  font: inherit;
  margin: 0;
}

button,
input,
optgroup,
select,
textarea {
  color: inherit;
  font: inherit;
  margin: 0;
}

input[type="email" i] {
  padding-block: 1px;
  padding-inline: 2px;
}

.forgot-password-action-button.btn-large {
  width: 100%;
}

.btn {
  font-size: 20px;
  min-height: 48px;
  min-width: 112px;
  padding: 14px 2em;
  background-color: #0080ff;
  border: none;
  color: white;
  font-weight: bold
}

.btn:hover {
  scale: 1.01;
  color: black;
}</style>
