index.html<!DOCTYPE html>
<html lang="am">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
    <title>Lawyers for Ethiopia | የህግ ባለሞያ ለኢትዮጵያ</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;400;500;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        body {
            font-family: 'Inter', sans-serif;
            background: #f8fafc;
            color: #0f172a;
            line-height: 1.5;
        }
        .header {
            background: linear-gradient(135deg, #0a2b3e 0%, #1e4a6e 100%);
            color: white;
            padding: 1rem 2rem;
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: 0 4px 12px rgba(0,0,0,0.1);
        }
        .header-container {
            max-width: 1400px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 1rem;
        }
        .logo-area {
            display: flex;
            align-items: center;
            gap: 1rem;
        }
        .profile-photo {
            width: 65px;
            height: 65px;
            background: #f59e0b;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            overflow: hidden;
            border: 2px solid #ffd966;
        }
        .profile-photo img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        .site-title h1 {
            font-size: 1.5rem;
            font-weight: 700;
        }
        .site-title p {
            font-size: 0.85rem;
            opacity: 0.9;
        }
        .lang-switch {
            display: flex;
            gap: 0.5rem;
            background: rgba(255,255,255,0.2);
            padding: 0.4rem 0.8rem;
            border-radius: 40px;
        }
        .lang-btn {
            background: none;
            border: none;
            color: white;
            font-weight: 600;
            cursor: pointer;
            padding: 0.3rem 0.8rem;
            border-radius: 30px;
            transition: all 0.2s;
        }
        .lang-btn.active {
            background: #f59e0b;
            color: #0f172a;
        }
        .container {
            max-width: 1400px;
            margin: 2rem auto;
            padding: 0 2rem;
        }
        .admin-panel {
            background: white;
            border-radius: 20px;
            padding: 1.5rem;
            margin-bottom: 2rem;
            box-shadow: 0 4px 14px rgba(0,0,0,0.05);
            border: 1px solid #e2e8f0;
            display: none;
        }
        .admin-panel.show {
            display: block;
        }
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 1.8rem;
            margin-bottom: 2rem;
        }
        .card {
            background: white;
            border-radius: 24px;
            padding: 1.5rem;
            box-shadow: 0 4px 12px rgba(0,0,0,0.05);
            border: 1px solid #e2e8f0;
            transition: 0.2s;
        }
        .card:hover {
            transform: translateY(-4px);
            box-shadow: 0 12px 24px rgba(0,0,0,0.1);
        }
        .card i {
            font-size: 2.2rem;
            color: #1e4a6e;
            margin-bottom: 1rem;
        }
        .btn {
            background: #1e4a6e;
            color: white;
            border: none;
            padding: 0.7rem 1.3rem;
            border-radius: 40px;
            font-weight: 500;
            cursor: pointer;
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
            transition: 0.2s;
        }
        .btn-warning {
            background: #f59e0b;
            color: #0f172a;
        }
        .btn-outline {
            background: transparent;
            border: 1px solid #1e4a6e;
            color: #1e4a6e;
        }
        .payment-options {
            background: #fef9e3;
            padding: 1rem;
            border-radius: 16px;
            margin: 1rem 0;
        }
        .social-links {
            display: flex;
            gap: 1rem;
            flex-wrap: wrap;
            margin-top: 1rem;
        }
        .social-link {
            background: #eef2ff;
            padding: 0.5rem 1rem;
            border-radius: 40px;
            text-decoration: none;
            color: #0f172a;
            font-weight: 500;
            transition: 0.2s;
        }
        .social-link:hover {
            background: #1e4a6e;
            color: white;
        }
        .section {
            background: white;
            border-radius: 24px;
            padding: 1.8rem;
            margin-bottom: 2rem;
            border: 1px solid #e2e8f0;
        }
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0,0,0,0.7);
            justify-content: center;
            align-items: center;
            z-index: 2000;
        }
        .modal-content {
            background: white;
            padding: 2rem;
            border-radius: 28px;
            max-width: 500px;
            width: 90%;
        }
        footer {
            text-align: center;
            padding: 2rem;
            background: #0f172a;
            color: #94a3b8;
            margin-top: 2rem;
        }
        .settings-cog {
            position: fixed;
            bottom: 30px;
            right: 30px;
            background: #1e4a6e;
            width: 55px;
            height: 55px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            box-shadow: 0 4px 12px rgba(0,0,0,0.3);
            z-index: 1500;
            color: white;
            font-size: 1.8rem;
            transition: 0.2s;
        }
        .settings-cog:hover {
            transform: scale(1.05);
            background: #0f3b55;
        }
        .settings-panel {
            position: fixed;
            top: 0;
            right: -450px;
            width: 450px;
            height: 100%;
            background: white;
            box-shadow: -2px 0 20px rgba(0,0,0,0.2);
            z-index: 1600;
            transition: right 0.3s ease;
            display: flex;
            flex-direction: column;
            overflow-y: auto;
        }
        .settings-panel.open {
            right: 0;
        }
        .settings-header {
            background: #0a2b3e;
            color: white;
            padding: 1.2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: sticky;
            top: 0;
        }
        .settings-body {
            padding: 1.5rem;
            flex: 1;
        }
        .setting-group {
            margin-bottom: 1.5rem;
            border-bottom: 1px solid #e2e8f0;
            padding-bottom: 1rem;
        }
        .setting-group label {
            display: block;
            font-weight: 600;
            margin-bottom: 0.5rem;
        }
        .setting-group input,
        .setting-group textarea,
        .setting-group select {
            width: 100%;
            padding: 0.5rem;
            border-radius: 8px;
            border: 1px solid #cbd5e1;
            font-family: inherit;
        }
        .btn-save {
            background: #10b981;
            color: white;
            width: 100%;
            margin-top: 1rem;
        }
        .overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0,0,0,0.4);
            z-index: 1550;
            display: none;
        }
        .overlay.show {
            display: block;
        }
        @media (max-width: 768px) {
            .container {
                padding: 0 1rem;
            }
            .settings-panel {
                width: 100%;
                right: -100%;
            }
        }
    </style>
