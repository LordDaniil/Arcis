<script setup>
defineProps({
  totalPrice: Number
})

const emit = defineEmits(['openDrawer'])
</script>

<template>
  <header class="flex justify-between border-b border-slate-300 px-8 py-8">
    <router-link to="/">
      <div class="flex items-center gap-4">
        <img src="/logo.png" alt="logo" class="w-27" />
      </div>
    </router-link>

    <div class="text-xl font-vold gap-4 text-wrap pt-10">
      <h1>Режим работы:</h1>
      <p>Ежедневно с 8:00 до 18:00</p>
    </div>
    <article class="text-xl font-vold gap-4 text-wrap pt-10">
      <h1>Желаете связаться с нами? Звоните по номеру:</h1>
      <p>+7-995-208-44-74 или +7-861-205-00-91</p>
    </article>

    <ul class="frex items-center gap-10 pt-8">
      <li
        @click="() => emit('openDrawer')"
        class="flex items-center cursor-pointer gap-3 text-grey-500 hover:text-black"
      >
        <img src="/cart.svg" alt="Cart" />
        <span>{{ totalPrice }}</span>
      </li>

      <router-link to="/favorites">
        <li class="flex items-center cursor-pointer gap-3 text-grey-500 hover:text-black">
          <img src="/heart.svg" alt="Cart" />
          <span>Избранное</span>
        </li>
      </router-link>

      <router-link to="/profile">
        <li class="flex items-center cursor-pointer gap-3 text-grey-500 hover:text-black">
          <img src="/profile.svg" alt="Cart" />
          <span>О нас</span>
        </li>
      </router-link>

      <router-link to="/conf">
        <li class="flex items-center cursor-pointer gap-3 text-grey-500 hover:text-black">
          <img
            src="C:\Users\Winadmin\Desktop\архив\vue-sait\public\product\password_protect_secure_security_privacy_lock_padlock_icon_219328.svg"
            alt="confi"
          />
          <span>Политика конфиденциальности</span>
        </li>
      </router-link>
    </ul>
  </header>
</template>
