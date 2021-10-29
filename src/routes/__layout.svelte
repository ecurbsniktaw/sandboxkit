<script>
	import Header from '$lib/header/Header.svelte';
	import '../app.css';
    import { page, session } from '$app/stores';
    import { amp, browser, dev, mode, prerendering } from '$app/env';
</script>

<Header />

<main>
	<slot />
</main>

<footer>
    <p>-- the page footer  --</p>
    
    <h3>page object from $app/stores</h3>
    page.host [{$page.host}]<br>
    page.path [{$page.path}]<br>
    page.params [{$page.params}]<br>
    page.query [{$page.query}]<br>

    <br><br>
    <h3>session object from $app/stores</h3>
    session [{$session}]
    <br><br>

    <h3>stuff from $app/env</h3>
    amp [{amp}]<br>
    browser [{browser}]<br>
    dev [{dev}]<br>
    mode [{mode}]<br>
    prerendering [{prerendering}]<br>

</footer>

<style>
    h3 {
        margin: 0;
    }
</style>