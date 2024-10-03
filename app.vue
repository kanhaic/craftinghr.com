<template>
  <div class="min-h-screen bg-gray-900">
    <TheHeader :logo-src="logoSrc" :company-name="companyName" :nav-items="navItems" />
    <HeroSection :title="heroTitle" :subtitle="heroSubtitle" :cta-text="heroCTAText" /> 
    <Stats :title="statsTitle" :subtitle="statsSubtitle" :stats="stats" />
    <ProductsSection :title="productsTitle" :products="products" />
    <Team :title="teamTitle" :team-members="teamMembers" />
    <ContactSection :title="contactTitle" :subtitle="contactSubtitle" :cta-text="contactCTAText" :email="contactEmail" />
    <TheFooter :company-name="companyName" />
  </div>
</template>

<script setup>
const logoSrc = '/logo.png'
const companyName = 'CraftingHR Software Solutions LLP'
const navItems = [
  { text: 'Products', href: '#products' },
  { text: 'Contact', href: '#contact' },
]

const heroTitle = 'Innovative HR and Routing Solutions'
const heroSubtitle = 'Streamline your HR processes and optimize your routes with our cutting-edge software'
const heroCTAText = 'Explore Our Products'

const productsTitle = 'Our Products'
const products = [
  {
    title: 'EasyHR',
    description: 'Simplify your HR management with our comprehensive solution.',
    link: 'https://easyhrworld.com',
    logo: '/easyhr-logo.png', // Add the path to your EasyHR logo
  },
  {
    title: 'EazyRoute',
    description: 'Optimize your routes and improve efficiency with our advanced routing software.',
    link: 'https://eazyroute.app',
    logo: '/eazyroute-logo.png', // Add the path to your EazyRoute logo
  },
]

const statsTitle = 'Trusted by Enterprises Worldwide'
const statsSubtitle = 'Empowering businesses with efficient HR and Sales solutions'

const stats = [
  { id: 1, name: 'Enterprises Served', value: '2000+' },
  { id: 2, name: 'Employees Served', value: '100000+' },
  { id: 3, name: 'Team Efficiency Increase', value: '40%' }
]

const contactTitle = 'Get in Touch'
const contactSubtitle = 'Interested in our solutions? Contact us for more information or a demo.'
const contactCTAText = 'Contact Us'
const contactEmail = 'info@craftinghr.com'
</script>