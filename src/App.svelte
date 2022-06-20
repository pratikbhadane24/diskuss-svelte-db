<script>
  import TopWaves from "./components/TopWaves.svelte";
  import Navbar from "./components/Navbar.svelte";
  import Aside from "./components/Aside.svelte";
  import NewDiss from "./components/NewDiss.svelte";
  import AllDiss from "./components/AllDiss.svelte";
</script>

<div id="app-container" class="app-container">
  <TopWaves />
  <Navbar />
  <section>
    <div class="container">
      <main>
        <NewDiss />
        <AllDiss />
      </main>

      <Aside />
    </div>
  </section>
</div>

<style>
  .container {
    max-width: 1000px;
    margin: 0 auto;
  }

  section .container {
    display: flex;
    flex-direction: row;
  }

  section .container main {
    flex-grow: 3;
    flex-basis: 600px;
    margin-left: 20px;
  }

  
</style>
