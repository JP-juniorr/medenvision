<template>
  <footer class="footer">
    <div class="footer-content">
      <div class="footer-section">
        <h4>Contact Us</h4>
        <p>1234 MedEnvision Street</p>
        <p>Healthcare City, HE 56789</p>
        <p>Email: contact@medenvision.com</p>
        <p>Phone: +1 (555) 123-4567</p>
        <p>&copy; 2025 MedEnvision. All rights reserved.</p>
      </div>
    </div>
  </footer>
</template>

<style scoped>
.footer {
  background-color: black;
  color: #fff;
  padding: 20px;
  font-family: "Courier New", Courier, monospace;
}
.footer-content {
  display: flex;
  justify-content: space-between;
  margin-bottom: 20px;
}
.footer-section {
  width: 30%;
}
.footer-section h4 {
  margin-bottom: 10px;
}
.footer-section p,
.footer-section ul {
  color: #fff;
  margin: 5px 0;
}
.footer-section ul {
  list-style-type: none;
  padding: 0;
}
.footer-section ul li {
  margin: 5px 0;
}
.footer-section ul li a {
  color: #fff;
  text-decoration: none;
}
.footer-section ul li a:hover {
  text-decoration: underline;
  color: #fff;
}
.footer-bottom {
  text-align: center;
  font-size: 0.8em;
}
.footer-bottom p {
  margin: 5px 0;
}
.footer-bottom a {
  color: #fff;
  text-decoration: none;
}
.footer-bottom a:hover {
  text-decoration: underline;
}
a {
  color: #fff !important;
  text-decoration: none;
}
</style>
