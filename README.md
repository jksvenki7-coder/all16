# all16<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>JKS Group of Business - All Services</title>
<style>
  body {
    font-family: Arial, sans-serif;
    margin:0; background: #22232c; color: #fff;
  }
  header {
    font-size: 2.2rem;
    font-weight: bold;
    color: #3aaaff;
    text-align: center;
    padding: 36px 10px 10px 10px;
    user-select: none;
  }
  #dashboard {
    max-width: 960px;
    margin: 20px auto;
    display: grid;
    grid-template-columns: repeat(4,1fr);
    gap: 20px;
  }
  .service-button {
    border: 2.5px solid #ffe066;
    border-radius: 12px;
    padding: 20px;
    text-align: center;
    cursor: pointer;
    font-weight: 600;
    color: #ffe066;
    background-color: #232335;
    box-shadow: 0 0 18px #ffe066aa;
    transition: all 0.3s ease;
    user-select: none;
  }
  .service-button:hover {
    color: #fffbd0;
    background-color: #232342;
    box-shadow: 0 0 38px #ffe066ff;
    transform: scale(1.05);
  }
  .section {
    max-width: 960px;
    margin: 20px auto;
    padding: 20px;
    background: #f9f9f9;
    color: #222;
    border-radius: 12px;
    display: none;
  }
  .section.active {
    display: block;
  }
  h2 {
    color: #205081;
    border-bottom: 3px solid #85bbeb;
    padding-bottom: 6px;
  }
  button.back-button, form button.submit-btn {
    margin-top: 20px;
    padding: 10px 15px;
    font-weight: 600;
    cursor: pointer;
    border: none;
    border-radius: 6px;
    background-color: #3498db;
    color: white;
  }
  a.whatsapp-btn {
    display: inline-block;
    margin: 15px 0;
    background: #25D366;
    color: white;
    padding: 10px 20px;
    border-radius: 6px;
    font-weight: 700;
    text-decoration: none;
  }
  input, textarea, select {
    width: 100%;
    padding: 8px;
    margin-top: 4px;
    border-radius: 6px;
    border: 1px solid #ccc;
    box-sizing: border-box;
  }
  label {
    font-weight: 600;
    margin-top: 12px;
    display: block;
  }
  nav.small-nav {
    display: flex;
    justify-content: center;
    gap: 12px;
    margin-bottom: 18px;
    flex-wrap: wrap;
  }
  nav.small-nav button {
    padding: 10px 14px;
    font-weight: 600;
    border-radius: 8px;
    border: none;
    cursor: pointer;
    background: #eef2ff;
    color: #3366cc;
    transition: background 0.3s, color 0.3s;
  }
  nav.small-nav button.selected {
    background: #3366cc;
    color: white;
  }
  nav.small-nav button:hover:not(.selected) {
    background: #d3d9f6;
  }
  #map {
    width: 100%;
    height: 300px;
    margin: 20px 0;
    border-radius: 12px;
  }
  video {
    display: block;
    margin: 20px auto;
    border-radius: 12px;
    max-width: 100%;
    height: auto;
  }
  .gallery {
    display: flex;
    gap: 12px;
    flex-wrap: wrap;
    margin-bottom: 20px;
  }
  .img-card {
    border: 1px solid #ccc;
    border-radius: 8px;
    overflow: hidden;
    width: 160px;
    text-align: center;
    background: white;
    cursor: pointer;
    box-shadow: 0 0 5px #aaa;
  }
  .img-card img {
    width: 100%;
    height: 90px;
    object-fit: cover;
  }
  .img-card p {
    margin: 8px 0;
    font-weight: 600;
    color: #205081;
  }
</style>
</head>
<body>
<header>JKS Group of Business</header>

<div id="dashboard">
  <div class="service-button" onclick="showSection('ecommerce')">My E-commerce</div>
  <div class="service-button" onclick="showSection('events')">Events & Catering</div>
  <div class="service-button" onclick="showSection('courier')">Courier & Ride Booking</div>
  <div class="service-button" onclick="showSection('job')">Job Consultancy & Services</div>
  <div class="service-button" onclick="showSection('tours')">Tours & Travels</div>
  <div class="service-button" onclick="showSection('realestate')">Real Estate & Construction</div>
  <div class="service-button" onclick="showSection('investment')">Investment & Business</div>
  <div class="service-button" onclick="showSection('loans')">Loans & Insurance</div>
  <div class="service-button" onclick="showSection('homeservices')">Home Services</div>
