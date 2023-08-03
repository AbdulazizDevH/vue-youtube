<template>
  <div class="header">
    <div class="2xl:container px-4 py-2 mx-auto flex items-center justify-between">
      
      <div class="navbar__item flex items-center justify-between">
        <div class="navbar__icon cursor-pointer w-10 h-10 flex items-center justify-center flex-col rounded-full border border-solid border-transparent">
          <span class="w-[18px] h-px inline-block my-[5px] bg-black"></span>
        </div>
        <a href="#" class="navbar__logo px-4">
          <img class="w-[90px!important]" src="@/assets/images/header/logo.webp" alt="">
        </a>
      </div>

      <div class="navbar__item w-[46%] flex items-center justify-between">
        <div class="navbar__search  flex items-center justify-between pl-4 relative border border-solid border-[#ccc] rounded-[40px] ">
          <input v-on:focus="" class="inline-block mr-dd bg-transparent outline-none border-none text-base font-normal" type="text" placeholder="Введите запрос">
          <span class="">
            <!-- <img class="w-[20px!important]" src="@/assets/images/header/search.webp" alt=""> -->
            <!-- <svg class="w-[20px!important]" viewBox="0 0 24 24" preserveAspectRatio="xMidYMid meet" focusable="false" style="pointer-events: none; display: block; width: 100%; height: 100%;"><g class="style-scope yt-icon"><path d="M20.87,20.17l-5.59-5.59C16.35,13.35,17,11.75,17,10c0-3.87-3.13-7-7-7s-7,3.13-7,7s3.13,7,7,7c1.75,0,3.35-0.65,4.58-1.71 l5.59,5.59L20.87,20.17z M10,16c-3.31,0-6-2.69-6-6s2.69-6,6-6s6,2.69,6,6S13.31,16,10,16z" class="style-scope yt-icon"></path></g></svg> -->
          </span>
          <img src="./assets/keyboard.png" alt="">
          <button class="py-[7px] px-5 bg-[#f8f8f8] hover:bg-[#0000000d] rounded-r-full border-l border-solid border-l-[#ccc] cursor-pointer">
            <img class="w-[24px!important] h-[24px!important]" src="@/assets/images/header/search.webp" alt="">
          </button>
        </div>
        <div class="navbar__voice-search bg-slate-500 w-10 h-10 flex items-center justify-center bg-[] rounded-full cursor-pointer">
          <img class="w-[24px!important] h-[24px!important]" src="@/assets/images/header/microphone.webp" alt="">
        </div>
      </div>

      <div class="navbar__item flex items-center justify-between">
        <div class="navbar__create-video w-10 h-10 flex items-center justify-center relative border border-solid border-transparent rounded-full cursor-pointer">
          <svg class="w-[24px!important] h-[24px!important]" viewBox="0 0 24 24" preserveAspectRatio="xMidYMid meet" focusable="false" style="pointer-events: none; display: block; width: 100%; height: 100%;"><g><path d="M14,13h-3v3H9v-3H6v-2h3V8h2v3h3V13z M17,6H3v12h14v-6.39l4,1.83V8.56l-4,1.83V6 M18,5v3.83L22,7v8l-4-1.83V19H2V5H18L18,5 z"></path></g></svg>
        </div>
        <div class="navbar__notification w-10 h-10 mx-2 flex items-center justify-center border border-solid border-transparent rounded-full cursor-pointer">
          <svg class="w-[24px!important] h-[24px!important]" viewBox="0 0 24 24" preserveAspectRatio="xMidYMid meet" focusable="false" style="pointer-events: none; display: block; width: 100%; height: 100%;"><g><path d="M10,20h4c0,1.1-0.9,2-2,2S10,21.1,10,20z M20,17.35V19H4v-1.65l2-1.88v-5.15c0-2.92,1.56-5.22,4-5.98V3.96 c0-1.42,1.49-2.5,2.99-1.76C13.64,2.52,14,3.23,14,3.96l0,0.39c2.44,0.75,4,3.06,4,5.98v5.15L20,17.35z M19,17.77l-2-1.88v-5.47 c0-2.47-1.19-4.36-3.13-5.1c-1.26-0.53-2.64-0.5-3.84,0.03C8.15,6.11,7,7.99,7,10.42v5.47l-2,1.88V18h14V17.77z"></path></g></svg>
        </div>
        <div class="navbar__avatar w-8 h-8 ml-3 mr-[18px] flex items-center justify-center bg-[#5c6bc0] text-[#f9f9f9] text-[15px] font-normal leading-8 border border-solid border-transparent rounded-full cursor-pointer">L</div>
      </div>

    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>

%effects {
  transition: background-color 0.2s linear;
  &:hover {
    background-color: #0000001a;
  }
  &:active {
    background-color: #00000033;
    border: 1px solid #00000033;
  }
}

@mixin width-height($width, $height) {
  width: $width;
  height: $height;
}
.navbar {
  &__icon {
    @extend %effects;
    &::before,
    &::after {
      display: inline-block;
      content: "";
      background-color: black;
      @include width-height(18px, 1px);
    }
  }


  &__search {
    box-shadow: inset 0 1px 2px #eee;
    span {
      display: none;
      align-items: center;
      justify-content: center;
      background-color: aquamarine;
      // @include width-height(auto, 40px);
      height: 40px;
      width: auto;
      position: absolute;
      left: -32px;
      right: 64px;
      padding-left: 15px;
      border-radius: 40px 0 0 40px;
    }
  }


  &__voice-search {
    @extend %effects;
  }

  &__create-video {
    @extend %effects;
    &::before {
      width: 2px;
      height: 14px;
      content: "";
      display: inline-block;
      position: absolute;
      left: -3.5px;
      background-color: #ccc;
      margin-right: 8px;
    }
  }

  &__notification {
    @extend %effects;
  }
}
</style>