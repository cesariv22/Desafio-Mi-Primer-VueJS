<template>
  <div id="app">
    <div class="container">
      <div class="row">
        <div class="col-12">
          <h1>Tabla de Datos</h1>
        </div>
        <div>
          <div>
            <div id="app">
              <table class="table">
                <thead>
                  <tr>
                    <th scope="col">#</th>
                    <th scope="col">Nombre</th>
                    <th scope="col">Apellido</th>
                    <th scope="col">Rut</th>
                    <th scope="col">Fecha de Nacimiento</th>
                    <th scope="col">Edad</th>
                  </tr>
                </thead>
                <tbody>
                  <tr v-for="(persona, i) in personas" :key="i">
                    <td>{{ i + 1 }}</td>
                    <td>{{ persona.nombre }}</td>
                    <td>{{ persona.apellido }}</td>
                    <td>{{ persona.rut }}</td>
                    <td>{{ persona.fechaNacimiento }}</td>
                    <td>{{ persona.edad }}</td>
                  </tr>
                </tbody>
              </table>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      personas: [
        {
          nombre: "Javiera",
          apellido: "Torres",
          rut: "13.456.789.1",
          fechaNacimiento: "11-05-1992",
          edad: "29",
        },
        {
          nombre: "Cesar",
          apellido: "Riveros",
          rut: "12.345.678-0",
          fechaNacimiento: "21-09-2012",
          edad: "9",
        },
        {
          nombre: "Antonio",
          apellido: "Martínez",
          rut: "19.876.543-K",
          fechaNacimiento: "15-01-1983",
          edad: "38",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
