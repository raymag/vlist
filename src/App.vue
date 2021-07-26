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
          <button>x</button>
        </article>
        <article>
          <span>Clear Room</span>
          <button>x</button>
        </article>
        <article>
          <span>Clear Room</span>
          <button>x</button>
        </article>
        <article>
          <span>Clear Room</span>
          <button>x</button>
        </article>
        <article>
          <span>Clear Room</span>
          <button>x</button>
        </article>
      </section>

    <span id="deleteAll">Apagar Tudo</span>
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
  background: #fafafa;
  min-width: 60%;
}
#header {
  width: 100%;
  background: rgb(36, 246, 211);
  margin-bottom: 30px;
  color: #fff;
  text-transform: uppercase;
  letter-spacing: 2px;
  font-weight: bold;
}

section {
  width: 100%; 
  padding: 20px;
}
input {
  width: 90%;
  font-size: 1.6em;
  outline: none;
  border: none;
  border-bottom: 3px solid #ccc;
  background: #fff;
  padding: 10px;
}
input:focus {
  border-color: rgb(29, 165, 142);
}
article {
  margin: auto;
  width: 90%;
  margin: 20px auto;
  margin-bottom: 0;
  border: solid 1px #ddd;
  border-radius: 3px;
  padding: 10px;
  background: #fff;
  display: flex;
  align-self: center;
  justify-content: space-between;
  font-size: 1.2em;
}
article button {
  border: none;
  background: none;
  font-weight: bold;
  font-size: 1.2em;
  color: rgb(165, 29, 29);
  cursor: pointer;
}
article button:hover {
  color: rgb(246, 36, 36);
}
article button:active {
  transform: translate(0, 2px);
}
article span {
  align-self: center;
}

#deleteAll {
  text-decoration: underline;
  color: rgba(69, 134, 123, 0.835);
  cursor: pointer;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: end;
  margin-right: 60px;
  margin-bottom: 30px;
}

</style>
