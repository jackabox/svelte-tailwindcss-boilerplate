<script>
	import { Router, Route } from "svelte-routing";
  import NavLink from "./components/NavLink.svelte";

	import Home from "./routes/Home.svelte";
  import Blog from "./routes/Blog.svelte";

  export let url = "";
  export let siteName;
</script>

<Router url="{url}">
	<header>
		<h1>{ siteName }</h1>

	  <nav>
	    <NavLink to="/">Home</NavLink>
	    <NavLink to="blog">Blog</NavLink>
	  </nav>
	</header>
  <main>
    <Route path="/" component="{Home}" />
    <Route path="blog/*" component="{Blog}" />
  </main>
</Router>

<style global>
  @tailwind base;
  @tailwind components;
  @tailwind utilities;
</style>
