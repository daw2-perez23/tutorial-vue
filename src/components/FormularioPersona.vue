<template>
  <div id="formulario-persona" @add-persona="agregarPersona">
    <form @submit.prevent="enviarFormulario">
      <div class="container">
        <div class="row">
          <div class="col-md-4">
            <div class="form-group">
              <label>Nombre</label>
              <input type="text" class="form-control" />
            </div>
          </div>
          <div class="col-md-4">
            <div class="form-group">
              <label>Apellido</label>
              <input type="text" class="form-control" />
            </div>
          </div>
          <div class="col-md-4">
            <div class="form-group">
              <label>Email</label>
              <input type="email" class="form-control" />
            </div>
          </div>
        </div>
        <div class="row">
          <div class="col-md-4">
            <div class="form-group">
              <button class="btn btn-primary">Añadir persona</button>
            </div>
          </div>
        </div>
      </div>
    </form>
  </div>
</template>

<script>
  export default {
    name: 'formulario-persona',
    data() {
      return {
        persona: {
          nombre: '',
          persona: '',
          apellido: '',
        },
      }
    },
    methods: {
    enviarFormulario() {
      this.$emit('add-persona', this.persona);
    },
  },
}

</script>

<style scoped>
  form {
    margin-bottom: 2rem;
  }
</style>