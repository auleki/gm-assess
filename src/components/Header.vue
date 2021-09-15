<script>
export default {
  name: "Header",
};
</script>

<template>
  <header>
    <div class="text">
      <h2>STAR WARS DIRECTORY</h2>
      <p>Find your favorite characters, films, species, starships, planets</p>
    </div>
    <section class="search__bar">
      <button type="submit">ICON</button>
      <input type="text" placeholder="Enter a search term" />
    </section>
  </header>
</template>

<style scoped lang="scss">
header {
  height: 200px * 2;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  background: #2163f1;
}

.search__bar {
  margin-top: 16px;
  background: #fff;
  padding: 6px;
  display: flex;
  gap: 0.5em;
  border-radius: 4px;
  input {
    padding: 16px;
    width: 100%;
    border: 2px dashed transparent;
    transition: border 200ms ease-in;
    outline: none;
    &:focus {
      border-color: crimson;
    }
  }
  button {
    color: crimson;
    background: transparent;
  }
}

@media (min-width: 578px) {
  .search__bar {
    width: 100px * 5;
  }
}
</style>