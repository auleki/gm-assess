<script>
export default {
  name: "ShipCard",
  data() {
    return {
      imageLink:
        "https://res.cloudinary.com/dyj6pqx6d/image/upload/v1629469831/starship-3_owmz27.jpg",
    };
  },
};
</script>

<template>
  <section>
    <img :src="this.imageLink" alt="" />
    <div class="ship__details">
      <h3>Ship Card</h3>
      <p>
        Loronar E-9 Explorer was a transport used by the Rebel Alliance during
        its fight against the Galactic Empire during the Galactic Civil War.
      </p>
      <div class="actions">
        <button class="button">
          <span class="text">Learn More</span>
          <!-- <span class="icon"></span> -->
        </button>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
section {
  background: #d8d8d8;
  display: flex;
  flex-direction: column;
  width: 360px;
  .actions {
    display: flex;
    margin: 16px 0;
    justify-content: flex-end;
    button {
      display: inline-flex;
    }
  }
  img {
    height: 250px;
    width: 360px;
  }
  .ship__details {
    padding: 1em;
    transition: all 200ms ease-in-out;
    transform: scaleY(0.95) translateX(0.5em) translateY(-0.2em);
    background: #f2f2f2;
    p {
      line-height: 21px;
    }
  }

  &:hover {
    /* .ship__details {
      transform: none;
    } */
  }
}
</style>