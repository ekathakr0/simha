<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AdvancedLocker - Secure Multi-Vault</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 50%, #f093fb 100%);
            min-height: 100vh;
        }

        .container {
            max-width: 1400px;
            margin: 0 auto;
            padding: 1rem;
        }

        /* Password Gate */
        .password-gate {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0,0,0,0.95);
            display: flex;
            align-items: center;
            justify-content: center;
            z-index: 9999;
            backdrop-filter: blur(10px);
        }

        .password-modal {
            background: linear-gradient(145deg, #2c3e50, #34495e);
            padding: 3rem;
            border-radius: 20px;
            text-align: center;
            color: white;
            box-shadow: 0 25px 50px rgba(0,0,0,0.5);
            max-width: 400px;
            width: 90%;
        }

        .password-input {
            width: 100%;
            padding: 1rem;
            font-size: 1.5rem;
            border: none;
            border-radius: 10px;
            margin: 1rem 0;
            text-align: center;
            background: rgba(255,255,255,0.1);
            color: white;
            backdrop-filter: blur(10px);
        }

        .unlock-btn {
            background: linear-gradient(45deg, #ff6b35, #f7931e);
            color: white;
            border: none;
            padding: 1rem 2rem;
            border-radius: 50px;
            font-size: 1.1rem;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s;
            margin-top: 1rem;
        }

        /* Main Interface */
        .locker-interface {
            display: none;
            animation: slideIn 0.5s ease;
        }

        @keyframes slideIn {
            from { opacity: 0; transform: translateY(30px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .header {
            text-align: center;
            color: white;
            margin-bottom: 2rem;
        }

        /* Control Panel */
        .control-panel {
            background: rgba(255,255,255,0.95);
            border-radius: 20px;
            padding: 1.5rem;
            margin-bottom: 2rem;
            box-shadow: 0 20px 40px rgba(0,0,0,0.2);
            backdrop-filter: blur(10px);
            display: flex;
            gap: 1rem;
            flex-wrap: wrap;
            justify-content: center;
            align-items: center;
        }

        .btn {
            padding: 0.8rem 1.5rem;
            border: none;
            border-radius: 25px;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s;
            font-size: 0.9rem;
        }

        .btn-primary { background: linear-gradient(45deg, #ff6b35, #f7931e); color: white; }
        .btn-danger { background: #e74c3c; color: white; }
        .btn-success { background: #27ae60; color: white; }

        .btn:hover { transform: translateY(-2px); box-shadow: 0 10px 20px rgba(0,0,0,0.2); }

        .vault-selector {
            background: white;
            padding: 0.8rem 1.5rem;
            border-radius: 25px;
            border: 2px solid #ff6b35;
            font-weight: bold;
        }

        /* Vault Grid */
        .vaults-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
            gap: 1.5rem;
            margin-bottom: 2rem;
        }

        .vault {
            background: rgba(255,255,255,0.95);
            border-radius: 20px;
            padding: 1.5rem;
            box-shadow: 0 20px 40px rgba(0,0,0,0.2);
            backdrop-filter: blur(10px);
            border-top: 4px solid;
        }

        .vault-a { border-top-color: #3498db; }
        .vault-b { border-top-color: #e74c3c; }
        .vault-c { border-top-color: #f39c12; }
        .vault-d { border-top-color: #9b59b6; }
        .vault-e { border-top-color: #1abc9c; }
        .vault-f { border-top-color: #34495e; }

        .vault-header {
            display: flex;
            align-items: center;
            justify-content: space-between;
            margin-bottom: 1rem;
        }

        .vault-title {
            font-size: 1.3rem;
            font-weight: bold;
        }

        .vault-count {
            background: rgba(255,255,255,0.7);
            padding: 0.3rem 0.8rem;
            border-radius: 15px;
            font-size: 0.8rem;
            font-weight: bold;
        }

        /* Image Gallery */
        .images-gallery {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(120px, 1fr));
            gap: 0.8rem;
            min-height: 200px;
        }

        .stored-image {
            position: relative;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 8px 25px rgba(0,0,0,0.15);
            transition: all 0.3s;
            cursor: pointer;
            height: 120px;
            background: #f8f9fa;
        }

        .stored-image:hover {
            transform: scale(1.05);
            box-shadow: 0 15px 35px rgba(0,0,0,0.25);
        }

        .stored-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .image-overlay {
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: rgba(0,0,0,0.8);
            color: white;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            opacity: 0;
            transition: opacity 0.3s;
        }

        .stored-image:hover .image-overlay {
            opacity: 1;
        }

        .delete-btn {
            position: absolute;
            top: 8px;
            right: 8px;
            background: #e74c3c;
            color: white;
            border: none;
            border-radius: 50%;
            width: 24px;
            height: 24px;
            cursor: pointer;
            font-size: 12px;
            font-weight: bold;
            display: none;
            z-index: 10;
        }

        .stored-image:hover .delete-btn {
            display: block;
        }

        /* Upload Zone */
        .upload-zone {
            border: 3px dashed #ff6b35;
            border-radius: 15px;
            padding: 2rem;
            text-align: center;
            transition: all 0.3s;
            cursor: pointer;
            background: rgba(255,107,53,0.1);
            margin-bottom: 1rem;
        }

        /* Stats */
        .stats-bar {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 1rem;
            background: rgba(255,255,255,0.9);
            padding: 1.5rem;
            border-radius: 15px;
            backdrop-filter: blur(10px);
        }

        /* Mobile */
        @media (max-width: 768px) {
            .container { padding: 0.5rem; }
            .header h1 { font-size: 1.8rem; }
            .vaults-grid { grid-template-columns: 1fr; }
            .images-gallery { 
                grid-template-columns: repeat(auto-fill, minmax(100px, 1fr));
            }
            .stored-image { height: 100px; }
            .control-panel { flex-direction: column; }
        }
    </style>
</head>
<body>
    <!-- Master Password Gate -->
    <div class="password-gate" id="masterPassword">
        <div class="password-modal">
            <h2>🔒 AdvancedLocker Pro</h2>
            <p>Enter your 4-digit access code</p>
            <input type="password" class="password-input" id="masterInput" placeholder="••••" maxlength="4" autofocus>
            <button class="unlock-btn" onclick="checkMasterPassword()">Unlock Vaults</button>
            <p style="margin-top: 1rem; font-size: 0.8rem; opacity: 0.7;">Hint: Numeric code</p>
        </div>
    </div>

    <!-- Main Interface -->
    <div class="locker-interface" id="mainInterface">
        <div class="container">
            <div class="header">
                <h1>🗄️ 6-Vault Secure Storage</h1>
                <p>Upload • Delete • Personal Use Only</p>
            </div>

            <!-- Control Panel (Share Code REMOVED) -->
            <div class="control-panel">
                <select id="vaultSelector" class="vault-selector">
                    <option value="all">All Vaults</option>
                    <option value="vaultA">Vault A (Blue)</option>
                    <option value="vaultB">Vault B (Red)</option>
                    <option value="vaultC">Vault C (Orange)</option>
                    <option value="vaultD">Vault D (Purple)</option>
                    <option value="vaultE">Vault E (Teal)</option>
                    <option value="vaultF">Vault F (Gray)</option>
                </select>
                <button class="btn btn-danger" onclick="deleteAllImages()" style="display:none;" id="deleteAllBtn">🗑️ Delete All</button>
                <input type="file" id="imageInput" multiple accept="image/*" style="display:none;">
            </div>

            <!-- Upload Zone -->
            <div class="upload-zone" id="uploadZone">
                <p>📤 Click or drag images here (Max 5MB each)</p>
                <p style="font-size: 0.9rem; opacity: 0.7;">Images auto-distributed across 6 vaults</p>
            </div>

            <!-- 6 Vaults -->
            <div class="vaults-grid">
                <div class="vault vault-a" id="vaultA">
                    <div class="vault-header">
                        <div class="vault-title">🔵 Vault A</div>
                        <div class="vault-count" id="countA">0</div>
                    </div>
                    <div class="images-gallery" id="galleryA"></div>
                </div>

                <div class="vault vault-b" id="vaultB">
                    <div class="vault-header">
                        <div class="vault-title">🔴 Vault B</div>
                        <div class="vault-count" id="countB">0</div>
                    </div>
                    <div class="images-gallery" id="galleryB"></div>
                </div>

                <div class="vault vault-c" id="vaultC">
                    <div class="vault-header">
                        <div class="vault-title">🟠 Vault C</div>
                        <div class="vault-count" id="countC">0</div>
                    </div>
                    <div class="images-gallery" id="galleryC"></div>
                </div>

                <div class="vault vault-d" id="vaultD">
                    <div class="vault-header">
                        <div class="vault-title">🟣 Vault D</div>
                        <div class="vault-count" id="countD">0</div>
                    </div>
                    <div class="images-gallery" id="galleryD"></div>
                </div>

                <div class="vault vault-e" id="vaultE">
                    <div class="vault-header">
                        <div class="vault-title">🟢 Vault E</div>
                        <div class="vault-count" id="countE">0</div>
                    </div>
                    <div class="images-gallery" id="galleryE"></div>
                </div>

                <div class="vault vault-f" id="vaultF">
                    <div class="vault-header">
                        <div class="vault-title">⚫ Vault F</div>
                        <div class="vault-count" id="countF">0</div>
                    </div>
                    <div class="images-gallery" id="galleryF"></div>
                </div>
            </div>

            <!-- Stats (Share Code REMOVED) -->
            <div class="stats-bar">
                <div><strong id="totalImages">0</strong> Images</div>
                <div><strong id="totalStorage">0</strong> MB</div>
                <div><strong id="activeVaults">0</strong>/6 Vaults</div>
            </div>
        </div>
    </div>

    <script>
        const MASTER_PASSWORD = '2411'; // Hidden from UI
        let vaults = JSON.parse(localStorage.getItem('imageVaults')) || {
            vaultA: [], vaultB: [], vaultC: [], vaultD: [], vaultE: [], vaultF: []
        };
        let imageCounter = 0;

        // Master Password Check
        function checkMasterPassword() {
            if (document.getElementById('masterInput').value === MASTER_PASSWORD) {
                document.getElementById('masterPassword').style.display = 'none';
                document.getElementById('mainInterface').style.display = 'block';
                loadVaults();
                document.getElementById('deleteAllBtn').style.display = 'inline-block';
            } else {
                document.getElementById('masterInput').value = '';
                shakeEffect();
            }
        }

        // Vault Management
        function loadVaults() {
            Object.keys(vaults).forEach(vault => {
                renderVault(vault);
                updateVaultCount(vault);
            });
            updateStats();
        }

        function renderVault(vaultName) {
            const gallery = document.getElementById('gallery' + vaultName.slice(-1).toUpperCase());
            gallery.innerHTML = '';
            vaults[vaultName].forEach((img, index) => {
                const imgDiv = createImageElement(img, vaultName, index);
                gallery.appendChild(imgDiv);
            });
        }

        function createImageElement(img, vaultName, index) {
            const imgDiv = document.createElement('div');
            imgDiv.className = 'stored-image';
            imgDiv.innerHTML = `
                <img src="${img.data}" alt="${img.name}" loading="lazy">
                <div class="image-overlay">
                    <div style="font-size: 0.8rem; margin-bottom: 0.5rem;">${img.name}</div>
                    <div style="font-size: 0.7rem; opacity: 0.8;">${img.size}MB</div>
                </div>
                <button class="delete-btn" onclick="deleteImage('${vaultName}', ${index}); event.stopPropagation();">×</button>
            `;
            imgDiv.onclick = (e) => {
                if (e.target.tagName !== 'BUTTON') showFullImage(img.data);
            };
            return imgDiv;
        }

        // Delete Functions
        function deleteImage(vaultName, index) {
            if (confirm('Delete this image forever?')) {
                vaults[vaultName].splice(index, 1);
                localStorage.setItem('imageVaults', JSON.stringify(vaults));
                renderVault(vaultName);
                updateVaultCount(vaultName);
                updateStats();
            }
        }

        function deleteAllImages() {
            if (confirm('⚠️ Delete ALL images from ALL 6 vaults? This is PERMANENT!')) {
                vaults = { vaultA: [], vaultB: [], vaultC: [], vaultD: [], vaultE: [], vaultF: [] };
                localStorage.setItem('imageVaults', JSON.stringify(vaults));
                loadVaults();
            }
        }

        // Upload Handler
        document.getElementById('uploadZone').addEventListener('click', () => {
            document.getElementById('imageInput').click();
        });

        document.getElementById('imageInput').addEventListener('change', (e) => handleFiles(e.target.files));
        
        ['dragover', 'dragenter'].forEach(event => {
            document.getElementById('uploadZone').addEventListener(event, (e) => {
                e.preventDefault();
                e.currentTarget.style.background = 'rgba(247,147,30,0.3)';
            });
        });

        ['dragleave', 'drop'].forEach(event => {
            document.getElementById('uploadZone').addEventListener(event, (e) => {
                e.preventDefault();
                e.currentTarget.style.background = 'rgba(255,107,53,0.1)';
                if (event === 'drop') handleFiles(e.dataTransfer.files);
            });
        });

        function handleFiles(files) {
            Array.from(files).forEach(file => {
                if (file.type.startsWith('image/') && file.size < 5 * 1024 * 1024) {
                    const reader = new FileReader();
                    reader.onload = (e) => {
                        const imgData = {
                            id: ++imageCounter,
                            data: e.target.result,
                            name: file.name,
                            size: (file.size / 1024 / 1024).toFixed(2),
                            date: new Date().toLocaleString()
                        };
                        const vaultNames = Object.keys(vaults);
                        const targetVault = vaultNames[imageCounter % vaultNames.length];
                        vaults[targetVault].push(imgData);
                        localStorage.setItem('imageVaults', JSON.stringify(vaults));
                        renderVault(targetVault);
                        updateVaultCount(targetVault);
                        updateStats();
                    };
                    reader.readAsDataURL(file);
                }
            });
        }

        // Utilities
        function updateVaultCount(vaultName) {
            const count = document.getElementById('count' + vaultName.slice(-1).toUpperCase());
            count.textContent = vaults[vaultName].length;
        }

        function updateStats() {
            const totalImages = Object.values(vaults).reduce((a, b) => a + b.length, 0);
            const totalSize = Object.values(vaults).reduce((a, b) => 
                a + b.reduce((x, y) => x + parseFloat(y.size), 0), 0);
            const activeVaults = Object.values(vaults).filter(v => v.length > 0).length;

            document.getElementById('totalImages').textContent = totalImages;
            document.getElementById('totalStorage').textContent = totalSize.toFixed(1);
            document.getElementById('activeVaults').textContent = activeVaults;
        }

        function showFullImage(src) {
            const modal = document.createElement('div');
            modal.style.cssText = `
                position: fixed; top: 0; left: 0; width: 100vw; height: 100vh;
                background: rgba(0,0,0,0.95); z-index: 10000; display: flex;
                align-items: center; justify-content: center; cursor: zoom-out;
            `;
            modal.innerHTML = `<img src="${src}" style="max-width: 95%; max-height: 95%; border-radius: 10px;">`;
            modal.onclick = () => modal.remove();
            document.body.appendChild(modal);
        }

        function shakeEffect() {
            document.querySelector('.password-modal').style.animation = 'shake 0.5s';
            setTimeout(() => document.querySelector('.password-modal').style.animation = '', 500);
        }

        // Event Listeners
        document.getElementById('masterInput').addEventListener('keypress', (e) => {
            if (e.key === 'Enter') checkMasterPassword();
        });

        // Shake Animation
        const style = document.createElement('style');
        style.textContent = `
            @keyframes shake {
                0%, 100% { transform: translateX(0); }
                25% { transform: translateX(-10px); }
                75% { transform: translateX(10px); }
            }
            @media (max-width: 480px) {
                .images-gallery { grid-template-columns: 1fr 1fr; }
                .stored-image { height: 110px; }
            }
        `;
        document.head.appendChild(style);
    </script>
</body>
</html>
