<script>
import { goto } from '$app/navigation';
import { onMount } from 'svelte';

export let data;
let response = "";

if (!data.user) {
  onMount(() => goto("/login"));
} else {
  response = JSON.stringify(data.user.name, null, 2).replace(/^"(.*)"$/, '$1');
}
</script>

{#if data.user}
<nav class="container">
    <ul>
      <li>
        <h1>Hello {response} you are logged in!</h1>
      </li>
      <li>
        <form action="/logout" method="POST">
          <button type="submit">Logout</button>
        </form>
      </li>
    </ul>
</nav>
{/if}

<style lang="scss">
  .container {
		display: grid;
		place-items: center;
		text-align: center;
		height: 100vh;
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

	h1 {
		position: relative;
		padding: .4rem;
		margin: 0rem auto 1rem;
		font-weight: 500;
		color: #f5f5f5;
		width: max-content;
	}

  ul, li {
    list-style: none;
  }
</style>