</head>
<body>

<div class="header">
    <div class="header-container">
        <div class="logo-area">
            <div class="profile-photo" id="profilePhotoBtn">
                <img id="profileImg" src="" alt="Profile" style="display: none; width: 100%; height: 100%; object-fit: cover;">
                <i id="defaultIcon" class="fas fa-user-graduate" style="font-size: 2rem;"></i>
            </div>
            <div class="site-title">
                <h1 id="siteTitle">Lawyers for Ethiopia</h1>
                <p id="siteSubtitle">የህግ ባለሞያ ለኢትዮጵያ | Legal Excellence</p>
            </div>
        </div>
        <div class="lang-switch">
            <button class="lang-btn active" data-lang="am">አማርኛ</button>
            <button class="lang-btn" data-lang="en">English</button>
        </div>
    </div>
</div>

<div class="container">
    <!-- Admin Panel (only for Yonatan Dawit Mengistu) -->
    <div id="adminPanel" class="admin-panel">
        <div style="display: flex; justify-content: space-between; align-items: center;">
            <h3><i class="fas fa-lock"></i> <span id="adminWelcome">Administrator Panel | Yonatan Dawit Mengistu</span></h3>
            <button id="logoutAdminBtn" class="btn-outline" style="padding: 0.3rem 1rem;"><i class="fas fa-sign-out-alt"></i> Logout</button>
        </div>
        <p style="margin: 10px 0;">Manage content, add media, delete items, update rulings.</p>
        <div style="margin-top: 1rem;">
            <input type="text" id="newMediaTitle" placeholder="New media title" style="width: 60%;">
            <select id="newMediaType">
                <option value="document">Document</option>
                <option value="video">Video</option>
                <option value="image">Image</option>
                <option value="audio">Audio</option>
            </select>
            <button id="addMediaBtn" class="btn">➕ Add</button>
            <button id="deleteLastMediaBtn" class="btn-outline" style="margin-left: 10px;">🗑️ Delete Last</button>
        </div>
    </div>

    <!-- Services Grid -->
    <div class="services-grid">
        <div class="card">
            <i class="fas fa-gavel"></i>
            <h3 data-key="consultTitle">የህግ ማማከር</h3>
            <p data-key="consultDesc">ከባለሙያ የህግ ምክር ያግኙ። ጥያቄዎን ይላኩልን።</p>
            <button id="consultBtn" class="btn"><i class="fas fa-comments"></i> <span data-key="consultBtnText">አማክሩኝ</span></button>
        </div>
        <div class="card">
            <i class="fas fa-video"></i>
            <h3 data-key="mediaTitle">የህግ ትምህርቶች</h3>
            <p data-key="mediaDesc">በዶክመንት፣ ቪዲዮ፣ ምስል እና ድምጽ ቅጂ ይገኛሉ።</p>
            <button id="viewMediaBtn" class="btn-outline"><i class="fas fa-play-circle"></i> <span data-key="viewMedia">ይዘቶችን ይመልከቱ</span></button>
        </div>
        <div class="card">
            <i class="fas fa-chalkboard-user"></i>
            <h3 data-key="trainingTitle">ቋሚ የህግ ስልጠናዎች</h3>
            <p data-key="trainingDesc">የወንጀል፣ ንግድ፣ ውል ህጎች ላይ ሙያዊ ስልጠና።</p>
            <button id="trainingsBtn" class="btn"><i class="fas fa-certificate"></i> <span data-key="trainingsBtn">ስልጠናዎች</span></button>
        </div>
        <div class="card">
            <i class="fas fa-share-alt"></i>
            <h3 data-key="socialTitle">ማህበራዊ ሚዲያ ስራዎች</h3>
            <p data-key="socialDesc">ይቀላቀሉና ያጋሩ።</p>
            <div id="socialLinks" class="social-links"></div>
        </div>
    </div>

    <!-- Media Library -->
    <div class="section" id="mediaSection">
        <h2><i class="fas fa-database"></i> <span data-key="libraryTitle">የህግ ማውጫ</span></h2>
        <div id="mediaGrid" style="display: grid; grid-template-columns: repeat(auto-fill, minmax(260px, 1fr)); gap: 1rem; margin-top: 1rem;"></div>
    </div>

    <!-- Supreme Court Rulings with Payment -->
    <div class="section">
        <h2><i class="fas fa-balance-scale"></i> <span data-key="rulingTitle">የኢፌድሪ ሰበር ሰሚ ችሎት ውሳኔዎች</span></h2>
        <p data-key="rulingDesc">ከ500 ብር ክፍያ በኋላ ውሳኔዎችን በዘርፍ ፈልገው ያግኙ።</p>
        <div id="paymentOptions" class="payment-options"></div>
        <button id="purchaseRulingBtn" class="btn btn-warning"><i class="fas fa-key"></i> <span data-key="purchaseAccess">የውሳኔ ፍለጋ መብት ግዙ (500 ብር)</span></button>
        <div id="rulingSearchArea" style="display: none; margin-top: 1.5rem;">
            <select id="rulingCategoryFilter">
                <option value="all">ሁሉም ዘርፎች</option>
            </select>
            <input type="text" id="rulingSearchInput" placeholder="በውሳኔ ቁጥር ወይም ይዘት ፈልግ" style="width: 60%; margin: 0 0.5rem;">
            <button id="searchRulingBtn" class="btn">ፈልግ</button>
            <div id="rulingResults" style="background: #f1f5f9; border-radius: 16px; padding: 1rem; margin-top: 1rem;"></div>
        </div>
    </div>

    <!-- Join Prerequisites -->
    <div class="section">
        <h2><i class="fas fa-user-plus"></i> <span data-key="joinTitle">ዌብሳይቱን መቀላቀል ለሚፈልጉ</span></h2>
        <p data-key="joinDesc">ቅድመ ሁኔታዎችን ከማህበራዊ ሚዲያ አካውንቶቻችን ይመልከቱ።</p>
        <div id="joinSocialLinks" class="social-links"></div>
    </div>
