<template>
  <b-row style="margin-left: 0;margin-right: 0;">
    <b-col md="12">
      <b-img
        :src="avatar"
        alt="Lermy Ferrer"
        img="@/assets/LermyNew.png"
      />
    </b-col>
    <b-col md="12">
      <h4 class="text-center intro animate__animated animate__fadeInUp animate__fast">
        Hola,
        <br />Soy Lermy Ferrer Peralta.
      </h4>
      <h4 class="text-center">Web developer</h4>
      <div class="col-md-12 info">
        
        <div
          class="text-center social-icons animate__animated animate__fadeInUp animate__delay-1s"
        >
          <a
            href="http://github.com/ingeniero1984"
            target="_blank"
            rel="noopener"
          >
            <GithubIcon />
          </a>
          <a
            href="www.linkedin.com/in/ing-lermy-ferrer-6a620668"
            target="_blank"
            rel="noopener"
          >
            <LinkedinIcon />
          </a>
          <a
            href="https://twitter.com/Lermyferrer"
            target="_blank"
            rel="noopener"
          >
            <TwitterIcon />
          </a>
          <a
            href="mailto:ingeniero.lermy84@gmail.com"
            target="_blank"
            rel="noopener"
          >
            <MailIcon />
          </a>
        </div>
      </div>
    </b-col>
  </b-row>
</template>

<script>
import GithubIcon from "vue-ionicons/dist/logo-github.vue";
import LinkedinIcon from "vue-ionicons/dist/logo-linkedin.vue";
import TwitterIcon from "vue-ionicons/dist/logo-twitter.vue";
import MailIcon from "vue-ionicons/dist/md-mail.vue";
export default {
  name: "Home",
  components: { GithubIcon, LinkedinIcon, TwitterIcon, MailIcon },
  data() {
    return {
      avatar: require("@/assets/LermyNew.png")
    };
  },
  head: {
    title: "Portfolio ⚡ - Asaolu Elijah",
    meta: [
      {
        hid: "description",
        name: "description",
        content:
          "Asaolu Elijah is an awesome front-end developer and technical writer, passionate about building solutions that works across multiple platforms with high accessibility approach. Elijah has vast knowledge in web development with over 3+ years experience in building actual products"
      },
      {
        hid: "og:title",
        name: "og:title",
        content: "Portfolio ⚡ - Asaolu Elijah"
      },
      {
        property: "og:description",
        content:
          "Asaolu Elijah is an awesome front-end developer and technical writer, passionate about building solutions that works across multiple platforms with high accessibility approach. Elijah has vast knowledge in web development with over 3+ years experience in building actual products"
      },
      { hid: "og:image", name: "og:image", content: require("@/assets/coding.png") }
    ]
  },
  methods: {},
  mounted() {
    this.$nextTick(() => {
      this.$nuxt.$loading.start();

      setTimeout(() => this.$nuxt.$loading.finish(), 500);
    });
  }
};
</script>

<style scoped>
.row {
  margin-top: 170px;
}
.action-btn {
  display: inline-table;
  margin: 7px;
}
.info {
  margin-top: 10px;
  text-align: left;
  line-height: 2em;
  font-size: 18px;
  font-weight: normal;
  margin-left: 7px;
}
img {
  background-color: rgb(46, 42, 42);
  border-radius: 100%;
  width: 230px;
  height: 230px;
  cursor: pointer;
}
.social-icons {
  margin-top: 20px;
}
.social-icons a {
  font-size: 25px;
  margin: 15px;
  color: rgba(0, 0, 0, 0.712);
}
.social-icons a:hover {
  color: #000;
}
.intro {
  font-size: 45px;
  text-align: left;
  margin-top: 20px;
  /* color: #000; */
}
/* for mobile devices */
@media screen and (max-width: 420px) {
  .row {
    margin-top: 0px;
  }
  img {
    width: 150px;
    height: 150px;
  }
  .intro {
    font-size: 30px;
    font-weight: bold;
  }
}
.btn-primary {
  background-color: #f00;
  border-color: #f00;
}
.btn-primary:hover {
  background-color: rgb(240, 0, 0);
  border-color: rgb(240, 0, 0);
}
</style>
