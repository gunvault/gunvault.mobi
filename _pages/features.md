---
layout: page
title: Features
include_in_header: true
permalink: /features/
---

<style>
/* Style the tab container */
.tab {
  overflow: hidden;
  border-bottom: 2px solid #f1f1f1;
  margin-bottom: 30px;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
}

/* === BASE BUTTON STYLE === */
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

/* === MAIN FEATURES (Organize, Use, Maintain, Analyze) === */
/* These are bolder and darker */
.tab button.main-feature {
  font-size: 17px;
  font-weight: 700;
  color: #222;
}

/* === SECONDARY FEATURES (Export, Secure) === */
/* These are slightly smaller and lighter */
.tab button.secondary-feature {
  font-size: 15px;
  font-weight: 500;
  color: #888;
}

/* === THE GAP/DIVIDER === */
/* This adds the visual line between Analyze and Export */
.tab button.separator {
  margin-left: 20px;
  padding-left: 30px;
  border-left: 2px solid #eee; 
}

/* Change background color of buttons on hover */
.tab button:hover {
  background-color: #f9f9f9;
  color: #000;
}

/* Create an active/current tablink class */
.tab button.active {
  border-bottom: 3px solid #007bff; /* Change to your brand color */
  color: #000;
}

/* Style the tab content */
.tabcontent {
  display: none;
  padding: 10px 20px;
  animation: fadeEffect 0.4s;
  max-width: 900px; /* Keep content readable width */
  margin: 0 auto;   /* Center content */
}

/* Fade in animation */
@keyframes fadeEffect {
  from {opacity: 0; transform: translateY(5px);}
  to {opacity: 1; transform: translateY(0);}
}

