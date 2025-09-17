<!DOCTYPE html>

<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Atelier Reimagined - Where timeless design meets conscious style</title>
    <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@300;400;500;600&family=Inter:wght@300;400;500&display=swap" rel="stylesheet">
    <style>
        :root {
            --off-white: #fdfcf9;
            --warm-white: #f8f6f2;
            --slate: #4a5568;
            --charcoal: #2d3748;
            --champagne: #d4af37;
            --champagne-light: #e8c968;
            --soft-gray: #e2e8f0;
            --text-muted: #718096;
        }

```
    /* Optimized animations - reduce motion for performance */
    * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }

    body {
        font-family: 'Inter', sans-serif;
        background-color: var(--off-white);
        color: var(--charcoal);
        line-height: 1.6;
        overflow-x: hidden;
    }

    .serif {
        font-family: 'Cormorant Garamond', serif;
    }

    /* Performance optimizations */
    img {
        will-change: auto;
    }

    .fade-in {
        opacity: 0;
        transform: translateY(20px);
        transition: opacity 0.4s ease, transform 0.4s ease;
    }

    .fade-in.visible {
        opacity: 1;
        transform: translateY(0);
    }

    /* Header */
    .header {
        position: fixed;
        top: 0;
        width: 100%;
        background: rgba(253, 252, 249, 0.95);
        backdrop-filter: blur(20px);
        z-index: 1000;
        border-bottom: 1px solid var(--soft-gray);
        transition: background 0.3s ease;
    }

    .nav {
        display: flex;
        justify-content: space-between;
        align-items: center;
        max-width: 1200px;
        margin: 0 auto;
        padding: 1.5rem 2rem;
    }

    .logo {
        font-family: 'Cormorant Garamond', serif;
        font-size: 1.8rem;
        font-weight: 500;
        color: var(--charcoal);
        letter-spacing: 1px;
    }

    .nav-links {
        display: flex;
        gap: 3rem;
        list-style: none;
    }

    .nav-links a {
        color: var(--slate);
        text-decoration: none;
        font-weight: 300;
        font-size: 0.95rem;
        letter-spacing: 0.5px;
        transition: color 0.3s ease;
    }

    .nav-links a:hover {
        color: var(--champagne);
    }

    /* Hero Section */
    .hero {
        height: 100vh;
        display: flex;
        align-items: center;
        justify-content: center;
        background: linear-gradient(135deg, var(--warm-white) 0%, var(--off-white) 100%);
        position: relative;
    }

    .hero-content {
        text-align: center;
        max-width: 700px;
        padding: 0 2rem;
    }

    .hero h1 {
        font-family: 'Cormorant Garamond', serif;
        font-size: 4.5rem;
        font-weight: 300;
        color: var(--charcoal);
        margin-bottom: 1.5rem;
        letter-spacing: 2px;
        line-height: 1.1;
    }

    .hero .tagline {
        font-size: 1.2rem;
        color: var(--text-muted);
        margin-bottom: 3rem;
        font-style: italic;
        font-weight: 300;
    }

    .hero-actions {
        display: flex;
        gap: 1.5rem;
        justify-content: center;
        flex-wrap: wrap;
    }

    .cta-button {
        display: inline-block;
        padding: 1rem 2.5rem;
        text-decoration: none;
        font-weight: 400;
        font-size: 0.95rem;
        letter-spacing: 1px;
        transition: all 0.3s ease;
        border: 1px solid var(--charcoal);
    }

    .cta-button.primary {
        background: var(--charcoal);
        color: var(--off-white);
    }

    .cta-button.primary:hover {
        background: transparent;
        color: var(--charcoal);
    }

    .cta-button.secondary {
        background: transparent;
        color: var(--champagne);
        border-color: var(--champagne);
    }

    .cta-button.secondary:hover {
        background: var(--champagne);
        color: var(--charcoal);
    }

    /* Style Board Preview Section */
    .style-board-preview {
        padding: 6rem 2rem;
        background: var(--warm-white);
    }

    .preview-content {
        max-width: 1200px;
        margin: 0 auto;
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 4rem;
        align-items: center;
    }

    .preview-text h2 {
        font-size: 2.5rem;
        font-weight: 400;
        color: var(--charcoal);
        margin-bottom: 1.5rem;
    }

    .preview-text p {
        color: var(--slate);
        line-height: 1.8;
        margin-bottom: 2rem;
        font-size: 1.1rem;
    }

    .preview-features {
        display: flex;
        flex-direction: column;
        gap: 1rem;
        margin-bottom: 2.5rem;
    }

    .feature-point {
        display: flex;
        align-items: center;
        gap: 1rem;
        color: var(--slate);
    }

    .feature-icon {
        font-size: 1.2rem;
        width: 2rem;
    }

    .preview-cta {
        color: var(--champagne);
        text-decoration: none;
        font-weight: 500;
        font-size: 1.1rem;
        transition: opacity 0.3s ease;
    }

    .preview-cta:hover {
        opacity: 0.7;
    }

    .style-board-mockup {
        background: var(--off-white);
        border-radius: 20px;
        padding: 3rem;
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 2rem;
        box-shadow: 0 20px 60px rgba(74, 85, 104, 0.1);
    }

    .mockup-slot {
        background: white;
        border: 2px solid var(--soft-gray);
        border-radius: 15px;
        padding: 2rem;
        text-align: center;
        transition: all 0.3s ease;
    }

    .mockup-slot:hover {
        border-color: var(--champagne);
        transform: scale(1.02);
    }

    .mockup-item {
        font-size: 3rem;
        opacity: 0.8;
    }

    /* Gallery Section */
    .gallery {
        padding: 6rem 2rem;
        max-width: 1200px;
        margin: 0 auto;
    }

    .section-header {
        text-align: center;
        margin-bottom: 4rem;
    }

    .section-header h2 {
        font-family: 'Cormorant Garamond', serif;
        font-size: 3rem;
        font-weight: 400;
        color: var(--charcoal);
        margin-bottom: 1rem;
    }

    .section-header p {
        color: var(--text-muted);
        font-size: 1.1rem;
        max-width: 600px;
        margin: 0 auto;
        line-height: 1.7;
    }

    .gallery-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
        gap: 4rem;
        margin-top: 4rem;
    }

    .gallery-item {
        background: var(--warm-white);
        transition: all 0.4s ease;
        cursor: pointer;
        border: 1px solid transparent;
    }

    .gallery-item:hover {
        transform: translateY(-8px);
        border-color: var(--soft-gray);
        box-shadow: 0 20px 60px rgba(74, 85, 104, 0.1);
    }

    .item-image {
        width: 100%;
        height: 400px;
        background: linear-gradient(135deg, var(--soft-gray) 0%, #f1f5f9 100%);
        display: flex;
        align-items: center;
        justify-content: center;
        font-size: 4rem;
        color: var(--text-muted);
        margin-bottom: 1.5rem;
    }

    .item-details {
        padding: 0 2rem 2rem;
    }

    .item-details h3 {
        font-family: 'Cormorant Garamond', serif;
        font-size: 1.8rem;
        font-weight: 500;
        color: var(--charcoal);
        margin-bottom: 0.5rem;
    }

    .item-meta {
        font-size: 0.9rem;
        color: var(--text-muted);
        margin-bottom: 1rem;
    }

    .item-story {
        color: var(--slate);
        line-height: 1.7;
        margin-bottom: 1.5rem;
    }

    .impact-note {
        font-size: 0.85rem;
        color: var(--champagne);
        font-style: italic;
        border-left: 2px solid var(--champagne);
        padding-left: 1rem;
    }

    /* Stylist's Edit */
    .stylists-edit {
        background: var(--warm-white);
        padding: 6rem 2rem;
    }

    .edit-container {
        max-width: 1200px;
        margin: 0 auto;
    }

    .lookbook-spread {
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 4rem;
        align-items: center;
        margin-top: 4rem;
    }

    .lookbook-content h3 {
        font-family: 'Cormorant Garamond', serif;
        font-size: 2.5rem;
        font-weight: 400;
        color: var(--charcoal);
        margin-bottom: 1.5rem;
    }

    .lookbook-description {
        color: var(--slate);
        line-height: 1.8;
        margin-bottom: 2rem;
    }

    .edit-items {
        display: flex;
        flex-direction: column;
        gap: 1rem;
    }

    .edit-item {
        display: flex;
        align-items: center;
        padding: 1rem 0;
        border-bottom: 1px solid var(--soft-gray);
    }

    .edit-item:last-child {
        border-bottom: none;
    }

    .item-thumbnail {
        width: 60px;
        height: 60px;
        background: var(--soft-gray);
        margin-right: 1.5rem;
        display: flex;
        align-items: center;
        justify-content: center;
        font-size: 1.5rem;
        color: var(--text-muted);
    }

    .edit-item-info h4 {
        color: var(--charcoal);
        font-size: 1.1rem;
        margin-bottom: 0.2rem;
    }

    .edit-item-info p {
        color: var(--text-muted);
        font-size: 0.9rem;
    }

    .lookbook-visual {
        background: linear-gradient(135deg, #f8f6f2 0%, #f1f5f9 100%);
        height: 500px;
        display: flex;
        align-items: center;
        justify-content: center;
        font-size: 6rem;
        color: var(--text-muted);
    }

    /* Journal Section */
    .journal {
        padding: 6rem 2rem;
        max-width: 800px;
        margin: 0 auto;
    }

    .journal-articles {
        margin-top: 4rem;
        display: grid;
        gap: 3rem;
    }

    .article-preview {
        padding: 2.5rem 0;
        border-bottom: 1px solid var(--soft-gray);
    }

    .article-preview:last-child {
        border-bottom: none;
    }

    .article-preview h3 {
        font-family: 'Cormorant Garamond', serif;
        font-size: 2rem;
        font-weight: 500;
        color: var(--charcoal);
        margin-bottom: 1rem;
    }

    .article-preview .excerpt {
        color: var(--slate);
        line-height: 1.8;
        margin-bottom: 1.5rem;
    }

    .read-more {
        color: var(--champagne);
        text-decoration: none;
        font-size: 0.9rem;
        letter-spacing: 0.5px;
        font-weight: 500;
        transition: opacity 0.3s ease;
    }

    .read-more:hover {
        opacity: 0.7;
    }

    /* Archive Exchange */
    .archive-exchange {
        background: var(--charcoal);
        color: var(--off-white);
        padding: 6rem 2rem;
        text-align: center;
    }

    .exchange-content {
        max-width: 600px;
        margin: 0 auto;
    }

    .exchange-content h2 {
        font-family: 'Cormorant Garamond', serif;
        font-size: 3rem;
        font-weight: 400;
        margin-bottom: 1.5rem;
    }

    .exchange-content p {
        color: var(--soft-gray);
        line-height: 1.8;
        margin-bottom: 2.5rem;
    }

    .invitation-button {
        display: inline-block;
        padding: 1rem 2.5rem;
        border: 1px solid var(--champagne);
        color: var(--champagne);
        text-decoration: none;
        font-weight: 400;
        letter-spacing: 1px;
        transition: all 0.3s ease;
    }

    .invitation-button:hover {
        background: var(--champagne);
        color: var(--charcoal);
    }

    /* Parallax Effect */
    .parallax-section {
        position: relative;
        overflow: hidden;
    }

    /* Responsive */
    @media (max-width: 768px) {
        .hero h1 { font-size: 3rem; }
        .nav-links { display: none; }
        .gallery-grid { grid-template-columns: 1fr; gap: 3rem; }
        .lookbook-spread { grid-template-columns: 1fr; gap: 3rem; }
        .section-header h2 { font-size: 2.5rem; }
        .preview-content { grid-template-columns: 1fr; gap: 2rem; text-align: center; }
        .hero-actions { flex-direction: column; gap: 1rem; }
        .form-row { grid-template-columns: 1fr; }
        .wardrobe-header { text-align: center; flex-direction: column; }
        .wardrobe-header h2 { font-size: 2.5rem; }
        .outfit-workspace { grid-template-columns: 1fr; gap: 3rem; }
        .outfit-canvas { grid-template-columns: 1fr 1fr; gap: 1rem; }
        .outfit-slot[data-type="dresses"] { grid-column: 1 / 3; }
        .outfit-slot.accessories-slot { grid-column: 1 / 3; }
    }

    /* Smooth scroll behavior */
    html {
        scroll-behavior: smooth;
    }

    /* Fade in animation */
    .fade-in {
        opacity: 0;
        transform: translateY(30px);
        transition: all 0.6s ease;
    }

    .fade-in.visible {
        opacity: 1;
        transform: translateY(0);
    }
</style>
```

