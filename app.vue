<template>
  <div class="min-h-screen bg-white dark:bg-gray-900 text-gray-900 dark:text-gray-100">
    <TheHeader
      :logo-src="logoSrc"
      :company-name="companyName"
      :nav-items="navItems"
    />
    <HeroSection
      :preTitle="heroData.preTitle"
      :title="heroData.title"
      :subtitle="heroData.subtitle"
      :ctaText="heroData.ctaText"
    />
    <Stats :title="statsTitle" :subtitle="statsSubtitle" :stats="stats" />
    <ProductsSection
      :preTitle="productsPreTitle"
      :title="productsTitle"
      :subtitle="productsSubtitle"
      :products="products"
      id="products"
    />
    <Team
      id="team"
      :title="teamTitle"
      :subtitle="teamSubtitle"
      :team-members="teamMembers"
    />
    <ContactSection
      :title="contactTitle"
      :subtitle="contactSubtitle"
      :cta-text="contactCTAText"
      :email="contactEmail"
    />
    <TheFooter :company-name="companyName" />
  </div>
</template>

<script setup>

const logoSrc = "/logo.png";
const companyName = "CraftingHR Software Solutions LLP";
const navItems = [
  { text: "Products", href: "#products" },
  { text: "Team", href: "#team" },
  { text: "Contact", href: "#contact" },
];

const heroData = ref({
  preTitle: "Revolutionizing HR Management",
  title: "Craft Your Perfect Sales and HR Strategy",
  subtitle: "Empower your organization with innovative HR solutions",
  ctaText: "Learn More",
});

const productsPreTitle = "Smart HR & Sales Software";
const productsTitle = "Our Products";
const productsSubtitle =
  "We provide HR & Sales Software for SMEs & Enterprises";
const products = [
  {
    name: "EasyHR",
    description:
      "Easy HR is simple & intuitive HR Software for SME & Enterprise. It provides HRIS records, leaves & attendance, Payroll, expenses, travel making it very easy to manage.",
    href: "https://easyhrworld.com",
    logo: "/easyhr-logo.png", // Make sure this path is correct
  },
  {
    name: "EazyRoute",
    description:
      "EazyRoute is a field service management software that helps businesses manage their field sales, route optimization, and customer management.",
    href: "https://eazyroute.app",
    logo: "/eazyroute-logo.png", // Make sure this path is correct
  },
];

const statsTitle = "Trusted by Enterprises Worldwide";
const statsSubtitle =
  "Empowering businesses with efficient HR and Sales solutions";

const stats = [
  { id: 1, name: "Enterprises Served", value: "2000+" },
  { id: 2, name: "Employees Served", value: "100000+" },
  { id: 3, name: "Team Efficiency Increase", value: "40%" },
];

const teamTitle = "Meet Our Team";
const teamSubtitle = "The passionate individuals behind our innovative HR solutions";
const teamMembers = [
  {
    name: "Shripal Shah",
    title: "Co-Founder, CEO",
    description: "Shripal brings over a decade of experience in IT and services. With an Engineering degree and MBA from Mumbai University, he excels in Business Process Management, Project Management, and Innovation across various sectors.",
    image: "/shripal-shah.jpg",
    linkedIn: "https://www.linkedin.com/in/shripalshah125"
  },
  {
    name: "Kanhai Chhugani",
    title: "Co-Founder, CTO",
    description: "Kanhai is a technology executive with a proven track record in developing and delivering technology-based products. He excels in product management, leading multinational development teams, and crafting product roadmaps.",
    image: "/kanhai-chhugani.webp",
    linkedIn: "https://www.linkedin.com/in/kanhaic"
  }
];

const contactTitle = "Get in Touch";
const contactSubtitle =
  "Interested in our solutions? Contact us for more information or a demo.";
const contactCTAText = "Contact Us";
const contactEmail = "info@craftinghr.com";
</script>
