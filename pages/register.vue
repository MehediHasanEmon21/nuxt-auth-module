<template>
<div class="container col-md-6 mt-5">
	<h2>Login</h2>
	<br>
	<form>
	  <div class="form-group">
	    <label>Full Name</label>
	    <input type="text" class="form-control" placeholder="Enter name">
	    <small class="form-text text-danger">show validate.</small>
	  </div>
	  <div class="form-group">
	    <label>Email address</label>
	    <input type="email" class="form-control" placeholder="Enter email">
	    <small class="form-text text-danger">show validate.</small>
	  </div>
	  <div class="form-group">
	    <label>Password</label>
	    <input type="password" class="form-control" placeholder="Password">
	    <small class="form-text text-danger">show validate.</small>
	  </div>
	  <button type="submit" class="btn btn-primary">Submit</button>
	</form>
	<br>
	<p>Already have an account? <nuxt-link to="/login">Login Here</nuxt-link></p>

</div>	


</template>

<script>
	
	export default {
		auth: 'guest'
	}

</script>