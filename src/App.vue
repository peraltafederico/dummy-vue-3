<template>
  <div>
    <user-data @set-active-user="handleSetActiveUser" />
    <active-user :username="username" :age="age" />
  </div>
</template>

<script>
export default {
  data() {
    return {
      username: "Fede",
      age: 25,
    };
  },
  methods: {
    handleSetActiveUser(user) {
      this.username = user.username;
      this.age = user.age;
    },
  },
};
</script>

<style>
body {
  font-family: sans-serif;
}

section {
  margin: 50px auto;
  padding: 25px;
  max-width: 800px;
  display: flex;
  justify-content: center;
  box-shadow: 2px 2px 5px 1px #ccc;
}

button {
  width: 100%;
  border: 0;
  background-color: rgb(138, 43, 226, 0.5);
  padding: 8px;
  cursor: pointer;
  font-size: 18px;
  font-weight: bold;
  box-shadow: 0px 0px 4px 1px grey;
}

button:hover {
  background-color: rgb(138, 43, 226);
  box-shadow: none;
}

button:focus {
  outline: none;
}

form div {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}

form label {
  font-size: 25px;
  margin: 0 auto;
}

form input {
  font-size: 25px;
  margin-left: 20px;
}

#user-info {
  display: flex;
  flex-direction: column;
  align-items: center;
}

#user-info h1 {
  margin: 0;
  font-size: 30px;
}

#user-info h2 {
  font-size: 25px;
  font-weight: normal;
  margin-bottom: 5px;
}

#user-info h3 {
  font-size: 20px;
  font-weight: normal;
  margin-bottom: 5px;
}

strong {
  color: rgb(138, 43, 226);
}
</style>