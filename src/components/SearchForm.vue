<template>
    <div class="container">
        <div class="row">
            <div class="col">

                <div class="fomr-group mb-2">
                    <label for="" class="sr-only">Escribe tu búsqueda</label>
                    <input type="text" v-model="search" class="form-control">
                </div>

                <div class="form-check form-check-inline">
                    <input type="radio" v-model="available" :value="true" class="form-radio-input">
                    Disponible
                </div>

                <div class="form-check form-check-inline">
                    <input type="radio" v-model="available" :value="false" class="form-radio-input">
                    No disponible
                </div>

            </div>
        </div>
    </div>
</template>

<script>
export default {
  computed: {
    search: {
      get() {
        return this.$store.state.filter.query;
      },
      set(val) {
        //settear state y mandar valor
        this.$store.commit('SET_QUERY', val);
      }
    },
    available: {
      get() {
        return this.$store.state.filter.available;
      },
      set() {
        this.$store.commit('SET_AVAILABLE');
      }
    }
  }
};
</script>

<style scoped>
</style>