<script>
	import { Router, Route, Link } from "svelte-routing";
	import Home from "./pages/Home.svelte";
	import About from "./pages/About.svelte";

	export let url = "";
</script>

<Router {url}>
	<nav>
		<Link to="/">Home</Link>
		<Link to="about">About</Link>
	</nav>

	<div>
		<Route path="/"><Home /></Route>
		<Route path="about" component={About} />
	</div>
</Router>
