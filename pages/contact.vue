<template lang="pug">
  .container
    // いずれここはコンポーネント化する
    section#contact
      h2.ttl Contact
      p Ask me something
      form#form(method="POST" netlify)
        ul.form-list
          li.form-item
            label(for="name1") Name
            input(id="name1" type="text" name="name1")
          li.form-item
            label(for="email") E-mail
            input(id="email" type="email" name="email")
          li.form-item
            label(for="message") Message
            textarea(id="message" type="message")
        button(type="submit") SEND
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.form-list {
  width: 800px;
  .form-item {
    margin-bottom: rem(16);
    label {
      display: block;
    }
    input {
      max-width: 280px;
      width: 100%;
    }
    textarea {
      max-width: 280px;
      width: 100%;
      height: 200px;
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
  &:hover {
  }
}
</style>
