<template>
  <div class="contianer">
    <div class="about">
      <div id="conphot">
        <img id="photo" :src="st + '/' + this.move.poster_path" />
        <div id="nam">
          <h4 style="display: flex; flex-flow: row, wrap; width: fit-content">
            {{ this.move.original_name }}
          </h4>
          <span class="fa fa-star checked"></span> {{ this.move.vote_average }}
        </div>
      </div>

      <hr id="hr1" />

      <div id="discrption">
        <h2>
          : تدور الاحدث حول
          <img style="width: 30px" src="../assets/quotation.png" />
        </h2>
        <p>{{ this.move.overview }}</p>
      </div>
      <div class="row" id="filminform">
        <div class="col-lg-6 col-md-4">
          <h2 id="informheader">
            : تفاصيل
            <img style="width: 30px" src="../assets/quotation.png" />
          </h2>
          <div class="col-lg-6 col-md-6">
            <ul id="listprant">
              <li>
                <span><h4>الاسم</h4></span>
                <h5>
                  {{ this.move.original_name }}
                </h5>
              </li>
              <hr />
              <li>
                <span><h4>الحلقات</h4></span>
                <h5>
                  {{ this.move.number_of_episodes }}
                </h5>
              </li>
              <hr />
              <li>
                <span><h4>الموسم</h4></span>
                <h5>{{ this.move.number_of_seasons }}</h5>
              </li>
              <hr />
              <li>
                <span><h4>الفئه</h4></span>
                <h5 v-for="(type, i) in this.move.genres" :key="i">
                  {{ type.name }}|
                </h5>
              </li>
              <hr />
              <li>
                <span><h4>الجودة</h4></span>
                <h5>1080</h5>
              </li>
              <hr />
              <li>
                <span><h4>اللغه</h4></span>
                <h5>{{ this.move.original_language }}</h5>
              </li>
              <hr />
              <li>
                <span><h4>السنه</h4></span>
                <h5>{{ this.move.last_air_date }}</h5>
              </li>
              <hr />
              <li>
                <span><h4>البلد</h4></span>
                <h5>{{ this.move.origin_country }}</h5>
              </li>
            </ul>
          </div>
        </div>
      </div>
      <hr />
      <div class="terial">
        <img id="terialphoto" :src="st + '/' + this.move.backdrop_path" />
      </div>
      <hr />
      <h2>
        : مشاهدت الحلقات
        <img style="width: 30px" src="../assets/quotation.png" />
      </h2>
      <h3>: متعدد الجودة</h3>
      <hr />
      <div id="links">
        <ul>
          <li><a>1080mp4</a></li>
          <li><a>360mp4</a></li>
          <li><a>144mp4</a></li>
        </ul>
      </div>
      <hr />
    </div>
  </div>
</template>
<style scoped>
.about {
  display: flex;
  flex-flow: column;
  justify-content: center;
  align-content: center;
}
#photo {
  position: relative;
  align-self: flex-start;
  width: 18rem;
  height: 400px;
}
#conphot {
  align-self: flex-end;
  position: relative;
  display: flex;
  flex-flow: column;
  align-items: center;
  text-align: center;
  left: -20px;
  top: 20px;
}
ul {
  list-style-type: none;
  text-decoration: none;
}
a {
  background-color: rgb(255, 69, 69);
  border-radius: 5px;
  padding: 10px;
  margin-block-end: 10px;
  cursor: pointer;
}
#discrption {
  display: flex;
  flex-flow: column;
  justify-content: start;
  align-content: end;
  position: relative;
}
#discrption h3 {
  align-self: flex-end;
}
h2 {
  display: flex;
  align-self: flex-end;
  margin-inline-end: 20px;
  gap: 10px;
}
#links ul {
  display: flex;
  flex-flow: row, wrap;
  justify-content: space-evenly;
  align-content: center;
}
.checked {
  color: orange;
}
span h4 {
  color: brown;
}
h3,
h2 {
  color: rgb(243, 237, 237);
}
#filminform {
  display: flex;
  flex-flow: row, wrap;
  justify-content: center;
  align-content: center;
  position: absolute;
  top: 20px;
  width: 100%;
  height: 400px;
  left: 300px;
}
#filminform li {
  color: #2c3e50;
  font-family: "Courier New", Courier, monospace;
  position: relative;
  display: inline-block;
}
#listprant {
  display: flex;
  flex-flow: row;
  justify-content: center;
  align-content: center;
  position: relative;
  gap: 20px;
  left: -300px;
}
#listprant li {
  width: 100px;
}
#terialphoto {
  width: 80%;
  height: 400px;
}
#informheader {
  position: relative;
  left: 200px;
  color: #fff9f9;
}
@media (max-width: 1366px) {
}
/*/tablet/*/
@media (max-width: 991px) {
  #filminform {
    display: flex;
    flex-flow: row, wrap;
    justify-content: center;
    align-content: center;
    position: relative;
    top: 20px;
    width: 50%;
    height: 400px;
  }
  #conphot {
    left: 0px;
  }
  /* contener ditelse movie */
  #filminform {
    width: 100%;
    left: 0px;
  }
  /* all item in onlly */
  #listprant li {
    width: 80px;
  }
  /* item in contener ditelze */
  #listprant {
    display: flex;
    flex-flow: row;
    justify-content: center;
    align-content: center;
    position: relative;
    gap: 15px;
    left: 70px;
  }
  /* header in ditilze contener */
  #informheader {
    left: 350px;
    width: fit-content;
  }
  #terial {
    width: 100%;
  }
}
/*/mobile/*/
@media (max-width: 500px) {
  #photo {
    position: relative;
    align-self: center;
    width: 18rem;
    height: 400px;
  }
  #conphot {
    align-self: center;
    position: relative;
    top: 20px;
  }
  /* contener ditelse movie */
  #filminform {
    display: flex;
    flex-flow: row;
    justify-content: center;
    align-content: center;
    position: relative;
    top: 20px;
    width: 100%;
    height: auto;
    left: 0px;
  }
  /* all item in onlly */
  #listprant li {
    width: 80px;
  }
  /* item in contener ditelze */
  #listprant {
    display: inline-block;
    position: relative;
    gap: 0px;
    left: 0px;
  }
  /* header in ditilze contener */
  #informheader {
    align-self: flex-start;
    left: 230px;
    width: fit-content;
  }
  #terial {
    width: 100%;
  }
}
</style>
<script>
import { mystore } from "@/store/count";
import { mapActions, mapState } from "pinia";
export default {
  data() {
    return {
      st: "https://image.tmdb.org/t/p/original",
      stvidow: "https://www.youtube.com/embed/",
      move: "",
      tv: "",
    };
  },
  computed: {
    ...mapState(mystore, ["singelTV", "trial"]),
  },
  methods: {
    ld() {
      window.scroll(0, 0);
    },
    ...mapActions(mystore, ["dogetTV", "getTrialmovie", "getTrialTv"]),
  },
  async mounted() {
    await this.dogetTV(this.$route.params.filmid);
    this.sr = this.$route.query.imgsrc;
    this.p = this.$route.query.discrptione;
    this.nam = this.$route.query.name;
    this.srv = this.$route.query.video;
    this.type = this.$route.query.type;
    this.ld();
    //for send params to fun
    //await this.doget(this.$route.params.filmid);

    // await this.getTrialmovie(this.$route.params.filmid);
    // await this.getTrialTv(this.$route.params.filmid),
    this.move = this.singelTV;
  },
};
</script>
