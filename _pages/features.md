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
  max-width: 1200px;
  margin: 0 auto;
}

/* ===========================
   FEATURE GRID LAYOUT
   =========================== */
.feature-container {
  display: flex;
  flex-wrap: wrap;
  align-items: center; 
  gap: 60px;
  margin-bottom: 80px;
  padding-bottom: 40px;
  border-bottom: 1px solid #f5f5f5;
}

.feature-container.reverse {
  flex-direction: row-reverse;
}

.feature-container:last-child {
  border-bottom: none;
  margin-bottom: 0;
}

.feature-text {
  flex: 1 1 350px; 
  min-width: 300px;
}

.feature-text h3 {
  margin-top: 0;
  color: #333;
  margin-bottom: 20px;
  font-size: 1.75rem;
}

.feature-text p {
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
  flex: 2 1 500px;
  display: flex;
  gap: 25px;
  justify-content: center;
  align-items: center;
  flex-wrap: wrap;
}

/* ===========================
   SCREENSHOT STYLING
   =========================== */
.app-screenshot {
  width: 230px; 
  height: auto;
  border-radius: 24px;
  box-shadow: 0 20px 40px rgba(0,0,0,0.12), 0 5px 10px rgba(0,0,0,0.05);
  border: 1px solid #eee;
  transition: transform 0.3s ease;
  background-color: #fff;
  cursor: zoom-in; /* Indicates clickable */
}

.app-screenshot:hover {
  transform: translateY(-8px);
  z-index: 10;
}

/* Mobile Adjustments */
@media (max-width: 900px) {
  .feature-container {
    flex-direction: column-reverse;
    gap: 30px;
    text-align: left;
  }
  
  .feature-container.reverse {
    flex-direction: column-reverse;
  }

  .feature-visual {
    width: 100%;
    flex: 1 1 auto;
  }
  
  .app-screenshot {
    max-width: 45%; 
    width: auto;
  }
}

/* ===========================
   LIGHTBOX / MODAL STYLES
   =========================== */
.modal {
  display: none; 
  position: fixed; 
  z-index: 10000; 
  left: 0; top: 0;
  width: 100%; height: 100%; 
  overflow: auto; 
  background-color: rgba(0,0,0,0.9); 
  backdrop-filter: blur(5px);
}

.modal-content {
  margin: auto;
  display: block;
  max-width: 90%;
  max-height: 85vh;
  margin-top: 60px;
  border-radius: 10px;
  box-shadow: 0 0 50px rgba(0,0,0,0.5);
  object-fit: contain;
}

.close-btn {
  position: absolute;
  top: 20px; right: 35px;
  color: #f1f1f1;
  font-size: 40px; font-weight: bold;
  cursor: pointer; z-index: 10001;
  transition: 0.3s;
}
.close-btn:hover { color: #bbb; }

.prev, .next {
  cursor: pointer;
  position: absolute; top: 50%;
  padding: 16px; margin-top: -50px;
  color: white; font-weight: bold; font-size: 30px;
  transition: 0.3s; user-select: none;
  border-radius: 3px;
}
.next { right: 0; border-radius: 3px 0 0 3px; }
.prev { left: 0; border-radius: 0 3px 3px 0; }
.prev:hover, .next:hover { background-color: rgba(255,255,255,0.1); }

#caption {
  text-align: center; color: #ccc; padding: 10px 0; font-size: 18px;
}
</style>

