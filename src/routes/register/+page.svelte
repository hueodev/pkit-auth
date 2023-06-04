<script>
	export let data
</script>

<div class="container">
	<div>
		<h2>Welcome to PKIT</h2>
		<p>Register an account or <a href="/login">login</a> if you already have an account.</p>
		<form method="POST" action="?/register">
			<div>
				<input type="text" name="name" placeholder="Name" required/>
			</div>
			<div>
				<input type="email" name="email" placeholder="Email" required/>
			</div>
			<div>
				<input type="password" name="password" placeholder="Password" required/>
			</div>
			<div>
				<input type="password" name="passwordConfirm" placeholder="Confirm Password" required/>
			</div>
			<div>
				<button>Register</button>
			</div>
		</form>
	</div>
</div>

<style lang="scss">
	.container {
		display: grid;
		place-items: center;
		text-align: center;
		height: 100vh;
	}

	input {
		position: relative;
		padding: .4rem;
		margin: .3rem;
		border-radius: 8px;
		height: 1.5rem;
		width: 20rem;
		background-color: #2f2f2f;
		color: #f5f5f5;
		border: 1px solid #282828;
		text-indent: .6rem;
		transition: ease-in-out all 250ms;
		&:focus {
      		outline: none;
		}
		&::placeholder {
			font-weight: 400;
			color: #838383;
			font-weight: 500;
		}
		&::-ms-reveal {
			filter: invert(100%);
		}
		&:hover {
			background-color: #3b3b3b;
		}
	}

	button {
		position: relative;
		padding: .4rem;
		margin: 1rem;
		border-radius: 8px;
		font-weight: 500;
		height: 1.4rem;
		width: 20rem;
		background-color: #0e88f1;
		border: none;
		color: #f5f5f5;
		transition: ease-in-out all 300ms;
		&:hover {
			background-color: #0a5ba2;
			cursor: pointer;
		}
	}

	p {
		position: relative;
		padding: .4rem;
		margin: 0rem auto 1rem;
		font-weight: 500;
		color: #767676;
		width: 20rem;
	}

	a {
		color: #1f5e95;
		font-weight: bold;
		text-decoration: none;
		transition: ease-in-out all 200ms;
		&:hover {
			color: #4ca9fa;
		}
	}
</style>