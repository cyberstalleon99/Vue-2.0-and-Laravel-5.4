<template>
	<div class="card text-white bg-dark">
		<div class="card-header">
			<div class="text-left">
				<h2>Register</h2>	
			</div>
		</div>
		<div class="card-body">
			<div class="form-group">
				<div class="text-left">
					<label class="pull-left">Fullname</label>
				</div>
				<input class="form-control" type="text" name="fullname" v-model="fullname">
			</div>
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
			<button class="btn btn-primary btn-block">Register</button>
		</div>
	</div>
</template>

<script>
	export default {
		data () {
			return {
				fullname: '',
				email: '',
				password: ''
			}
		}
	}
</script>

<style>
	
</style>