<div class="tab">
  <button class="tablinks main-feature" data-tab="Organize">Organize</button>
  <button class="tablinks main-feature" data-tab="Use">Use</button>
  <button class="tablinks main-feature" data-tab="Maintain">Maintain</button>
  <button class="tablinks main-feature" data-tab="Analyze">Analyze</button>
  
  <button class="tablinks secondary-feature separator" data-tab="Export">Export</button>
  <button class="tablinks secondary-feature" data-tab="Secure">Secure</button>
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
      <img src="/assets/images/Guns_List.jpeg" alt="Gun List Interface" class="app-screenshot">
      <img src="/assets/images/Guns_Gallery.jpeg" alt="Gun Gallery View" class="app-screenshot">
      <img src="/assets/images/Guns_Details.jpeg" alt="Gun Details Screen" class="app-screenshot">      
    </div>
  </div>

  <div class="feature-container reverse"> 
    <div class="feature-text">
      <h3>Inventory Management</h3>
      <p>Keep your supplies organized and accessible.</p>
      <ul>
        <li><strong>Ammo Stockpile:</strong> Track inventory by caliber, grain, and manufacturer. Know exactly how many rounds of training vs. defensive ammo you have on hand.</li>
        <li><strong>Gear & Accessories:</strong> Catalog holsters, optics, lights, and modifications. Assign them to specific firearms to build virtual loadouts.</li>
        <li><strong>Photo Documentation:</strong> Attach high-resolution photos to every item to document condition, custom markings, and receipts.</li>
      </ul>
    </div>
    <div class="feature-visual">
      <img src="/assets/images/Ammo_List.jpeg" alt="Ammo List Interface" class="app-screenshot">

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
      <img src="/assets/images/Range_Session_List.jpeg" alt="Range Sessions" class="app-screenshot">
      <img src="/assets/images/Range_Session_Details.jpeg" alt="Range Session Details" class="app-screenshot">
      <img src="/assets/images/Range_Drills_List.jpeg" alt="Drills List" class="app-screenshot">         
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
      <img src="/assets/images/Maintenance_Sessions_List.jpeg" alt="Maintenance Sessions" class="app-screenshot">
      <img src="/assets/images/Maintenance_Sessions_Details.jpeg" alt="Maintenance Session Details" class="app-screenshot">
      <img src="/assets/images/Maintenance_Sessions_Upsert.jpeg" alt="Maintenance Session Upsert" class="app-screenshot">         
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
      <img src="/assets/images/Collection_Health.jpeg" alt="Collection Health" class="app-screenshot">
      <img src="/assets/images/Gun_Health_Healthy.jpeg" alt="Gun Health Healthy" class="app-screenshot">
      <img src="/assets/images/Gun_Health_Unhealthy.jpeg" alt="Gun Health Unhealthy" class="app-screenshot">        
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
      <img src="/assets/images/Collection_Usage_Stats.jpeg" alt="Collection-level Usage Dashboard" class="app-screenshot">
      <img src="/assets/images/Collection_Usage_Stats_2.jpeg" alt="Collection-level Dashboard" class="app-screenshot">
      <img src="/assets/images/Gun_Usage_Stats.jpeg" alt="Individual Gun Stats" class="app-screenshot">       
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
          <img src="/assets/images/User_Stats.jpeg" alt="User Dashboard" class="app-screenshot">
          <img src="/assets/images/Ammo_Usage_Stats.jpg" alt="Individual Ammo Stats" class="app-screenshot">          
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
          <img src="/assets/images/Reports_Report_List.jpeg" alt="Report List" class="app-screenshot">
          <img src="/assets/images/Reports_Gun_Catalog_Cover.jpeg" alt="Gun Catalog Cover" class="app-screenshot">
          <img src="/assets/images/Reports_Gun_Catalog_Item.jpeg" alt="Gun Catalog Item" class="app-screenshot">
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
          <img src="/assets/images/Reports_Gun_Inventory.jpeg" alt="Gun Inventory" class="app-screenshot">
          <img src="/assets/images/Reports_Ammo_List.jpeg" alt="Ammo Inventory" class="app-screenshot">
          <img src="/assets/images/Exports_CSV_List.jpeg" alt="CSV Exports" class="app-screenshot">    
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

<div id="imageModal" class="modal">
  <span class="close-btn">&times;</span>
  <a class="prev">&#10094;</a>
  <a class="next">&#10095;</a>
  <img class="modal-content" id="modalImg">
  <div id="caption"></div>
</div>

<script>
$(document).ready(function() {

    // ============================
    // 1. TAB LOGIC
    // ============================
    function switchTab(tabId) {
        $('.tabcontent').hide();
        $('.tablinks').removeClass('active');
        $('#' + tabId).fadeIn(400);
        $('.tablinks[data-tab="' + tabId + '"]').addClass('active');
    }

    $('.tablinks').on('click', function() {
        var tabId = $(this).data('tab');
        switchTab(tabId);
        if(history.pushState) {
            history.pushState(null, null, '#' + tabId);
        } else {
            location.hash = '#' + tabId;
        }
    });

    // Initial Load
    var hash = window.location.hash.substring(1);
    if (hash && $('#' + hash).length) {
        switchTab(hash);
    } else {
        switchTab('Organize');
    }

    // ============================
    // 2. SLIDESHOW / LIGHTBOX LOGIC
    // ============================
    var $galleryImages; // Stores images of current tab
    var currentIndex = 0;

    // Open Modal on Click
    $('.app-screenshot').on('click', function() {
        // Find images ONLY in the current visible tab
        var $parentTab = $(this).closest('.tabcontent');
        $galleryImages = $parentTab.find('.app-screenshot');
        
        // Find index of clicked image
        currentIndex = $galleryImages.index(this);
        
        updateModal();
        $('#imageModal').fadeIn(300);
    });

    // Close Modal (Click X or Outside)
    $('.close-btn, .modal').on('click', function(e) {
        if (e.target !== this) return; // Don't close if clicking the image
        $('#imageModal').fadeOut(300);
    });

    // Navigate Next/Prev
    $('.next').on('click', function(e) {
        e.stopPropagation(); // Prevent closing modal
        changeSlide(1);
    });
    $('.prev').on('click', function(e) {
        e.stopPropagation();
        changeSlide(-1);
    });

    function changeSlide(direction) {
        currentIndex += direction;
        // Loop logic
        if (currentIndex >= $galleryImages.length) currentIndex = 0;
        if (currentIndex < 0) currentIndex = $galleryImages.length - 1;
        updateModal();
    }

    function updateModal() {
        var $img = $galleryImages.eq(currentIndex);
        $('#modalImg').attr('src', $img.attr('src'));
        $('#caption').text($img.attr('alt'));
    }

    // Keyboard Navigation
    $(document).on('keydown', function(e) {
        if ($('#imageModal').is(':visible')) {
            if (e.key === "Escape") $('#imageModal').fadeOut(300);
            if (e.key === "ArrowRight") changeSlide(1);
            if (e.key === "ArrowLeft") changeSlide(-1);
        }
    });

});
</script>