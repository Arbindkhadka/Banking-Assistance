// index.html
const html = `
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Banking Services Lead Generator</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="styles.css" />
</head>
<body>
  <header>
    <h1>Banking Services Portal</h1>
    <nav>
      <ul>
        <li><a href="#home-loan">Home Loan</a></li>
        <li><a href="#lap">Loan Against Property</a></li>
        <li><a href="#bbg">Business Banking</a></li>
        <li><a href="#account-services">Account Services</a></li>
      </ul>
    </nav>
  </header>

  <main>
    <section class="hero">
      <h2>Find the Best Banking Solutions in One Place</h2>
      <p>Compare, Apply, and Get Help Instantly!</p>
    </section>

    <section id="home-loan" class="service card">
      <h2>Home Loan</h2>
      <img src="https://source.unsplash.com/600x400/?home,loan" alt="Home Loan" />
      <p>Find the best home loan options with lowest interest rates and fastest processing.</p>
      <button onclick="openLeadForm('Home Loan')">Apply Now</button>
    </section>

    <section id="lap" class="service card">
      <h2>Loan Against Property</h2>
      <img src="https://source.unsplash.com/600x400/?realestate,property" alt="Loan Against Property" />
      <p>Get secured loans by leveraging your property's value.</p>
      <button onclick="openLeadForm('Loan Against Property')">Apply Now</button>
    </section>

    <section id="bbg" class="service card">
      <h2>Business Banking & BBG</h2>
      <img src="https://source.unsplash.com/600x400/?business,finance" alt="Business Banking" />
      <p>Access working capital and other financial products tailored for your business.</p>
      <button onclick="openLeadForm('Business Banking')">Apply Now</button>
    </section>

    <section id="account-services" class="service card">
      <h2>Account Services</h2>
      <img src="https://source.unsplash.com/600x400/?banking,account" alt="Account Services" />
      <p>Open or close saving/current accounts with hassle-free assistance and expert help.</p>
      <button onclick="openLeadForm('Account Services')">Apply Now</button>
    </section>

    <section class="leads-table">
      <h2>Submitted Leads</h2>
      <table id="leads">
        <thead>
          <tr>
            <th>Name</th>
            <th>Phone</th>
            <th>Email</th>
            <th>Service</th>
            <th>Message</th>
          </tr>
        </thead>
        <tbody>
          <!-- Leads will appear here -->
        </tbody>
      </table>
    </section>
  </main>

  <div id="lead-form" class="modal">
    <div class="modal-content">
      <span class="close" onclick="closeLeadForm()">&times;</span>
      <h2>Get Help with <span id="form-service"></span></h2>
      <form id="leadCaptureForm">
        <label for="name">Name</label>
        <input type="text" name="name" id="name" placeholder="Your Name" required />

        <label for="phone">Phone Number</label>
        <input type="tel" name="phone" id="phone" placeholder="Phone Number" required />

        <label for="email">Email Address</label>
        <input type="email" name="email" id="email" placeholder="Email Address" required />

        <label for="message">Your Requirement</label>
        <textarea name="message" id="message" placeholder="Tell us your need" required></textarea>

        <input type="hidden" name="service" id="serviceType" />
        <button type="submit">Submit</button>
      </form>
    </div>
  </div>

  <footer>
    <p>&copy; 2025 Banking Services Lead Portal</p>
  </footer>

  <script src="script.js"></script>
</body>
</html>`;
