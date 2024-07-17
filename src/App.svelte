<script lang="ts">
  import { Router, Route } from "svelte-routing";
  import { AppBar, SoftwareKey } from "./components";
  import { Home, Room } from "./routes";
  import { onMount } from "svelte";
  import { Localization } from "./utils/localization";

  export let localization = new Localization("en-US", "langs");
  export let appBar = null;
  export let softwareKey = null;

  export const getAppProp = () => {
    return { appBar, softwareKey, localization };
  };

  onMount(() => {
    // console.log('onMount', 'App');
  });
</script>

<Router>
  <div id="kai-status-bar"></div>
  <AppBar bind:this={appBar} />
  <main>
    <Route primary={false} path="index.html">
      <svelte:component this={Home} {getAppProp} />
    </Route>
    <Route primary={false} path="/">
      <svelte:component this={Home} {getAppProp} />
    </Route>
    <Route primary={false} path="room">
      <svelte:component this={Room} {getAppProp} />
    </Route>
  </main>
  <SoftwareKey bind:this={softwareKey} />
</Router>

<style>
  #kai-status-bar {
    height: 26px;
    width: 100%;
    background-color: var(--themeColor);
  }
  main {
    display: flex;
    top: 54px;
    margin: 0px;
    padding: 0px;
    position: fixed;
    text-align: center;
    width: 100%;
    height: calc(100% - 84px);
    overflow: scroll;
  }
  :global(._toastItem) {
    text-align: center !important;
  }
</style>
