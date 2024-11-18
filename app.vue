<template>
  <div>
    <!-- Accessibility announcer -->
    <NuxtRouteAnnouncer />

    <!-- Application content goes here -->
    <header>
      <h1>Peenya Manufacturing Directory</h1>
      <nav>
        <ul>
          <li><NuxtLink to="/">Home</NuxtLink></li>
          <li><NuxtLink to="/about">About</NuxtLink></li>
          <li><NuxtLink to="/contact">Contact</NuxtLink></li>
        </ul>
      </nav>
    </header>

    <!-- Page content rendered here -->
    <main>
      <NuxtPage />
    </main>

    <footer>
      <p>© 2024 Peenya Manufacturing Directory. All Rights Reserved.</p>
    </footer>
  </div>
</template>
