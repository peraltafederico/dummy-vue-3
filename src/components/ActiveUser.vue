<template>
  <section id="user-info">
    <h1>Active User Information</h1>
    <div>
      <h2>
        Username: <strong> {{ username }} </strong>
      </h2>
      <h3>
        Age: <strong> {{ age }} </strong>
      </h3>
    </div>
  </section>
</template>

<script>
export default {
  props: {
    username: {
      type: String,
      required: true,
    },
    age: {
      type: Number,
      required: true,
    },
  },
};
</script>