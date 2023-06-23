<script lang="ts">
  import { Router, Link, Route } from "svelte-routing";
  import Home from "./layout/Home.svelte";
  import Settings from "./layout/Settings.svelte";

  export let url = "/";
</script>

<svelte:head>
  <title>Home - FuserSM</title>
</svelte:head>

<Router {url}>
  <nav>
    <Link to="/">Home</Link>
    <Link to="/settings">Settings</Link>
  </nav>
  <div>
    <Route path="/"><Home /></Route>
  </div>
</Router>
<Home />
