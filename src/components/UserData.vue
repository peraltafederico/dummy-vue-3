<template>
  <section>
    <form @submit.prevent="setActiveUser">
      <div>
        <label for="username">Username</label>
        <input v-model="username" id="username" required />
      </div>
      <div>
        <label for="age">Age</label>
        <input v-model="age" id="age" type="number" required />
      </div>
      <div>
        <button>Confirm</button>
      </div>
    </form>
  </section>
</template>

<script>
export default {
  data() {
    return {
      username: "",
      age: "",
    };
  },
  events: ["set-active-user"],
  methods: {
    setActiveUser() {
      this.$emit("set-active-user", {
        username: this.username,
        age: +this.age,
      });
    },
  },
};
</script>