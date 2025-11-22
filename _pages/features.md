---
layout: page
title: Features
include_in_header: true
permalink: /features/
order: 2
---

<style>
/* ===========================
   TAB NAVIGATION STYLES
   =========================== */
.tab {
  overflow: hidden;
  border-bottom: 2px solid #f1f1f1;
  margin-bottom: 50px;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
}

.tab button {
  background-color: inherit;
  border: none;
  outline: none;
  cursor: pointer;
  padding: 14px 24px;
  transition: 0.3s;
  font-family: inherit;
  border-bottom: 3px solid transparent;
}

.tab button.main-feature {
  font-size: 17px;
  font-weight: 700;
  color: #222;
}

.tab button.secondary-feature {
  font-size: 15px;
  font-weight: 500;
  color: #888;
}

.tab button.separator {
  margin-left: 20px;
  padding-left: 30px;
  border-left: 2px solid #eee; 
}

.tab button:hover {
  background-color: #f9f9f9;
  color: #000;
}

.tab button.active {
  border-bottom: 3px solid #007bff;
  color: #000;
}

/* ===========================
   TAB CONTENT WRAPPER
   =========================== */
.tabcontent {
  display: none;
  padding: 10px 0px;
  animation: fadeEffect 0.4s;
  max-width: 1200px; /* Wide enough for side-by-side layout */
  margin: 0 auto;
}

@keyframes fadeEffect {
  from {opacity: 0; transform: translateY(5px);}
  to {opacity: 1; transform: translateY(0);}
}

/* ===========================
   FEATURE GRID LAYOUT (UPDATED)
   =========================== */
.feature-container {
  display: flex;
  flex-wrap: wrap;
  
  /* FIX 1: Vertically center text. 
     This solves the "Short Text / Tall Image" whitespace issue. */
  align-items: center; 
  
  gap: 60px; /* Generous gap between text and phone */
  margin-bottom: 80px;
  padding-bottom: 40px;
  border-bottom: 1px solid #f5f5f5;
}

/* Optional: Use this class <div class="feature-container reverse"> to flip text/image side */
.feature-container.reverse {
  flex-direction: row-reverse;
}

.feature-container:last-child {
  border-bottom: none;
  margin-bottom: 0;
}

.feature-text {
  /* Text takes up less space, allowing images to breathe */
  flex: 1 1 350px; 
  min-width: 300px;
}

/* Typography within features */
.feature-text h3 {
  margin-top: 0;
  color: #333;
  margin-bottom: 20px;
  font-size: 1.75rem;
}

.feature-text p {
  /* font-size: 1.1rem; */
  line-height: 1.6;
  color: #444;
  margin-bottom: 20px;
}

.feature-text ul {
  padding-left: 20px;
  margin-bottom: 15px;
}

.feature-text li {
  margin-bottom: 12px;
  line-height: 1.5;
  color: #555;
}

.feature-visual {
  /* FIX 2: Make visual container wider (500px basis).
     This encourages the browser to put 2 phones side-by-side
     instead of stacking them vertically. */
  flex: 2 1 500px;
  
  display: flex;
  gap: 25px;
  justify-content: center; /* Centers 1 image, or centers the group of 2 */
  align-items: center;
  flex-wrap: wrap;
}

/* ===========================
   SCREENSHOT STYLING
   =========================== */
.app-screenshot {
  /* FIX 3: Slightly smaller width ensures 2 phones fit on standard laptop screens */
  width: 230px; 
  height: auto;
  border-radius: 24px;
  box-shadow: 0 20px 40px rgba(0,0,0,0.12), 0 5px 10px rgba(0,0,0,0.05);
  border: 1px solid #eee;
  transition: transform 0.3s ease;
  background-color: #fff;
}

.app-screenshot:hover {
  transform: translateY(-8px);
  z-index: 10;
}

/* Mobile Adjustments */
@media (max-width: 900px) {
  .feature-container {
    flex-direction: column-reverse; /* Images on top, Text on bottom */
    gap: 30px;
    text-align: left;
  }
  
  .feature-container.reverse {
    flex-direction: column-reverse; /* Keep consistent on mobile */
  }

  .feature-visual {
    width: 100%;
    flex: 1 1 auto;
  }
  
  .app-screenshot {
    /* On mobile, make them small enough to sit side-by-side */
    max-width: 45%; 
    width: auto;
  }
}
</style>

<div class="tab">
  <button class="tablinks main-feature" onclick="openFeature(event, 'Organize')" id="defaultOpen">Organize</button>
  <button class="tablinks main-feature" onclick="openFeature(event, 'Use')">Use</button>
  <button class="tablinks main-feature" onclick="openFeature(event, 'Maintain')">Maintain</button>
  <button class="tablinks main-feature" onclick="openFeature(event, 'Analyze')">Analyze</button>
  
  <button class="tablinks secondary-feature separator" onclick="openFeature(event, 'Export')">Export</button>
  <button class="tablinks secondary-feature" onclick="openFeature(event, 'Secure')">Secure</button>