</div>

<!-- E-commerce -->
<div id="ecommerce" class="section">
  <h2>My E-commerce</h2>
  <nav class="small-nav">
    <button class="selected" onclick="switchEcommTab('groceries', this)">Groceries</button>
    <button onclick="switchEcommTab('food', this)">Food</button>
    <button onclick="switchEcommTab('pharmacy', this)">Pharmacy</button>
    <button onclick="switchEcommTab('camera', this)">Camera</button>
    <button onclick="switchEcommTab('maps', this)">Location Map</button>
  </nav>
  <div id="groceriesTab" class="ecomm-tab active">
    <h3>Groceries Categories</h3>
    <div class="gallery">
      <div class="img-card"><img src="https://source.unsplash.com/160x90/?milk" alt="Milk"/><p>Milk</p></div>
      <div class="img-card"><img src="https://source.unsplash.com/160x90/?meat" alt="Meat"/><p>Meat</p></div>
      <div class="img-card"><img src="https://source.unsplash.com/160x90/?fruits" alt="Fruits"/><p>Fruits</p></div>
      <div class="img-card"><img src="https://source.unsplash.com/160x90/?vegetables" alt="Vegetables"/><p>Vegetables</p></div>
    </div>
    <form id="ecommerceGroceriesForm">
      <label for="nameEcomGro">Name</label>
      <input type="text" id="nameEcomGro" name="nameEcomGro" required />
      <label for="mobileEcomGro">Mobile Number</label>
      <input type="tel" id="mobileEcomGro" name="mobileEcomGro" />
      <label for="orderEcomGro">Order Details</label>
      <textarea id="orderEcomGro" name="orderEcomGro" rows="3" required></textarea>
      <label for="addressEcomGro">Delivery Address</label>
      <textarea id="addressEcomGro" name="addressEcomGro" rows="2" required></textarea>
      <button type="submit" class="submit-btn">Place Order via WhatsApp</button>
    </form>
  </div>
  <div id="foodTab" class="ecomm-tab" style="display:none;">
    <h3>Food Categories</h3>
    <div class="gallery">
      <div class="img-card"><img src="https://source.unsplash.com/160x90/?biriyani" alt="Biriyani"/><p>Biriyani</p></div>
      <div class="img-card"><img src="https://source.unsplash.com/160x90/?tiffins" alt="Tiffins"/><p>Tiffins</p></div>
      <div class="img-card"><img src="https://source.unsplash.com/160x90/?icecream" alt="Ice Cream"/><p>Ice Cream</p></div>
    </div>
    <form id="ecommerceFoodForm">
      <label for="nameEcomFood">Name</label>
      <input type="text" id="nameEcomFood" name="nameEcomFood" required />
      <label for="mobileEcomFood">Mobile Number</label>
      <input type="tel" id="mobileEcomFood" name="mobileEcomFood"/>
      <label for="orderEcomFood">Order Details</label>
      <textarea id="orderEcomFood" name="orderEcomFood" rows="3" required></textarea>
      <label for="addressEcomFood">Delivery Address</label>
      <textarea id="addressEcomFood" name="addressEcomFood" rows="2" required></textarea>
      <button type="submit" class="submit-btn">Place Order via WhatsApp</button>
    </form>
  </div>
  <div id="pharmacyTab" class="ecomm-tab" style="display:none;">
    <h3>Pharmacy</h3>
    <div class="gallery">
      <div class="img-card"><img src="https://source.unsplash.com/160x90/?medicine" alt="Medicines"/><p>Medicines</p></div>
      <div class="img-card"><img src="https://source.unsplash.com/160x90/?health" alt="Health Products"/><p>Health Products</p></div>
    </div>
    <form id="ecommercePharmacyForm">
      <label for="nameEcomPhar">Name</label>
      <input type="text" id="nameEcomPhar" name="nameEcomPhar" required />
      <label for="mobileEcomPhar">Mobile Number</label>
      <input type="tel" id="mobileEcomPhar" name="mobileEcomPhar"/>
      <label for="orderEcomPhar">Order Details</label>
      <textarea id="orderEcomPhar" name="orderEcomPhar" rows="3" required></textarea>
      <label for="addressEcomPhar">Delivery Address</label>
      <textarea id="addressEcomPhar" name="addressEcomPhar" rows="2" required></textarea>
      <button type="submit" class="submit-btn">Place Order via WhatsApp</button>
    </form>
  </div>

  <div id="cameraTab" class="ecomm-tab" style="display:none;">
    <h3>Camera Access</h3>
    <button onclick="openCamera()">Start Camera</button>
    <video id="video" autoplay></video>
  </div>
  <div id="mapsTab" class="ecomm-tab" style="display:none;">
    <h3>Location Map</h3>
    <div id="map"></div>
  </div>
  <button class="back-button" onclick="backToDashboard()">Back to Dashboard</button>
