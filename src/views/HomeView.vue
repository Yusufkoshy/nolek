<template>
  <div class="home">
    <section
      class="intro flex flex-col lg:flex lg:flex-row-reverse items-center justify-center mx-3"
    >
      <div
        class="container flex flex-col lg:flex lg:flex-row-reverse items-center justify-center"
      >
        <img
          class="section__pic my-5 rounded-xl"
          src="../assets/images/engineer-2.jpg"
          alt=""
        />
        <div class="text p-7">
          <h2 class="text-3xl mb-2">مقدمة</h2>
          <p class="yusuf mb-2">
            إن طموح شركة نولك وشغف التميز يجعلنا في سعي دائما لإن تكون الإفضل في
            حجم إعمالنا وذلك بالتطوير الدائم لإدائنا بما يواكب طموحاتنا وتنويع
            خدماتنا بما يتماشى مع رغبات عملاءنا لتقوية قدراتنا التنافسية في جميع
            الإنشطة التي نعمل بها , ولإنكون واحدة من إولى شركات المقاولات
            والبناء في المملكة العربية السعودية , يجب إن ينظر إلينا الشركاء
            والعملاء كجزء لا يتجزاء من عميلة نجاحهم فالشركة لديها الخبرات
            والمهارات والموارد لمواجهة ظروف إعمال المقاولات ولذلك نحن نتوقع
            إحتياجاتهم ونحقق كافة إلتزاماتنا إتجاهم , فنحن إهلا للمسؤولية إمام
            المجتمع ونملك تاريخآ من التخطيط الدقيق وإدارة مواقع عمل إمنة
            وملتزمين بالعامل الزمني وتحقيق الجودة والتميز في الإداء , لذا شركة
            نولك للمقاولات تؤدي واجباتها الاجتماعية كما غنها تحافظ علة مشروعاتها
            .
          </p>
          <h2 class="text-3xl mb-2">من نحن</h2>
          <p class="mb-2">
            تإسست شركة نولك للمقاولات وقفنا لمعايير فريدة وخبرات عميقة نستلهم
            منها رؤيتنا الراسخة لتقديم منتجات وخدمات إنشائية تتسم بإعلى درجات
            الجودة والإتفان
          </p>
        </div>
      </div>
    </section>
    <!-- <HelloWorld msg="Welcome to Your Vue.js App" /> -->
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "HomeView",
  components: {
    // HelloWorld,
  },
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
.section__pic {
  border-radius: 2%;
}

.section__pic {
  width: 40em;
}

@media (max-width: 1240px) {
  .section__pic {
    min-width: 30em;
  }
}

@media (max-width: 1040px) {
  .section__pic {
    min-width: 30em;
  }
}

@media (max-width: 590px) {
  .section__pic {
    min-width: 30em;
  }
}

@media (max-width: 480px) {
  .section__pic {
    min-width: 20em;
  }
}

section h2,
p {
  line-height: 26px;
  word-wrap: break-word;
  font-weight: bold;
  letter-spacing: 0.5px;
  word-wrap: nowrap;
}

section p {
  font-size: 18px;
  font-family: cairo;
}
</style>
