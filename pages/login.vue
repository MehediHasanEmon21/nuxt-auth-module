<template>
<div class="container col-md-6 mt-5">
	<h2>Login</h2>
	<br>
	<form @submit.prevent="submit">
	  <div class="form-group">
	    <label>Email address</label>
	    <input type="email" class="form-control" v-model="form.email" aria-describedby="emailHelp" placeholder="Enter email">
	    <small class="form-text text-danger">show validate.</small>
	  </div>
	  <div class="form-group">
	    <label>Password</label>
	    <input type="password" class="form-control" v-model="form.password" placeholder="Password">
	    <small class="form-text text-danger">show validate.</small>
	  </div>
	  <button type="submit" class="btn btn-primary">Submit</button>
	</form>
	<br>
	<p>Dont't have an account? <nuxt-link to="/register">Register Here</nuxt-link></p>

</div>	


</template>

<script>
	
	export default {
		middleware: 'guest',
		data(){
			return {
				form: {
					email: 'emon@gmail.com',
					password: '12345678',
				}
			}
		},
		methods:{
			async submit(){
				await this.$auth.loginWith('local', { data: this.form });
				this.$router.push({ path: '/' });
			}
		}
	}

</script>