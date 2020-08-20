<template>
  <div class = "auto">
    <div class="container-xl" id="aa">
      <img src="pic/IMG_5721.JPG" class="design" />
      <hr />
      <div class="row">
        <div class="col-md">
          <button v-on:click="$ok" class="btn btn-info" id="indigo">
            <i class="fas fa-check"></i>
          </button>
        </div>

        <div class="col-md">
          <button v-on:click="$like" class="btn btn-info" id="indigo">
            <i class="fas fa-thumbs-up"></i>
          </button>
        </div>

        <div class="col-md">
          <button v-on:click="$love" class="btn btn-info" id="indigo">
            <i class="fas fa-heart"></i>
          </button>
        </div>

        <div class="col-md">
          <button v-on:click="$eiei" class="btn btn-info" id="indigo">
            <i class="fas fa-laugh-beam"></i>
          </button>
        </div>

        <div class="col-md">
          <button v-on:click="$reset" class="btn btn-info" id="indigo">
            <i class="fas fa-trash-restore-alt"></i>
          </button>
        </div>
      </div>

      <hr />

      <p>จำนวนผู้เยี่ยมชม {{ok+like+love+eiei}} คน</p>
      <p>จำนวนคะแนนที่มีผู้มากดทั้งหมด {{total}}</p>
      <br>
    </div>

    <br><br>
    
    <div class="container-xl" id="bb">
      <img src="pic\IMG_1394.JPG" class="design" />
      <hr />
      <div class="row">
        <div class="col-md">
          <button v-on:click="$ok1" class="btn btn-info" id="indigo">
            <i class="fas fa-check"></i>
          </button>
        </div>

        <div class="col-md">
          <button v-on:click="$like1" class="btn btn-info" id="indigo">
            <i class="fas fa-thumbs-up"></i>
          </button>
        </div>

        <div class="col-md">
          <button v-on:click="$love1" class="btn btn-info" id="indigo">
            <i class="fas fa-heart"></i>
          </button>
        </div>

        <div class="col-md">
          <button v-on:click="$eiei1" class="btn btn-info" id="indigo">
            <i class="fas fa-laugh-beam"></i>
          </button>
        </div>

        <div class="col-md">
          <button v-on:click="$reset1" class="btn btn-info" id="indigo">
            <i class="fas fa-trash-restore-alt"></i>
          </button>
        </div>
      </div>

      <br>
      <p>จำนวนผู้เยี่ยมชม {{ok1+like1+love1+eiei1}} คน</p>
      <p>จำนวนคะแนนที่มีผู้มากดทั้งหมด {{total1}}</p>
    <br>
    </div>

    <br>
  </div>
</template>

  

<script>
export default {
  data: function () {
    return {
      counter: 0,
      fsize: 1,
      ok: 0,
      like: 0,
      love: 0,
      eiei: 0,
      score: 0,
      total: 0,

      counter1: 0,
      ok1: 0,
      like1: 0,
      love1: 0,
      eiei1: 0,
      score1: 0,
      total1: 0,
    };
  },

  props: {
    lable: String,
  },

  methods: {
    $ok: function () {
      this.total = this.total + 1;
      this.counter = 1;
      this.ok = this.ok + 1;
      this.$emit("cc", this.counter);
      console.log("counter=" + this.counter);
    },

    $like: function () {
      this.total = this.total + 2;
      this.counter = 2;
      this.like = this.like + 1;
      this.$emit("cc", this.counter);
      console.log("counter=" + this.counter);
    },

    $love: function () {
      this.total = this.total + 3;
      this.counter = 3;
      this.love = this.love + 1;
      this.$emit("cc", this.counter);
      console.log("counter=" + this.counter);
    },

    $eiei: function () {
      this.total = this.total + 4;
      this.counter = 4;
      this.eiei = this.eiei + 1;
      this.$emit("cc", this.counter);
      console.log("counter=" + this.counter);
    },

    $reset: function () {
      this.counter = 0;
      this.ok = 0;
      this.like = 0;
      this.love = 0;
      this.eiei = 0;
      this.total = 0;
      console.log("counter=" + this.counter);
    },







    $ok1: function () {
      this.total1 = this.total1 + 1;
      this.counter1 = 1;
      this.ok1 = this.ok1 + 1;
      this.$emit("cc", this.counter1);
      console.log("counter=" + this.counter1);
    },

    $like1: function () {
      this.total1 = this.total1 + 2;
      this.counter1 = 2;
      this.like1 = this.like1 + 1;
      this.$emit("cc", this.counter1);
      console.log("counter=" + this.counter1);
    },

    $love1: function () {
      this.total1 = this.total1 + 3;
      this.counter1 = 3;
      this.love1 = this.love1 + 1;
      this.$emit("cc", this.counter1);
      console.log("counter=" + this.counter1);
    },

    $eiei1: function () {
      this.total1 = this.total1 + 4;
      this.counter1 = 4;
      this.eiei1 = this.eiei1 + 1;
      this.$emit("cc", this.counter1);
      console.log("counter=" + this.counter1);
    },

    $reset1: function () {
      this.counter1 = 0;
      this.ok1 = 0;
      this.like1 = 0;
      this.love1 = 0;
      this.eiei1 = 0;
      this.total1 = 0;
      console.log("counter=" + this.counter1);
    },


    //downFunction: function (){
    //this.counter-=1
    //this.fsize-=1

    //console.log('fsize='-this.fsize);
    //console.log('counter='-this.counter);
    //},
  },
};
</script>

<style>
#aa {
  background-image: url(/pic/Purple_gaussian_blur_backgrounds_2560x1600.jpg);
  color: white;
  margin: center;
  width: 65%;
  background-color: whitesmoke;
}

.design {
  border-radius: 30px;
  margin-top: 25px;
  width: 30%;
}

#bb {
  background-image: url(/pic/purple_planet_space_nebula_stars_art_1920x1080.jpg);
  color: white;
  margin: center;
  width: 65%;
  background-color: whitesmoke;
}

#auto{
  font-style:inherit;
}
</style>