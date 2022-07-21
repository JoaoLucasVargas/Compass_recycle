<template>
  <div class="page-home">
    <div class="header">
      <div class="logo">
        <ImageBase image="logo2" desc="logo" class="" id="image-logo2" />
      </div>
      <div class="time">
        <ApiClock />
      </div>

      <div class="temp">
        <ApiWeather />
      </div>
    </div>
    <div class="container">
      <div class="image">
        <img src="@/assets/uol2.png" alt="" id="uol-img" />
      </div>
      <div class="message">
        <TextBase
          size="size-24px"
          text="Our mission is"
          id="red-bold"
          class="item-message"
        />
        <TextBase
          size="size-24px"
          text="Nossa missão é"
          id="black"
          class="item-message"
        />
        <TextBase
          size="size-40px"
          text="to transform the world"
          id="red-bold"
          class="item-message"
        />
        <TextBase
          size="size-20px"
          text="transformar o mundo"
          id="black"
          class="item-message"
        />
        <TextBase
          size="size-40px"
          text="building digital experiences"
          id="red-bold"
          class="item-message"
        />
        <TextBase
          size="size-20px"
          text="construindo experiências digitais"
          id="black"
          class="item-message"
        />
        <TextBase
          size="size-40px"
          text="that enable our client’s growth"
          id="red-bold"
          class="item-message"
        />
        <TextBase
          size="size-20px"
          text="que permitam o crescimento dos nossos clientes"
          id="black"
          class="item-message"
        />
      </div>
    </div>

    <div class="footer">
      <div class="text1">
        <TextBase
          size="size-13px"
          text="Essa janela do navegador é usada para manter sua sessão de autenticação ativa."
        />
        <TextBase
          size="size-13px"
          text=" Deixe-a aberta em segundo plano e abra uma nova janela para continuar a navegar."
        />
      </div>
      <div class="text2">
        <TextBase size="size-16px" text="Application refresh in" />
      </div>
      <div class="text3">
        <TimerBase />
      </div>
      <div class="buttons">
        <div class="button1" @click="continuar()">
          <TextBase
            size="size-16px"
            text="Continuar Navegando"
            id="red-bold"
            class="button"
          />
        </div>
        <div class="button2" @click="logout()">
          <TextBase size="size-16px" text="Logout" class="button" />
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import ImageBase from "@/components/ImageBase/ImageBase.vue";
import TextBase from "@/components/TextBase/TextBase.vue";
import ApiWeather from "@/components/ApiWeather/ApiWeather.vue";
import ApiClock from "@/components/ApiClock/ApiClock.vue";
import TimerBase from "@/components/TimerBase/TimerBase.vue";

export default {
  name: "PageHom",
  components: {
    ImageBase,
    TextBase,
    ApiWeather,
    ApiClock,
    TimerBase,
  },
  created() {},
  methods: {
    continuar() {
      this.$router.push("/home");
    },
    logout() {
      localStorage.setItem("token", false);
      this.$router.push("/");
    },
  },
};
</script>

<style lang="scss" scoped>
@import "./PageHome.scss";
</style>
