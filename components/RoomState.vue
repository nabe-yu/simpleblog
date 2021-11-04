<template>
  <section>
    <div class="circle">
      <b-field>
        <b-switch v-model="inputedValue" type="is-success" size="is-large" />
      </b-field>
      <p v-if="inUse">
        使用中
      </p>
      <p v-else>
        空室
      </p>
    </div>
  </section>
</template>

<script>
export default {
  model: {
    prop: 'inUse',
    event: 'change'
  },
  props: {
    inUse: {
      type: Boolean,
      required: true
    }
  },
  computed: {
    inputedValue: {
      get() {
        return this.inUse
      },
      set(newValue) {
        this.$emit('change', newValue)
      }
    }
  },
  methods: {}
}
</script>

<style scoped lang="css">
.circle{
  width: 40%;
  aspect-ratio: 1 / 1;
  border-radius: 50%;
  background-color: rgb(155, 235, 140);
}
</style>