</div>

<div id="Organize" class="tabcontent">

  <div class="feature-container">
    <div class="feature-text">
      <h3>Digital Armory</h3>
      <p>Create a comprehensive digital twin of your physical collection.</p>
      <ul>
        <li><strong>Detailed Records:</strong> Log every specific attribute including make, model, caliber, barrel length, and action type.</li>
        <li><strong>Serial Number Tracking:</strong> Securely store serial numbers for insurance and identification.</li>
        <li><strong>Financial Data:</strong> Track purchase dates, acquisition costs, and current estimated values to understand your investment.</li>
      </ul>
    </div>
    <div class="feature-visual">
      <img src="/assets/images/Guns_List.png" alt="Gun List Interface" class="app-screenshot">
    </div>
  </div>

  <div class="feature-container reverse"> <div class="feature-text">
      <h3>Inventory Management</h3>
      <p>Keep your supplies organized and accessible.</p>
      <ul>
        <li><strong>Ammo Stockpile:</strong> Track inventory by caliber, grain, and manufacturer. Know exactly how many rounds of training vs. defensive ammo you have on hand.</li>
        <li><strong>Gear & Accessories:</strong> Catalog holsters, optics, lights, and modifications. Assign them to specific firearms to build virtual loadouts.</li>
        <li><strong>Photo Documentation:</strong> Attach high-resolution photos to every item to document condition, custom markings, and receipts.</li>
      </ul>
    </div>
    <div class="feature-visual">
      <img src="/assets/images/Guns_Gallery.png" alt="Gun Gallery View" class="app-screenshot">
      <img src="/assets/images/Guns_Details.png" alt="Gun Details Screen" class="app-screenshot">
    </div>
  </div>

</div>

<div id="Use" class="tabcontent">

  <div class="feature-container">
    <div class="feature-text">
      <h3>Range & Training Log</h3>
      <p>Move beyond simple round counts. Treat your range sessions as a training diary.</p>
      <ul>
        <li><strong>Detailed Session Logging:</strong> Record the date, firearms, and specific ammo used for every trip to the range.</li>
        <li><strong>Performance Metrics:</strong> Track rounds fired versus rounds jammed to build a long-term reliability profile for every gun.</li>
        <li><strong>Drill Tracking:</strong> Note specific drills status to monitor your skill progression.</li>
      </ul>
    </div>
    <div class="feature-visual">
      </div>
  </div>

  <div class="feature-container">
    <div class="feature-text">
      <h3>Usage History</h3>
      <p>Understand the lifecycle of your equipment.</p>
      <ul>
        <li><strong>Barrel Log:</strong> Automatically aggregate round counts from your sessions to track total barrel wear over time.</li>
        <li><strong>Ammo Consumption:</strong> See exactly which ammo was used in which firearms to correlate ammunition performance with reliability issues.</li>
        <li><strong>Visual Timeline:</strong> Scroll through a history of your range visits to see your frequency and training consistency.</li>
      </ul>
    </div>
    <div class="feature-visual">
      </div>
  </div>

</div>

<div id="Maintain" class="tabcontent">

  <div class="feature-container">
    <div class="feature-text">
      <h3>Service Records</h3>
      <p>Protect your investment with a dedicated maintenance log.</p>
      <ul>
        <li><strong>Maintenance History:</strong> Keep a digital service record for every firearm. Log cleaning dates, springs changed, parts replaced, and gunsmithing notes.</li>
        <li><strong>Task Tracking:</strong> Define specific actions performed (e.g., "Deep Clean," "Sight Adjustment," "Lubrication") to maintain a standard of care.</li>
      </ul>
    </div>
    <div class="feature-visual">
      </div>
  </div>

  <div class="feature-container">
    <div class="feature-text">
      <h3>Proactive Care</h3>
      <p>Prevent issues before they happen.</p>
      <ul>
        <li><strong>Health Monitor:</strong> See firearms that are "Neglected" or approaching high round counts without recent service.</li>
        <li><strong>Interval Management:</strong> Quickly identify guns that haven't been cleaned in 6+ months or 1,000+ rounds, ensuring nothing rusts in the back of the safe.</li>
        <li><strong>Reliability Correlation:</strong> Compare maintenance dates with range failure rates to see if your cleaning schedule affects performance.</li>
      </ul>
    </div>
    <div class="feature-visual">
      </div>
  </div>

</div>

