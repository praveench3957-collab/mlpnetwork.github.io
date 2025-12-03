<!DOCTYPE html>
<html lang="en">
<head>
 <meta charset="UTF-8" />
 <meta name="viewport" content="width=device-width, initial-scale=1.0" />
 <title>MLP Network | Travel Agency Hyderabad - Book Now</title>
 <style>
 * { box-sizing: border-box; margin: 0; padding: 0; }
 body {
 font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
 line-height: 1.6;
 color: #222;
 background-color: #f8f9fa;
 }
 header {
 background: linear-gradient(120deg, #0066cc, #00bcd4);
 color: #fff;
 padding: 20px 40px;
 position: sticky;
 top: 0;
 z-index: 100;
 box-shadow: 0 2px 10px rgba(0,0,0,0.1);
 }
 header h1 { font-size: 28px; margin-bottom: 5px; }
 header p { font-size: 15px; opacity: 0.95; }
 nav {
 margin-top: 15px;
 }
 nav a {
 color: #e3f2fd;
 margin-right: 20px;
 text-decoration: none;
 font-weight: 500;
 font-size: 15px;
 transition: color 0.3s;
 }
 nav a:hover { color: #fff; }
 .hero {
 padding: 60px 40px;
 background: linear-gradient(rgba(0,102,204,0.85), rgba(0,188,212,0.85)), url('https://images.unsplash.com/photo-1506905925346-21bda4d32df4?ixlib=rb-4.0.3&auto=format&fit=crop&w=2070&q=80');
 background-size: cover;
 background-position: center;
 color: #fff;
 min-height: 400px;
 display: flex;
 flex-direction: column;
 justify-content: center;
 text-align: center;
 }
 .hero h2 {
 font-size: 36px;
 margin-bottom: 15px;
 text-shadow: 0 2px 4px rgba(0,0,0,0.5);
 }
 .hero p {
 max-width: 600px;
 margin: 0 auto 25px;
 font-size: 18px;
 }
 .cta-btn {
 background: linear-gradient(120deg, #ff9800, #ff6f00);
 color: #fff;
 border: none;
 padding: 15px 30px;
 font-size: 16px;
 border-radius: 50px;
 cursor: pointer;
 box-shadow: 0 4px 15px rgba(255,152,0,0.4);
 transition: all 0.3s;
 text-transform: uppercase;
 letter-spacing: 1px;
 font-weight: 600;
 }
 .cta-btn:hover {
 transform: translateY(-2px);
 box-shadow: 0 6px 20px rgba(255,152,0,0.5);
 }
 section {
 padding: 60px 40px;
 }
 .section-title {
 font-size: 28px;
 margin-bottom: 15px;
 color: #004c97;
 text-align: center;
 }
 .section-subtitle {
 font-size: 16px;
 margin-bottom: 40px;
 color: #555;
 text-align: center;
 max-width: 700px;
 margin-left: auto;
 margin-right: auto;
 }
 .flex {
 display: flex;
 flex-wrap: wrap;
 gap: 25px;
 justify-content: center;
 }
 .card {
 background: #fff;
 border-radius: 12px;
 box-shadow: 0 5px 20px rgba(0,0,0,0.08);
 padding: 25px;
 flex: 1 1 300px;
 min-width: 280px;
 transition: all 0.3s;
 border-top: 4px solid #0066cc;
 }
 .card:hover {
 transform: translateY(-5px);
 box-shadow: 0 15px 40px rgba(0,0,0,0.15);
 }
 .card h3 {
 font-size: 20px;
 margin-bottom: 10px;
 color: #0066cc;
 }
 .badge {
 display: inline-block;
 background: linear-gradient(120deg, #e3f2fd, #bbdefb);
 color: #1565c0;
 font-size: 12px;
 padding: 5px 12px;
 border-radius: 20px;
 margin-bottom: 12px;
 text-transform: uppercase;
 letter-spacing: 0.5px;
 font-weight: 600;
 }
 ul {
 margin-left: 20px;
 font-size: 15px;
 margin-bottom: 15px;
 }
 li { margin-bottom: 8px; }
 .tagline {
 font-style: italic;
 font-size: 14px;
 color: #666;
 margin-bottom: 15px;
 }
 .package-meta {
 font-size: 14px;
 margin-top: 10px;
 color: #444;
 font-weight: 500;
 }
 .btn-small {
 margin-top: 15px;
 display: inline-block;
 padding: 10px 20px;
 font-size: 14px;
 border-radius: 25px;
 background: linear-gradient(120deg, #0066cc, #00bcd4);
 color: #fff;
 text-decoration: none;
 transition: all 0.3s;
 }
 .btn-small:hover {
 transform: translateY(-2px);
 box-shadow: 0 5px 15px rgba(0,102,204,0.4);
 }
 .contact-grid {
 display: grid;
 grid-template-columns: 1fr 1fr;
 gap: 40px;
 }
 form input, form textarea, form select {
 width: 100%;
 padding: 12px;
 margin: 8px 0 18px;
 border: 2px solid #e0e0e0;
 border-radius: 8px;
 font-size: 15px;
 transition: border-color 0.3s;
 }
 form input:focus, form textarea:focus, form select:focus {
 outline: none;
 border-color: #0066cc;
 }
 form button {
 background: linear-gradient(120deg, #0066cc, #00bcd4);
 color: #fff;
 border: none;
 padding: 15px 30px;
 border-radius: 8px;
 cursor: pointer;
 font-size: 16px;
 font-weight: 600;
 width: 100%;
 transition: all 0.3s;
 }
 form button:hover {
 transform: translateY(-2px);
 box-shadow: 0 5px 20px rgba(0,102,204,0.4);
 }
 .pay-btn {
 width: 48%;
 padding: 12px;
 margin: 6px;
 border: none;
 border-radius: 8px;
 font-size: 15px;
 font-weight: 600;
 cursor: pointer;
 transition: all 0.3s;
 }
 #razorpay-btn { background: linear-gradient(120deg, #00bcd4, #0097a7); color: #fff; }
 #paytm-btn { background: linear-gradient(120deg, #ff9800, #f57c00); color: #fff; }
 .pay-btn:hover { transform: translateY(-2px); box-shadow: 0 5px 15px rgba(0,0,0,0.2); }
 .success-box {
 background: linear-gradient(120deg, #e8f5e8, #c8e6c9);
 padding: 20px;
 border-radius: 8px;
 border-left: 5px solid #4caf50;
 margin-top: 20px;
 }
 footer {
 background: linear-gradient(120deg, #001f3f, #003d82);
 color: #e0e0e0;
 padding: 30px 40px;
 font-size: 14px;
 text-align: center;
 }
 @media (max-width: 768px) {
 .contact-grid { grid-template-columns: 1fr; gap: 30px; }
 header, section, .hero, footer { padding-left: 20px; padding-right: 20px; }
 .hero h2 { font-size: 28px; }
 nav a { margin-right: 15px; font-size: 14px; }
 }
 </style>
</head>
<body>
 <header>
 <h1>MLP Network</h1>
 <p> Domestic & International Travel | Hyderabad | Instant Bookings | UPI Payments</p>
 <nav>
 <a href="#about">About</a>
 <a href="#domestic">Domestic</a>
 <a href="#international">International</a>
 <a href="#contact">Book Now</a>
 </nav>
 </header>

 <section class="hero">
 <h2>Book Your Dream Holiday from Hyderabad</h2>
 <p>Domestic & International packages with detailed itineraries. Secure UPI/Card payments. Instant WhatsApp confirmation.</p>
 <button class="cta-btn" onclick="document.getElementById('contact').scrollIntoView({behavior:'smooth'});">Book Package Now</button>
 </section>

 <section id="about">
 <h2 class="section-title">Why Choose MLP Network</h2>
 <p class="section-subtitle">Hyderabad's trusted travel agency for personalized domestic & international tours with complete itineraries.</p>
 <div class="flex">
 <div class="card">
 <h3> Instant Bookings</h3>
 <ul>
 <li>20% advance via UPI/Cards</li>
 <li>Balance on departure</li>
 <li>EMI options available</li>
 </ul>
 </div>
 <div class="card">
 <h3> Hyderabad Support</h3>
 <ul>
 <li>RGIA Airport pickup</li>
 <li>24x7 WhatsApp help</li>
 <li>Local office visits</li>
 </ul>
 </div>
 <div class="card">
 <h3> Complete Packages</h3>
 <ul>
 <li>Flights + Hotels + Sightseeing</li>
 <li>Day-wise itineraries</li>
 <li>Visa & transfers included</li>
 </ul>
 </div>
 </div>
 </section>

 <section id="domestic" style="background: #f0f8ff;">
 <h2 class="section-title">Domestic Packages from Hyderabad</h2>
 <p class="section-subtitle">Popular weekend getaways & family holidays with flights included.</p>
 <div class="flex">
 <div class="card">
 <span class="badge">Domestic</span>
 <h3>Goa Beach Escape</h3>
 <p class="tagline">4D/3N | ₹15,999/person</p>
 <ul>
 <li>Return flights HYD-GOA</li>
 <li>Beach resort + breakfast</li>
 <li>North & South Goa tours</li>
 </ul>
 <p class="package-meta">2-6 travellers | All weekends</p>
 <a href="#contact" class="btn-small">Book Now</a>
 </div>
 <div class="card">
 <span class="badge">Domestic</span>
 <h3>Kashmir Paradise</h3>
 <p class="tagline">6D/5N | ₹29,999/person</p>
 <ul>
 <li>Srinagar + Gulmarg + Pahalgam</li>
 <li>Houseboat stay</li>
 <li>Shikara ride included</li>
 </ul>
 <p class="package-meta">Family special | Flights incl.</p>
 <a href="#contact" class="btn-small">Book Now</a>
 </div>
 <div class="card">
 <span class="badge">Domestic</span>
 <h3>Kerala Backwaters</h3>
 <p class="tagline">5D/4N | ₹24,999/person</p>
 <ul>
 <li>Munnar + Alleppey houseboat</li>
 <li>Thekkady wildlife</li>
 <li>Private cab transfers</li>
 </ul>
 <p class="package-meta">Honeymoon special</p>
 <a href="#contact" class="btn-small">Book Now</a>
 </div>
 </div>
 </section>

 <section id="international">
 <h2 class="section-title">International Packages</h2>
 <p class="section-subtitle">Budget-friendly tours with visa assistance from Hyderabad.</p>
 <div class="flex">
 <div class="card">
 <span class="badge">International</span>
 <h3>Singapore-Malaysia</h3>
 <p class="tagline">6D/5N | ₹45,999/person</p>
 <ul>
 <li>Singapore city tour</li>
 <li>Kuala Lumpur + Genting</li>
 <li>Flights + Visa included</li>
 </ul>
 <p class="package-meta">Family groups | Monthly deps.</p>
 <a href="#contact" class="btn-small">Book Now</a>
 </div>
 <div class="card">
 <span class="badge">International</span>
 <h3>Dubai Explorer</h3>
 <p class="tagline">5D/4N | ₹33,999/person</p>
 <ul>
 <li>Desert safari + BBQ</li>
 <li>Burj Khalifa + Marina</li>
 <li>Visa on arrival help</li>
 </ul>
 <p class="package-meta">Short holidays | All months</p>
 <a href="#contact" class="btn-small">Book Now</a>
 </div>
 <div class="card">
 <span class="badge">International</span>
 <h3>Thailand Delight</h3>
 <p class="tagline">5D/4N | ₹28,999/person</p>
 <ul>
 <li>Bangkok + Pattaya</li>
 <li>Island speedboat tour</li>
 <li>Flights + Visa included</li>
 </ul>
 <p class="package-meta">Friends & couples</p>
 <a href="#contact" class="btn-small">Book Now</a>
 </div>
 </div>
 </section>

 <section id="contact">
 <h2 class="section-title">Instant Booking Form</h2>
 <p class="section-subtitle">Fill details → Pay 20% advance → Get WhatsApp itinerary within 30 mins. Cancel anytime.</p>
 <div class="contact-grid">
 <div>
 <h3> Booking Details</h3>
 <form id="bookingForm">
 <label for="name">Full Name *</label>
 <input type="text" id="name" name="name" required />

 <label for="phone">WhatsApp Number *</label>
 <input type="tel" id="phone" name="phone" placeholder="+91-98XXXXXXX" required />

 <label for="email">Email</label>
 <input type="email" id="email" name="email" />

 <label for="package">Select Package *</label>
 <select id="package" name="package" onchange="calculateAdvance()" required>
 <option value="">Choose package</option>
 <option value="goa" data-price="15999">Goa (₹15,999)</option>
 <option value="kashmir" data-price="29999">Kashmir (₹29,999)</option>
 <option value="kerala" data-price="24999">Kerala (₹24,999)</option>
 <option value="singapore" data-price="45999">Singapore (₹45,999)</option>
 <option value="dubai" data-price="33999">Dubai (₹33,999)</option>
 <option value="thailand" data-price="28999">Thailand (₹28,999)</option>
 <option value="custom">Custom Package</option>
 </select>

 <label for="travellers">No. of People *</label>
 <input type="number" id="travellers" name="travellers" min="1" max="20" value="2" onchange="calculateAdvance()" required />

 <label for="travel-date">Travel Start Date</label>
 <input type="date" id="travel-date" name="travel-date" />

 <label for="advance-amount">Advance (20%)</label>
 <input type="text" id="advance-amount" name="advance" readonly placeholder="₹0" />

 <label for="message">Special Requests</label>
 <textarea id="message" name="message" rows="3" placeholder="Dietary needs, hotel prefs, visa help..."></textarea>

 <button type="submit"> Confirm & Pay Advance</button>
 </form>

 <div id="payment-options" style="display: none; margin-top: 25px;">
 <div class="success-box">
 <h4> Booking Confirmed!</h4>
 <p>Pay 20% advance securely. Balance on departure day.</p>
 </div>
 <h4 style="margin: 20px 0 10px 0;"> Payment Options</h4>
 <button type="button" id="razorpay-btn" class="pay-btn">Pay with Razorpay</button>
 <button type="button" id="paytm-btn" class="pay-btn">Pay with Paytm</button>
 <p style="font-size: 13px; margin-top: 15px; color: #666;">
 <strong>OR</strong> UPI: <code>mlpnetwork@paytm</code><br>
 Bank: MLP Network | IFSC: SBIN000XXXX
 </p>
 </div>
 </div>
 
 <div>
 <h3> Hyderabad Office</h3>
 <div style="background: #e3f2fd; padding: 25px; border-radius: 12px; margin-bottom: 25px;">
 <p><strong>MLP Network Travel Agency</strong></p>
 <p>Hyderabad, Telangana<br> Near RGIA Airport (25 mins)</p>
 <p> <strong>+91-XXXXXXXXXX</strong> (24x7)</p>
 <p> bookings@mlpnetwork.com</p>
 </div>
 
 <div style="background: #fff3e0; padding: 20px; border-radius: 12px; border-left: 5px solid #ff9800;">
 <h4> Why Hyderabad Loves Us</h4>
 <ul style="font-size: 14px; margin-left: 0;">
 <li> UPI instant payments</li>
 <li> Airport pickup included</li>
 <li> EMI on all packages</li>
 <li> Free cancellations</li>
 <li> WhatsApp support</li>
 </ul>
 </div>
 </div>
 </div>
 </section>

 <footer>
 <p>© 2025 MLP Network | Hyderabad's #1 Travel Agency | <a href="#contact" style="color: #fff;">Book Now</a></p>
 <p>Domestic & International Tours | Secure UPI Payments | Detailed Itineraries</p>
 </footer>

 <script>
 function calculateAdvance() {
 const pkg = document.getElementById('package');
 const travellers = document.getElementById('travellers').value || 1;
 const price = pkg.selectedOptions[0]?.dataset?.price || 0;
 const total = parseInt(price) * parseInt(travellers);
 const advance = Math.round(total * 0.2);
 document.getElementById('advance-amount').value = 
 `₹${advance.toLocaleString()} (Total: ₹${total.toLocaleString()})`;
 }

 document.getElementById('bookingForm').addEventListener('submit', function(e) {
 e.preventDefault();
 document.getElementById('payment-options').style.display = 'block';
 document.getElementById('bookingForm').scrollIntoView({behavior: 'smooth'});
 
 // Collect booking data
 const formData = new FormData(this);
 const data = Object.fromEntries(formData);
 console.log(' New Booking:', data);
 
 // Simulate WhatsApp confirmation
 alert(' Booking received!\n\nWhatsApp confirmation sent.\nChoose payment below.');
 });

 // Demo payment handlers
 document.getElementById('razorpay-btn')?.addEventListener('click', function() {
 alert(' Razorpay opened!\n(Replace with real Razorpay key from dashboard.razorpay.com)');
 });

 document.getElementById('paytm-btn')?.addEventListener('click', function() {
 alert(' Paytm opened!\n(Replace with real Paytm merchant account)');
 });

 // Smooth scrolling for nav links
 document.querySelectorAll('a[href^="#"]').forEach(anchor => {
 anchor.addEventListener('click', function(e) {
 e.preventDefault();
 document.querySelector(this.getAttribute('href')).scrollIntoView({behavior: 'smooth'});
 });
 });
 </script>
</body>
</html>
