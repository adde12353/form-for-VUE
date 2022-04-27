<template>
  <form>
    <label>Email</label>
    <input type="email" required v-model="email">
    
    <label>Password</label>
    <input type="password" required v-model="password">
    
    <label>Role</label>
    <select v-model="role">
    <option value="developer">Webdeveloper</option>
    <option value="agent">Agent</option>
    </select>

<div class="terms">
    <input v-model="checkbox" type="checkbox" required>
    <label>Accept terms and conditions</label>
</div>

  </form>
  <p>Email : {{email}}</p>
  <p>Password : {{password}}</p>
  <p>Roll : {{role}}</p>
  <p>Check : {{checkbox}}</p>
</template>

<script>
export default {
    data() {
        return {
            email: '',
            password: '',
            role: '',
            checkbox: false,
        }
    }
}
</script>

<style>
form{
    max-width: 400px;
    margin: 50px auto;
    display: flex;
    align-items: left;
    flex-direction: column;
    background-color:white;
    padding: 30px;
    border-radius: 10px;
    border: 1px solid black
}
input{
    width: 100%;
    font-size: 20px;
}
label{
    text-align: left;
    font-size: 18px;
    margin-bottom: 10px;
    opacity: 80;
}

.terms{
    display: flex;
    justify-content: start;
    margin-top: 10px;
}
.terms input{
    padding: 0;
    width: 20px;
}
</style>