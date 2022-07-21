<template>
  <div class="page-login">
    <div class="date">
      <div class="container">
        <image-base image="logo" desc="logo" class="logo-mobile" />
        <title-base type="h1" content="Olá," size="size-60px" class="title" />
        <text-base
          size="size-16px"
          text="Para continuar navegando de forma segura, efetue o login na rede."
        />
        <title-base type="h2" content="Login" size="size-30px" class="login" />
        <div class="input-icon">
          <label for="user"><i class="fa fa-user"></i></label>
          <input-base
            Type="text"
            idInputs="user"
            classInputs="inputs"
            placeholder="Usuário"
            class="input"
          />
        </div>
        <div class="input-icon">
          <label for="password"><i class="fa fa-lock"></i></label>
          <input-base
            Type="password"
            idInputs="password"
            classInputs="inputs"
            placeholder="Senha"
            class="input"
          />
        </div>
        <div class="error">
          <text-base
            size="size-16px"
            id="erro"
            text="Ops, usuário ou senha inválidos. Tente novamente!"
          />
        </div>
        <input-base
          Type="submit"
          idInputs="submit"
          classInputs="register"
          value="Continuar"
        />
      </div>
    </div>
    <div class="img">
      <div class="fundo">
        <image-base image="logo" desc="logo" id="image-logo" />
      </div>
    </div>
  </div>
</template>

<script>
import TitleBase from '../../components/TitleBase/TitleBase.vue';
import TextBase from '../../components/TextBase/TextBase.vue';
import InputBase from '../../components/InputBase/InputBase.vue';
import ImageBase from '../../components/ImageBase/ImageBase.vue';

export default {
  name: "PageLogin",
  components: {
    TitleBase,
    TextBase,
    InputBase,
    ImageBase,
  },
};
</script>

<style lang="scss" scoped>
@import "./PageLogin.scss";
</style>
