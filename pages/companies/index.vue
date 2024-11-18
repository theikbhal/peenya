<template>
    <div class="companies-page">
      <header class="page-header">
        <h1>Top Manufacturing Companies in Peenya, Bangalore</h1>
        <p>Explore the notable manufacturing companies driving innovation and growth in Peenya.</p>
      </header>
  
      <section class="companies-list">
        <article v-for="(company, index) in companies" :key="index" class="company-card">
          <h2>{{ company.name }}</h2>
          <p>{{ company.description }}</p>
          <ul class="company-details">
            <li><strong>Net Worth:</strong> {{ company.netWorth }}%</li>
            <li><strong>Revenue:</strong> {{ company.revenue }}</li>
          </ul>
        </article>
      </section>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        companies: [
          {
            name: "Sami Sabinsa Group Limited",
            description:
              "Specializing in phytonutrients and herbal extracts, Sami Labs caters to nutritional, pharmaceutical, and food industries.",
            netWorth: 30.52,
            revenue: "INR 500+ crores",
          },
          {
            name: "Dynamatic Technologies Limited",
            description:
              "Focusing on aerospace, automotive, and hydraulic products, it is a key player in engineered solutions.",
            netWorth: 11.22,
            revenue: "INR 500+ crores",
          },
          {
            name: "Ajax Engineering Private Limited",
            description:
              "Known for Self-Loading Mobile Concrete Mixers and Batching Plants, Ajax is a leader in construction equipment.",
            netWorth: 12.97,
            revenue: "Robust Financial Standing",
          },
          // Add the rest of the companies here
        ],
      };
    },
  };
  </script>
  
  <style src="@/assets/styles/companies.css" scoped></style>
  