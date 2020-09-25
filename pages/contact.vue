<template lang="pug">
  .container
    section#contact
      h2.ttl Contact
      p Ask me something
      form#form(method="POST" netlify data-netlify-honeypot="bot-field")
        //- netlify用のhiddenを埋め込み
        input(type="hidden" name="form-name" value="contact")
        ul.form-list
          li.form-item
            label(for="name1") Name
            input(id="name" type="text" name="name" v-model="name")
          li.form-item
            label(for="email") E-mail
            input(id="email" type="email" name="email" v-model="email")
          li.form-item
            label(for="message") Message
            textarea(id="message" type="message" v-model="message")
          li.form-item(v-show="false")
            label(for="m")
            input(type="text" name="bot-field" v-model="botField")
        button(type="submit") SEND
</template>

<script>
export default {
  data() {
    return {
      name: "",
      email: "",
      message: "",
      botField: ""
    };
  }
};
</script>

<style lang="scss" scoped>
.form-list {
  // max-width: 800px;
  .form-item {
    margin-bottom: rem(16);
    label {
      display: block;
    }
    input {
      max-width: 280px;
      width: 100%;
      @include sp {
        height: 32px;
        max-width: 100%;
      }
    }
    textarea {
      max-width: 400px;
      width: 100%;
      height: 200px;
      @include sp {
        max-width: 100%;
      }
    }
  }
}
button {
  background-color: transparent;
  border: none;
  cursor: pointer;
  outline: none;
  padding: 0;
  appearance: none;

  width: 100px;
  padding: rem(8) 0;
  font-size: rem(16);
  background-color: $c_white;
  border-radius: 4px;
  transition: 0.2s;
  &:hover {
    background: $c_black;
    color: $c_white;
  }
}
</style>