/* Formatting for headers inside tabs */
.tabcontent h3 {
  margin-top: 0;
  color: #333;
  border-bottom: 1px solid #eee;
  padding-bottom: 10px;
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

<div id="Organize" class="tabcontent" markdown="1">

### Digital Armory
Create a comprehensive digital twin of your physical collection.
- **Detailed Records:** Log every specific attribute including make, model, caliber, barrel length, and action type.
- **Serial Number Tracking:** Securely store serial numbers for insurance and identification.
- **Financial Data:** Track purchase dates, acquisition costs, and current estimated values to understand your investment.

### Inventory Management
Keep your supplies organized and accessible.
- **Ammo Stockpile:** Track inventory by caliber, grain, and manufacturer. Know exactly how many rounds of training vs. defensive ammo you have on hand.
- **Gear & Accessories:** Catalog holsters, optics, lights, and modifications. Assign them to specific firearms to build virtual loadouts.
- **Photo Documentation:** Attach high-resolution photos to every item to document condition, custom markings, and receipts.
</div>

<div id="Use" class="tabcontent" markdown="1">

### Range & Training Log
Move beyond simple round counts. Treat your range sessions as a training diary.
- **Detailed Session Logging:** Record the date, firearms, and specific ammo used for every trip to the range.
- **Performance Metrics:** Track rounds fired versus rounds jammed to build a long-term reliability profile for every gun.
- **Drill Tracking:** Note specific drills status to monitor your skill progression.

### Usage History
Understand the lifecycle of your equipment.
- **Barrel Log:** Automatically aggregate round counts from your sessions to track total barrel wear over time.
- **Ammo Consumption:** See exactly which ammo was used in which firearms to correlate ammunition performance with reliability issues.
- **Visual Timeline:** Scroll through a history of your range visits to see your frequency and training consistency.
</div>

<div id="Maintain" class="tabcontent" markdown="1">

### Service Records
Protect your investment with a dedicated maintenance log.
- **Maintenance History:** Keep a digital service record for every firearm. Log cleaning dates, springs changed, parts replaced, and gunsmithing notes.
- **Task Tracking:** Define specific actions performed (e.g., "Deep Clean," "Sight Adjustment," "Lubrication") to maintain a standard of care.

### Proactive Care
Prevent issues before they happen.
- **Health Monitor:** See firearms that are "Neglected" or approaching high round counts without recent service.
- **Interval Management:** Quickly identify guns that haven't been cleaned in 6+ months or 1,000+ rounds, ensuring nothing rusts in the back of the safe.
- **Reliability Correlation:** Compare maintenance dates with range failure rates to see if your cleaning schedule affects performance.
</div>

<div id="Analyze" class="tabcontent" markdown="1">

### Collection Analytics
Turn data into actionable insights.
- **Armory Dashboard:** Get a bird's-eye view of your entire collection. Track total monetary value, total volume fired, and overall reliability across your vault.
- **Visual Meters:** Instantly gauge the "Volume" (total rounds), "Frequency" (trips/month), "Intensity" (rounds/trip), and "Reliability" (jam rate) of your collection.

### Performance & Insights
Drill down into the details.
- **Gun-Level Stats:** View individual metrics for every firearm to compare which guns you shoot the most and which are the most reliable.
- **Ammo Insights:** Analyze specific ammo types to track failure rates and monitor your burn rate vs. restock rate.
- **Shooter Dashboard:** Visualize your personal progress with total rounds fired and activity statistics over the last year.
</div>

<div id="Export" class="tabcontent" markdown="1">

### Reporting Tools
Your data shouldn't be trapped in the app.
- **Insurance Reports:** Generate professional PDF reports listing all firearms, serial numbers, and values. Perfect for declaring value to insurance agents or filing claims after theft/fire.
- **Estate Planning:** Create a clear, cataloged list of assets to help family members identify items and values in the future.
- **Inventory Manifests:** Print physical checklists of your ammo and accessories to help with physical auditing and organizing your safe.

### Data Freedom
You own your data, always.
- **CSV Export:** Export your gun collection, ammo inventory, or range logs to CSV/Excel formats for custom spreadsheet analysis.
- **Backup Archives:** Create full data dumps to store on external hard drives or secure USB keys for redundancy.
- **Compliance Helper:** Quickly access acquisition dates and seller information if needed for legal or compliance checks.
</div>

<div id="Secure" class="tabcontent" markdown="1">

### Privacy by Design
We built GunVault with a "Zero-Knowledge" architecture.
- **No Accounts, No Servers:** We do not require a login. We do not have a database of your guns. Your data lives on your device or in your personal iCloud.
- **Offline First:** The app works fully offline. You can access your serial numbers and records even when you have no cell service or Wi-Fi.
- **Private Sync:** Sync data seamlessly across your iPhone, iPad, and Mac using Apple's CloudKit. The data is encrypted by Apple and accessible only by you.

### Data Sovereignty
Security features designed for peace of mind.
- **Device Security:** The app relies on your device's native security (FaceID/TouchID/Passcode) to prevent unauthorized physical access.
- **Network Isolation:** Because there is no 3rd-party server, there is no central "honey pot" of user data for hackers to target.
- **User Controlled Backups:** You control when and where your backups are stored, ensuring your digital armory is as secure as your physical one.
</div>

<script>
function openFeature(evt, featureName) {
  var i, tabcontent, tablinks;
  
  // 1. Hide all tab content
  tabcontent = document.getElementsByClassName("tabcontent");
  for (i = 0; i < tabcontent.length; i++) {
    tabcontent[i].style.display = "none";
  }
  
  // 2. Remove active class from all buttons
  tablinks = document.getElementsByClassName("tablinks");
  for (i = 0; i < tablinks.length; i++) {
    tablinks[i].className = tablinks[i].className.replace(" active", "");
  }
  
  // 3. Show the current tab
  var targetTab = document.getElementById(featureName);
  if (targetTab) {
      targetTab.style.display = "block";
  }
  
  // 4. Add active class to the clicked button
  if (evt) {
    evt.currentTarget.className += " active";
    // Update URL hash
    if(history.pushState) {
        history.pushState(null, null, '#' + featureName);
    } else {
        location.hash = '#' + featureName;
    }
  } else {
      // If triggered by page load (no event), find button by matching onclick text
      for (i = 0; i < tablinks.length; i++) {
          if (tablinks[i].getAttribute('onclick').includes(featureName)) {
              tablinks[i].className += " active";
          }
      }
  }
}

// 5. Handle Page Load (Deep Linking)
document.addEventListener("DOMContentLoaded", function() {
    var hash = window.location.hash.substring(1); // Remove the #
    if (hash && document.getElementById(hash)) {
        openFeature(null, hash);
    } else {
        document.getElementById("defaultOpen").click();
    }
});
</script>