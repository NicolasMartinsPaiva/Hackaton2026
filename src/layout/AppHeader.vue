<template>
  <header class="header-wrapper">
    <div class="header">
      <!-- Logo -->
      <div class="logo">
        <span class="logo-icon">G</span>
        <span class="logo-text">Guey</span>
      </div>

      <!-- Busca -->
      <div class="search-bar">
        <svg class="search-icon" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
          <circle cx="11" cy="11" r="7" stroke="currentColor" stroke-width="2"/>
          <line x1="21" y1="21" x2="16.65" y2="16.65" stroke="currentColor" stroke-width="2" stroke-linecap="round"/>
        </svg>
        <input
          type="text"
          v-model="searchQuery"
          placeholder="Buscar profissionais ou serviços..."
        />
      </div>

      <!-- Navegação -->
      <nav class="nav-links">
        <a href="#" class="nav-link">Categorias</a>
        <a href="#" class="nav-link">Como funciona</a>
        <a href="#" class="nav-link login-link">
          <svg viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" width="16" height="16">
            <path d="M15 3h4a2 2 0 0 1 2 2v14a2 2 0 0 1-2 2h-4" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
            <polyline points="10 17 15 12 10 7" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
            <line x1="15" y1="12" x2="3" y2="12" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
          </svg>
          Login
        </a>
        <button class="cadastrar-btn">Cadastrar</button>
      </nav>
    </div>

    <!-- Barra azul inferior -->
    <div class="bottom-bar"></div>
  </header>
</template>

<script setup>
import { ref } from 'vue'

const searchQuery = ref('')
</script>

<style scoped>
.header-wrapper {
  width: 100%;
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Arial, sans-serif;
}

.header {
  display: flex;
  align-items: center;
  gap: 24px;
  padding: 14px 24px;
  background: #ffffff;
  border-radius: 12px;
}

/* Logo */
.logo {
  display: flex;
  align-items: center;
  gap: 8px;
  flex-shrink: 0;
}

.logo-icon {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 32px;
  height: 32px;
  background: #2563eb;
  color: #fff;
  font-weight: 700;
  font-size: 16px;
  border-radius: 8px;
}

.logo-text {
  font-weight: 700;
  font-size: 20px;
  color: #111827;
}

/* Busca */
.search-bar {
  flex: 1;
  display: flex;
  align-items: center;
  gap: 8px;
  background: #f3f4f6;
  border: 1px solid #e5e7eb;
  border-radius: 10px;
  padding: 10px 14px;
  max-width: 640px;
}

.search-icon {
  width: 18px;
  height: 18px;
  color: #9ca3af;
  flex-shrink: 0;
}

.search-bar input {
  border: none;
  outline: none;
  background: transparent;
  width: 100%;
  font-size: 14px;
  color: #374151;
}

.search-bar input::placeholder {
  color: #9ca3af;
}

/* Navegação */
.nav-links {
  display: flex;
  align-items: center;
  gap: 24px;
  flex-shrink: 0;
}

.nav-link {
  display: flex;
  align-items: center;
  gap: 6px;
  color: #2563eb;
  text-decoration: none;
  font-size: 14px;
  font-weight: 500;
  white-space: nowrap;
}

.login-link {
  color: #374151;
}

.cadastrar-btn {
  background: #2563eb;
  color: #fff;
  border: none;
  padding: 10px 20px;
  border-radius: 8px;
  font-size: 14px;
  font-weight: 600;
  cursor: pointer;
  white-space: nowrap;
}

.cadastrar-btn:hover {
  background: #1d4ed8;
}

/* Barra azul inferior */
.bottom-bar {
  height: 6px;
  background: #2563eb;
  width: 100%;
}

/* Responsivo */
@media (max-width: 768px) {
  .header {
    flex-wrap: wrap;
  }

  .nav-links {
    gap: 16px;
  }
}
</style>
