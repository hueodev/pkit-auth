<script>
	export let form
</script>

<div class="container">
	<div>
		<h2>Welcome to PKIT</h2>
		<p>Sign in to your account or <a class="redirect" href="/register">register</a> if you don't already have an account.</p>
		<form method="POST" action="?/login">
			<div>
				<input type="email" name="email" placeholder="Email" />
			</div>
			<div>
				<input class="password" type="password" name="password" placeholder="Password" />
			</div>
				<span class="reset"><a href="/reset-password">Forgot Password?</a></span>
			<div>
				<button>Login</button>
			</div>
		</form>
		{#if form?.notVerified}
		<div class="noti">
			<span>You must verify your email before you can login!</span>
		</div>
		{/if}
	</div>
</div>

<style lang="scss">
	.container {
		display: grid;
		justify-content: center;
		align-items: center;
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

	.password {
		margin-bottom: .6rem;
	}

	button {
		position: relative;
		padding: .4rem;
		margin: .8rem;
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

	.redirect {
		color: #1f5e95;
		font-weight: bold;
		text-decoration: none;
		transition: ease-in-out all 200ms;
		&:hover {
			color: #4ca9fa;
		}
	}

	span a {
		text-align: center;
		font-size: .9rem;
		font-weight: 500;
		text-decoration: none;
		color: #1666ab;
		transition: ease-in-out all 200ms;
		&:hover {
			color: #4ca9fa;
		}
	}

	.noti {
		position: absolute;
		margin: auto;
		bottom: 16rem;
		background: rgba(47, 47, 47, 0.501);
		padding: .8rem;
		border-radius: .6rem;
		font-size: .9rem;
	}
</style>