</div>

<!-- Events & Catering -->
<div id="events" class="section">
  <h2>Events & Catering</h2>
  <nav class="small-nav">
    <button class="selected" onclick="switchEventTab('package', this)">Package</button>
    <button onclick="switchEventTab('customized', this)">Customized</button>
    <button onclick="switchEventTab('premium', this)">Premium</button>
  </nav>

  <div id="packageTab" class="tab-content">
    <p>Choose your package and services.</p>
    <ul>
      <li>Silver: 50,000 - 1,00,000</li>
      <li>Gold: 1,00,000 - 3,00,000</li>
      <li>Diamond: 3,00,000 - 5,00,000</li>
      <li>Platinum: 5,00,000 - 8,00,000</li>
    </ul>
    <form id="eventsPackageForm">
      <label for="namePackage">Name</label>
      <input type="text" id="namePackage" name="namePackage" required />
      <label for="mobilePackage">Mobile Number</label>
      <input type="tel" id="mobilePackage" name="mobilePackage" required />
      <label for="emailPackage">Email</label>
      <input type="email" id="emailPackage" name="emailPackage" required />
      <label for="messagePackage">Message</label>
      <textarea id="messagePackage" name="messagePackage" rows="3" required></textarea>
      <button type="submit" class="submit-btn">Send Inquiry via WhatsApp</button>
    </form>
  </div>

  <div id="customizedTab" class="tab-content" style="display:none;">
    <p>Select one or more customized services:</p>
    <ul>
      <li><input type="checkbox" id="decoration" /> <label for="decoration">Decoration Items</label></li>
      <li><input type="checkbox" id="dj" /> <label for="dj">DJ, Dance & Singing</label></li>
      <li><input type="checkbox" id="games" /> <label for="games">Games & Entertainment</label></li>
      <li><input type="checkbox" id="jewellery" /> <label for="jewellery">Jewellery</label></li>
      <li><input type="checkbox" id="convention" /> <label for="convention">Convention</label></li>
      <li><input type="checkbox" id="photography" /> <label for="photography">Photography & Videography</label></li>
      <li><input type="checkbox" id="anchor" /> <label for="anchor">Anchors & Artists</label></li>
      <li><input type="checkbox" id="returngifts" /> <label for="returngifts">Return Gifts</label></li>
      <li><input type="checkbox" id="cloths" /> <label for="cloths">Clothing & Accessories</label></li>
      <li><input type="checkbox" id="makeup" /> <label for="makeup">Makeup Artist</label></li>
      <li><input type="checkbox" id="mehndi" /> <label for="mehndi">Mehndi Artist</label></li>
      <li><input type="checkbox" id="guestrooms" /> <label for="guestrooms">Guest House & Rooms</label></li>
      <li><input type="checkbox" id="hotel" /> <label for="hotel">Hotels</label></li>
      <li><input type="checkbox" id="transport" /> <label for="transport">Car/Bus/Truck/Auto Rentals</label></li>
      <li><input type="checkbox" id="catering" /> <label for="catering">Catering & Food Services</label></li>
      <li><input type="checkbox" id="lighting" /> <label for="lighting">Lighting</label></li>
      <li><input type="checkbox" id="sound" /> <label for="sound">Sound Systems</label></li>
      <li><input type="checkbox" id="invitation" /> <label for="invitation">Invitation Cards</label></li>
      <li><input type="checkbox" id="returngifts2" /> <label for="returngifts2">Return Gifts (Extra)</label></li>
    </ul>
    <label>Any Special Requests:</label>
    <textarea id="specialRequests" rows="4" style="width:100%;"></textarea>
    <form id="eventsCustomizedForm" style="margin-top:20px;">
      <label for="nameCustom">Name</label>
      <input type="text" id="nameCustom" name="nameCustom" required />
      <label for="mobileCustom">Mobile Number</label>
      <input type="tel" id="mobileCustom" name="mobileCustom" required />
      <label for="emailCustom">Email</label>
      <input type="email" id="emailCustom" name="emailCustom" required />
      <label for="messageCustom">Message</label>
      <textarea id="messageCustom" name="messageCustom" rows="3" required></textarea>
      <button type="submit" class="submit-btn">Send Inquiry via WhatsApp</button>
    </form>
  </div>

  <div id="premiumTab" class="tab-content" style="display:none;">
    <p>Premium services include:</p>
    <ul>
      <li>Exclusive Venue Booking</li>
      <li>International Catering Options</li>
      <li>DJ Services</li>
      <li>Special Lighting & Effects</li>
    </ul>
    <form id="eventsPremiumForm" style="margin-top:20px;">
      <label for="namePremium">Name</label>
      <input type="text" id="namePremium" name="namePremium" required />
      <label for="mobilePremium">Mobile Number</label>
      <input type="tel" id="mobilePremium" name="mobilePremium" required />
      <label for="emailPremium">Email</label>
      <input type="email" id="emailPremium" name="emailPremium" required />
      <label for="messagePremium">Message</label>
      <textarea id="messagePremium" name="messagePremium" rows="3" required></textarea>
      <button type="submit" class="submit-btn">Send Inquiry via WhatsApp</button>
    </form>
  </div>

  <button class="back-button" onclick="backToDashboard()">Back to Dashboard</button>
