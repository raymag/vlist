<template>
  <div id="app">
    <main>
      <div id="header">
        <h1>VList</h1>
      </div>
      <input type="text" placeholder="Task" />
      <section>
        <article>
          <span>Clear Room</span>
          <button>Delete</button>
        </article>
        <article>
          <span>Clear Room</span>
          <button>Delete</button>
        </article>
        <article>
          <span>Clear Room</span>
          <button>Delete</button>
        </article>
        <article>
          <span>Clear Room</span>
          <button>Delete</button>
        </article>
        <article>
          <span>Clear Room</span>
          <button>Delete</button>
        </article>
      </section>
    </main>
  </div>
</template>

<script>
export default {
  name: 'App',
  components: {
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  width: 100%;
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  background: #222;
}
html, body {
  padding: 0;
  margin: 0;
}

main {
  border: 1px solid #ccc;
  border-radius: 3px;
  display: flex;
  align-items: center;
  justify-content: flex-start;
  flex-direction: column;
  background: #fff;
  min-width: 60%;
}
#header {
  width: 100%;
  background: rgb(36, 246, 211);
  margin-bottom: 30px;
  color: #fff;
  text-transform: uppercase;
  letter-spacing: 2px;
}

section {
  /* width: 100%; */
  padding: 10px 20px;
}
input {
  width: 90%;
  font-size: 1.5em;
}
article {
  width: 90%;
  border: solid 1px #ddd;
}

</style>
