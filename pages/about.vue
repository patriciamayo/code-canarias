<template>
  <div class="container">
    <h1>¿Qué queremos conseguir?</h1>
    <p>
      Queremos tener un lugar para mostrar el potencial de los canarios en
      tecnología y aumentar el empleo en las islas.
      <span style="color: rgb(0, 245, 233)"><strong>Code</strong>Canarias</span>
      es el sitio para encontrar personas excepcionales a las que seguir, buscar
      un mentor o descubrir personas con talento a las que contratar.
    </p>
    <h1>Si quieres formar parte de esta comunidad</h1>
    <p>
      ¡Es muy fácil! Si eres de las Islas Canarias y te dedicas al campo de la
      informática y el desarrollo, puedes añadir tu perfil para que aparezca en
      nuestra lista de "coders". Te explicamos como hacerlo 👇
    </p>
    <vs-button
      relief
      href="https://github.com/patriciamayo/code-canarias"
      class="cta"
    >
      Apúntate
    </vs-button>
    <p>
      Si eres una empresa y te gustaría aparecer en nuestra lista de
      Patrocinadores mándanos un email. No solo serás incluido en la lista, sino
      que también aparecerás en la página principal de manera aleatoria
    </p>
    <vs-button relief class="cta"> Contáctanos </vs-button>
  </div>
</template>

<script>
export default {}
</script>

<style scoped>
h1 {
  font-size: 36px;
  padding: 16px;
}

p {
  font-size: 18px;
  padding: 16px;
}

.cta {
  margin: 16px;
}

.container {
  max-width: 800px;
  margin: auto;
  padding: 128px 32px;
}

div {
  color: white !important;
}
</style>
