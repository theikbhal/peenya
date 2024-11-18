<template>
  <div class="container">
    <header class="header">
      <h1>Manufacturing Companies in Peenya, Bangalore</h1>
    </header>

    <main class="main-content">
      <ul class="company-list">
        <li class="company-card" v-for="company in companies" :key="company.name">
          <h2>{{ company.name }}</h2>
          <p><strong>Address:</strong> {{ company.address }}</p>
          <p><strong>Contact:</strong> {{ company.contact }}</p>
          <p><strong>Products:</strong></p>
          <ul>
            <li v-for="product in company.products" :key="product">{{ product }}</li>
          </ul>
        </li>
      </ul>
    </main>

    <footer class="footer">
      <p>© 2024 Peenya Manufacturing Directory. All Rights Reserved.</p>
    </footer>
  </div>
</template>

<script setup>
import companies from "../data/companies.json"; // Ensure the JSON path is correct
</script>

<style scoped>
/* General Styles */
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
  background-color: #f8f9fa;
  color: #333;
}

.container {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

/* Header Styles */
.header {
  background-color: #1e3a8a; /* Steel blue */
  color: white;
  padding: 1.5rem;
  text-align: center;
}

.header h1 {
  margin: 0;
  font-size: 2rem;
}

/* Main Content */
.main-content {
  flex: 1;
  padding: 2rem;
}

.company-list {
  list-style: none;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 1.5rem;
  padding: 0;
  margin: 0;
}

.company-card {
  background-color: white;
  border: 1px solid #ddd;
  border-radius: 8px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  padding: 1.5rem;
  transition: transform 0.2s, box-shadow 0.2s;
}

.company-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 6px 12px rgba(0, 0, 0, 0.15);
}

.company-card h2 {
  color: #1e3a8a;
  margin-top: 0;
  margin-bottom: 0.5rem;
}

.company-card p {
  margin: 0.25rem 0;
}

.company-card ul {
  list-style: disc;
  margin: 0.5rem 0 0 1.5rem;
}

/* Footer */
.footer {
  background-color: #333;
  color: white;
  text-align: center;
  padding: 1rem;
  font-size: 0.875rem;
}
</style>
