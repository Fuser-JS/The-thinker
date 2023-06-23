<script lang="ts">
  import { Router, Route } from "svelte-routing";
  import Home from "./layout/Home.svelte";
  import Settings from "./layout/Settings.svelte";
  import Navbar from "./components/Navbar.svelte";

  export let url = "/";
</script>

<svelte:head>
  <title>Home - FuserSM</title>
</svelte:head>

<Router {url}>
  <Navbar />
  <div>
    <Route path="/settings"><Settings /></Route>
    <Route path="/"><Home /></Route>
  </div>
</Router>
