<template>
  <NuxtRouteAnnouncer />
  <main class="login-page">
    <section class="login-card">
      <h1 class="title">To-Do List</h1>
      <p class="subtitle">Управляйте задачами эффективно</p>

      <form class="login-form" @submit.prevent>
        <input class="input" type="email" placeholder="Email" />
        <input class="input" type="password" placeholder="Пароль" />

        <label class="remember">
          <input type="checkbox" />
          <span>Запомнить меня</span>
        </label>

        <button type="submit" class="login-btn">Войти</button>
      </form>

      <a href="#" class="forgot-link">Забыли пароль?</a>
    </section>
  </main>
</template>

<style scoped>
:global(*) {
  box-sizing: border-box;
}

:global(body) {
  margin: 0;
  font-family: Inter, "Segoe UI", Arial, sans-serif;
  background: #f5f7fb;
  color: #24364d;
}

.login-page {
  min-height: 100vh;
  display: grid;
  place-items: center;
  padding: 24px;
}

.login-card {
  width: 100%;
  max-width: 480px;
  text-align: center;
}

.title {
  margin: 0;
  font-size: 56px;
  font-weight: 700;
  line-height: 1.05;
  letter-spacing: -0.02em;
}

.subtitle {
  margin: 12px 0 42px;
  font-size: 34px;
  line-height: 1.2;
  color: #6f829a;
}

.login-form {
  display: grid;
  gap: 18px;
}

.input {
  width: 100%;
  height: 70px;
  border: 2px solid #d8e0eb;
  border-radius: 8px;
  padding: 0 24px;
  font-size: 34px;
  color: #30465f;
  outline: none;
  background: #fff;
}

.input::placeholder {
  color: #93a2b4;
}

.input:focus {
  border-color: #5f9be0;
}

.remember {
  margin-top: 2px;
  display: flex;
  align-items: center;
  gap: 14px;
  color: #3f536a;
  font-size: 38px;
  justify-self: start;
}

.remember input {
  width: 34px;
  height: 34px;
  border-radius: 6px;
}

.login-btn {
  margin-top: 6px;
  width: 100%;
  height: 72px;
  border: none;
  border-radius: 8px;
  background: #2f7fde;
  color: #fff;
  font-size: 42px;
  font-weight: 600;
  cursor: pointer;
}

.login-btn:hover {
  background: #2774cf;
}

.forgot-link {
  margin-top: 28px;
  display: inline-block;
  color: #3b86dc;
  font-size: 42px;
  text-decoration: none;
  font-weight: 600;
}

.forgot-link:hover {
  text-decoration: underline;
}

@media (max-width: 1200px) {
  .title {
    font-size: 44px;
  }

  .subtitle {
    font-size: 28px;
    margin-bottom: 30px;
  }

  .input {
    height: 60px;
    font-size: 24px;
    padding: 0 18px;
  }

  .remember {
    font-size: 24px;
  }

  .remember input {
    width: 24px;
    height: 24px;
  }

  .login-btn {
    height: 60px;
    font-size: 30px;
  }

  .forgot-link {
    font-size: 28px;
  }
}
</style>
