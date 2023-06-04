<script>
	export let form;
</script>

<div class="container">
    <div>
        <h2>Reset Your Password</h2>
        <p>We'll send you an email with a link to reset your password.</p>
        <form action="?/resetPassword" method="POST">
            <div>
                <input type="email" name="email" placeholder="Email"/>
            </div>
            <div>
                <button type="submit">Request Password Reset</button>
            </div>
            {#if form?.success}
                <div class="noti">
                    <span>An email has been sent to reset your password!</span>
                </div>
            {/if}
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