<template>
  <div
    class="main-content"
    :class="{
      yellow: yellowmode,
      white: whiteMode,
      pink: pinkMode,
      default: defaultMode,
    }"
  >
    <div class="side-one">
      <div class="links">
        <ul>
          <li>Home</li>
          <li>About</li>
          <li>Sports</li>
          <li>Contact</li>
        </ul>
      </div>
      <div class="content">
        <img src="../assets/skate.png" alt="" />
        <h1>
          SPEEDY <br />
          QUADS
        </h1>
      </div>
    </div>
    <div class="side-two">
      <h1>CHICAGO SKATES Men's</h1>
      <h6>Premium Black Quad Rink Skates</h6>
      <h3>$103.77</h3>
      <p>
        The Chicago Rink Skate features a controlled high top for optimum safety
        as well as high quality laces for maximum protection, leaving your foot
        comfortable and secure. The urethane wheels hold up well against the
        normal wear and tear of skating, provide traction and control, and the
        semi-precision bearings keep you rolling smooth and fast. This iconic
        Rink Skate from Chicago is strategically designed for gliding and is
        also a popular choice for all-around rink and social skating for
        decades.
      </p>
      <div class="color">
        <h2>Select Color :</h2>
        <div class="color-panel">
          <div
            class="div-1"
            @click="
              (defaultMode = !defaultMode),
                (yellowmode = false),
                (whiteMode = false),
                (pinkMode = false)
            "
          >
            .
          </div>
          <div
            class="div-2"
            @click="
              (pinkMode = !pinkMode),
                (yellowmode = false),
                (whiteMode = false),
                (defaultMode = false)
            "
          >
            .
          </div>
          <div
            class="div-3"
            @click="
              (yellowmode = !yellowmode),
                (pinkMode = false),
                (defaultMode = false),
                (whiteMode = false)
            "
          >
            .
          </div>
          <div
            class="div-4"
            @click="
              (whiteMode = !whiteMode),
                (yellowmode = false),
                (pinkMode = false),
                (defaultMode = false)
            "
          >
            .
          </div>
        </div>
      </div>
      <div class="size-section">
        <h4>Select Size :</h4>
        <div class="select-option">
          <div class="select">
            <select id="standard-select">
              <option value="Option 1">Size 40</option>
              <option value="Option 2">Size 42</option>
              <option value="Option 3">Size 45</option>
            </select>
          </div>
        </div>
      </div>
      <button>Buy Now</button>
    </div>
    <div class="footer">
      <hr />

      <img src="../assets/tyrell.png" alt="" />
      <h5>Website Designed by team tyrell</h5>
    </div>
  </div>
</template>

<script>
export default {
  data: () => {
    return {
      defaultMode: false,
      yellowmode: false,
      whiteMode: false,
      pinkMode: false,
    };
  },
};
</script>

<style scoped>
.main-content {
  color: #ffffff;
  background: #047fa9;
  padding: 3rem !important;
  display: grid;
  grid-template-columns: 2fr 2fr;
}
.default {
  color: #ffffff;
  background: #047fa9;
  padding: 3rem !important;
  display: grid;
  grid-template-columns: 2fr 2fr;
}
.yellow {
  color: #000000;
  background: yellow;
  padding: 3rem !important;
  display: grid;
  grid-template-columns: 2fr 2fr;
}
.white {
  color: #000000;
  background: white;
  padding: 3rem !important;
  display: grid;
  grid-template-columns: 2fr 2fr;
}
.pink {
  color: #000000;
  background: #c155a1;
  padding: 3rem !important;
  display: grid;
  grid-template-columns: 2fr 2fr;
}
.side-one {
  padding: 2rem;
}
.content {
  padding: 1rem;
}
.links ul {
  padding: 1rem;
  display: flex;
  justify-content: space-around;
  list-style: none;
}
.links ul li {
  list-style: none;
}
.content {
  display: grid;
  padding: 4rem !important;
  place-items: center;
}
.content img {
  width: 340px;
  display: inline-block;
  position: relative;
}
.content h1 {
  position: absolute;
  top: 26rem;
  left: 15rem;
  font-size: 4rem;
  font-weight: 200;
}
.side-two {
  padding: 1.5rem !important;
  line-height: 1.8;
}
.side-two p {
  line-height: 1.6;
  margin-top: 1rem !important;
}
.color {
  display: flex;
  margin-top: 1rem !important;
}
.color-panel {
  display: flex;
  width: 200px;
  justify-content: space-around;
}
.div-1,
.div-2,
.div-3,
.div-4 {
  width: 2.7rem;
  border: 2px solid white;
  border-radius: 50%;
}
.div-1 {
  background: #047fa9;
}
.div-2 {
  background: #c155a1;
}
.div-3 {
  background: yellow;
}
.div-4 {
  background: white;
}
.div-1:hover {
  background: #099dce;
}
.div-2:hover {
  background: #c70c8f;
}
.div-3:hover {
  background: rgb(158, 158, 5);
}
.div-4:hover {
  background: rgb(221, 214, 214);
}
select {
  cursor: pointer;
  display: inline-block;
  position: relative;
  font-size: 16px;
  border: 2px solid white;
  width: 220px;
  height: 25px;
  margin-left: 0.5rem !important;
}
.size-section {
  display: flex;
  margin-top: 1rem !important;
}
button {
  background: #c155a1;
  border: none;
  margin-top: 1rem !important;
  color: white;
  padding: 15px 32px !important;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 16px;
  transition: 0.5s ease-in-out;
}
button:hover {
  background: #e07cc2;
}
.footer {
  display: none;
}

@media (max-width: 600px) {
  .main-content {
    display: flex;
    flex-direction: column;
    background: #047fa9;
  }
  .side-one {
    padding: 0.1rem !important;
  }
  .links ul {
    display: flex;
    padding: 0 !important;
  }
  .content {
    padding: 2.55rem !important;
  }
  .content img {
    width: 300px;
    display: block;
    position: relative;
  }
  .content h1 {
    position: absolute;
    top: 22rem;
    left: 6rem;
    font-size: 3.6rem;
    font-weight: 200;
  }
  .side-two {
    padding: 1rem !important;
    font-size: 14px;
  }
  .footer {
    display: block;
    text-align: center;
  }
  .footer hr {
    margin-bottom: 1rem !important;
  }
  .footer img {
    width: 100px;
  }
}
</style>
