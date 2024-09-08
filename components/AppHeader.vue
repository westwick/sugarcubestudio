<template>
  <header class="px-2 md:px-4">
    <div class="container mx-auto flex items-center justify-between">
      <NuxtLink to="/" class="text-white text-lg md:text-xl font-bold flex items-center hover:text-yellow-200"
        exact-active-class="text-yellow-300">
        <img src="@/assets/images/logo.png" class="logo mr-4" /><span class="hidden md:block">Sugar Cube Studio</span>
      </NuxtLink>
      <div class="flex items-center space-x-4 ml-auto">
        <NuxtLink to="/" class="ml-4 navlink text-white text-md font-bold hover:text-yellow-200"
          exact-active-class="link-active text-yellow-300">
          HOME
        </NuxtLink>
        <div class="text-slate-700">/</div>
        <NuxtLink to="/apps" class="navlink text-white text-md font-bold hover:text-yellow-200"
          exact-active-class="link-active text-yellow-300">
          APPS
        </NuxtLink>
        <div class="text-slate-700">/</div>
        <NuxtLink to="/contact" class="navlink text-white text-md font-bold hover:text-yellow-200"
          exact-active-class="link-active text-yellow-300">
          CONTACT
        </NuxtLink>
      </div>
    </div>
  </header>
</template>

<style>
header {
  background: #171926;
}

header a {
  transition: all ease-in-out 0.2s;
}

.navlink {
  border-bottom: 3px solid transparent;
  border-top: 3px solid transparent;
  padding: 16px 8px;
}

.logo {
  width: 40px;
  height: auto;
  transform: rotate(0);
  transition: all 0.3s ease-in-out;
}

.logo:hover {
  transform: rotate(180deg);
}

.link-active {
  border-bottom: 3px solid #67a1d6;
  position: relative;
}

.link-active::before {
  content: "";
  position: absolute;
  left: 50%;
  bottom: -7px;
  transform: translateX(-50%);
  border-left: 6px solid transparent;
  border-right: 6px solid transparent;
  border-top: 6px solid #67a1d6;
  z-index: 2;
}
</style>