</div>

<!-- Courier & Ride Booking -->
<div id="courier" class="section">
  <h2>Courier & Ride Booking</h2>
  <form id="courierForm">
    <label for="nameCourier">Name</label>
    <input type="text" id="nameCourier" name="nameCourier" required />
    <label for="mobileCourier">Mobile Number</label>
    <input type="tel" id="mobileCourier" name="mobileCourier" />
    <label for="detailsCourier">Courier Details</label>
    <textarea id="detailsCourier" name="detailsCourier" rows="3" required></textarea>
    <button type="submit" class="submit-btn">Send Request via WhatsApp</button>
  </form>
  <button class="back-button" onclick="backToDashboard()">Back to Dashboard</button>
</div>

<script>
function showSection(id) {
  document.getElementById('dashboard').style.display = 'none';
  document.querySelectorAll('.section').forEach(sec => {
    sec.classList.remove('active');
  });
  document.getElementById(id).classList.add('active');
}
function backToDashboard() {
  document.getElementById('dashboard').style.display = 'grid';
  document.querySelectorAll('.section').forEach(sec => {
    sec.classList.remove('active');
  });
}
['jobForm', 'loansForm', 'toursForm', 'realestateForm', 'homeSvcForm',
'eventsPackageForm', 'eventsCustomizedForm', 'eventsPremiumForm', 'courierForm'].forEach(formId => {
  const form = document.getElementById(formId);
  form.onsubmit = function(e){
    e.preventDefault();
    const name = this.querySelector('input[type=text]').value.trim();
    const mobile = this.querySelector('input[type=tel]').value.trim();
    const emailInput = this.querySelector('input[type=email]');
    const email = emailInput ? emailInput.value.trim() : '';
    const details = this.querySelector('textarea').value.trim();
    const prefixMap = {
      jobForm: 'Job Consultancy Inquiry',
      loansForm: 'Loans & Insurance Inquiry',
      toursForm: 'Tours & Travels Booking',
      realestateForm: 'Real Estate & Construction Inquiry',
      homeSvcForm: 'Home Service Inquiry',
      eventsPackageForm: 'Events Package Inquiry',
      eventsCustomizedForm: 'Events Customized Inquiry',
      eventsPremiumForm: 'Events Premium Inquiry',
      courierForm: 'Courier & Ride Booking Request'
    };
    const prefix = prefixMap[formId] || 'Inquiry';
    let message = `${prefix}\nName: ${name}\nMobile: ${mobile}\n`;
    if(email.length > 0) message += `Email: ${email}\n`;
    message += `Details: ${details}`;
    window.open('https://wa.me/918977143043?text=' + encodeURIComponent(message), '_blank');
  }
});
</script>
<script async defer src="https://maps.googleapis.com/maps/api/js?key=YOUR_API_KEY&callback=initMap"></script>
</body>
</html>