</div>

<footer>
    <p>© 2025 Lawyers for Ethiopia | የህግ ባለሞያ ለኢትዮጵያ | Admin: Yonatan Dawit Mengistu (LLB)</p>
</footer>

<!-- Settings Cog & Panel -->
<div class="settings-cog" id="settingsCog"><i class="fas fa-cog"></i></div>
<div class="overlay" id="settingsOverlay"></div>
<div class="settings-panel" id="settingsPanel">
    <div class="settings-header">
        <span><i class="fas fa-sliders-h"></i> ⚙️ የዌብሳይት ማዋቀሪያ (Settings)</span>
        <button id="closeSettingsBtn" style="background: none; border: none; color: white; font-size: 1.8rem;">&times;</button>
    </div>
    <div class="settings-body">
        <div class="setting-group"><label>Site Title (Amharic)</label><input type="text" id="setTitleAm" placeholder="የህግ ባለሞያ ለኢትዮጵያ"></div>
        <div class="setting-group"><label>Site Title (English)</label><input type="text" id="setTitleEn" placeholder="Lawyers for Ethiopia"></div>
        <div class="setting-group"><label>Profile Image URL (e.g., profile.jpg)</label><input type="text" id="setProfilePic" placeholder="profile.jpg"></div>
        <div class="setting-group"><label>Commercial Bank Account</label><input type="text" id="setBank" value="1000417819437"></div>
        <div class="setting-group"><label>CBE / Telebirr Number</label><input type="text" id="setMobile" value="0951727278"></div>
        <div class="setting-group"><label>TikTok URL</label><input type="text" id="setTiktok" value="https://www.tiktok.com/@lawyersforethiopia"></div>
        <div class="setting-group"><label>Facebook URL</label><input type="text" id="setFacebook" value="https://www.facebook.com/Lawyeryonatandawit"></div>
        <div class="setting-group"><label>Telegram URL</label><input type="text" id="setTelegram" value="https://t.me/LAWYERSFORETHIOPIA"></div>
        <div class="setting-group"><label>Ruling Price (ETB)</label><input type="number" id="setRulingPrice" value="500"></div>
        <div class="setting-group"><label>Media Items (JSON)</label><textarea id="setMediaItems" rows="4"></textarea></div>
        <div class="setting-group"><label>Rulings (JSON)</label><textarea id="setRulings" rows="4"></textarea></div>
        <button id="saveSettingsBtn" class="btn-save"><i class="fas fa-save"></i> Save Settings</button>
        <button id="exportSettingsBtn" class="btn" style="background: #6c757d; margin-top: 0.5rem;"><i class="fas fa-download"></i> Export Config as JS</button>
        <p style="font-size: 0.75rem; margin-top: 1rem;">Changes saved in your browser. Use export to update GitHub file.</p>
    </div>
