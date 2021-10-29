<script>
	import { page } from '$app/stores';
</script>

<header>
    
    <nav>
        <ul>
            <li class:active={$page.path === '/'}><a href="/">Home</a></li>
            <li class:active={$page.path === '/cookbook'}><a href="/cookbook">Cookbook</a></li>
        </ul>
    </nav>
   
</header>

<style>

	nav {
		display: flex;
		/* justify-content: center; */
		background-color: rgb(245, 241, 241);
        margin: 0;
        border: 0;
	}

	ul {
		position: relative;
		padding: 0;
		margin: 0;
		height: 1.5em;
		display: flex;
		justify-content: center;
		align-items: center;
		list-style: none;
		background: var(--background);
		background-size: contain;
	}

	li {
		position: relative;
		height: 100%;
        color:darkblue;
	}

    li.active {
        color:chocolate;
    }

    /* li.active::before {
        content: '*';
    } */
        

    nav a {
		display: flex;
		height: 100%;
		align-items: center;
		padding: 0 1em;
		color: var(--heading-color);
		font-weight: 700;
		font-size: 1.0rem;
		text-transform: uppercase;
		letter-spacing: 0.1em;
		text-decoration: none;
		transition: color 0.2s linear;
	}

	a:hover {
		color: var(--accent-color);
	}

</style>