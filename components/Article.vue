<template>
  <div class="box content p-5 m-4">
    <span class="tag is-danger">
      New!
    </span>
    <h1 class="title is-5">
      {{ title }}
    </h1>
    <p>
      {{ content }}
    </p>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      default: ''
    },
    content: {
      type: String,
      default: ''
    }
  }
}
</script>