<div id="Analyze" class="tabcontent">

  <div class="feature-container">
    <div class="feature-text">
      <h3>Collection Analytics</h3>
      <p>Turn data into actionable insights.</p>
      <ul>
        <li><strong>Armory Dashboard:</strong> Get a bird's-eye view of your entire collection. Track total monetary value, total volume fired, and overall reliability across your vault.</li>
        <li><strong>Visual Meters:</strong> Instantly gauge the "Volume" (total rounds), "Frequency" (trips/month), "Intensity" (rounds/trip), and "Reliability" (jam rate) of your collection.</li>
      </ul>
    </div>
    <div class="feature-visual">
      </div>
  </div>

  <div class="feature-container">
    <div class="feature-text">
      <h3>Performance & Insights</h3>
      <p>Drill down into the details.</p>
      <ul>
        <li><strong>Gun-Level Stats:</strong> View individual metrics for every firearm to compare which guns you shoot the most and which are the most reliable.</li>
        <li><strong>Ammo Insights:</strong> Analyze specific ammo types to track failure rates and monitor your burn rate vs. restock rate.</li>
        <li><strong>Shooter Dashboard:</strong> Visualize your personal progress with total rounds fired and activity statistics over the last year.</li>
      </ul>
    </div>
    <div class="feature-visual">
      </div>
  </div>

</div>

<div id="Export" class="tabcontent">

  <div class="feature-container">
    <div class="feature-text">
      <h3>Reporting Tools</h3>
      <p>Your data shouldn't be trapped in the app.</p>
      <ul>
        <li><strong>Insurance Reports:</strong> Generate professional PDF reports listing all firearms, serial numbers, and values. Perfect for declaring value to insurance agents or filing claims after theft/fire.</li>
        <li><strong>Estate Planning:</strong> Create a clear, cataloged list of assets to help family members identify items and values in the future.</li>
        <li><strong>Inventory Manifests:</strong> Print physical checklists of your ammo and accessories to help with physical auditing and organizing your safe.</li>
      </ul>
    </div>
    <div class="feature-visual">
       </div>
  </div>

  <div class="feature-container">
    <div class="feature-text">
      <h3>Data Freedom</h3>
      <p>You own your data, always.</p>
      <ul>
        <li><strong>CSV Export:</strong> Export your gun collection, ammo inventory, or range logs to CSV/Excel formats for custom spreadsheet analysis.</li>
        <li><strong>Backup Archives:</strong> Create full data dumps to store on external hard drives or secure USB keys for redundancy.</li>
        <li><strong>Compliance Helper:</strong> Quickly access acquisition dates and seller information if needed for legal or compliance checks.</li>
      </ul>
    </div>
    <div class="feature-visual">
       </div>
  </div>

</div>

<div id="Secure" class="tabcontent">

  <div class="feature-container">
    <div class="feature-text">
      <h3>Privacy by Design</h3>
      <p>We built GunVault with a "Zero-Knowledge" architecture.</p>
      <ul>
        <li><strong>No Accounts, No Servers:</strong> We do not require a login. We do not have a database of your guns. Your data lives on your device or in your personal iCloud.</li>
        <li><strong>Offline First:</strong> The app works fully offline. You can access your serial numbers and records even when you have no cell service or Wi-Fi.</li>
        <li><strong>Private Sync:</strong> Sync data seamlessly across your iPhone, iPad, and Mac using Apple's CloudKit. The data is encrypted by Apple and accessible only by you.</li>
      </ul>
    </div>
    <div class="feature-visual">
       </div>
  </div>

  <div class="feature-container">
    <div class="feature-text">
      <h3>Data Sovereignty</h3>
      <p>Security features designed for peace of mind.</p>
      <ul>
        <li><strong>Device Security:</strong> The app relies on your device's native security (FaceID/TouchID/Passcode) to prevent unauthorized physical access.</li>
        <li><strong>Network Isolation:</strong> Because there is no 3rd-party server, there is no central "honey pot" of user data for hackers to target.</li>
        <li><strong>User Controlled Backups:</strong> You control when and where your backups are stored, ensuring your digital armory is as secure as your physical one.</li>
      </ul>
    </div>
    <div class="feature-visual">
       </div>
  </div>

</div>

<script>
function openFeature(evt, featureName) {
  var i, tabcontent, tablinks;
  
  tabcontent = document.getElementsByClassName("tabcontent");
  for (i = 0; i < tabcontent.length; i++) {
    tabcontent[i].style.display = "none";
  }
  
  tablinks = document.getElementsByClassName("tablinks");
  for (i = 0; i < tablinks.length; i++) {
    tablinks[i].className = tablinks[i].className.replace(" active", "");
  }
  
  var targetTab = document.getElementById(featureName);
  if (targetTab) {
      targetTab.style.display = "block";
  }
  
  if (evt) {
    evt.currentTarget.className += " active";
    if(history.pushState) {
        history.pushState(null, null, '#' + featureName);
    } else {
        location.hash = '#' + featureName;
    }
  } else {
      for (i = 0; i < tablinks.length; i++) {
          if (tablinks[i].getAttribute('onclick').includes(featureName)) {
              tablinks[i].className += " active";
          }
      }
  }
}

document.addEventListener("DOMContentLoaded", function() {
    var hash = window.location.hash.substring(1); 
    if (hash && document.getElementById(hash)) {
        openFeature(null, hash);
    } else {
        document.getElementById("defaultOpen").click();
    }
});
</script>