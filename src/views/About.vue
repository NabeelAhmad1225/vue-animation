<template>
  <div class="about">
    <transition
      appear=""
      name="fade"
      @before-enter="beforeEnter"
      @enter="enter"
      @after-enter="afterEnter"
    >
      <h1>About</h1>
    </transition>
    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Cum aperiam
      officia possimus delectus inventore quod quisquam culpa voluptas iusto,
      quae maiores quo dolorum, corporis laboriosam a dolore consequatur
      assumenda nam!
    </p>
    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Cum aperiam
      officia possimus delectus inventore quod quisquam culpa voluptas iusto,
      quae maiores quo dolorum, corporis laboriosam a dolore consequatur
      assumenda nam!
    </p>
    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Cum aperiam
      officia possimus delectus inventore quod quisquam culpa voluptas iusto,
      quae maiores quo dolorum, corporis laboriosam a dolore consequatur
      assumenda nam!
    </p>
  </div>
</template>

<script>
export default {
  setup() {
    const beforeEnter = () => {
      console.log("Before Enter");
    };
    const enter = () => {
      console.log(" Enter");
    };
    const afterEnter = () => {
      console.log("After Enter");
    };
    return { beforeEnter, enter, afterEnter };
  },
};
</script>

<style>
.about {
  max-width: 600px;
  margin: 20px auto;
}
.fade-enter-from {
  opacity: 0;
}
.fade-enter-active {
  transition: all 3s ease;
}
.fade-leave-to {
  opacity: 0;
}
.fade-leave-active {
  transition: all 3s ease;
}
</style>
