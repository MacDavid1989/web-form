<template>
  <form action="">
    <label for="">Email:</label>
    <input type="email" required v-model="email" />

    <label for="">Password:</label>
    <input type="password" required v-model="password" />

    <label for="">Role:</label>
    <select name="" id="" v-model="role">
      <option value="developer">Web Developer</option>
      <option value="designer">Web Designer</option>
    </select>

    <div class="terms">
      <input type="checkbox" required v-model="terms" />
      <label for="">Accpet Terms and Conditions</label>
    </div>

    <div>
      <input type="checkbox" value="shaun" v-model="names" />
      <label for="">Shaun</label>
    </div>
    <div>
      <input type="checkbox" value="dave" v-model="names" />
      <label for="">Dave</label>
    </div>
    <div>
      <input type="checkbox" value="yoshi" v-model="names" />
      <label for="">Yoshi</label>
    </div>
  </form>
  <p>Email: {{ email }}</p>
  <p>Password: {{ password }}</p>
  <p>Role: {{ role }}</p>
  <p>Terms: {{ terms }}</p>
  <p>Names: {{ names }}</p>
</template>

<script>
export default {
  name: "SignupForm",
  data() {
    return {
      email: "",
      password: "",
      role: "",
      terms: false,
      names: [],
    };
  },
};
</script>

<style scoped>
form {
  max-width: 420px;
  margin: 20px auto;
  background: white;
  text-align: left;
  padding: 40px;
  border-radius: 10px;
}
label {
  color: #aaa;
  display: inline-block;
  margin: 25px 0 15px;
  font-size: 0.6em;
  text-transform: uppercase;
  letter-spacing: 1px;
  font-weight: bold;
}
input,
select {
  display: block;
  padding: 10px 5px;
  width: 100%;
  box-sizing: border-box;
  border: none;
  border-bottom: 1px solid #ddd;
  color: #555;
}
input[type="checkbox"] {
  display: inline-block;
  width: 16px;
  margin: 0 10px 0 0;
  position: relative;
  top: 2px;
}
</style>