</head>
<body>
    <header class="header">
        <nav class="nav">
            <div class="logo serif">Atelier Reimagined</div>
            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#gallery">Gallery</a></li>
                <li><a href="#edit">Stylist's Edit</a></li>
                <li><a href="#journal">Journal</a></li>
                <li><a href="#exchange">Archive</a></li>
            </ul>
        </nav>
    </header>

```
<section class="hero parallax-section" id="home">
    <div class="hero-content fade-in">
        <h1 class="serif">Atelier Reimagined</h1>
        <p class="tagline">Where timeless design meets conscious style.</p>
        <div class="hero-actions">
            <a href="#gallery" class="cta-button primary">Enter the Gallery</a>
            <a href="#" onclick="showOutfitCreator(); return false;" class="cta-button secondary">Style Board</a>
        </div>
    </div>
</section>

<!-- Style Board Preview Section -->
<section class="style-board-preview">
    <div class="preview-content fade-in">
        <div class="preview-text">
            <h2 class="serif">Create Your Perfect Look</h2>
            <p>Mix and match pieces from your wardrobe to discover new styling possibilities. Our digital styling board lets you experiment with combinations before you wear them.</p>
            <div class="preview-features">
                <div class="feature-point">
                    <span class="feature-icon">✨</span>
                    <span>Drag & drop styling</span>
                </div>
                <div class="feature-point">
                    <span class="feature-icon">💾</span>
                    <span>Save favorite looks</span>
                </div>
                <div class="feature-point">
                    <span class="feature-icon">🎲</span>
                    <span>Discover new combinations</span>
                </div>
            </div>
            <a href="#" onclick="showOutfitCreator(); return false;" class="preview-cta">Try Style Board →</a>
        </div>
        <div class="preview-visual">
            <div class="style-board-mockup">
                <div class="mockup-slot">
                    <div class="mockup-item">🧥</div>
                </div>
                <div class="mockup-slot">
                    <div class="mockup-item">👕</div>
                </div>
                <div class="mockup-slot">
                    <div class="mockup-item">👖</div>
                </div>
                <div class="mockup-slot">
                    <div class="mockup-item">👠</div>
                </div>
            </div>
        </div>
    </div>
</section>

<section class="gallery" id="gallery">
    <div class="section-header fade-in">
        <h2 class="serif">The Digital Wardrobe Gallery</h2>
        <p>Each piece in your collection, presented as an exhibit—with its story, journey, and lasting impact carefully documented.</p>
    </div>

    <div class="gallery-grid">
        <div class="gallery-item fade-in">
            <div class="item-image">🧥</div>
            <div class="item-details">
                <h3 class="serif">The Heritage Coat</h3>
                <div class="item-meta">Wool blend • Acquired Spring 2023</div>
                <p class="item-story">A timeless silhouette crafted from regenerative wool, designed to evolve with your wardrobe across decades. The structured shoulders and flowing lines create an elegant foundation for any ensemble.</p>
                <div class="impact-note">This coat's journey: 85 wears, 3 seasons, 1 repair. Its value grows with time.</div>
            </div>
        </div>

        <div class="gallery-item fade-in">
            <div class="item-image">👗</div>
            <div class="item-details">
                <h3 class="serif">Midnight in Milan</h3>
                <div class="item-meta">Silk alternative • Archive piece</div>
                <p class="item-story">An evening dress that whispers sophistication—cut from innovative fiber made from citrus waste, with hand-finished details that catch light like captured starlight.</p>
                <div class="impact-note">Worn to 12 occasions, each creating new memories while honoring its craft.</div>
            </div>
        </div>

        <div class="gallery-item fade-in">
            <div class="item-image">👚</div>
            <div class="item-details">
                <h3 class="serif">The Essential Blouse</h3>
                <div class="item-meta">Organic cotton • Core collection</div>
                <p class="item-story">Perfect proportions in the purest cotton, grown without compromise. A foundation piece that adapts from morning meetings to evening gatherings with effortless grace.</p>
                <div class="impact-note">127 wears and counting—a testament to thoughtful design and quality.</div>
            </div>
        </div>
    </div>
</section>

<section class="stylists-edit parallax-section" id="edit">
    <div class="edit-container">
        <div class="section-header fade-in">
            <h2 class="serif">The Stylist's Edit</h2>
            <p>Curated capsule collections and seasonal lookbooks, presented like the pages of your most treasured fashion journal.</p>
        </div>

        <div class="lookbook-spread">
            <div class="lookbook-content fade-in">
                <h3 class="serif">Autumn Minimalism</h3>
                <p class="lookbook-description">A carefully considered edit for the season of transformation. Each piece selected for its ability to layer, transition, and endure—creating a wardrobe that speaks to both sophistication and sustainability.</p>
                
                <div class="edit-items">
                    <div class="edit-item">
                        <div class="item-thumbnail">🧥</div>
                        <div class="edit-item-info">
                            <h4>The Heritage Coat</h4>
                            <p>Your anchor piece for layering</p>
                        </div>
                    </div>
                    <div class="edit-item">
                        <div class="item-thumbnail">🧶</div>
                        <div class="edit-item-info">
                            <h4>Cashmere Pullover</h4>
                            <p>Soft luxury for cooler days</p>
                        </div>
                    </div>
                    <div class="edit-item">
                        <div class="item-thumbnail">👖</div>
                        <div class="edit-item-info">
                            <h4>Wide-leg Trousers</h4>
                            <p>Effortless elegance in organic wool</p>
                        </div>
                    </div>
                </div>
            </div>
            <div class="lookbook-visual fade-in">📖</div>
        </div>
    </div>
</section>

<section class="journal" id="journal">
    <div class="section-header fade-in">
        <h2 class="serif">The Atelier Journal</h2>
        <p>Artisan wisdom, care rituals, and the deeper stories behind conscious fashion—curated like the finest editorial content.</p>
    </div>

    <div class="journal-articles">
        <article class="article-preview fade-in">
            <h3 class="serif">The Ritual of Cashmere Care</h3>
            <p class="excerpt">Like tending a garden, caring for cashmere is an act of mindfulness. Learn the gentle techniques that preserve both fiber and soul, ensuring your cherished pieces age gracefully through countless seasons of wear.</p>
            <a href="#" class="read-more">Continue Reading →</a>
        </article>

        <article class="article-preview fade-in">
            <h3 class="serif">Understanding Regenerative Fibers</h3>
            <p class="excerpt">Beyond sustainability lies regeneration—fabrics that give back to the earth. Discover how innovative textiles are healing ecosystems while creating the most luxurious materials you'll ever touch.</p>
            <a href="#" class="read-more">Continue Reading →</a>
        </article>

        <article class="article-preview fade-in">
            <h3 class="serif">The Art of Thoughtful Mending</h3>
            <p class="excerpt">In Japanese culture, kintsugi celebrates the beauty of repair. Apply these principles to your wardrobe, where each mend becomes a golden thread in your garment's ongoing story.</p>
            <a href="#" class="read-more">Continue Reading →</a>
        </article>
    </div>
</section>

<section class="archive-exchange parallax-section" id="exchange">
    <div class="exchange-content fade-in">
        <h2 class="serif">Archive Exchanges</h2>
        <p>For the rarest pieces in your collection—those treasured garments that deserve new chapters. An exclusive invitation to participate in considered exchanges with fellow collectors.</p>
        <a href="#" class="invitation-button">Request Invitation</a>
    </div>
</section>

<!-- Wardrobe Management Modal -->
<div id="wardrobeModal" class="modal" style="display: none;">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <h2 class="serif">Add to Your Wardrobe</h2>
        
        <form id="addItemForm" onsubmit="addWardrobeItem(event)">
            <div class="form-group">
                <label>Item Photo</label>
                <input type="file" id="itemPhoto" accept="image/*" required>
                <div id="photoPreview"></div>
            </div>
            
            <div class="form-row">
                <div class="form-group">
                    <label>Item Name</label>
                    <input type="text" id="itemName" required>
                </div>
                <div class="form-group">
                    <label>Category</label>
                    <select id="itemCategory" required>
                        <option value="">Select Category</option>
                        <option value="tops">Tops</option>
                        <option value="bottoms">Bottoms</option>
                        <option value="outerwear">Outerwear</option>
                        <option value="dresses">Dresses</option>
                        <option value="accessories">Accessories</option>
                        <option value="shoes">Shoes</option>
                    </select>
                </div>
            </div>
            
            <div class="form-row">
                <div class="form-group">
                    <label>Brand</label>
                    <input type="text" id="itemBrand">
                </div>
                <div class="form-group">
                    <label>Color</label>
                    <input type="text" id="itemColor">
                </div>
            </div>
            
            <div class="form-row">
                <div class="form-group">
                    <label>Fabric</label>
                    <input type="text" id="itemFabric">
                </div>
                <div class="form-group">
                    <label>Purchase Date</label>
                    <input type="date" id="itemPurchaseDate">
                </div>
            </div>
            
            <div class="form-group">
                <label>Notes</label>
                <textarea id="itemNotes" placeholder="Special care instructions, styling notes, or memories..."></textarea>
            </div>
            
            <button type="submit" class="submit-btn">Add to Wardrobe</button>
        </form>
    </div>
</div>

<!-- Outfit Creator Section -->
<section class="outfit-creator" id="outfit-creator" style="display: none;">
    <div class="outfit-header">
        <h2 class="serif">Style Your Collection</h2>
        <p>Create beautiful looks from your wardrobe pieces. Drag items to the styling board to build your outfit.</p>
    </div>
    
    <div class="outfit-workspace">
        <div class="wardrobe-picker">
            <h3 class="serif">Your Pieces</h3>
            <div class="picker-filters">
                <button class="picker-filter active" onclick="filterPicker('all')">All</button>
                <button class="picker-filter" onclick="filterPicker('tops')">Tops</button>
                <button class="picker-filter" onclick="filterPicker('bottoms')">Bottoms</button>
                <button class="picker-filter" onclick="filterPicker('outerwear')">Layers</button>
                <button class="picker-filter" onclick="filterPicker('dresses')">Dresses</button>
                <button class="picker-filter" onclick="filterPicker('accessories')">Accessories</button>
                <button class="picker-filter" onclick="filterPicker('shoes')">Shoes</button>
            </div>
            <div id="wardrobePicker" class="picker-grid"></div>
        </div>
        
        <div class="styling-board">
            <h3 class="serif">Styling Board</h3>
            <div class="outfit-canvas" id="outfitCanvas">
                <div class="outfit-slot" data-type="outerwear" onclick="removeFromOutfit(this)">
                    <div class="slot-label">Outerwear</div>
                    <div class="slot-placeholder">Drag a jacket or coat here</div>
                </div>
                <div class="outfit-slot" data-type="tops" onclick="removeFromOutfit(this)">
                    <div class="slot-label">Top</div>
                    <div class="slot-placeholder">Drag a top here</div>
                </div>
                <div class="outfit-slot" data-type="bottoms" onclick="removeFromOutfit(this)">
                    <div class="slot-label">Bottom</div>
                    <div class="slot-placeholder">Drag pants or skirt here</div>
                </div>
                <div class="outfit-slot" data-type="dresses" onclick="removeFromOutfit(this)">
                    <div class="slot-label">Dress</div>
                    <div class="slot-placeholder">Or drag a dress here</div>
                </div>
                <div class="outfit-slot" data-type="shoes" onclick="removeFromOutfit(this)">
                    <div class="slot-label">Shoes</div>
                    <div class="slot-placeholder">Drag shoes here</div>
                </div>
                <div class="outfit-slot accessories-slot" data-type="accessories" onclick="removeFromOutfit(this)">
                    <div class="slot-label">Accessories</div>
                    <div class="slot-placeholder">Add accessories</div>
                </div>
            </div>
            
            <div class="outfit-actions">
                <button onclick="saveOutfit()" class="save-outfit-btn">Save This Look</button>
                <button onclick="clearOutfit()" class="clear-outfit-btn">Clear Board</button>
                <button onclick="randomOutfit()" class="random-outfit-btn">Surprise Me</button>
            </div>
        </div>
    </div>
    
    <div class="saved-outfits">
        <h3 class="serif">Saved Looks</h3>
        <div id="savedOutfitsGrid" class="saved-outfits-grid"></div>
    </div>
</section>

<!-- Personal Wardrobe Section -->
<section class="personal-wardrobe" id="my-wardrobe" style="display: none;">
    <div class="wardrobe-header">
        <h2 class="serif">Your Personal Collection</h2>
        <div class="wardrobe-stats" id="wardrobeStats"></div>
        <button onclick="openModal()" class="add-item-btn">Add New Piece</button>
    </div>
    
    <div class="wardrobe-filters">
        <button class="filter-btn active" onclick="filterWardrobe('all')">All Items</button>
        <button class="filter-btn" onclick="filterWardrobe('tops')">Tops</button>
        <button class="filter-btn" onclick="filterWardrobe('bottoms')">Bottoms</button>
        <button class="filter-btn" onclick="filterWardrobe('outerwear')">Outerwear</button>
        <button class="filter-btn" onclick="filterWardrobe('dresses')">Dresses</button>
        <button class="filter-btn" onclick="filterWardrobe('accessories')">Accessories</button>
        <button class="filter-btn" onclick="filterWardrobe('shoes')">Shoes</button>
    </div>
    
    <div id="personalWardrobeGrid" class="wardrobe-grid"></div>
</section>

<style>
    /* Modal Styles */
    .modal {
        position: fixed;
        z-index: 2000;
        left: 0;
        top: 0;
        width: 100%;
        height: 100%;
        background-color: rgba(45, 55, 72, 0.8);
        backdrop-filter: blur(10px);
    }

    .modal-content {
        background-color: var(--off-white);
        margin: 5% auto;
        padding: 3rem;
        border-radius: 10px;
        width: 90%;
        max-width: 600px;
        max-height: 80vh;
        overflow-y: auto;
        position: relative;
    }

    .close {
        color: var(--text-muted);
        float: right;
        font-size: 2rem;
        font-weight: bold;
        cursor: pointer;
        position: absolute;
        right: 1.5rem;
        top: 1.5rem;
    }

    .close:hover {
        color: var(--charcoal);
    }

    .form-group {
        margin-bottom: 1.5rem;
    }

    .form-row {
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 1rem;
    }

    .form-group label {
        display: block;
        margin-bottom: 0.5rem;
        color: var(--charcoal);
        font-weight: 500;
    }

    .form-group input,
    .form-group select,
    .form-group textarea {
        width: 100%;
        padding: 0.8rem;
        border: 1px solid var(--soft-gray);
        border-radius: 5px;
        background: var(--warm-white);
        color: var(--charcoal);
        font-family: inherit;
    }

    .form-group textarea {
        resize: vertical;
        height: 80px;
    }

    #photoPreview {
        margin-top: 1rem;
        text-align: center;
    }

    #photoPreview img {
        max-width: 200px;
        max-height: 200px;
        border-radius: 10px;
        box-shadow: 0 4px 20px rgba(74, 85, 104, 0.1);
    }

    .submit-btn {
        background: var(--charcoal);
        color: var(--off-white);
        padding: 1rem 2rem;
        border: none;
        border-radius: 5px;
        cursor: pointer;
        font-size: 1rem;
        width: 100%;
        transition: all 0.3s ease;
    }

    .submit-btn:hover {
        background: var(--champagne);
        color: var(--charcoal);
    }

    /* Personal Wardrobe Styles */
    .personal-wardrobe {
        padding: 6rem 2rem;
        max-width: 1200px;
        margin: 0 auto;
    }

    .wardrobe-header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 3rem;
        flex-wrap: wrap;
        gap: 1rem;
    }

    .wardrobe-header h2 {
        color: var(--charcoal);
        font-size: 3rem;
        font-weight: 400;
    }

    .wardrobe-stats {
        color: var(--text-muted);
        font-size: 1.1rem;
    }

    .add-item-btn {
        background: var(--champagne);
        color: var(--charcoal);
        padding: 1rem 2rem;
        border: none;
        border-radius: 25px;
        cursor: pointer;
        font-weight: 500;
        transition: all 0.3s ease;
    }

    .add-item-btn:hover {
        background: var(--champagne-light);
        transform: translateY(-2px);
    }

    .wardrobe-filters {
        display: flex;
        gap: 1rem;
        margin-bottom: 3rem;
        flex-wrap: wrap;
        justify-content: center;
    }

    .wardrobe-filters .filter-btn {
        padding: 0.8rem 1.5rem;
        background: var(--warm-white);
        border: 1px solid var(--soft-gray);
        color: var(--slate);
        border-radius: 25px;
        cursor: pointer;
        transition: all 0.3s ease;
        font-size: 0.9rem;
    }

    .wardrobe-filters .filter-btn:hover,
    .wardrobe-filters .filter-btn.active {
        background: var(--champagne);
        color: var(--charcoal);
        border-color: var(--champagne);
    }

    .wardrobe-grid {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
        gap: 2rem;
    }

    .wardrobe-item {
        background: var(--warm-white);
        border-radius: 15px;
        overflow: hidden;
        transition: all 0.3s ease;
        cursor: pointer;
        border: 1px solid transparent;
    }

    .wardrobe-item:hover {
        transform: translateY(-5px);
        border-color: var(--soft-gray);
        box-shadow: 0 15px 40px rgba(74, 85, 104, 0.1);
    }

    .wardrobe-item img {
        width: 100%;
        height: 250px;
        object-fit: cover;
    }

    .wardrobe-item-info {
        padding: 1.5rem;
    }

    .wardrobe-item-info h4 {
        color: var(--charcoal);
        font-size: 1.2rem;
        margin-bottom: 0.5rem;
        font-family: 'Cormorant Garamond', serif;
    }

    .wardrobe-item-meta {
        color: var(--text-muted);
        font-size: 0.9rem;
        margin-bottom: 1rem;
    }

    .wardrobe-item-notes {
        color: var(--slate);
        font-size: 0.85rem;
        line-height: 1.5;
    }

    /* Outfit Creator Styles */
    .outfit-creator {
        padding: 6rem 2rem;
        max-width: 1400px;
        margin: 0 auto;
        background: var(--warm-white);
    }

    .outfit-header {
        text-align: center;
        margin-bottom: 4rem;
    }

    .outfit-header h2 {
        color: var(--charcoal);
        font-size: 3rem;
        font-weight: 400;
        margin-bottom: 1rem;
    }

    .outfit-header p {
        color: var(--text-muted);
        font-size: 1.1rem;
        max-width: 600px;
        margin: 0 auto;
    }

    .outfit-workspace {
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 4rem;
        margin-bottom: 4rem;
    }

    .wardrobe-picker h3,
    .styling-board h3 {
        color: var(--charcoal);
        font-size: 1.8rem;
        font-weight: 400;
        margin-bottom: 1.5rem;
    }

    .picker-filters {
        display: flex;
        gap: 0.5rem;
        margin-bottom: 2rem;
        flex-wrap: wrap;
    }

    .picker-filter {
        padding: 0.5rem 1rem;
        background: var(--off-white);
        border: 1px solid var(--soft-gray);
        color: var(--slate);
        border-radius: 20px;
        cursor: pointer;
        transition: all 0.3s ease;
        font-size: 0.85rem;
    }

    .picker-filter:hover,
    .picker-filter.active {
        background: var(--champagne);
        color: var(--charcoal);
        border-color: var(--champagne);
    }

    .picker-grid {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(120px, 1fr));
        gap: 1rem;
        max-height: 400px;
        overflow-y: auto;
        padding: 1rem;
        background: var(--off-white);
        border-radius: 10px;
    }

    .picker-item {
        background: white;
        border-radius: 8px;
        overflow: hidden;
        cursor: grab;
        transition: all 0.3s ease;
        border: 2px solid transparent;
        position: relative;
    }

    .picker-item:hover {
        transform: scale(1.05);
        border-color: var(--champagne);
        box-shadow: 0 8px 25px rgba(212, 175, 55, 0.2);
    }

    .picker-item:active {
        cursor: grabbing;
    }

    .picker-item img {
        width: 100%;
        height: 100px;
        object-fit: cover;
    }

    .picker-item-name {
        padding: 0.5rem;
        font-size: 0.8rem;
        color: var(--charcoal);
        text-align: center;
        background: white;
    }

    .outfit-canvas {
        background: var(--off-white);
        border-radius: 15px;
        padding: 2rem;
        min-height: 500px;
        display: grid;
        grid-template-columns: 1fr 1fr 1fr;
        grid-template-rows: auto auto;
        gap: 1.5rem;
        position: relative;
    }

    .outfit-slot {
        background: white;
        border: 2px dashed var(--soft-gray);
        border-radius: 10px;
        padding: 1rem;
        text-align: center;
        transition: all 0.3s ease;
        cursor: pointer;
        position: relative;
        min-height: 120px;
        display: flex;
        flex-direction: column;
        justify-content: center;
    }

    .outfit-slot.has-item {
        border-style: solid;
        border-color: var(--champagne);
        background: var(--warm-white);
    }

    .outfit-slot.drag-over {
        border-color: var(--champagne);
        background: rgba(212, 175, 55, 0.1);
        transform: scale(1.02);
    }

    .outfit-slot[data-type="outerwear"] {
        grid-column: 1 / 2;
        grid-row: 1 / 2;
    }

    .outfit-slot[data-type="tops"] {
        grid-column: 2 / 3;
        grid-row: 1 / 2;
    }

    .outfit-slot[data-type="bottoms"] {
        grid-column: 3 / 4;
        grid-row: 1 / 2;
    }

    .outfit-slot[data-type="dresses"] {
        grid-column: 1 / 3;
        grid-row: 2 / 3;
    }

    .outfit-slot[data-type="shoes"] {
        grid-column: 3 / 4;
        grid-row: 2 / 3;
    }

    .outfit-slot.accessories-slot {
        grid-column: 1 / 4;
        grid-row: 3 / 4;
        min-height: 80px;
    }

    .slot-label {
        font-size: 0.9rem;
        color: var(--champagne);
        font-weight: 500;
        margin-bottom: 0.5rem;
    }

    .slot-placeholder {
        color: var(--text-muted);
        font-size: 0.85rem;
        font-style: italic;
    }

    .slot-item {
        position: relative;
    }

    .slot-item img {
        width: 100%;
        height: 80px;
        object-fit: cover;
        border-radius: 5px;
        margin-bottom: 0.5rem;
    }

    .slot-item-name {
        font-size: 0.8rem;
        color: var(--charcoal);
        font-weight: 500;
    }

    .remove-item {
        position: absolute;
        top: -5px;
        right: -5px;
        background: var(--champagne);
        color: white;
        border: none;
        border-radius: 50%;
        width: 20px;
        height: 20px;
        cursor: pointer;
        font-size: 0.7rem;
        display: flex;
        align-items: center;
        justify-content: center;
    }

    .outfit-actions {
        display: flex;
        gap: 1rem;
        margin-top: 2rem;
        justify-content: center;
        flex-wrap: wrap;
    }

    .outfit-actions button {
        padding: 0.8rem 1.5rem;
        border: none;
        border-radius: 25px;
        cursor: pointer;
        font-weight: 500;
        transition: all 0.3s ease;
    }

    .save-outfit-btn {
        background: var(--champagne);
        color: var(--charcoal);
    }

    .save-outfit-btn:hover {
        background: var(--champagne-light);
        transform: translateY(-2px);
    }

    .clear-outfit-btn {
        background: var(--soft-gray);
        color: var(--slate);
    }

    .clear-outfit-btn:hover {
        background: var(--text-muted);
        color: white;
    }

    .random-outfit-btn {
        background: var(--charcoal);
        color: var(--off-white);
    }

    .random-outfit-btn:hover {
        background: var(--slate);
    }

    .saved-outfits {
        margin-top: 4rem;
    }

    .saved-outfits h3 {
        color: var(--charcoal);
        font-size: 2rem;
        font-weight: 400;
        margin-bottom: 2rem;
        text-align: center;
    }

    .saved-outfits-grid {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
        gap: 2rem;
    }

    .saved-outfit {
        background: white;
        border-radius: 15px;
        padding: 1.5rem;
        box-shadow: 0 4px 20px rgba(74, 85, 104, 0.1);
        transition: all 0.3s ease;
        cursor: pointer;
    }

    .saved-outfit:hover {
        transform: translateY(-5px);
        box-shadow: 0 8px 30px rgba(74, 85, 104, 0.15);
    }

    .saved-outfit-preview {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(60px, 1fr));
        gap: 0.5rem;
        margin-bottom: 1rem;
    }

    .saved-outfit-item img {
        width: 100%;
        height: 60px;
        object-fit: cover;
        border-radius: 5px;
    }

    .saved-outfit-name {
        font-family: 'Cormorant Garamond', serif;
        font-size: 1.2rem;
        color: var(--charcoal);
        margin-bottom: 0.5rem;
    }

    .saved-outfit-date {
        color: var(--text-muted);
        font-size: 0.85rem;
    }

    .no-items-message {
        text-align: center;
        color: var(--text-muted);
        font-style: italic;
        padding: 2rem;
        grid-column: 1 / -1;
    }

    @media (max-width: 768px) {
        .outfit-workspace {
            grid-template-columns: 1fr;
            gap: 3rem;
        }
        
        .outfit-canvas {
            grid-template-columns: 1fr 1fr;
            gap: 1rem;
        }
        
        .outfit-slot[data-type="dresses"] {
            grid-column: 1 / 3;
        }
        
        .outfit-slot.accessories-slot {
            grid-column: 1 / 3;
        }
    }
</style>

<script>
    // Wardrobe Management System
    let personalWardrobe = JSON.parse(localStorage.getItem('personalWardrobe')) || [];
    
    function openModal() {
        document.getElementById('wardrobeModal').style.display = 'block';
        document.body.style.overflow = 'hidden';
    }
    
    function closeModal() {
        document.getElementById('wardrobeModal').style.display = 'none';
        document.body.style.overflow = 'auto';
        document.getElementById('addItemForm').reset();
        document.getElementById('photoPreview').innerHTML = '';
    }
    
    // Photo preview functionality
    document.getElementById('itemPhoto').addEventListener('change', function(e) {
        const file = e.target.files[0];
        if (file) {
            const reader = new FileReader();
            reader.onload = function(e) {
                document.getElementById('photoPreview').innerHTML = 
                    `<img src="${e.target.result}" alt="Item preview">`;
            };
            reader.readAsDataURL(file);
        }
    });
    
    function addWardrobeItem(event) {
        event.preventDefault();
        
        const formData = new FormData(event.target);
        const photoFile = document.getElementById('itemPhoto').files[0];
        
        if (photoFile) {
            const reader = new FileReader();
            reader.onload = function(e) {
                const newItem = {
                    id: Date.now(),
                    name: document.getElementById('itemName').value,
                    category: document.getElementById('itemCategory').value,
                    brand: document.getElementById('itemBrand').value,
                    color: document.getElementById('itemColor').value,
                    fabric: document.getElementById('itemFabric').value,
                    purchaseDate: document.getElementById('itemPurchaseDate').value,
                    notes: document.getElementById('itemNotes').value,
                    photo: e.target.result,
                    addedDate: new Date().toISOString(),
                    wearCount: 0
                };
                
                personalWardrobe.push(newItem);
                localStorage.setItem('personalWardrobe', JSON.stringify(personalWardrobe));
                
                closeModal();
                showPersonalWardrobe();
                renderWardrobe();
                updateWardrobeStats();
            };
            reader.readAsDataURL(photoFile);
        }
    }
    
    function renderWardrobe() {
        const grid = document.getElementById('personalWardrobeGrid');
        if (!grid) return;
        
        if (personalWardrobe.length === 0) {
            grid.innerHTML = `
                <div style="grid-column: 1/-1; text-align: center; padding: 4rem; color: var(--text-muted);">
                    <h3 class="serif" style="margin-bottom: 1rem;">Your wardrobe awaits</h3>
                    <p>Start building your sustainable collection by adding your first piece.</p>
                    <button onclick="openModal()" style="margin-top: 2rem; background: var(--champagne); color: var(--charcoal); padding: 1rem 2rem; border: none; border-radius: 25px; cursor: pointer;">Add Your First Item</button>
                </div>
            `;
            return;
        }
        
        grid.innerHTML = personalWardrobe.map(item => `
            <div class="wardrobe-item" data-category="${item.category}" onclick="viewItem(${item.id})">
                <img src="${item.photo}" alt="${item.name}" loading="lazy">
                <div class="wardrobe-item-info">
                    <h4>${item.name}</h4>
                    <div class="wardrobe-item-meta">
                        ${item.brand ? item.brand + ' • ' : ''}${item.category} ${item.color ? '• ' + item.color : ''}
                    </div>
                    <div class="wardrobe-item-notes">
                        ${item.notes || 'A timeless addition to your conscious collection.'}
                    </div>
                </div>
            </div>
        `).join('');
    }
    
    function filterWardrobe(category) {
        // Update filter button states
        document.querySelectorAll('.wardrobe-filters .filter-btn').forEach(btn => {
            btn.classList.remove('active');
        });
        event.target.classList.add('active');
        
        // Filter items
        const items = document.querySelectorAll('.wardrobe-item');
        items.forEach(item => {
            if (category === 'all' || item.dataset.category === category) {
                item.style.display = 'block';
            } else {
                item.style.display = 'none';
            }
        });
    }
    
    function updateWardrobeStats() {
        const stats = document.getElementById('wardrobeStats');
        if (stats) {
            const totalItems = personalWardrobe.length;
            const categories = [...new Set(personalWardrobe.map(item => item.category))].length;
            stats.innerHTML = `${totalItems} pieces • ${categories} categories`;
        }
    }
    
    function viewItem(itemId) {
        const item = personalWardrobe.find(i => i.id === itemId);
        if (item) {
            alert(`${item.name}\n\nBrand: ${item.brand || 'N/A'}\nFabric: ${item.fabric || 'N/A'}\nAdded: ${new Date(item.addedDate).toLocaleDateString()}\nWear Count: ${item.wearCount}\n\nNotes: ${item.notes || 'No notes yet.'}`);
            
            // In a full app, this would open a detailed view modal
        }
    }
    
    function showPersonalWardrobe() {
        // Hide gallery, show personal wardrobe
        document.getElementById('gallery').style.display = 'none';
        document.getElementById('edit').style.display = 'none';
        document.getElementById('journal').style.display = 'none';
        document.getElementById('exchange').style.display = 'none';
        
        let wardrobeSection = document.getElementById('my-wardrobe');
        if (!wardrobeSection) {
            // Create the section if it doesn't exist
            wardrobeSection = document.createElement('section');
            wardrobeSection.id = 'my-wardrobe';
            wardrobeSection.className = 'personal-wardrobe';
            document.querySelector('#exchange').insertAdjacentElement('beforebegin', wardrobeSection);
        }
        
        wardrobeSection.style.display = 'block';
        wardrobeSection.innerHTML = `
            <div class="wardrobe-header">
                <h2 class="serif">Your Personal Collection</h2>
                <div class="wardrobe-stats" id="wardrobeStats"></div>
                <button onclick="openModal()" class="add-item-btn">Add New Piece</button>
            </div>
            
            <div class="wardrobe-filters">
                <button class="filter-btn active" onclick="filterWardrobe('all')">All Items</button>
                <button class="filter-btn" onclick="filterWardrobe('tops')">Tops</button>
                <button class="filter-btn" onclick="filterWardrobe('bottoms')">Bottoms</button>
                <button class="filter-btn" onclick="filterWardrobe('outerwear')">Outerwear</button>
                <button class="filter-btn" onclick="filterWardrobe('dresses')">Dresses</button>
                <button class="filter-btn" onclick="filterWardrobe('accessories')">Accessories</button>
                <button class="filter-btn" onclick="filterWardrobe('shoes')">Shoes</button>
            </div>
            
            <div id="personalWardrobeGrid" class="wardrobe-grid"></div>
        `;
        
        renderWardrobe();
        updateWardrobeStats();
    }
    
    // Outfit Creator System
    let savedOutfits = JSON.parse(localStorage.getItem('savedOutfits')) || [];
    let currentOutfit = {};

    function showOutfitCreator() {
        // Hide other sections
        document.getElementById('gallery').style.display = 'none';
        document.getElementById('edit').style.display = 'none';
        document.getElementById('journal').style.display = 'none';
        document.getElementById('exchange').style.display = 'none';
        document.getElementById('my-wardrobe').style.display = 'none';
        
        // Show outfit creator
        document.getElementById('outfit-creator').style.display = 'block';
        
        renderWardrobePicker();
        renderSavedOutfits();
    }

    function renderWardrobePicker() {
        const picker = document.getElementById('wardrobePicker');
        if (!picker) return;

        if (personalWardrobe.length === 0) {
            picker.innerHTML = `
                <div class="no-items-message">
                    Add items to your wardrobe first to start creating outfits!
                    <br><br>
                    <button onclick="showPersonalWardrobe()" style="background: var(--champagne); color: var(--charcoal); padding: 0.8rem 1.5rem; border: none; border-radius: 20px; cursor: pointer;">Add Items to Wardrobe</button>
                </div>
            `;
            return;
        }

        picker.innerHTML = personalWardrobe.map(item => `
            <div class="picker-item" draggable="true" data-item-id="${item.id}" data-category="${item.category}">
                <img src="${item.photo}" alt="${item.name}" loading="lazy">
                <div class="picker-item-name">${item.name}</div>
            </div>
        `).join('');

        // Add drag event listeners
        picker.querySelectorAll('.picker-item').forEach(item => {
            item.addEventListener('dragstart', handleDragStart);
            item.addEventListener('click', handlePickerItemClick);
        });
    }

    function filterPicker(category) {
        // Update filter button states
        document.querySelectorAll('.picker-filter').forEach(btn => {
            btn.classList.remove('active');
        });
        event.target.classList.add('active');

        // Filter items
        const items = document.querySelectorAll('.picker-item');
        items.forEach(item => {
            if (category === 'all' || item.dataset.category === category) {
                item.style.display = 'block';
            } else {
                item.style.display = 'none';
            }
        });
    }

    function handleDragStart(e) {
        e.dataTransfer.setData('text/plain', e.target.dataset.itemId);
        e.dataTransfer.setData('application/json', JSON.stringify({
            itemId: e.target.dataset.itemId,
            category: e.target.dataset.category
        }));
    }

    function handlePickerItemClick(e) {
        const itemId = parseInt(e.currentTarget.dataset.itemId);
        const category = e.currentTarget.dataset.category;
        const item = personalWardrobe.find(i => i.id === itemId);
        
        if (item) {
            addToOutfit(item, category);
        }
    }

    function addToOutfit(item, category) {
        // Find appropriate slot
        let targetSlot = document.querySelector(`.outfit-slot[data-type="${category}"]`);
        
        // If it's a dress, it can go in either dresses or tops slot
        if (category === 'dresses' && !targetSlot.querySelector('.slot-item')) {
            targetSlot = document.querySelector('.outfit-slot[data-type="dresses"]');
        } else if (category === 'dresses') {
            targetSlot = document.querySelector('.outfit-slot[data-type="tops"]');
        }

        if (targetSlot && (!targetSlot.querySelector('.slot-item') || category === 'accessories')) {
            if (category === 'accessories') {
                // Accessories can have multiple items
                if (!targetSlot.querySelector('.accessories-container')) {
                    targetSlot.innerHTML = `
                        <div class="slot-label">Accessories</div>
                        <div class="accessories-container"></div>
                    `;
                }
                const container = targetSlot.querySelector('.accessories-container');
                const accessoryDiv = document.createElement('div');
                accessoryDiv.className = 'slot-item accessory-item';
                accessoryDiv.innerHTML = `
                    <img src="${item.photo}" alt="${item.name}">
                    <div class="slot-item-name">${item.name}</div>
                    <button class="remove-item" onclick="removeAccessory(this, ${item.id})">&times;</button>
                `;
                container.appendChild(accessoryDiv);
            } else {
                targetSlot.innerHTML = `
                    <div class="slot-label">${category.charAt(0).toUpperCase() + category.slice(1)}</div>
                    <div class="slot-item">
                        <img src="${item.photo}" alt="${item.name}">
                        <div class="slot-item-name">${item.name}</div>
                        <button class="remove-item" onclick="removeFromSlot(this)">&times;</button>
                    </div>
                `;
            }
            targetSlot.classList.add('has-item');
            currentOutfit[category] = currentOutfit[category] || [];
            if (!currentOutfit[category].find(i => i.id === item.id)) {
                currentOutfit[category].push(item);
            }
        }
    }

    function removeFromOutfit(slot) {
        if (slot.classList.contains('has-item')) {
            const category = slot.dataset.type;
            const label = category.charAt(0).toUpperCase() + category.slice(1);
            
            if (category === 'accessories') {
                slot.innerHTML = `
                    <div class="slot-label">Accessories</div>
                    <div class="slot-placeholder">Add accessories</div>
                `;
            } else {
                slot.innerHTML = `
                    <div class="slot-label">${label}</div>
                    <div class="slot-placeholder">${getPlaceholderText(category)}</div>
                `;
            }
            
            slot.classList.remove('has-item');
            delete currentOutfit[category];
        }
    }

    function removeFromSlot(button) {
        const slot = button.closest('.outfit-slot');
        removeFromOutfit(slot);
    }

    function removeAccessory(button, itemId) {
        button.parentElement.remove();
        const slot = button.closest('.outfit-slot');
        
        if (currentOutfit.accessories) {
            currentOutfit.accessories = currentOutfit.accessories.filter(item => item.id !== itemId);
            if (currentOutfit.accessories.length === 0) {
                delete currentOutfit.accessories;
                slot.classList.remove('has-item');
                slot.innerHTML = `
                    <div class="slot-label">Accessories</div>
                    <div class="slot-placeholder">Add accessories</div>
                `;
            }
        }
    }

    function getPlaceholderText(category) {
        const placeholders = {
            'outerwear': 'Drag a jacket or coat here',
            'tops': 'Drag a top here',
            'bottoms': 'Drag pants or skirt here',
            'dresses': 'Or drag a dress here',
            'shoes': 'Drag shoes here',
            'accessories': 'Add accessories'
        };
        return placeholders[category] || 'Drag item here';
    }

    function clearOutfit() {
        currentOutfit = {};
        document.querySelectorAll('.outfit-slot').forEach(slot => {
            removeFromOutfit(slot);
        });
    }

    function randomOutfit() {
        clearOutfit();
        
        if (personalWardrobe.length === 0) return;

        // Get random items from each category
        const categories = ['tops', 'bottoms', 'outerwear', 'shoes'];
        categories.forEach(category => {
            const categoryItems = personalWardrobe.filter(item => item.category === category);
            if (categoryItems.length > 0) {
                const randomItem = categoryItems[Math.floor(Math.random() * categoryItems.length)];
                addToOutfit(randomItem, category);
            }
        });

        // Maybe add some accessories
        const accessories = personalWardrobe.filter(item => item.category === 'accessories');
        if (accessories.length > 0 && Math.random() > 0.5) {
            const randomAccessory = accessories[Math.floor(Math.random() * accessories.length)];
            addToOutfit(randomAccessory, 'accessories');
        }
    }

    function saveOutfit() {
        const outfitItems = Object.values(currentOutfit).flat();
        if (outfitItems.length === 0) {
            alert('Add some items to your outfit first!');
            return;
        }

        const outfitName = prompt('Give your outfit a name:', `Look ${savedOutfits.length + 1}`);
        if (!outfitName) return;

        const newOutfit = {
            id: Date.now(),
            name: outfitName,
            items: currentOutfit,
            createdDate: new Date().toISOString(),
            allItems: outfitItems
        };

        savedOutfits.push(newOutfit);
        localStorage.setItem('savedOutfits', JSON.stringify(savedOutfits));
        renderSavedOutfits();
        
        alert('Outfit saved successfully!');
    }

    function renderSavedOutfits() {
        const grid = document.getElementById('savedOutfitsGrid');
        if (!grid) return;

        if (savedOutfits.length === 0) {
            grid.innerHTML = `
                <div style="grid-column: 1/-1; text-align: center; padding: 3rem; color: var(--text-muted);">
                    <p>No saved outfits yet. Create your first look!</p>
                </div>
            `;
            return;
        }

        grid.innerHTML = savedOutfits.map(outfit => `
            <div class="saved-outfit" onclick="loadOutfit(${outfit.id})">
                <div class="saved-outfit-preview">
                    ${outfit.allItems.slice(0, 4).map(item => `
                        <div class="saved-outfit-item">
                            <img src="${item.photo}" alt="${item.name}" loading="lazy">
                        </div>
                    `).join('')}
                </div>
                <div class="saved-outfit-name">${outfit.name}</div>
                <div class="saved-outfit-date">
                    Created ${new Date(outfit.createdDate).toLocaleDateString()}
                </div>
            </div>
        `).join('');
    }

    function loadOutfit(outfitId) {
        const outfit = savedOutfits.find(o => o.id === outfitId);
        if (!outfit) return;

        clearOutfit();
        
        // Load each category of items
        Object.entries(outfit.items).forEach(([category, items]) => {
            items.forEach(item => {
                addToOutfit(item, category);
            });
        });

        alert(`Loaded outfit: ${outfit.name}`);
    }

    // Setup drag and drop for outfit slots
    document.addEventListener('DOMContentLoaded', function() {
        // Add outfit creator link to navigation
        const navLinks = document.querySelector('.nav-links');
        const outfitLink = document.createElement('li');
        outfitLink.innerHTML = '<a href="#" onclick="showOutfitCreator(); return false;">Style Board</a>';
        navLinks.appendChild(outfitLink);

        // Setup drag and drop
        setTimeout(() => {
            const slots = document.querySelectorAll('.outfit-slot');
            slots.forEach(slot => {
                slot.addEventListener('dragover', handleDragOver);
                slot.addEventListener('drop', handleDrop);
                slot.addEventListener('dragenter', handleDragEnter);
                slot.addEventListener('dragleave', handleDragLeave);
            });
        }, 500);
    });

    function handleDragOver(e) {
        e.preventDefault();
    }

    function handleDragEnter(e) {
        e.preventDefault();
        e.target.classList.add('drag-over');
    }

    function handleDragLeave(e) {
        e.target.classList.remove('drag-over');
    }

    function handleDrop(e) {
        e.preventDefault();
        e.target.classList.remove('drag-over');
        
        const itemId = parseInt(e.dataTransfer.getData('text/plain'));
        const item = personalWardrobe.find(i => i.id === itemId);
        const slotType = e.target.dataset.type || e.target.closest('.outfit-slot').dataset.type;
        
        if (item && slotType) {
            // Check if item category matches slot or if it's a flexible item
            if (item.category === slotType || 
               (item.category === 'dresses' && (slotType === 'dresses' || slotType === 'tops')) ||
               slotType === 'accessories') {
                addToOutfit(item, item.category);
            } else {
                alert(`This ${item.category} doesn't fit in the ${slotType} slot. Try a different slot!`);
            }
        }
    }

    // Smooth scrolling
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
        anchor.addEventListener('click', function (e) {
            e.preventDefault();
            const target = document.querySelector(this.getAttribute('href'));
            if (target) {
                target.scrollIntoView({
                    behavior: 'smooth',
                    block: 'start'
                });
            }
        });
    });

    // Performance optimizations
    const observerOptions = {
        threshold: 0.1,
        rootMargin: '0px 0px -30px 0px'
    };

    const observer = new IntersectionObserver(function(entries) {
        entries.forEach(entry => {
            if (entry.isIntersecting) {
                entry.target.classList.add('visible');
                // Unobserve after animation to save performance
                observer.unobserve(entry.target);
            }
        });
    }, observerOptions);

    // Throttled scroll handler for better performance
    let ticking = false;
    function updateOnScroll() {
        if (!ticking) {
            requestAnimationFrame(() => {
                const scrolled = window.pageYOffset;
                
                // Header background
                const header = document.querySelector('.header');
                if (scrolled > 50) {
                    header.style.background = 'rgba(253, 252, 249, 0.98)';
                } else {
                    header.style.background = 'rgba(253, 252, 249, 0.95)';
                }

                // Reduced parallax effect for performance
                const parallaxElements = document.querySelectorAll('.parallax-section');
                parallaxElements.forEach(element => {
                    const speed = 0.1; // Reduced from 0.3
                    element.style.transform = `translate3d(0, ${scrolled * speed}px, 0)`;
                });
                
                ticking = false;
            });
            ticking = true;
        }
    }

    // Smooth scrolling
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
        anchor.addEventListener('click', function (e) {
            e.preventDefault();
            const target = document.querySelector(this.getAttribute('href'));
            if (target) {
                target.scrollIntoView({
                    behavior: 'smooth',
                    block: 'start'
                });
            }
        });
    });

    // Optimized fade-in animation setup
    document.addEventListener('DOMContentLoaded', function() {
        // Observe fade-in elements
        document.querySelectorAll('.fade-in').forEach(el => {
            observer.observe(el);
        });

        // Add navigation links with debounced click handlers
        const navLinks = document.querySelector('.nav-links');
        
        const wardrobeLink = document.createElement('li');
        wardrobeLink.innerHTML = '<a href="#" onclick="showPersonalWardrobe(); return false;">My Wardrobe</a>';
        navLinks.appendChild(wardrobeLink);

        const outfitLink = document.createElement('li');
        outfitLink.innerHTML = '<a href="#" onclick="showOutfitCreator(); return false;">Style Board</a>';
        navLinks.appendChild(outfitLink);

        // Setup optimized drag and drop with delay to prevent render blocking
        setTimeout(() => {
            const slots = document.querySelectorAll('.outfit-slot');
            slots.forEach(slot => {
                slot.addEventListener('dragover', handleDragOver, { passive: false });
                slot.addEventListener('drop', handleDrop, { passive: false });
                slot.addEventListener('dragenter', handleDragEnter, { passive: true });
                slot.addEventListener('dragleave', handleDragLeave, { passive: true });
            });
        }, 1000);

        // Load existing data without blocking
        requestIdleCallback(() => {
            if (personalWardrobe.length > 0) {
                updateWardrobeStats();
            }
        });
    });

    // Use passive scroll listener for better performance
    window.addEventListener('scroll', updateOnScroll, { passive: true });

    // Gallery item interactions
    document.querySelectorAll('.gallery-item').forEach(item => {
        item.addEventListener('click', function() {
            // Simulate opening detailed view
            const itemTitle = this.querySelector('h3').textContent;
            alert(`Opening detailed view for: ${itemTitle}\n\nThis would show the full story, care instructions, styling suggestions, and impact metrics in an elegant overlay.`);
        });
    });

    // Lookbook interactions
    document.querySelectorAll('.edit-item').forEach(item => {
        item.addEventListener('click', function() {
            const itemName = this.querySelector('h4').textContent;
            alert(`Viewing ${itemName} in the lookbook spread.\n\nThis would show styling details, care notes, and how this piece integrates with the seasonal edit.`);
        });
    });
</script>
```

</body>
</html>
