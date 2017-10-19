<template>
	<div class="card text-white bg-dark">
		<div class="card-header">
			<div class="text-left">
				<h2>Login</h2>	
			</div>
		</div>
		<div class="card-body">
			<div class="form-group">
				<div class="text-left">
					<label class="pull-left">Email</label>
				</div>
				<input class="form-control" type="email" name="email" v-model="email">
			</div>

			<div class="form-group">
				<div class="text-left">
					<label class="pull-left">Password</label>
				</div>
				<input class="form-control" type="password" name="password" v-model="password">
			</div>
			<button class="btn btn-primary btn-block" @click="login">Login</button>
		</div>
	</div>
</template>

<script>
	export default {
		data () {
			return {
				email: '',
				password: ''
			}
		},

		methods: {
			login() {
				var data = {
					client_id: 2,
					client_secret: '5u3SUju4G3pcXV55tJBZfpnQIYpqvVfA0SWOHRAa',
					grant_type: 'password',
					username: this.email,
					password: this.password
				}
				this.$http.post('http://localhost:8000/oauth/token', data)
					.then(function (response){
						console.log(response)
					})	
			}
		}
	}
</script>

<style>
	
</style>