<template>
  <header>
    <nav class="py-3">
      <a class="p-1 rounded-xl logo m-3 mr-auto" href="/">
        <a class="" href="/">
          <img
            class="w-32 h-12 lg:w-48 lg:h-24 md:w-48 md:h-24 rounded-xl"
            src="./assets/images/Nolek_logo-removebg-preview.png"
            alt="Logo"
          />
        </a>
      </a>
      <div class="nav__links mt-6 hidden lg:block md:block">
        <router-link
          class="nav__hover mx-2 px-2 rounded-md text-white lg:px-6 lg:py-2 md:px-6 md:py-2"
          to="/"
          >الرئيسية</router-link
        >
        <router-link
          class="nav__hover mx-2 px-2 rounded-md text-white lg:px-6 lg:py-2 md:px-6 md:py-2"
          to="/projects"
          >المشاريع</router-link
        >
        <a
          class="nav__hover mx-2 px-2 rounded-md text-white lg:px-6 lg:py-2 md:px-6 md:py-2"
          href="#home"
          >اتصل بنا</a
        >
      </div>
      <div class="mobile__menu lg:hidden md:hidden">
        <a class="mobile__drop p-1" href="#">
          <img
            class="mr-3 mt-5 w-7 cursor-pointer"
            src="./assets/images/menu.svg.png"
            alt=""
          />
        </a>
        <ul
          class="drop__down bg-white flex flex-col items-center w-full rounded-xl"
        >
          <li class="my-3 text-xl w-full text-center">
            <a
              class="nav__hover mx-2 py-5 rounded-md lg:px-6 lg:py-2 md:px-6 md:py-2 w-full text-black"
              href=""
              >الرئيسية</a
            >
          </li>
          <li class="my-3 text-xl w-full text-center">
            <a
              class="nav__hover mx-2 py-5 rounded-md lg:px-6 lg:py-2 md:px-6 md:py-2 w-full text-black"
              href=""
              >المشاريع</a
            >
          </li>
          <li class="my-3 text-xl w-full text-center">
            <a
              class="nav__hover mx-2 py-5 rounded-md lg:px-6 lg:py-2 md:px-6 md:py-2 w-full text-black"
              href=""
            >
              اتصل بنا</a
            >
          </li>
        </ul>
      </div>
    </nav>
    <h1
      class="text-white text-4xl lg:text-7xl md:text-7xl text-center pt-96 font-extrabold"
    >
      شركة نولك للمقاولات
    </h1>
    <p class="text-white text-3xl lg:text-4xl md:text-4xl text-center pt-8">
      .Nolec Contracting Co
    </p>
  </header>
  <router-view />
  <footer
    class="text-gray-700 bg-white pb-11 flex flex-col items-center"
    id="home"
  >
    <h3 class="text-2xl p-2 rounded-md text-white">إبقى على تواصل :</h3>
    <div
      class="contact__info flex flex-col items-center lg:flex lg:flex-row md:flex md:flex-row"
    >
      <div class="phone mx-1 my-2">
        <a
          class="footer__hover text-white pr-3 py-3 px-2 rounded-md flex flex-row-reverse"
          href="tel:+9660500518950"
        >
          <img
            class="w-7 mx-1"
            src="./assets/images/phone.png"
            alt=""
          />9660500518950+
        </a>
      </div>
      <div class="mail my-4">
        <a
          class="footer__hover text-lg text-white pr-3 py-2 px-2 rounded-md"
          href="mailto:info@airmenu.net"
          >Mail: info@airmenu.net</a
        >
      </div>
    </div>
    <div class="address text-white text-lg mt-2 p-2 flex flex-col">
      <span class="text-center">الرياض حي الحمراء شارع المصانع </span>
      <span>رقم المبنى 3944 الرمز البريدي 13217</span>
    </div>
  </footer>
</template>

<script>
export default {
  methods: {
    navScroll() {
      const nav = document.querySelector(".nav");
      if (window.scrollY > nav.offsetHeight + 150) {
        nav.classList.add("nav__background");
      }
    },
  },
};
</script>

<style lang="scss">
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
  text-decoration: none;
  list-style: none;
}

body {
  font-family: "Noto Sans Arabic", sans-serif;
  color: #636e72;
}

html {
  scroll-behavior: smooth;
  scroll-margin: 2em;
}

/* Start of scrollbar style*/

::-webkit-scrollbar {
  width: 15px;
}

::-webkit-scrollbar-track {
  background: transparent;
}

::-webkit-scrollbar-thumb {
  background: rgb(14 165 233);
}

::-webkit-scrollbar-thumb:hover {
  background-color: rgb(8, 134, 192);
}

/* End of scrollbar style*/

/* Start of header and nav styles*/

header {
  background-image: url(./assets/images/cover1.jpg);
  background-size: cover;
  background-position: center;
  background-attachment: fixed;
  padding-bottom: 25em;
  font-family: cairo;

  a {
    // color: rgb(14 165 233)
    &.router-link-exact-active {
      color: #f4f8f6;
    }
  }
  .nav__hover:hover {
    color: rgb(14 165 233);
    background-color: #f4f8f6;
    transition: 0.6s ease;
  }
}

.logo {
  float: left;
}

.logo {
  background: rgba(0, 0, 0, 0.7);
}

nav {
  margin-top: 3px;
  position: fixed;
  width: 100%;
}

nav div a {
  display: inline-block;
}

.nav__links {
  text-align: center;
  margin: 0;
  transition: 1s;
  letter-spacing: 2.5px;
  font-size: 20px;
  padding-inline: 100px;
}

.nav__links a {
  border-bottom: 3px solid white;
  padding-inline: 50px;
}

.nav__background {
  background-color: black;
}

/* start of mobile menu styles*/

.drop__down {
  display: none !important;
}

.mobile__menu:hover .drop__down {
  display: block !important;
}

.mobile__menu:active .drop__down {
  display: block !important;
}

/* End of mobile menu styles*/

/* End of header and nav styles*/

/* Start of footer styles*/

.footer__hover:hover {
  color: rgb(14 165 233);
  background-color: #f4f8f6;
  transition: 0.6s ease;
}

footer {
  background-image: url(./assets/images/footer.jpg);
  background-size: cover;
  background-position: center;
}
/* End of footer styles*/
</style>