</div>

<!-- Consultation Modal -->
<div id="consultModal" class="modal">
    <div class="modal-content">
        <h3>📩 የህግ ማማከር አገልግሎት</h3>
        <textarea id="consultQuestion" rows="4" placeholder="የህግ ጥያቄዎን በዝርዝር ይጻፉ..." style="width: 100%; margin: 1rem 0;"></textarea>
        <button id="sendConsultBtn" class="btn">Send / ላክ</button>
        <button id="closeConsultBtn" class="btn-outline" style="margin-left: 0.5rem;">Close</button>
    </div>
</div>

<script>
    // -------------------- DEFAULT CONFIGURATION --------------------
    const defaultConfig = {
        siteTitle_am: "የህግ ባለሞያ ለኢትዮጵያ",
        siteTitle_en: "Lawyers for Ethiopia",
        siteSubtitle_am: "የህግ እውቀት ለሁሉም",
        siteSubtitle_en: "Legal Knowledge for Everyone",
        profileImageUrl: "",
        paymentBank: "1000417819437",
        paymentMobile: "0951727278",
        social: {
            tiktok: "https://www.tiktok.com/@lawyersforethiopia",
            facebook: "https://www.facebook.com/Lawyeryonatandawit",
            telegram: "https://t.me/LAWYERSFORETHIOPIA"
        },
        rulingPrice: 500,
        mediaItems: [
            { id: 1, type: "document", title: "የወንጀል ህግ ማውጫ", url: "#", desc: "የኢትዮጵያ ወንጀል ህግ ሰነድ" },
            { id: 2, type: "video", title: "የውል ህግ ትምህርት", url: "https://www.youtube.com/embed/dQw4w9WgXcQ", desc: "ቪዲዮ ማብራሪያ" },
            { id: 3, type: "image", title: "የንግድ ህግ ማጠቃለያ", url: "https://picsum.photos/id/1/200/150", desc: "ምስላዊ ማብራሪያ" }
        ],
        rulings: [
            { id: 1, category: "የወንጀል ህግ", caseNumber: "ሰበር 101/2012", summary: "የህይወት እስራት ውሳኔ", fileRef: "ሰ/ሰ/101" },
            { id: 2, category: "የንግድ ህግ", caseNumber: "ሰበር 45/2018", summary: "የንግድ ውል አለመፈጸም", fileRef: "ን/45/2018" },
            { id: 3, category: "የውል ህግ", caseNumber: "ሰበር 22/2020", summary: "የኪራይ ውል አለመከበር", fileRef: "ውል 22/2020" }
        ]
    };

    let config = JSON.parse(localStorage.getItem("lawyersEthiopiaConfig")) || defaultConfig;
    let currentLang = "am";
    let isAdmin = false;
    let rulingsAccess = false;

    // ---------- Helper Functions ----------
    function applyConfigToUI() {
        document.getElementById("siteTitle").innerText = currentLang === "am" ? config.siteTitle_am : config.siteTitle_en;
        document.getElementById("siteSubtitle").innerText = currentLang === "am" ? config.siteSubtitle_am : config.siteSubtitle_en;
        const profileImg = document.getElementById("profileImg");
        const defaultIcon = document.getElementById("defaultIcon");
        if (config.profileImageUrl && config.profileImageUrl.trim() !== "") {
            profileImg.src = config.profileImageUrl;
            profileImg.style.display = "block";
            defaultIcon.style.display = "none";
        } else {
            profileImg.style.display = "none";
            defaultIcon.style.display = "flex";
        }
        document.getElementById("paymentOptions").innerHTML = `<i class="fas fa-money-bill-wave"></i> <strong>${currentLang === "am" ? "የክፍያ አማራጮች:" : "Payment Options:"}</strong><br>🏦 Commercial Bank: <strong>${config.paymentBank}</strong><br>📱 CBE / Telebirr: <strong>${config.paymentMobile}</strong>`;
        
        const socialContainer = document.getElementById("socialLinks");
        const joinContainer = document.getElementById("joinSocialLinks");
        const socialHtml = `
            <a href="${config.social.tiktok}" target="_blank" class="social-link"><i class="fab fa-tiktok"></i> TikTok</a>
            <a href="${config.social.facebook}" target="_blank" class="social-link"><i class="fab fa-facebook"></i> Facebook</a>
            <a href="${config.social.telegram}" target="_blank" class="social-link"><i class="fab fa-telegram"></i> Telegram</a>
        `;
        socialContainer.innerHTML = socialHtml;
        joinContainer.innerHTML = socialHtml;
        
        renderMedia(config.mediaItems);
        updateRulingPriceText();
        populateCategoryFilter();
    }

    function renderMedia(mediaArray) {
        const grid = document.getElementById("mediaGrid");
        if (!grid) return;
        grid.innerHTML = "";
        mediaArray.forEach(item => {
            const card = document.createElement("div");
            card.style.background = "#fff";
            card.style.padding = "1rem";
            card.style.borderRadius = "16px";
            card.style.border = "1px solid #e2e8f0";
            let inner = "";
            if (item.type === "document") inner = `<i class="fas fa-file-pdf" style="font-size:2rem;"></i><h4>${item.title}</h4><p>${item.desc || ""}</p><a href="${item.url}" target="_blank">Open</a>`;
            else if (item.type === "video") inner = `<i class="fas fa-video"></i><h4>${item.title}</h4><iframe width="100%" height="150" src="${item.url}" frameborder="0"></iframe>`;
            else if (item.type === "image") inner = `<img src="${item.url}" width="100%" style="border-radius:12px;"><h4>${item.title}</h4>`;
            else if (item.type === "audio") inner = `<i class="fas fa-headphones"></i><h4>${item.title}</h4><audio controls src="${item.url}" style="width:100%"></audio>`;
            card.innerHTML = inner;
            grid.appendChild(card);
        });
    }

    function updateRulingPriceText() {
        const purchaseBtn = document.getElementById("purchaseRulingBtn");
        if (purchaseBtn) {
            purchaseBtn.innerHTML = `<i class="fas fa-key"></i> ${currentLang === "am" ? `የውሳኔ ፍለጋ መብት ግዙ (${config.rulingPrice} ብር)` : `Purchase Ruling Access (${config.rulingPrice} ETB)`}`;
        }
        const rulingDesc = document.querySelector("[data-key='rulingDesc']");
        if (rulingDesc) rulingDesc.innerText = currentLang === "am" ? `ከ${config.rulingPrice} ብር ክፍያ በኋላ ውሳኔዎችን ፈልገው ያግኙ።` : `After ${config.rulingPrice} ETB payment, you can search rulings.`;
    }

    function populateCategoryFilter() {
        const filterSelect = document.getElementById("rulingCategoryFilter");
        if (!filterSelect) return;
        const categories = [...new Set(config.rulings.map(r => r.category))];
        filterSelect.innerHTML = '<option value="all">ሁሉም / All</option>' + categories.map(c => `<option value="${c}">${c}</option>`).join('');
    }

    function searchRulings() {
        if (!rulingsAccess) {
            alert(currentLang === "am" ? "እባክዎ መጀመሪያ ክፍያ ያድርጉ!" : "Please make payment first!");
            return;
        }
        const category = document.getElementById("rulingCategoryFilter").value;
        const query = document.getElementById("rulingSearchInput").value.toLowerCase();
        const filtered = config.rulings.filter(r => (category === "all" || r.category === category) && (r.caseNumber.toLowerCase().includes(query) || r.summary.toLowerCase().includes(query)));
        const resultsDiv = document.getElementById("rulingResults");
        if (filtered.length === 0) resultsDiv.innerHTML = "<p>ምንም ውጤት አልተገኘም / No results</p>";
        else resultsDiv.innerHTML = filtered.map(r => `<div style="border-bottom:1px solid #cbd5e1; padding:0.5rem;"><strong>${r.caseNumber}</strong> (${r.category})<br>${r.summary}<br><small>ፋይል ቁጥር: ${r.fileRef}</small></div>`).join("");
    }

    // ---------- Admin Authentication ----------
    function promptAdmin() {
        let pwd = prompt("Enter admin password (የአስተዳዳሪ ይለፍ ቃል):");
        if (pwd === "yonatan2025") {
            isAdmin = true;
            document.getElementById("adminPanel").classList.add("show");
        } else if (pwd !== null) alert("Incorrect password / የይለፍ ቃል ተሳስቷል");
    }
    setTimeout(promptAdmin, 300);
    document.getElementById("logoutAdminBtn")?.addEventListener("click", () => {
        isAdmin = false;
        document.getElementById("adminPanel").classList.remove("show");
    });

    // Admin actions
    document.getElementById("addMediaBtn")?.addEventListener("click", () => {
        if (!isAdmin) return alert("Admin only");
        const title = document.getElementById("newMediaTitle").value;
        const type = document.getElementById("newMediaType").value;
        if (!title) return alert("Enter title");
        let url = "#";
        if (type === "video") url = "https://www.youtube.com/embed/dQw4w9WgXcQ";
        if (type === "image") url = "https://picsum.photos/id/20/200/150";
        if (type === "audio") url = "https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3";
        config.mediaItems.push({ id: Date.now(), type, title, url, desc: "New item" });
        localStorage.setItem("lawyersEthiopiaConfig", JSON.stringify(config));
        renderMedia(config.mediaItems);
        document.getElementById("newMediaTitle").value = "";
    });
    document.getElementById("deleteLastMediaBtn")?.addEventListener("click", () => {
        if (!isAdmin) return alert("Admin only");
        config.mediaItems.pop();
        localStorage.setItem("lawyersEthiopiaConfig", JSON.stringify(config));
        renderMedia(config.mediaItems);
    });

    // ---------- Settings Panel ----------
    const cog = document.getElementById("settingsCog");
    const panel = document.getElementById("settingsPanel");
    const overlay = document.getElementById("settingsOverlay");
    function openSettings() {
        document.getElementById("setTitleAm").value = config.siteTitle_am;
        document.getElementById("setTitleEn").value = config.siteTitle_en;
        document.getElementById("setProfilePic").value = config.profileImageUrl || "";
        document.getElementById("setBank").value = config.paymentBank;
        document.getElementById("setMobile").value = config.paymentMobile;
        document.getElementById("setTiktok").value = config.social.tiktok;
        document.getElementById("setFacebook").value = config.social.facebook;
        document.getElementById("setTelegram").value = config.social.telegram;
        document.getElementById("setRulingPrice").value = config.rulingPrice;
        document.getElementById("setMediaItems").value = JSON.stringify(config.mediaItems, null, 2);
        document.getElementById("setRulings").value = JSON.stringify(config.rulings, null, 2);
        panel.classList.add("open");
        overlay.classList.add("show");
    }
    function closeSettings() {
        panel.classList.remove("open");
        overlay.classList.remove("show");
    }
    cog.addEventListener("click", openSettings);
    document.getElementById("closeSettingsBtn").addEventListener("click", closeSettings);
    overlay.addEventListener("click", closeSettings);
    document.getElementById("saveSettingsBtn").addEventListener("click", () => {
        config.siteTitle_am = document.getElementById("setTitleAm").value;
        config.siteTitle_en = document.getElementById("setTitleEn").value;
        config.profileImageUrl = document.getElementById("setProfilePic").value;
        config.paymentBank = document.getElementById("setBank").value;
        config.paymentMobile = document.getElementById("setMobile").value;
        config.social.tiktok = document.getElementById("setTiktok").value;
        config.social.facebook = document.getElementById("setFacebook").value;
        config.social.telegram = document.getElementById("setTelegram").value;
        config.rulingPrice = parseInt(document.getElementById("setRulingPrice").value) || 500;
        try {
            config.mediaItems = JSON.parse(document.getElementById("setMediaItems").value);
            config.rulings = JSON.parse(document.getElementById("setRulings").value);
        } catch(e) { alert("Invalid JSON"); return; }
        localStorage.setItem("lawyersEthiopiaConfig", JSON.stringify(config));
        applyConfigToUI();
        updateLanguage();
        closeSettings();
        alert("Settings saved! Page updated.");
    });
    document.getElementById("exportSettingsBtn").addEventListener("click", () => {
        const exportCode = `// Generated config for Lawyers for Ethiopia\nconst CONFIG = ${JSON.stringify(config, null, 2)};`;
        const blob = new Blob([exportCode], {type: "text/javascript"});
        const a = document.createElement("a");
        a.href = URL.createObjectURL(blob);
        a.download = "lawyers_config.js";
        a.click();
        URL.revokeObjectURL(blob);
    });

    // ---------- Language Translations ----------
    const translations = {
        am: {
            consultTitle: "የህግ ማማከር",
            consultDesc: "ከባለሙያ የህግ ምክር ያግኙ።",
            consultBtnText: "አማክሩኝ",
            mediaTitle: "የህግ ትምህርቶች",
            mediaDesc: "በዶክመንት፣ ቪዲዮ፣ ምስል እና ድምጽ ቅጂ",
            viewMedia: "ይዘቶችን ይመልከቱ",
            trainingTitle: "ቋሚ የህግ ስልጠናዎች",
            trainingDesc: "የወንጀል፣ ንግድ፣ ውል ህጎች ላይ ሙያዊ ስልጠና",
            trainingsBtn: "ስልጠናዎች",
            socialTitle: "ማህበራዊ ሚዲያ ስራዎች",
            socialDesc: "ይቀላቀሉና ያጋሩ።",
            libraryTitle: "የህግ ማውጫ",
            rulingTitle: "የኢፌድሪ ሰበር ሰሚ ችሎት ውሳኔዎች",
            purchaseAccess: `የውሳኔ ፍለጋ መብት ግዙ (${config.rulingPrice} ብር)`,
            joinTitle: "ዌብሳይቱን መቀላቀል ለሚፈልጉ",
            joinDesc: "ቅድመ ሁኔታዎችን ከማህበራዊ ሚዲያ ይመልከቱ።"
        },
        en: {
            consultTitle: "Legal Consultation",
            consultDesc: "Get professional legal advice.",
            consultBtnText: "Consult Now",
            mediaTitle: "Law Tutorials",
            mediaDesc: "Documents, videos, images, audio",
            viewMedia: "Browse Media",
            trainingTitle: "Permanent Legal Trainings",
            trainingDesc: "Criminal, Commercial, Contract law courses",
            trainingsBtn: "Trainings",
            socialTitle: "Social Media Works",
            socialDesc: "Join and share.",
            libraryTitle: "Legal Library",
            rulingTitle: "Federal Supreme Court Cassation Decisions",
            purchaseAccess: `Purchase Ruling Access (${config.rulingPrice} ETB)`,
            joinTitle: "Join the Website",
            joinDesc: "Check prerequisites on our social media."
        }
    };
    function updateLanguage() {
        const t = translations[currentLang];
        for (let key in t) {
            const el = document.querySelector(`[data-key="${key}"]`);
            if (el) el.innerText = t[key];
        }
        applyConfigToUI();
        updateRulingPriceText();
    }
    document.querySelectorAll(".lang-btn").forEach(btn => {
        btn.addEventListener("click", () => {
            currentLang = btn.getAttribute("data-lang");
            document.querySelectorAll(".lang-btn").forEach(b => b.classList.remove("active"));
            btn.classList.add("active");
            updateLanguage();
        });
    });

    // ---------- Event Listeners for UI ----------
    document.getElementById("consultBtn").addEventListener("click", () => document.getElementById("consultModal").style.display = "flex");
    document.getElementById("closeConsultBtn").addEventListener("click", () => document.getElementById("consultModal").style.display = "none");
    document.getElementById("sendConsultBtn").addEventListener("click", () => {
        const q = document.getElementById("consultQuestion").value;
        if (q) alert("ጥያቄዎ ተልኳል! በቅርቡ እንመልሳለን.\nYour question has been sent.");
        else alert("እባክዎ ጥያቄ ይጻፉ");
        document.getElementById("consultModal").style.display = "none";
    });
    document.getElementById("trainingsBtn").addEventListener("click", () => alert(currentLang === "am" ? "ስልጠናዎች በቅርቡ ይጀምራሉ። ለዝርዝር በቴሌግራም ይመዝገቡ።" : "Trainings coming soon. Join Telegram for updates."));
    document.getElementById("viewMediaBtn").addEventListener("click", () => document.getElementById("mediaSection").scrollIntoView({ behavior: "smooth" }));
    document.getElementById("profilePhotoBtn").addEventListener("click", () => alert("👨‍⚖️ Yonatan Dawit Mengistu (LLB)\n⚖️ Founder & Lead Attorney | Lawyers for Ethiopia"));
    document.getElementById("purchaseRulingBtn").addEventListener("click", () => {
        if (confirm(currentLang === "am" ? `እባክዎ ${config.rulingPrice} ብር ከላይ ባለው ቁጥር ይክፈሉ። ከከፈሉ በኋላ ፍለጋ ይከፈታል።` : `Please pay ${config.rulingPrice} ETB using the details above. Then search will be enabled.`)) {
            rulingsAccess = true;
            document.getElementById("rulingSearchArea").style.display = "block";
        }
    });
    document.getElementById("searchRulingBtn").addEventListener("click", searchRulings);

    // Initialize
    applyConfigToUI();
    updateLanguage();
</script>
</body>
</html>
