[[Uploading aqua_fish_farm_studio.html…]()
shastha-site.html](https://github.com/user-attachments/files/32759325/shastha-site.html)
[shastha-site.html](https://github.com/user-attachments/files/32759282/shastha-site.html)
[Uploading shastha-site.html…]()
[index-2.html](https://github.com/user-attachments/files/32739161/index-2.html)
[index.html](https://github.com/user-attachments/files/32738961/index.html)
<!DOCTYPE html><!DOCTYPE html<!DOCTYPE html>
<html lang="en">
<head><!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Aqua Fish Farm - Premium Ornamental Fish & Supplies</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- FontAwesome for Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- Google Fonts: Inter -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                    },
                    colors: {
                        aqua: {
                            50: '#ecfeff',
                            100: '#cffafe',
                            500: '#06b6d4',
                            600: '#0891b2',
                            700: '#0e7490',
                            800: '#155e75',
                            900: '#164e63',
                        }
                    }
                }
            }
        }
    </script>
    <style>
        ::-webkit-scrollbar { width: 8px; }
        ::-webkit-scrollbar-track { background: #f1f5f9; }
        ::-webkit-scrollbar-thumb { background: #cbd5e1; border-radius: 4px; }
        ::-webkit-scrollbar-thumb:hover { background: #94a3b8; }
        .fade-in { animation: fadeIn 0.3s ease-in-out forwards; }
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(6px); }
            to { opacity: 1; transform: translateY(0); }
        }
    </style>
</head>
<body class="bg-slate-50 text-slate-800 font-sans antialiased min-h-screen flex flex-col justify-between">

    <header class="sticky top-0 z-40 bg-white/95 backdrop-blur border-b border-slate-200 shadow-sm">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 h-20 flex items-center justify-between">
            <!-- Farm Logo / Branding -->
            <div class="flex items-center space-x-3 cursor-pointer" onclick="filterCategory('All'); window.scrollTo({top: 0, behavior: 'smooth'});">
                <div class="w-12 h-12 bg-gradient-to-tr from-cyan-600 to-blue-600 rounded-2xl flex items-center justify-center text-white shadow-md shadow-cyan-500/20">
                    <i class="fa-solid fa-fish text-2xl"></i>
                </div>
                <div>
                    <h1 id="brandTitle" class="text-xl sm:text-2xl font-black tracking-tight text-slate-900">Aqua Fish Farm</h1>
                    <p id="brandSubtitle" class="text-xs text-slate-500 font-medium">Direct Breeder & Supplier</p>
                </div>
            </div>

            <!-- Navigation Actions -->
            <div class="flex items-center space-x-3 sm:space-x-4">
                <!-- Admin Mode Toggle -->
                <button onclick="toggleAdminMode()" id="adminToggleBtn" class="flex items-center space-x-2 px-3.5 py-2 rounded-xl text-xs sm:text-sm font-semibold transition border border-slate-200 bg-slate-100 hover:bg-slate-200 text-slate-700">
                    <i class="fa-solid fa-shield-halved text-cyan-600"></i>
                    <span id="adminToggleText">Admin Mode: OFF</span>
                </button>

                <!-- Cart Button -->
                <button onclick="toggleCartModal(true)" class="relative flex items-center space-x-2 bg-cyan-600 hover:bg-cyan-700 text-white px-4 py-2.5 rounded-xl font-semibold shadow-lg shadow-cyan-600/20 transition transform active:scale-95">
                    <i class="fa-solid fa-cart-shopping"></i>
                    <span class="hidden sm:inline">Cart</span>
                    <span id="cartBadge" class="absolute -top-1.5 -right-1.5 bg-rose-500 text-white text-xs w-5 h-5 rounded-full flex items-center justify-center font-bold shadow-md">0</span>
                </button>
            </div>
        </div>
    </header>

    <section class="relative bg-gradient-to-r from-cyan-900 via-slate-900 to-blue-950 text-white py-14 px-4 sm:px-6 lg:px-8 overflow-hidden shadow-inner">
        <div class="absolute inset-0 opacity-15 bg-[radial-gradient(#06b6d4_1px,transparent_1px)] [background-size:16px_16px]"></div>
        <div class="max-w-7xl mx-auto relative z-10 flex flex-col md:flex-row items-center justify-between gap-8">
            <div class="max-w-2xl text-center md:text-left">
                <span class="inline-flex items-center space-x-2 px-3.5 py-1.5 rounded-full text-xs font-semibold bg-cyan-500/20 text-cyan-300 border border-cyan-500/30 mb-4">
                    <i class="fa-solid fa-water"></i>
                    <span>High Quality Aquatic Livestock, Videos & Reviews</span>
                </span>
                <h2 id="heroHeading" class="text-3xl sm:text-5xl font-extrabold tracking-tight mb-4">
                    Healthy Fish. Vibrant Aquariums. Direct From Our Farm.
                </h2>
                <p id="heroSubheading" class="text-slate-300 text-sm sm:text-base leading-relaxed mb-6">
                    Explore our premium selection featuring live videos of specimens, customer ratings, specialized feeds, and secure ordering!
                </p>
                <div class="flex flex-wrap justify-center md:justify-start gap-3">
                    <a href="#catalogSection" class="bg-cyan-500 hover:bg-cyan-600 text-white font-semibold px-6 py-3 rounded-xl shadow-lg shadow-cyan-500/25 transition">
                        Browse Catalog
                    </a>
                    <button onclick="openFarmSettingsModal()" id="editFarmBtn" class="hidden bg-white/10 hover:bg-white/20 text-white font-semibold px-5 py-3 rounded-xl backdrop-blur border border-white/20 transition">
                        <i class="fa-solid fa-pen-to-square mr-2"></i> Edit Farm Details
                    </button>
                </div>
            </div>
            <div class="w-full md:w-auto flex justify-center">
                <div class="relative w-72 sm:w-80 h-48 sm:h-56 rounded-3xl overflow-hidden shadow-2xl border-4 border-white/10 bg-slate-800 flex items-center justify-center">
                    <img id="heroImage" src="https://images.unsplash.com/photo-1522069169874-c58ec4b76be5?auto=format&fit=crop&w=800&q=80" alt="Aquarium fish" class="w-full h-full object-cover opacity-90">
                    <div class="absolute inset-0 bg-gradient-to-t from-slate-950/80 via-transparent to-transparent flex items-end p-4">
                        <p class="text-xs text-cyan-300 font-semibold flex items-center"><i class="fa-solid fa-circle-check mr-1.5"></i> Farm Verified Stock</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <main id="catalogSection" class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-10 flex-grow w-full">
        <!-- Section Header & Controls -->
        <div class="flex flex-col md:flex-row md:items-center md:justify-between gap-4 mb-8">
            <div>
                <h3 class="text-2xl font-bold text-slate-900 tracking-tight">Farm Catalog & Inventory</h3>
                <p class="text-sm text-slate-500">Click any product to watch videos, inspect photos, and read/write customer reviews.</p>
            </div>

            <!-- Add Product Button (Visible only in Admin Mode) -->
            <div id="adminActionContainer" class="hidden">
                <button onclick="openProductModal()" class="bg-emerald-600 hover:bg-emerald-700 text-white px-5 py-2.5 rounded-xl font-semibold shadow-md shadow-emerald-600/20 flex items-center space-x-2 transition">
                    <i class="fa-solid fa-plus-circle"></i>
                    <span>Add New Product</span>
                </button>
            </div>
        </div>

        <!-- Filters and Search Bar -->
        <div class="bg-white p-4 rounded-2xl shadow-sm border border-slate-200 mb-8 flex flex-col lg:flex-row gap-4 items-center justify-between">
            <!-- Category Tabs -->
            <div id="categoryTabs" class="flex flex-wrap gap-2 w-full lg:w-auto">
                <button onclick="filterCategory('All')" class="category-btn px-4 py-2 rounded-xl text-sm font-semibold transition bg-cyan-600 text-white shadow-sm" data-category="All">
                    All Items
                </button>
                <button onclick="filterCategory('Live Fish & Plants')" class="category-btn px-4 py-2 rounded-xl text-sm font-semibold transition bg-slate-100 text-slate-600 hover:bg-slate-200" data-category="Live Fish & Plants">
                    Live Fish & Plants
                </button>
                <button onclick="filterCategory('Feed & Cultures')" class="category-btn px-4 py-2 rounded-xl text-sm font-semibold transition bg-slate-100 text-slate-600 hover:bg-slate-200" data-category="Feed & Cultures">
                    Feed & Cultures
                </button>
                <button onclick="filterCategory('Dry Items & Medicine')" class="category-btn px-4 py-2 rounded-xl text-sm font-semibold transition bg-slate-100 text-slate-600 hover:bg-slate-200" data-category="Dry Items & Medicine">
                    Dry Items & Medicine
                </button>
            </div>

            <!-- Search Input -->
            <div class="relative w-full lg:w-72">
                <i class="fa-solid fa-search absolute left-3.5 top-3.5 text-slate-400"></i>
                <input type="text" id="searchInput" oninput="handleSearch()" placeholder="Search fish, feed, medicine..." class="w-full pl-10 pr-4 py-2.5 bg-slate-50 border border-slate-200 rounded-xl text-sm focus:outline-none focus:ring-2 focus:ring-cyan-500 focus:bg-white transition">
            </div>
        </div>

        <!-- Product Grid -->
        <div id="productGrid" class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-6">
            <!-- Dynamically populated via JavaScript -->
        </div>

        <!-- Empty State -->
        <div id="emptyState" class="hidden text-center py-16">
            <div class="w-16 h-16 bg-slate-100 text-slate-400 rounded-full flex items-center justify-center mx-auto mb-4 text-2xl">
                <i class="fa-solid fa-box-open"></i>
            </div>
            <h4 class="text-lg font-bold text-slate-700">No products found</h4>
            <p class="text-sm text-slate-500 mt-1">Try searching for something else or add a new product in Admin Mode.</p>
        </div>
    </main>

    <div id="cartModal" class="fixed inset-0 z-50 overflow-hidden hidden">
        <div class="absolute inset-0 bg-slate-900/60 backdrop-blur-sm transition-opacity" onclick="toggleCartModal(false)"></div>
        <div class="absolute inset-y-0 right-0 max-w-full flex pl-10">
            <div class="w-screen max-w-md bg-white shadow-2xl flex flex-col justify-between">
                <!-- Cart Header -->
                <div class="p-6 border-b border-slate-200 flex items-center justify-between bg-slate-50">
                    <div class="flex items-center space-x-2">
                        <i class="fa-solid fa-cart-shopping text-cyan-600"></i>
                        <h3 class="text-lg font-bold text-slate-900">Your Shopping Cart</h3>
                    </div>
                    <button onclick="toggleCartModal(false)" class="text-slate-400 hover:text-slate-600 p-2 rounded-lg">
                        <i class="fa-solid fa-xmark text-xl"></i>
                    </button>
                </div>

                <!-- Cart Items List -->
                <div id="cartItemsList" class="p-6 overflow-y-auto flex-grow divide-y divide-slate-100">
                    <!-- Populated dynamically -->
                </div>

                <!-- Cart Footer & Checkout -->
                <div class="p-6 border-t border-slate-200 bg-slate-50">
                    <div class="flex items-center justify-between mb-4">
                        <span class="text-sm font-medium text-slate-600">Subtotal:</span>
                        <span id="cartSubtotal" class="text-xl font-black text-slate-900">₹0.00</span>
                    </div>
                    <button onclick="openCheckoutModal()" id="checkoutBtn" class="w-full bg-cyan-600 hover:bg-cyan-700 text-white py-3.5 rounded-xl font-bold shadow-lg shadow-cyan-600/20 transition flex items-center justify-center space-x-2">
                        <span>Proceed to Checkout</span>
                        <i class="fa-solid fa-arrow-right"></i>
                    </button>
                </div>
            </div>
        </div>
    </div>

    <div id="productDetailModal" class="fixed inset-0 z-50 overflow-y-auto hidden">
        <div class="min-h-screen px-4 text-center flex items-center justify-center">
            <div class="fixed inset-0 bg-slate-900/70 backdrop-blur-sm transition-opacity" onclick="closeProductDetailModal()"></div>
            <div class="inline-block w-full max-w-3xl p-6 my-8 text-left align-middle transition-all transform bg-white shadow-2xl rounded-3xl relative z-10 max-h-[90vh] overflow-y-auto">
                <div class="flex items-center justify-between pb-4 border-b border-slate-100 mb-6">
                    <div class="flex items-center space-x-3">
                        <span id="detailCategory" class="px-3 py-1 bg-cyan-50 text-cyan-700 text-xs font-bold rounded-full border border-cyan-200">Category</span>
                        <span id="detailStock" class="px-3 py-1 bg-emerald-50 text-emerald-700 text-xs font-bold rounded-full border border-emerald-200">In Stock</span>
                    </div>
                    <button onclick="closeProductDetailModal()" class="text-slate-400 hover:text-slate-600 p-2 rounded-full hover:bg-slate-100"><i class="fa-solid fa-xmark text-lg"></i></button>
                </div>

                <div class="grid grid-cols-1 md:grid-cols-2 gap-6 mb-6">
                    <!-- Media Area (Image or Video) -->
                    <div>
                        <div id="detailMediaContainer" class="w-full h-64 rounded-2xl overflow-hidden bg-slate-900 shadow-inner flex items-center justify-center relative">
                            <!-- Populated dynamically: Image or Video embed -->
                        </div>
                        <div id="videoToggleContainer" class="flex gap-2 mt-3">
                            <button onclick="switchDetailMedia('photo')" id="photoTabBtn" class="flex-1 py-2 bg-cyan-600 text-white text-xs font-bold rounded-xl shadow-sm transition">
                                <i class="fa-solid fa-image mr-1"></i> Photo View
                            </button>
                            <button onclick="switchDetailMedia('video')" id="videoTabBtn" class="flex-1 py-2 bg-slate-100 text-slate-700 text-xs font-bold rounded-xl hover:bg-slate-200 transition">
                                <i class="fa-solid fa-video mr-1"></i> Watch Video
                            </button>
                        </div>
                    </div>

                    <!-- Info Area -->
                    <div class="flex flex-col justify-between">
                        <div>
                            <h3 id="detailTitle" class="text-2xl font-extrabold text-slate-900 mb-2">Product Name</h3>
                            <div class="text-2xl font-black text-cyan-700 mb-4" id="detailPrice">₹0.00</div>
                            <p id="detailDesc" class="text-sm text-slate-600 leading-relaxed mb-6">Detailed description goes here...</p>
                        </div>
                        <div id="detailActionArea">
                            <button id="detailAddToCartBtn" class="w-full bg-cyan-600 hover:bg-cyan-700 text-white py-3 rounded-xl font-bold shadow-lg shadow-cyan-600/20 transition flex items-center justify-center space-x-2">
                                <i class="fa-solid fa-cart-plus"></i>
                                <span>Add to Cart</span>
                            </button>
                        </div>
                    </div>
                </div>

                <!-- Customer Reviews Section -->
                <div class="border-t border-slate-200 pt-6 mt-6">
                    <div class="flex items-center justify-between mb-4">
                        <h4 class="text-lg font-bold text-slate-900 flex items-center">
                            <i class="fa-solid fa-star text-amber-400 mr-2"></i> Customer Reviews & Ratings
                            <span id="reviewCountBadge" class="ml-2 text-xs bg-slate-100 text-slate-600 px-2.5 py-0.5 rounded-full font-semibold">0</span>
                        </h4>
                    </div>

                    <!-- Reviews List -->
                    <div id="reviewsList" class="space-y-3 mb-6 max-h-60 overflow-y-auto pr-2">
                        <!-- Populated dynamically -->
                    </div>

                    <!-- Add Review Form -->
                    <div class="bg-slate-50 p-4 rounded-2xl border border-slate-200">
                        <h5 class="text-sm font-bold text-slate-800 mb-3">Leave Your Review</h5>
                        <form onsubmit="submitReview(event)" class="space-y-3">
                            <input type="hidden" id="reviewProductId">
                            <div class="grid grid-cols-1 sm:grid-cols-2 gap-3">
                                <div>
                                    <label class="block text-xs font-semibold text-slate-600 mb-1">Your Name</label>
                                    <input type="text" id="reviewerName" required class="w-full px-3 py-2 bg-white border border-slate-200 rounded-xl text-sm focus:outline-none focus:ring-2 focus:ring-cyan-500" placeholder="Ananya Sharma">
                                </div>
                                <div>
                                    <label class="block text-xs font-semibold text-slate-600 mb-1">Rating</label>
                                    <select id="reviewRating" class="w-full px-3 py-2 bg-white border border-slate-200 rounded-xl text-sm focus:outline-none focus:ring-2 focus:ring-cyan-500">
                                        <option value="5">⭐⭐⭐⭐⭐ (5/5 - Excellent)</option>
                                        <option value="4">⭐⭐⭐⭐ (4/5 - Very Good)</option>
                                        <option value="3">⭐⭐⭐ (3/5 - Good)</option>
                                        <option value="2">⭐⭐ (2/5 - Average)</option>
                                        <option value="1">⭐ (1/5 - Poor)</option>
                                    </select>
                                </div>
                            </div>
                            <div>
                                <label class="block text-xs font-semibold text-slate-600 mb-1">Your Feedback / Experience</label>
                                <textarea id="reviewComment" rows="2" required class="w-full px-3 py-2 bg-white border border-slate-200 rounded-xl text-sm focus:outline-none focus:ring-2 focus:ring-cyan-500" placeholder="Super healthy fish, active swimming and arrived safely!"></textarea>
                            </div>
                            <div class="flex justify-end">
                                <button type="submit" class="bg-slate-900 hover:bg-slate-800 text-white px-5 py-2 rounded-xl text-xs font-bold shadow transition">
                                    Submit Review
                                </button>
                            </div>
                        </form>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <div id="productModal" class="fixed inset-0 z-50 overflow-y-auto hidden">
        <div class="min-h-screen px-4 text-center flex items-center justify-center">
            <div class="fixed inset-0 bg-slate-900/60 backdrop-blur-sm transition-opacity" onclick="closeProductModal()"></div>
            <div class="inline-block w-full max-w-lg p-6 my-8 text-left align-middle transition-all transform bg-white shadow-2xl rounded-2xl relative z-10">
                <div class="flex items-center justify-between pb-4 border-b border-slate-100 mb-4">
                    <h3 id="productModalTitle" class="text-lg font-bold text-slate-900">Add New Product</h3>
                    <button onclick="closeProductModal()" class="text-slate-400 hover:text-slate-600"><i class="fa-solid fa-xmark text-lg"></i></button>
                </div>
                <form id="productForm" onsubmit="saveProduct(event)" class="space-y-4">
                    <input type="hidden" id="productId">
                    <div>
                        <label class="block text-xs font-semibold uppercase tracking-wider text-slate-600 mb-1">Product Name</label>
                        <input type="text" id="prodName" required class="w-full px-3.5 py-2.5 bg-slate-50 border border-slate-200 rounded-xl text-sm focus:outline-none focus:ring-2 focus:ring-cyan-500" placeholder="e.g., Guppy Pair / Artemia Cysts">
                    </div>
                    <div>
                        <label class="block text-xs font-semibold uppercase tracking-wider text-slate-600 mb-1">Category</label>
                        <select id="prodCategory" class="w-full px-3.5 py-2.5 bg-slate-50 border border-slate-200 rounded-xl text-sm focus:outline-none focus:ring-2 focus:ring-cyan-500">
                            <option value="Live Fish & Plants">Live Fish & Plants</option>
                            <option value="Feed & Cultures">Feed & Cultures</option>
                            <option value="Dry Items & Medicine">Dry Items & Medicine</option>
                        </select>
                    </div>
                    <div class="grid grid-cols-2 gap-4">
                        <div>
                            <label class="block text-xs font-semibold uppercase tracking-wider text-slate-600 mb-1">Price (₹)</label>
                            <input type="number" step="0.01" id="prodPrice" required class="w-full px-3.5 py-2.5 bg-slate-50 border border-slate-200 rounded-xl text-sm focus:outline-none focus:ring-2 focus:ring-cyan-500" placeholder="150">
                        </div>
                        <div>
                            <label class="block text-xs font-semibold uppercase tracking-wider text-slate-600 mb-1">Stock Status</label>
                            <select id="prodStock" class="w-full px-3.5 py-2.5 bg-slate-50 border border-slate-200 rounded-xl text-sm focus:outline-none focus:ring-2 focus:ring-cyan-500">
                                <option value="In Stock">In Stock</option>
                                <option value="Low Stock">Low Stock</option>
                                <option value="Out of Stock">Out of Stock</option>
                            </select>
                        </div>
                    </div>
                    <div>
                        <label class="block text-xs font-semibold uppercase tracking-wider text-slate-600 mb-1">Photo Image URL</label>
                        <input type="url" id="prodImage" required class="w-full px-3.5 py-2.5 bg-slate-50 border border-slate-200 rounded-xl text-sm focus:outline-none focus:ring-2 focus:ring-cyan-500" placeholder="https://images.unsplash.com/...">
                    </div>
                    <div>
                        <label class="block text-xs font-semibold uppercase tracking-wider text-slate-600 mb-1">Video URL (YouTube embed or MP4 link)</label>
                        <input type="url" id="prodVideo" class="w-full px-3.5 py-2.5 bg-slate-50 border border-slate-200 rounded-xl text-sm focus:outline-none focus:ring-2 focus:ring-cyan-500" placeholder="https://www.youtube.com/embed/... or MP4 link">
                    </div>
                    <div>
                        <label class="block text-xs font-semibold uppercase tracking-wider text-slate-600 mb-1">Description</label>
                        <textarea id="prodDesc" rows="3" class="w-full px-3.5 py-2.5 bg-slate-50 border border-slate-200 rounded-xl text-sm focus:outline-none focus:ring-2 focus:ring-cyan-500" placeholder="Write details about size, water parameters, feeding habits..."></textarea>
                    </div>
                    <div class="flex justify-end space-x-3 pt-3">
                        <button type="button" onclick="closeProductModal()" class="px-4 py-2.5 rounded-xl border border-slate-200 text-sm font-semibold text-slate-600 hover:bg-slate-100">Cancel</button>
                        <button type="submit" class="px-5 py-2.5 bg-cyan-600 hover:bg-cyan-700 text-white rounded-xl text-sm font-semibold shadow-md shadow-cyan-600/20">Save Product</button>
                    </div>
                </form>
            </div>
        </div>
    </div>

    <div id="farmModal" class="fixed inset-0 z-50 overflow-y-auto hidden">
        <div class="min-h-screen px-4 text-center flex items-center justify-center">
            <div class="fixed inset-0 bg-slate-900/60 backdrop-blur-sm transition-opacity" onclick="closeFarmSettingsModal()"></div>
            <div class="inline-block w-full max-w-md p-6 my-8 text-left align-middle transition-all transform bg-white shadow-2xl rounded-2xl relative z-10">
                <div class="flex items-center justify-between pb-4 border-b border-slate-100 mb-4">
                    <h3 class="text-lg font-bold text-slate-900">Edit Farm Branding</h3>
                    <button onclick="closeFarmSettingsModal()" class="text-slate-400 hover:text-slate-600"><i class="fa-solid fa-xmark text-lg"></i></button>
                </div>
                <form id="farmForm" onsubmit="saveFarmSettings(event)" class="space-y-4">
                    <div>
                        <label class="block text-xs font-semibold uppercase tracking-wider text-slate-600 mb-1">Farm Name</label>
                        <input type="text" id="farmNameInput" required class="w-full px-3.5 py-2.5 bg-slate-50 border border-slate-200 rounded-xl text-sm focus:outline-none focus:ring-2 focus:ring-cyan-500">
                    </div>
                    <div>
                        <label class="block text-xs font-semibold uppercase tracking-wider text-slate-600 mb-1">Subtitle / Tagline</label>
                        <input type="text" id="farmSubtitleInput" required class="w-full px-3.5 py-2.5 bg-slate-50 border border-slate-200 rounded-xl text-sm focus:outline-none focus:ring-2 focus:ring-cyan-500">
                    </div>
                    <div>
                        <label class="block text-xs font-semibold uppercase tracking-wider text-slate-600 mb-1">Hero Heading</label>
                        <input type="text" id="farmHeroHeadingInput" required class="w-full px-3.5 py-2.5 bg-slate-50 border border-slate-200 rounded-xl text-sm focus:outline-none focus:ring-2 focus:ring-cyan-500">
                    </div>
                    <div>
                        <label class="block text-xs font-semibold uppercase tracking-wider text-slate-600 mb-1">Hero Image URL</label>
                        <input type="url" id="farmHeroImageInput" required class="w-full px-3.5 py-2.5 bg-slate-50 border border-slate-200 rounded-xl text-sm focus:outline-none focus:ring-2 focus:ring-cyan-500">
                    </div>
                    <div class="flex justify-end space-x-3 pt-3">
                        <button type="button" onclick="closeFarmSettingsModal()" class="px-4 py-2.5 rounded-xl border border-slate-200 text-sm font-semibold text-slate-600 hover:bg-slate-100">Cancel</button>
                        <button type="submit" class="px-5 py-2.5 bg-cyan-600 hover:bg-cyan-700 text-white rounded-xl text-sm font-semibold shadow-md shadow-cyan-600/20">Update Farm</button>
                    </div>
                </form>
            </div>
        </div>
    </div>

    <div id="checkoutModal" class="fixed inset-0 z-50 overflow-y-auto hidden">
        <div class="min-h-screen px-4 text-center flex items-center justify-center">
            <div class="fixed inset-0 bg-slate-900/60 backdrop-blur-sm transition-opacity" onclick="closeCheckoutModal()"></div>
            <div class="inline-block w-full max-w-lg p-6 my-8 text-left align-middle transition-all transform bg-white shadow-2xl rounded-2xl relative z-10">
                <div class="flex items-center justify-between pb-4 border-b border-slate-100 mb-4">
                    <h3 class="text-lg font-bold text-slate-900">Complete Your Order</h3>
                    <button onclick="closeCheckoutModal()" class="text-slate-400 hover:text-slate-600"><i class="fa-solid fa-xmark text-lg"></i></button>
                </div>
                <form onsubmit="submitOrder(event)" class="space-y-4">
                    <div>
                        <label class="block text-xs font-semibold uppercase tracking-wider text-slate-600 mb-1">Full Name</label>
                        <input type="text" id="customerName" required class="w-full px-3.5 py-2.5 bg-slate-50 border border-slate-200 rounded-xl text-sm focus:outline-none focus:ring-2 focus:ring-cyan-500" placeholder="Rajesh Kumar">
                    </div>
                    <div class="grid grid-cols-2 gap-4">
                        <div>
                            <label class="block text-xs font-semibold uppercase tracking-wider text-slate-600 mb-1">Phone Number</label>
                            <input type="tel" id="customerPhone" required class="w-full px-3.5 py-2.5 bg-slate-50 border border-slate-200 rounded-xl text-sm focus:outline-none focus:ring-2 focus:ring-cyan-500" placeholder="9876543210">
                        </div>
                        <div>
                            <label class="block text-xs font-semibold uppercase tracking-wider text-slate-600 mb-1">City / Location</label>
                            <input type="text" id="customerCity" required class="w-full px-3.5 py-2.5 bg-slate-50 border border-slate-200 rounded-xl text-sm focus:outline-none focus:ring-2 focus:ring-cyan-500" placeholder="Bangalore">
                        </div>
                    </div>
                    <div>
                        <label class="block text-xs font-semibold uppercase tracking-wider text-slate-600 mb-1">Delivery Address</label>
                        <textarea id="customerAddress" rows="2" required class="w-full px-3.5 py-2.5 bg-slate-50 border border-slate-200 rounded-xl text-sm focus:outline-none focus:ring-2 focus:ring-cyan-500" placeholder="House No, Street, Landmark..."></textarea>
                    </div>
                    <div class="p-3.5 bg-cyan-50 rounded-xl border border-cyan-100 text-xs text-cyan-900">
                        <i class="fa-solid fa-circle-info mr-1.5 text-cyan-600"></i> Orders are dispatched directly from our breeding farm via bus parcel, train cargo, or local door delivery.
                    </div>
                    <div class="flex justify-end space-x-3 pt-3">
                        <button type="button" onclick="closeCheckoutModal()" class="px-4 py-2.5 rounded-xl border border-slate-200 text-sm font-semibold text-slate-600 hover:bg-slate-100">Cancel</button>
                        <button type="submit" class="px-5 py-2.5 bg-emerald-600 hover:bg-emerald-700 text-white rounded-xl text-sm font-semibold shadow-md shadow-emerald-600/20">Confirm Order</button>
                    </div>
                </form>
            </div>
        </div>
    </div>

    <div id="toastNotification" class="fixed bottom-6 right-6 z-50 transform translate-y-20 opacity-0 transition-all duration-300 pointer-events-none">
        <div class="bg-slate-900 text-white px-5 py-3.5 rounded-2xl shadow-2xl flex items-center space-x-3 border border-slate-700">
            <i id="toastIcon" class="fa-solid fa-circle-check text-emerald-400 text-lg"></i>
            <div>
                <h5 id="toastTitle" class="text-sm font-bold">Success</h5>
                <p id="toastMsg" class="text-xs text-slate-300">Item updated successfully.</p>
            </div>
        </div>
    </div>

    <footer class="bg-slate-900 text-white border-t border-slate-800 mt-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-12">
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8 mb-8">
                <div>
                    <div class="flex items-center space-x-3 mb-4">
                        <div class="w-10 h-10 bg-cyan-600 rounded-xl flex items-center justify-center text-white">
                            <i class="fa-solid fa-fish text-xl"></i>
                        </div>
                        <h4 id="footerBrand" class="text-lg font-bold">Aqua Fish Farm</h4>
                    </div>
                    <p class="text-slate-400 text-sm leading-relaxed">
                        Dedicated breeding and supply of healthy ornamental fish, top-grade artemia/infusoria cultures, and specialized aquaculture medicines with video inspection.
                    </p>
                </div>
                <div>
                    <h5 class="text-sm font-bold uppercase tracking-wider text-cyan-400 mb-4">Quick Links</h5>
                    <ul class="space-y-2 text-sm text-slate-300">
                        <li><a href="#catalogSection" class="hover:text-cyan-400 transition">Live Fish Inventory</a></li>
                        <li><a href="#catalogSection" class="hover:text-cyan-400 transition">Feed & Cultures</a></li>
                        <li><a href="#catalogSection" class="hover:text-cyan-400 transition">Medicines & Care</a></li>
                        <li><button onclick="toggleAdminMode()" class="hover:text-cyan-400 transition text-left">Admin & Catalog Manager</button></li>
                    </ul>
                </div>
                <div>
                    <h5 class="text-sm font-bold uppercase tracking-wider text-cyan-400 mb-4">Farm Contact & Support</h5>
                    <ul class="space-y-2 text-sm text-slate-300">
                        <li class="flex items-center space-x-2"><i class="fa-solid fa-phone text-cyan-500 w-5"></i> <span>+91 98765 43210</span></li>
                        <li class="flex items-center space-x-2"><i class="fa-solid fa-envelope text-cyan-500 w-5"></i> <span>support@aquafishfarm.com</span></li>
                        <li class="flex items-center space-x-2"><i class="fa-solid fa-location-dot text-cyan-500 w-5"></i> <span>Aquarium Breeding Hub, India</span></li>
                    </ul>
                </div>
            </div>
            <div class="border-t border-slate-800 pt-6 text-center text-xs text-slate-500">
                &copy; <span id="footerYear">2026</span> <span id="footerBrandName">Aqua Fish Farm</span>. All rights reserved. Built with live video & reviews studio.
            </div>
        </div>
    </footer>

    <script>
        // Initial Farm Details State
        let farmSettings = JSON.parse(localStorage.getItem('aqua_farm_settings')) || {
            name: "Aqua Fish Farm",
            subtitle: "Direct Breeder & Supplier",
            heroHeading: "Healthy Fish. Vibrant Aquariums. Direct From Our Farm.",
            heroImage: "https://images.unsplash.com/photo-1522069169874-c58ec4b76be5?auto=format&fit=crop&w=800&q=80"
        };

        // Initial Products State with Video URLs & Reviews
        const defaultProducts = [
            {
                id: 1,
                name: "Red Cobra Guppy Pair",
                category: "Live Fish & Plants",
                price: 250,
                stock: "In Stock",
                image: "https://images.unsplash.com/photo-1534567153574-2b12153a87f0?auto=format&fit=crop&w=600&q=80",
                video: "https://www.youtube.com/embed/dQw4w9WgXcQ", // Demo embed
                desc: "Active, healthy young breeding pair with vibrant red cobra tail patterns.",
                reviews: [
                    { name: "Suresh Rao", rating: 5, comment: "Active swimmers and very vibrant red coloration!" },
                    { name: "Priya Menon", rating: 5, comment: "Healthy pair received safely in Bangalore." }
                ]
            },
            {
                id: 2,
                name: "Halfmoon Betta Male",
                category: "Live Fish & Plants",
                price: 350,
                stock: "In Stock",
                image: "https://images.unsplash.com/photo-1522069169874-c58ec4b76be5?auto=format&fit=crop&w=600&q=80",
                video: "",
                desc: "Stunning finnage and rich coloration. Conditioned on high-protein pellets.",
                reviews: [
                    { name: "Kiran Kumar", rating: 4, comment: "Gorgeous fins, flared right out of the box." }
                ]
            },
            {
                id: 3,
                name: "Artemia Cysts (Brine Shrimp Eggs)",
                category: "Feed & Cultures",
                price: 480,
                stock: "In Stock",
                image: "https://images.unsplash.com/photo-1544551763-46a013bb70d5?auto=format&fit=crop&w=600&q=80",
                video: "",
                desc: "High hatch rate (90%+) premium quality brine shrimp eggs for fry feeding.",
                reviews: [
                    { name: "Dr. Ramesh", rating: 5, comment: "Excellent hatch rate within 24 hours. Fry love it." }
                ]
            },
            {
                id: 4,
                name: "Live Infusoria Culture",
                category: "Feed & Cultures",
                price: 150,
                stock: "Low Stock",
                image: "https://images.unsplash.com/photo-1518709268805-4e9042af9f23?auto=format&fit=crop&w=600&q=80",
                video: "",
                desc: "Essential first food for newborn egg-scattering fry (Betta, Tetras).",
                reviews: []
            },
            {
                id: 5,
                name: "Anti-Ich & Fungus Liquid",
                category: "Dry Items & Medicine",
                price: 180,
                stock: "In Stock",
                image: "https://images.unsplash.com/photo-1584308666744-24d5c474f2ae?auto=format&fit=crop&w=600&q=80",
                video: "",
                desc: "Rapid relief treatment for white spots, fin rot, and velvet in freshwater tanks.",
                reviews: [
                    { name: "Amit Patel", rating: 5, comment: "Cured white spot within 3 days. Must-have medicine." }
                ]
            },
            {
                id: 6,
                name: "Amazon Sword Live Plant",
                category: "Live Fish & Plants",
                price: 120,
                stock: "In Stock",
                image: "https://images.unsplash.com/photo-1524704654690-b56c05c78a00?auto=format&fit=crop&w=600&q=80",
                video: "",
                desc: "Hardy background aquarium plant that absorbs nitrates and oxygenates water.",
                reviews: []
            }
        ];

        let products = JSON.parse(localStorage.getItem('aqua_products')) || defaultProducts;
        let cart = JSON.parse(localStorage.getItem('aqua_cart')) || [];
        let isAdminMode = false;
        let currentCategory = 'All';
        let searchQuery = '';
        let currentDetailProduct = null;
        let activeMediaTab = 'photo';

        // Helper function for logo / home reset
        function switchTab(tabName) {
            if (tabName === 'shop') {
                filterCategory('All');
                window.scrollTo({ top: 0, behavior: 'smooth' });
            }
        }

        // Initialize App on Load
        window.onload = function() {
            renderFarmSettings();
// ... existing code ... -->
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Shastha Guppy Farm</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Baloo+2:wght@500;600;700&family=Karla:wght@400;500;700&display=swap" rel="stylesheet">
<style>
  :root{
    --ink:#12324F;         /* deep navy text on white */
    --paper:#FFFFFF;       /* clean white page */
    --panel:#EEF5FF;       /* pale blue panels */
    --violet:#2E7BE0;      /* secondary blue */
    --magenta:#4A90E2;     /* light blue accent */
    --gold:#1E6FD9;        /* main blue accent */
    --teal:#0F4C9A;        /* deep blue, used sparingly */
    --line:#CFE0F5;        /* soft blue hairline */
    --radius:14px;
  }
  *{box-sizing:border-box;}
  html{scroll-behavior:smooth;}
  body{
    margin:0; background:var(--paper); color:var(--ink);
    font-family:'Karla',sans-serif; line-height:1.55;
    padding-bottom:env(safe-area-inset-bottom,0px);
  }
  h1,h2,h3,.brand,.tagline{font-family:'Baloo 2',sans-serif;}

  header{
    position:sticky; top:0; z-index:30; background:var(--paper);
    border-bottom:2px solid var(--line);
    padding:calc(env(safe-area-inset-top,0px) + 12px) 20px 12px;
    display:flex; align-items:center; justify-content:space-between; gap:12px;
  }
  .brand{display:flex; align-items:center; gap:10px; font-size:1.2rem; font-weight:700; color:var(--ink);}
  .brand .fin{
    width:40px;height:40px;border-radius:50%;
    object-fit:cover; flex-shrink:0; background:#000;
  }
  .cart-btn{
    background:var(--ink); color:var(--paper); border:none; border-radius:999px;
    padding:10px 18px; font-family:'Karla'; font-weight:700; font-size:.88rem;
    cursor:pointer; display:flex; align-items:center; gap:8px;
  }
  .cart-count{background:var(--gold); color:#fff; border-radius:999px; padding:1px 9px; font-size:.78rem; font-weight:700;}

  .hero{
    padding:52px 20px 40px; max-width:920px; margin:0 auto;
    display:flex; flex-direction:column; gap:14px;
  }
  .tagline{
    font-size:.85rem; letter-spacing:.02em; color:var(--teal); font-weight:600;
    text-transform:lowercase;
  }
  .hero h1{
    font-size:clamp(2.1rem,6vw,3.2rem); margin:0; font-weight:700; line-height:1.08;
    max-width:16ch;
  }
  .hero h1 .accent{color:var(--magenta);}
  .hero p{max-width:52ch; font-size:1.05rem; margin:2px 0 0; color:#3D5A80;}
  .tail-row{display:flex; gap:10px; margin-top:6px; font-size:1.6rem;}

  main{max-width:1000px; margin:0 auto; padding:0 20px 90px;}
  .tabs{display:flex; gap:10px; overflow-x:auto; padding:4px 0 26px;}
  .tab{
    border:2px solid var(--ink); background:transparent; color:var(--ink);
    padding:9px 18px; border-radius:999px; font-size:.9rem; font-weight:700;
    cursor:pointer; white-space:nowrap; font-family:'Karla';
  }
  .tab[aria-selected="true"]{background:var(--ink); color:var(--paper);}

  .grid{display:grid; grid-template-columns:repeat(auto-fill,minmax(220px,1fr)); gap:20px;}
  .card{
    background:var(--panel); border-radius:var(--radius); overflow:hidden;
    display:flex; flex-direction:column;
    box-shadow:0 1px 0 var(--line);
    border:1px solid var(--line);
  }
  .media{
    width:100%; aspect-ratio:4/3; background:linear-gradient(160deg,#E6F0FC,#D3E4F9);
    display:flex; align-items:center; justify-content:center; font-size:1.1rem; letter-spacing:.08em; color:#6E8FB8; font-weight:700;
    position:relative; overflow:hidden;
  }
  .media img, .media video{width:100%; height:100%; object-fit:cover;}
  .media .play-badge{
    position:absolute; bottom:8px; right:8px; background:rgba(27,16,53,.75); color:#fff;
    font-size:.7rem; padding:3px 8px; border-radius:999px; font-weight:700;
  }
  .card-body{padding:14px 14px 16px; display:flex; flex-direction:column; gap:6px; flex:1;}
  .card-body .cat{font-size:.72rem; font-weight:700; color:var(--violet); text-transform:lowercase;}
  .card-body h3{margin:0; font-size:1.05rem; font-weight:600; color:var(--ink);}
  .card-body .price{font-weight:700; margin-top:auto; font-size:1.05rem;}
  .qty-row{display:flex; align-items:center; gap:10px; margin-top:4px;}
  .qty-row button{
    width:30px; height:30px; border-radius:8px; border:2px solid var(--ink);
    background:var(--paper); color:var(--ink); font-size:1rem; cursor:pointer; font-weight:700;
  }
  .add-btn{
    background:var(--violet); color:#fff; border:none; border-radius:8px;
    padding:10px; font-weight:700; cursor:pointer; font-family:'Karla'; font-size:.92rem;
    margin-top:4px;
  }
  .add-btn:active{background:var(--magenta);}

  .overlay{position:fixed; inset:0; background:rgba(10,30,60,.4); z-index:40; display:none;}
  .overlay.open{display:block;}
  .drawer{
    position:fixed; top:0; right:0; bottom:0; width:min(400px,92vw);
    background:var(--panel); z-index:41; transform:translateX(105%);
    transition:transform .25s ease; display:flex; flex-direction:column;
    padding-top:env(safe-area-inset-top,0px); padding-bottom:env(safe-area-inset-bottom,0px);
  }
  .drawer.open{transform:translateX(0);}
  .drawer-head{padding:18px 20px; border-bottom:2px solid var(--line); display:flex; justify-content:space-between; align-items:center;}
  .drawer-head h2{margin:0; font-size:1.25rem;}
  .drawer-head button{background:none; border:none; font-size:1.3rem; cursor:pointer; color:var(--ink);}
  .drawer-items{flex:1; overflow-y:auto; padding:14px 20px;}
  .line{display:flex; justify-content:space-between; align-items:center; gap:8px; padding:12px 0; border-bottom:1px solid var(--line);}
  .line-name{font-size:.92rem; font-weight:600;}
  .line-qty{display:flex; align-items:center; gap:6px;}
  .line-qty button{width:26px;height:26px;border-radius:6px;border:2px solid var(--ink);background:var(--paper);cursor:pointer;font-weight:700;}
  .drawer-foot{padding:18px 20px; border-top:2px solid var(--line);}
  .total-row{display:flex; justify-content:space-between; font-weight:700; margin-bottom:14px; font-size:1.1rem;}
  .checkout-btn{
    width:100%; background:#25D366; color:#062A16; border:none; border-radius:10px;
    padding:14px; font-weight:700; font-size:1rem; cursor:pointer; font-family:'Karla';
    display:flex; align-items:center; justify-content:center; gap:8px;
  }
  .empty-note{color:var(--violet); opacity:.85; font-size:.92rem; padding:24px 0; text-align:center;}
  footer{text-align:center; padding:26px 20px 40px; font-size:.82rem; opacity:.6;}

  .add-btn[disabled]{background:#DDE6F1;color:#8095AF;cursor:not-allowed;}
  #adminPanel{position:fixed;inset:0;z-index:60;background:var(--paper);overflow-y:auto;padding:calc(env(safe-area-inset-top,0px) + 16px) 16px 60px;}
  #adminPanel[hidden]{display:none;}
  .ad-head{display:flex;justify-content:space-between;align-items:center;gap:8px;flex-wrap:wrap;}
  .ad-head h2{margin:0;}
  .ad-save,.ad-x,.ad-add{border:none;border-radius:8px;padding:10px 14px;font-weight:700;cursor:pointer;font-family:'Karla';}
  .ad-save{background:var(--gold);color:#fff;} .ad-x{background:var(--line);color:var(--ink);}
  .ad-add{background:var(--panel);color:var(--gold);border:2px dashed var(--gold);width:100%;margin-top:14px;}
  .ad-note{font-size:.85rem;opacity:.75;}
  .ad-wa{display:block;font-size:.85rem;margin:8px 0 14px;}
  .ad-wa input,.ad-row input,.ad-row select{background:var(--panel);color:var(--ink);border:1px solid var(--line);border-radius:6px;padding:8px;font-family:'Karla';font-size:.9rem;width:100%;}
  .ad-row{display:grid;grid-template-columns:2fr 1fr 1fr;gap:6px;background:var(--panel);border:1px solid var(--line);border-radius:10px;padding:10px;margin-bottom:8px;}
  .ad-row .full{grid-column:1/-1;display:flex;justify-content:space-between;align-items:center;font-size:.85rem;}
  .ad-row .del{background:none;border:none;color:#e0705a;font-weight:700;cursor:pointer;}

  /* ---------- product detail popup ---------- */
  .card{cursor:pointer;}
  .detail-overlay{
    position:fixed; inset:0; background:rgba(10,30,60,.55); z-index:60;
    display:flex; align-items:flex-end; justify-content:center;
    opacity:0; pointer-events:none; transition:opacity .28s ease;
  }
  .detail-overlay.open{opacity:1; pointer-events:auto;}
  @media (min-width:720px){ .detail-overlay{align-items:center;} }
  .detail-card{
    background:var(--panel); border:2px solid var(--line); border-radius:20px 20px 0 0;
    width:100%; max-width:560px; max-height:88vh; overflow-y:auto;
    padding:0 0 26px; position:relative;
    transform:translateY(28px) scale(.97); opacity:0;
    transition:transform .32s cubic-bezier(.2,.9,.25,1.1), opacity .28s ease;
  }
  .detail-overlay.open .detail-card{transform:translateY(0) scale(1); opacity:1;}
  @media (min-width:720px){ .detail-card{border-radius:20px;} }
  .detail-close{
    position:absolute; top:14px; right:14px; z-index:2;
    background:rgba(255,255,255,.92); color:var(--ink); border:1px solid var(--line);
    border-radius:999px; width:36px; height:36px; font-size:1.1rem; cursor:pointer;
  }
  .detail-media{width:100%; aspect-ratio:1/1; background:#000; overflow:hidden; border-radius:20px 20px 0 0;}
  .detail-media img, .detail-media video{width:100%; height:100%; object-fit:cover; display:block;
    animation:detailZoom .5s ease;}
  @keyframes detailZoom{from{transform:scale(1.08); opacity:.4;} to{transform:scale(1); opacity:1;}}
  .detail-media .media{height:100%; border-radius:0;}
  .detail-body{padding:20px 22px 4px;}
  .detail-body .cat{display:block; margin-bottom:4px;}
  .detail-body h2{margin:2px 0 8px; font-size:1.5rem;}
  .detail-body .price{font-size:1.2rem; font-weight:700; color:var(--gold); display:block; margin-bottom:16px;}
  .detail-actions{display:flex; gap:10px;}

  .brand{cursor:pointer;}
  .social{display:flex;justify-content:center;gap:14px;margin:26px 0 0;}
  .social a{width:44px;height:44px;border:1.5px solid var(--line);border-radius:999px;display:grid;place-items:center;color:var(--gold);transition:transform .2s,background .2s;}
  .social a:hover{transform:translateY(-2px);background:rgba(30,111,217,.10);}
  .social svg{width:22px;height:22px;fill:none;stroke:currentColor;stroke-width:1.8;stroke-linecap:round;stroke-linejoin:round;}
  .about-body{padding:26px 22px 8px;text-align:center;}
  .about-body img{width:84px;height:84px;border-radius:50%;object-fit:cover;margin-bottom:6px;}
  .about-text{white-space:pre-line;line-height:1.6;margin:8px 0 6px;}
  .about-body .social{margin:16px 0 0;}
  .ad-f{display:block;margin:12px 0;font-size:.85rem;}
  .ad-f input,.ad-f textarea{display:block;width:100%;margin-top:4px;padding:10px;border-radius:10px;border:1px solid var(--line);background:var(--paper);color:var(--ink);font:inherit;box-sizing:border-box;}
</style>
</head>
<body>

<header>
  <div class="brand"><img class="fin" src="data:image/jpeg;base64,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" alt="Shastha Guppy Farm logo">Shastha Guppy Farm</div>
  <button class="cart-btn" id="editBtn" hidden style="background:var(--gold);color:#fff;margin-left:auto">Edit shop</button>
  <button class="cart-btn" id="cartOpenBtn">Order <span class="cart-count" id="cartCount">0</span></button>
</header>

<div class="hero">
  <div class="tagline">fifty plus guppy varieties, bred and raised here</div>
  <h1>Colour that <span class="accent">swims</span></h1>
  <p>Live guppies in every colour and tail shape we raise, plus the food that keeps them thriving. Pick your favourites and send the order straight to us on WhatsApp.</p>
</div>

<main>
  <div class="tabs" id="tabs"></div>
  <div class="grid" id="grid"></div>
</main>

<div class="social" id="socialBar"></div>
<footer>Shastha Guppy Farm &mdash; orders confirmed over WhatsApp.</footer>


<section id="adminPanel" hidden>
  <div class="ad-head"><h2>Edit shop</h2><div><button id="adSave" class="ad-save">Save changes</button> <button id="adClose" class="ad-x">Close</button></div></div>
  <p class="ad-note">Only you see this screen. Changes go live for all customers after you press Save.</p>
  <label class="ad-wa">WhatsApp number (country code first, no + or spaces)<input id="adWa" inputmode="numeric"></label>
  <label class="ad-f">Instagram page link<input id="adIg" placeholder="https://instagram.com/yourpage"></label>
  <label class="ad-f">Facebook page link<input id="adFb" placeholder="https://facebook.com/yourpage"></label>
  <label class="ad-f">YouTube channel link<input id="adYt" placeholder="https://youtube.com/@yourchannel"></label>
  <label class="ad-f">About Shastha Guppy Farm (shown when customers tap the name)<textarea id="adAbout" rows="6"></textarea></label>
  <div id="adminList"></div>
  <button id="adAdd" class="ad-add">+ Add new item</button>
</section>
<div class="overlay" id="overlay"></div>
<aside class="drawer" id="drawer">
  <div class="drawer-head"><h2>Your order</h2><button id="drawerClose" aria-label="Close">X</button></div>
  <div class="drawer-items" id="drawerItems"></div>
  <div class="drawer-foot">
    <div class="total-row"><span>Total</span><span id="totalAmt">Rs. 0</span></div>
    <button class="checkout-btn" id="checkoutBtn">Send order on WhatsApp</button>
  </div>
</aside>

<div class="detail-overlay" id="detailOverlay">
  <div class="detail-card" id="detailCard">
    <button class="detail-close" id="detailClose" aria-label="Close">X</button>
    <div class="detail-media" id="detailMedia"></div>
    <div class="detail-body">
      <span class="cat" id="detailCat"></span>
      <h2 id="detailName"></h2>
      <span class="price" id="detailPrice"></span>
      <div class="detail-actions" id="detailActions"></div>
    </div>
  </div>
</div>

<div class="detail-overlay" id="aboutOverlay">
  <div class="detail-card">
    <button class="detail-close" id="aboutClose" aria-label="Close">X</button>
    <div class="about-body">
      <img id="aboutLogo" alt="Shastha Guppy Farm">
      <h2>Shastha Guppy Farm</h2>
      <p class="about-text" id="aboutText"></p>
      <div class="social" id="aboutSocial"></div>
    </div>
  </div>
</div>

<script type="application/json" id="state">{"whatsapp": "918088820799", "products": [{"id": "g1", "name": "Albino Platinum White Guppy (pair)", "cat": "Guppies", "price": 300, "inStock": true}, {"id": "g2", "name": "Albino Redlace Guppy (pair)", "cat": "Guppies", "price": 250, "inStock": true}, {"id": "g3", "name": "Albino Silvarado Red Ear Guppy (pair)", "cat": "Guppies", "price": 240, "inStock": true}, {"id": "g4", "name": "AFR Guppy (pair)", "cat": "Guppies", "price": 230, "inStock": true}, {"id": "g5", "name": "Masco Blue Guppy (pair)", "cat": "Guppies", "price": 220, "inStock": true}, {"id": "g6", "name": "Black Guppy (pair)", "cat": "Guppies", "price": 180, "inStock": true}, {"id": "g7", "name": "Platinum White Dumbo Guppy (pair)", "cat": "Guppies", "price": 450, "inStock": true}, {"id": "g8", "name": "Silvarado Mosaic Guppy (pair)", "cat": "Guppies", "price": 180, "inStock": true}, {"id": "g9", "name": "White Texido Guppy (pair)", "cat": "Guppies", "price": 180, "inStock": true}, {"id": "g10", "name": "Japanese Blue Guppy (pair)", "cat": "Guppies", "price": 250, "inStock": true}, {"id": "g11", "name": "Platinum Big Ear Guppy (pair)", "cat": "Guppies", "price": 250, "inStock": true}, {"id": "g12", "name": "Chilli Mosaic Dumbo Guppy (pair)", "cat": "Guppies", "price": 205, "inStock": true}, {"id": "g13", "name": "Gold Guppy (pair)", "cat": "Guppies", "price": 250, "inStock": true}, {"id": "g14", "name": "Gold Ribbon Guppy (pair)", "cat": "Guppies", "price": 500, "inStock": true}, {"id": "g15", "name": "Red Granite Guppy (pair)", "cat": "Guppies", "price": 215, "inStock": true}, {"id": "g16", "name": "Blue Panda Guppy (pair)", "cat": "Guppies", "price": 230, "inStock": true}, {"id": "g17", "name": "Purple Burry Guppy (pair)", "cat": "Guppies", "price": 250, "inStock": true}, {"id": "g18", "name": "Tiger HM Guppy (pair)", "cat": "Guppies", "price": 180, "inStock": true}, {"id": "g19", "name": "Yellow Pingu Guppy (pair)", "cat": "Guppies", "price": 215, "inStock": true}, {"id": "g20", "name": "Lazuli Blue Guppy (pair)", "cat": "Guppies", "price": 190, "inStock": true}, {"id": "g21", "name": "Black Bar Endler Guppy (pair)", "cat": "Guppies", "price": 200, "inStock": true}, {"id": "g22", "name": "Red Scarlet Endler Guppy (pair)", "cat": "Guppies", "price": 200, "inStock": true}, {"id": "g23", "name": "Ivory Purple Guppy (pair)", "cat": "Guppies", "price": 250, "inStock": true}, {"id": "g24", "name": "Red Coral Endler Guppy (pair)", "cat": "Guppies", "price": 250, "inStock": true}, {"id": "g25", "name": "Zee Through Koi Guppy (pair)", "cat": "Guppies", "price": 250, "inStock": true}, {"id": "g26", "name": "Santha Clause SB Guppy (pair)", "cat": "Guppies", "price": 400, "inStock": true}, {"id": "g27", "name": "Wildred Guppy (pair)", "cat": "Guppies", "price": 210, "inStock": true}, {"id": "g28", "name": "Albino Metal Redlace Guppy (pair)", "cat": "Guppies", "price": 230, "inStock": true}, {"id": "g29", "name": "Red Dragon HM Guppy (pair)", "cat": "Guppies", "price": 250, "inStock": true}, {"id": "f1", "name": "Guppy Flake Food 100g", "cat": "Food", "price": 120, "inStock": true}, {"id": "f2", "name": "Live Daphnia Culture", "cat": "Food", "price": 80, "inStock": true}, {"id": "f3", "name": "Baby Guppy Fry Food", "cat": "Food", "price": 100, "inStock": true}]}</script>
<script>
let state = JSON.parse(document.getElementById('state').textContent);
let PRODUCTS = state.products;
const CATS = ['All','Guppies','Food'];
let cart = {}, activeCat = 'All';
const $ = id => document.getElementById(id);
const money = n => '\u20b9' + Number(n).toLocaleString('en-IN');
const esc = s => String(s).replace(/[&<>"']/g, c => ({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'}[c]));
const find = id => PRODUCTS.find(p => p.id === id);

function renderTabs(){
  $('tabs').innerHTML = '';
  CATS.forEach(c => {
    const b = document.createElement('button');
    b.className = 'tab'; b.textContent = c;
    b.setAttribute('aria-selected', c === activeCat ? 'true' : 'false');
    b.onclick = () => { activeCat = c; renderTabs(); renderGrid(); };
    $('tabs').appendChild(b);
  });
}
function mediaHtml(p){
  if(p.video) return '<div class="media"><video src="'+p.video+'" '+(p.photo?'poster="'+p.photo+'" ':'')+'controls preload="none" playsinline></video></div>';
  if(p.photo) return '<div class="media"><img src="'+p.photo+'" alt="'+esc(p.name)+'" loading="lazy"></div>';
  return '<div class="media">'+(p.cat==='Guppies'?'GUPPY':'FOOD')+'</div>';
}
function renderGrid(){
  const grid = $('grid'); grid.innerHTML = '';
  PRODUCTS.filter(p => activeCat === 'All' || p.cat === activeCat).forEach(p => {
    const q = cart[p.id] || 0;
    const action = !p.inStock ? '<button class="add-btn" disabled>Sold out</button>'
      : q === 0 ? '<button class="add-btn" data-add="'+p.id+'">Add to order</button>'
      : '<div class="qty-row"><button data-dec="'+p.id+'">-</button><span>'+q+'</span><button data-inc="'+p.id+'">+</button></div>';
    const card = document.createElement('div'); card.className = 'card';
    card.innerHTML = mediaHtml(p)+'<div class="card-body"><span class="cat">'+esc(p.cat)+'</span><h3>'+esc(p.name)+'</h3><span class="price">'+money(p.price)+'</span>'+action+'</div>';
    card.addEventListener('click', (ev) => { if(ev.target.closest('button')) return; openDetail(p.id); });
    grid.appendChild(card);
  });
  bind(grid);
}

function openDetail(id){
  const p = find(id); if(!p) return;
  $('detailMedia').innerHTML = mediaHtml(p);
  const vid = $('detailMedia').querySelector('video');
  if(vid){ vid.muted = true; vid.autoplay = true; vid.loop = true; vid.play().catch(()=>{}); }
  $('detailCat').textContent = p.cat;
  $('detailName').textContent = p.name;
  $('detailPrice').textContent = money(p.price);
  const q = cart[p.id] || 0;
  $('detailActions').innerHTML = !p.inStock ? '<button class="add-btn" disabled>Sold out</button>'
    : q === 0 ? '<button class="add-btn" data-add="'+p.id+'">Add to order</button>'
    : '<div class="qty-row"><button data-dec="'+p.id+'">-</button><span>'+q+'</span><button data-inc="'+p.id+'">+</button></div>';
  bind($('detailActions'));
  $('detailOverlay').classList.add('open');
}
function closeDetail(){ $('detailOverlay').classList.remove('open'); }
$('detailClose').onclick = closeDetail;
$('detailOverlay').onclick = (ev) => { if(ev.target === $('detailOverlay')) closeDetail(); };
function bind(root){
  root.querySelectorAll('[data-add]').forEach(b => b.onclick = () => { cart[b.dataset.add] = 1; renderAll(); });
  root.querySelectorAll('[data-inc]').forEach(b => b.onclick = () => { cart[b.dataset.inc]++; renderAll(); });
  root.querySelectorAll('[data-dec]').forEach(b => b.onclick = () => { const id = b.dataset.dec; if(--cart[id] <= 0) delete cart[id]; renderAll(); });
}
const cartTotal = () => Object.entries(cart).reduce((s,[id,q]) => s + (find(id)?.price||0)*q, 0);
const cartCount = () => Object.values(cart).reduce((a,b) => a+b, 0);
function renderDrawer(){
  $('cartCount').textContent = cartCount();
  const w = $('drawerItems'), e = Object.entries(cart).filter(([id]) => find(id));
  w.innerHTML = e.length ? e.map(([id,q]) => { const p = find(id);
    return '<div class="line"><div><div class="line-name">'+esc(p.name)+'</div><div style="font-size:.82rem;opacity:.65">'+money(p.price)+' x '+q+'</div></div><div class="line-qty"><button data-dec="'+id+'">-</button><span>'+q+'</span><button data-inc="'+id+'">+</button></div></div>'; }).join('')
    : '<p class="empty-note">Your order is empty.<br>Add guppies or food from the catalog.</p>';
  bind(w);
  $('totalAmt').textContent = money(cartTotal());
}
function renderAll(){ renderGrid(); renderDrawer(); refreshDetailActions(); }
function refreshDetailActions(){
  if(!$('detailOverlay').classList.contains('open')) return;
  const id = $('detailActions').querySelector('[data-add],[data-inc],[data-dec]');
  if(!id) return;
  const pid = id.dataset.add || id.dataset.inc || id.dataset.dec;
  const p = find(pid); if(!p) return;
  const q = cart[p.id] || 0;
  $('detailActions').innerHTML = !p.inStock ? '<button class="add-btn" disabled>Sold out</button>'
    : q === 0 ? '<button class="add-btn" data-add="'+p.id+'">Add to order</button>'
    : '<div class="qty-row"><button data-dec="'+p.id+'">-</button><span>'+q+'</span><button data-inc="'+p.id+'">+</button></div>';
  bind($('detailActions'));
}
const setDrawer = on => { $('overlay').classList.toggle('open', on); $('drawer').classList.toggle('open', on); };
$('cartOpenBtn').onclick = () => setDrawer(true);
$('drawerClose').onclick = $('overlay').onclick = () => setDrawer(false);

$('checkoutBtn').onclick = () => {
  const e = Object.entries(cart).filter(([id]) => find(id));
  if(!e.length){ alert('Add at least one item to your order first.'); return; }
  let msg = "Hello Shastha Guppy Farm, I'd like to order:\n\n";
  e.forEach(([id,q]) => { const p = find(id); msg += '- '+p.name+' x'+q+' = '+money(p.price*q)+'\n'; });
  msg += '\nTotal: '+money(cartTotal())+'\n\nPlease confirm availability and delivery.';
  window.open('https://wa.me/'+state.whatsapp+'?text='+encodeURIComponent(msg), '_blank');
};

/* ---------- owner-only edit mode ---------- */
let draft;
function buildDoc(s){
  const c = document.documentElement.cloneNode(true);
  ['grid','tabs','drawerItems','adminList','detailMedia','detailActions','socialBar','aboutSocial'].forEach(id => { const e = c.querySelector('#'+id); if(e) e.innerHTML = ''; });
  c.querySelector('#state').textContent = JSON.stringify(s).replace(/</g,'\\u003c');
  c.querySelectorAll('.open').forEach(e => e.classList.remove('open'));
  c.querySelector('#editBtn').setAttribute('hidden','');
  c.querySelector('#aboutText').textContent = '';
  c.querySelector('#aboutLogo').removeAttribute('src');
  c.querySelector('#adminPanel').setAttribute('hidden','');
  c.querySelector('#cartCount').textContent = '0';
  c.querySelector('#totalAmt').textContent = money(0);
  return '<!DOCTYPE html>\n' + c.outerHTML;
}
function readData(f){ return new Promise((res,rej)=>{ const r=new FileReader(); r.onload=()=>res(r.result); r.onerror=rej; r.readAsDataURL(f); }); }
async function shrink(f){
  const img = new Image(); img.src = await readData(f); await img.decode();
  const s = Math.min(1, 640/img.width), c = document.createElement('canvas');
  c.width = Math.round(img.width*s); c.height = Math.round(img.height*s);
  c.getContext('2d').drawImage(img,0,0,c.width,c.height);
  return c.toDataURL('image/jpeg',0.72);
}
function renderAdmin(){
  $('adminList').innerHTML = draft.products.map((p,i) =>
    '<div class="ad-row"><input data-f="name" data-i="'+i+'" value="'+esc(p.name)+'"><input data-f="price" data-i="'+i+'" inputmode="numeric" value="'+p.price+'"><select data-f="cat" data-i="'+i+'"><option'+(p.cat==='Guppies'?' selected':'')+'>Guppies</option><option'+(p.cat==='Food'?' selected':'')+'>Food</option></select>'
    +'<div class="full"><span>Photo: '+(p.photo?'added <button class="del" data-rmp="'+i+'">remove</button>':'<input type="file" accept="image/*" data-photo="'+i+'" style="width:auto">')+'</span></div>'
    +'<div class="full"><span>Video: '+(p.video?'added <button class="del" data-rmv="'+i+'">remove</button>':'<input type="file" accept="video/*" data-video="'+i+'" style="width:auto">')+'</span></div>'
    +'<div class="full"><label><input type="checkbox" style="width:auto" data-f="inStock" data-i="'+i+'"'+(p.inStock?' checked':'')+'> In stock</label><button class="del" data-del="'+i+'">Delete</button></div></div>').join('');
  const L = $('adminList');
  L.querySelectorAll('[data-f]').forEach(el => el.onchange = () => {
    const p = draft.products[el.dataset.i], f = el.dataset.f;
    p[f] = f==='inStock' ? el.checked : f==='price' ? (Number(el.value)||0) : el.value.trim();
  });
  L.querySelectorAll('[data-photo]').forEach(el => el.onchange = async () => { const f = el.files[0]; if(!f) return; draft.products[el.dataset.photo].photo = await shrink(f); renderAdmin(); });
  L.querySelectorAll('[data-video]').forEach(el => el.onchange = async () => {
    const f = el.files[0]; if(!f) return;
    if(f.size > 2*1048576){ alert('This video is '+(f.size/1048576).toFixed(1)+' MB. Please compress it under 2 MB first.'); el.value=''; return; }
    draft.products[el.dataset.video].video = await readData(f); renderAdmin();
  });
  L.querySelectorAll('[data-rmp]').forEach(b => b.onclick = () => { delete draft.products[b.dataset.rmp].photo; renderAdmin(); });
  L.querySelectorAll('[data-rmv]').forEach(b => b.onclick = () => { delete draft.products[b.dataset.rmv].video; renderAdmin(); });
  L.querySelectorAll('[data-del]').forEach(b => b.onclick = () => { if(confirm('Delete this item?')){ draft.products.splice(b.dataset.del,1); renderAdmin(); } });
}
const DEFAULT_ABOUT = 'Shastha Guppy Farm breeds and raises fifty plus varieties of guppies, along with the food that keeps them healthy.\n\nPick your favourites, send the order on WhatsApp, and we will confirm it with you directly.';
const ICONS = {
  whatsapp:'<svg viewBox="0 0 24 24"><path d="M3 21l1.6-4.6A9 9 0 1 1 8 19.6L3 21z"/><path d="M9 8.5c0 3 2.5 5.5 5.5 5.5l1-1.5-2-1-1 .8c-.8-.4-1.5-1.1-1.9-1.9l.8-1-1-2L9 8.5z" style="fill:currentColor;stroke:none"/></svg>',
  instagram:'<svg viewBox="0 0 24 24"><rect x="3" y="3" width="18" height="18" rx="5"/><circle cx="12" cy="12" r="4"/><circle cx="17.5" cy="6.5" r="1" style="fill:currentColor"/></svg>',
  facebook:'<svg viewBox="0 0 24 24"><path d="M14 8h3V4h-3a4 4 0 0 0-4 4v3H7v4h3v6h4v-6h3l1-4h-4V8z"/></svg>',
  youtube:'<svg viewBox="0 0 24 24"><rect x="2" y="5" width="20" height="14" rx="4"/><path d="M10 9l5 3-5 3z" style="fill:currentColor"/></svg>'
};
const normUrl = u => { u = String(u||'').trim(); return !u ? '' : (/^https?:\/\//i.test(u) ? u : 'https://' + u); };
function renderSocial(){
  const s = state.social || {};
  const items = [['whatsapp','https://wa.me/'+state.whatsapp,'WhatsApp'],['instagram',s.instagram,'Instagram'],['facebook',s.facebook,'Facebook'],['youtube',s.youtube,'YouTube']];
  const h = items.filter(x => x[1]).map(x => '<a href="'+esc(x[1])+'" target="_blank" rel="noopener" aria-label="'+x[2]+'">'+ICONS[x[0]]+'</a>').join('');
  $('socialBar').innerHTML = h; $('aboutSocial').innerHTML = h;
  $('aboutText').textContent = state.about || DEFAULT_ABOUT;
}
$('aboutClose').onclick = () => $('aboutOverlay').classList.remove('open');
$('aboutOverlay').onclick = ev => { if(ev.target === $('aboutOverlay')) $('aboutOverlay').classList.remove('open'); };
document.querySelector('.brand').onclick = () => { $('aboutLogo').src = document.querySelector('.brand img').src; $('aboutOverlay').classList.add('open'); };
const isOwnerLink = () => location.hash === '#owner';
window.addEventListener('hashchange', () => { $('editBtn').hidden = !isOwnerLink(); });

const OWNER_PASSWORD = 'shastha2026'; // change this to any password you like

function initAdmin(){
  $('editBtn').hidden = !isOwnerLink();
  $('editBtn').onclick = () => {
    if(!sessionStorage.getItem('ownerOk')){
      const pw = prompt('Enter shop owner password:');
      if(pw !== OWNER_PASSWORD){ if(pw !== null) alert('Wrong password.'); return; }
      sessionStorage.setItem('ownerOk','1');
    }
    draft = JSON.parse(JSON.stringify(state)); $('adWa').value = draft.whatsapp; const sc = draft.social || {}; $('adIg').value = sc.instagram || ''; $('adFb').value = sc.facebook || ''; $('adYt').value = sc.youtube || ''; $('adAbout').value = draft.about || DEFAULT_ABOUT; renderAdmin(); $('adminPanel').hidden = false;
  };
  $('adClose').onclick = () => { $('adminPanel').hidden = true; };
  $('adAdd').onclick = () => { draft.products.unshift({id:'n'+Date.now(), name:'New guppy (pair)', cat:'Guppies', price:0, inStock:true}); renderAdmin(); };
  $('adSave').onclick = () => {
    draft.whatsapp = $('adWa').value.replace(/\D/g,'') || draft.whatsapp;
    draft.social = {instagram: normUrl($('adIg').value), facebook: normUrl($('adFb').value), youtube: normUrl($('adYt').value)};
    draft.about = $('adAbout').value.trim();
    if(JSON.stringify(draft).length > 12e6){ alert('Too much photo/video data for one page (limit about 12 MB). Remove a few videos.'); return; }
    state = draft; PRODUCTS = state.products;
    const blob = new Blob([buildDoc(state)], {type:'text/html'});
    const url = URL.createObjectURL(blob);
    const a = document.createElement('a');
    a.href = url; a.download = 'index.html';
    document.body.appendChild(a); a.click(); a.remove();
    URL.revokeObjectURL(url);
    $('adminPanel').hidden = true;
    renderTabs(); renderAll(); renderSocial();
    alert('Saved! A file was downloaded. On GitHub, upload it, delete the old index.html, and rename the new file to index.html. The live site then updates in a minute or two.');
  };
}
initAdmin();


renderTabs(); renderAll(); renderSocial();
</script>
</body>
</html>
>
<html lang="en"><!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Shastha Guppy Farm</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Baloo+2:wght@500;600;700&family=Karla:wght@400;500;700&display=swap" rel="stylesheet">
<style>
  :root{
    --ink:#12324F;         /* deep navy text on white */
    --paper:#FFFFFF;       /* clean white page */
    --panel:#EEF5FF;       /* pale blue panels */
    --violet:#2E7BE0;      /* secondary blue */
    --magenta:#4A90E2;     /* light blue accent */
    --gold:#1E6FD9;        /* main blue accent */
    --teal:#0F4C9A;        /* deep blue, used sparingly */
    --line:#CFE0F5;        /* soft blue hairline */
    --radius:14px;
  }
  *{box-sizing:border-box;}
  html{scroll-behavior:smooth;}
  body{
    margin:0; background:var(--paper); color:var(--ink);
    font-family:'Karla',sans-serif; line-height:1.55;
    padding-bottom:env(safe-area-inset-bottom,0px);
  }
  h1,h2,h3,.brand,.tagline{font-family:'Baloo 2',sans-serif;}

  header{
    position:sticky; top:0; z-index:30; background:var(--paper);
    border-bottom:2px solid var(--line);
    padding:calc(env(safe-area-inset-top,0px) + 12px) 20px 12px;
    display:flex; align-items:center; justify-content:space-between; gap:12px;
  }
  .brand{display:flex; align-items:center; gap:10px; font-size:1.2rem; font-weight:700; color:var(--ink);}
  .brand .fin{
    width:40px;height:40px;border-radius:50%;
    object-fit:cover; flex-shrink:0; background:#000;
  }
  .cart-btn{
    background:var(--ink); color:var(--paper); border:none; border-radius:999px;
    padding:10px 18px; font-family:'Karla'; font-weight:700; font-size:.88rem;
    cursor:pointer; display:flex; align-items:center; gap:8px;
  }
  .cart-count{background:var(--gold); color:#fff; border-radius:999px; padding:1px 9px; font-size:.78rem; font-weight:700;}

  .hero{
    padding:52px 20px 40px; max-width:920px; margin:0 auto;
    display:flex; flex-direction:column; gap:14px;
  }
  .tagline{
    font-size:.85rem; letter-spacing:.02em; color:var(--teal); font-weight:600;
    text-transform:lowercase;
  }
  .hero h1{
    font-size:clamp(2.1rem,6vw,3.2rem); margin:0; font-weight:700; line-height:1.08;
    max-width:16ch;
  }
  .hero h1 .accent{color:var(--magenta);}
  .hero p{max-width:52ch; font-size:1.05rem; margin:2px 0 0; color:#3D5A80;}
  .tail-row{display:flex; gap:10px; margin-top:6px; font-size:1.6rem;}

  main{max-width:1000px; margin:0 auto; padding:0 20px 90px;}
  .tabs{display:flex; gap:10px; overflow-x:auto; padding:4px 0 26px;}
  .tab{
    border:2px solid var(--ink); background:transparent; color:var(--ink);
    padding:9px 18px; border-radius:999px; font-size:.9rem; font-weight:700;
    cursor:pointer; white-space:nowrap; font-family:'Karla';
  }
  .tab[aria-selected="true"]{background:var(--ink); color:var(--paper);}

  .grid{display:grid; grid-template-columns:repeat(auto-fill,minmax(220px,1fr)); gap:20px;}
  .card{
    background:var(--panel); border-radius:var(--radius); overflow:hidden;
    display:flex; flex-direction:column;
    box-shadow:0 1px 0 var(--line);
    border:1px solid var(--line);
  }
  .media{
    width:100%; aspect-ratio:4/3; background:linear-gradient(160deg,#E6F0FC,#D3E4F9);
    display:flex; align-items:center; justify-content:center; font-size:1.1rem; letter-spacing:.08em; color:#6E8FB8; font-weight:700;
    position:relative; overflow:hidden;
  }
  .media img, .media video{width:100%; height:100%; object-fit:cover;}
  .media .play-badge{
    position:absolute; bottom:8px; right:8px; background:rgba(27,16,53,.75); color:#fff;
    font-size:.7rem; padding:3px 8px; border-radius:999px; font-weight:700;
  }
  .card-body{padding:14px 14px 16px; display:flex; flex-direction:column; gap:6px; flex:1;}
  .card-body .cat{font-size:.72rem; font-weight:700; color:var(--violet); text-transform:lowercase;}
  .card-body h3{margin:0; font-size:1.05rem; font-weight:600; color:var(--ink);}
  .card-body .price{font-weight:700; margin-top:auto; font-size:1.05rem;}
  .qty-row{display:flex; align-items:center; gap:10px; margin-top:4px;}
  .qty-row button{
    width:30px; height:30px; border-radius:8px; border:2px solid var(--ink);
    background:var(--paper); color:var(--ink); font-size:1rem; cursor:pointer; font-weight:700;
  }
  .add-btn{
    background:var(--violet); color:#fff; border:none; border-radius:8px;
    padding:10px; font-weight:700; cursor:pointer; font-family:'Karla'; font-size:.92rem;
    margin-top:4px;
  }
  .add-btn:active{background:var(--magenta);}

  .overlay{position:fixed; inset:0; background:rgba(10,30,60,.4); z-index:40; display:none;}
  .overlay.open{display:block;}
  .drawer{
    position:fixed; top:0; right:0; bottom:0; width:min(400px,92vw);
    background:var(--panel); z-index:41; transform:translateX(105%);
    transition:transform .25s ease; display:flex; flex-direction:column;
    padding-top:env(safe-area-inset-top,0px); padding-bottom:env(safe-area-inset-bottom,0px);
  }
  .drawer.open{transform:translateX(0);}
  .drawer-head{padding:18px 20px; border-bottom:2px solid var(--line); display:flex; justify-content:space-between; align-items:center;}
  .drawer-head h2{margin:0; font-size:1.25rem;}
  .drawer-head button{background:none; border:none; font-size:1.3rem; cursor:pointer; color:var(--ink);}
  .drawer-items{flex:1; overflow-y:auto; padding:14px 20px;}
  .line{display:flex; justify-content:space-between; align-items:center; gap:8px; padding:12px 0; border-bottom:1px solid var(--line);}
  .line-name{font-size:.92rem; font-weight:600;}
  .line-qty{display:flex; align-items:center; gap:6px;}
  .line-qty button{width:26px;height:26px;border-radius:6px;border:2px solid var(--ink);background:var(--paper);cursor:pointer;font-weight:700;}
  .drawer-foot{padding:18px 20px; border-top:2px solid var(--line);}
  .total-row{display:flex; justify-content:space-between; font-weight:700; margin-bottom:14px; font-size:1.1rem;}
  .checkout-btn{
    width:100%; background:#25D366; color:#062A16; border:none; border-radius:10px;
    padding:14px; font-weight:700; font-size:1rem; cursor:pointer; font-family:'Karla';
    display:flex; align-items:center; justify-content:center; gap:8px;
  }
  .empty-note{color:var(--violet); opacity:.85; font-size:.92rem; padding:24px 0; text-align:center;}
  footer{text-align:center; padding:26px 20px 40px; font-size:.82rem; opacity:.6;}

  .add-btn[disabled]{background:#DDE6F1;color:#8095AF;cursor:not-allowed;}
  #adminPanel{position:fixed;inset:0;z-index:60;background:var(--paper);overflow-y:auto;padding:calc(env(safe-area-inset-top,0px) + 16px) 16px 60px;}
  #adminPanel[hidden]{display:none;}
  .ad-head{display:flex;justify-content:space-between;align-items:center;gap:8px;flex-wrap:wrap;}
  .ad-head h2{margin:0;}
  .ad-save,.ad-x,.ad-add{border:none;border-radius:8px;padding:10px 14px;font-weight:700;cursor:pointer;font-family:'Karla';}
  .ad-save{background:var(--gold);color:#fff;} .ad-x{background:var(--line);color:var(--ink);}
  .ad-add{background:var(--panel);color:var(--gold);border:2px dashed var(--gold);width:100%;margin-top:14px;}
  .ad-note{font-size:.85rem;opacity:.75;}
  .ad-wa{display:block;font-size:.85rem;margin:8px 0 14px;}
  .ad-wa input,.ad-row input,.ad-row select{background:var(--panel);color:var(--ink);border:1px solid var(--line);border-radius:6px;padding:8px;font-family:'Karla';font-size:.9rem;width:100%;}
  .ad-row{display:grid;grid-template-columns:2fr 1fr 1fr;gap:6px;background:var(--panel);border:1px solid var(--line);border-radius:10px;padding:10px;margin-bottom:8px;}
  .ad-row .full{grid-column:1/-1;display:flex;justify-content:space-between;align-items:center;font-size:.85rem;}
  .ad-row .del{background:none;border:none;color:#e0705a;font-weight:700;cursor:pointer;}

  /* ---------- product detail popup ---------- */
  .card{cursor:pointer;}
  .detail-overlay{
    position:fixed; inset:0; background:rgba(10,30,60,.55); z-index:60;
    display:flex; align-items:flex-end; justify-content:center;
    opacity:0; pointer-events:none; transition:opacity .28s ease;
  }
  .detail-overlay.open{opacity:1; pointer-events:auto;}
  @media (min-width:720px){ .detail-overlay{align-items:center;} }
  .detail-card{
    background:var(--panel); border:2px solid var(--line); border-radius:20px 20px 0 0;
    width:100%; max-width:560px; max-height:88vh; overflow-y:auto;
    padding:0 0 26px; position:relative;
    transform:translateY(28px) scale(.97); opacity:0;
    transition:transform .32s cubic-bezier(.2,.9,.25,1.1), opacity .28s ease;
  }
  .detail-overlay.open .detail-card{transform:translateY(0) scale(1); opacity:1;}
  @media (min-width:720px){ .detail-card{border-radius:20px;} }
  .detail-close{
    position:absolute; top:14px; right:14px; z-index:2;
    background:rgba(255,255,255,.92); color:var(--ink); border:1px solid var(--line);
    border-radius:999px; width:36px; height:36px; font-size:1.1rem; cursor:pointer;
  }
  .detail-media{width:100%; aspect-ratio:1/1; background:#000; overflow:hidden; border-radius:20px 20px 0 0;}
  .detail-media img, .detail-media video{width:100%; height:100%; object-fit:cover; display:block;
    animation:detailZoom .5s ease;}
  @keyframes detailZoom{from{transform:scale(1.08); opacity:.4;} to{transform:scale(1); opacity:1;}}
  .detail-media .media{height:100%; border-radius:0;}
  .detail-body{padding:20px 22px 4px;}
  .detail-body .cat{display:block; margin-bottom:4px;}
  .detail-body h2{margin:2px 0 8px; font-size:1.5rem;}
  .detail-body .price{font-size:1.2rem; font-weight:700; color:var(--gold); display:block; margin-bottom:16px;}
  .detail-actions{display:flex; gap:10px;}

  .brand{cursor:pointer;}
  .social{display:flex;justify-content:center;gap:14px;margin:26px 0 0;}
  .social a{width:44px;height:44px;border:1.5px solid var(--line);border-radius:999px;display:grid;place-items:center;color:var(--gold);transition:transform .2s,background .2s;}
  .social a:hover{transform:translateY(-2px);background:rgba(30,111,217,.10);}
  .social svg{width:22px;height:22px;fill:none;stroke:currentColor;stroke-width:1.8;stroke-linecap:round;stroke-linejoin:round;}
  .about-body{padding:26px 22px 8px;text-align:center;}
  .about-body img{width:84px;height:84px;border-radius:50%;object-fit:cover;margin-bottom:6px;}
  .about-text{white-space:pre-line;line-height:1.6;margin:8px 0 6px;}
  .about-body .social{margin:16px 0 0;}
  .ad-f{display:block;margin:12px 0;font-size:.85rem;}
  .ad-f input,.ad-f textarea{display:block;width:100%;margin-top:4px;padding:10px;border-radius:10px;border:1px solid var(--line);background:var(--paper);color:var(--ink);font:inherit;box-sizing:border-box;}
</style>
</head>
<body>

<header>
  <div class="brand"><img class="fin" src="data:image/jpeg;base64,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" alt="Shastha Guppy Farm logo">Shastha Guppy Farm</div>
  <button class="cart-btn" id="editBtn" hidden style="background:var(--gold);color:#fff;margin-left:auto">Edit shop</button>
  <button class="cart-btn" id="cartOpenBtn">Order <span class="cart-count" id="cartCount">0</span></button>
</header>

<div class="hero">
  <div class="tagline">fifty plus guppy varieties, bred and raised here</div>
  <h1>Colour that <span class="accent">swims</span></h1>
  <p>Live guppies in every colour and tail shape we raise, plus the food that keeps them thriving. Pick your favourites and send the order straight to us on WhatsApp.</p>
</div>

<main>
  <div class="tabs" id="tabs"></div>
  <div class="grid" id="grid"></div>
</main>

<div class="social" id="socialBar"></div>
<footer>Shastha Guppy Farm &mdash; orders confirmed over WhatsApp.</footer>


<section id="adminPanel" hidden>
  <div class="ad-head"><h2>Edit shop</h2><div><button id="adSave" class="ad-save">Save changes</button> <button id="adClose" class="ad-x">Close</button></div></div>
  <p class="ad-note">Only you see this screen. Changes go live for all customers after you press Save.</p>
  <label class="ad-wa">WhatsApp number (country code first, no + or spaces)<input id="adWa" inputmode="numeric"></label>
  <label class="ad-f">Instagram page link<input id="adIg" placeholder="https://instagram.com/yourpage"></label>
  <label class="ad-f">Facebook page link<input id="adFb" placeholder="https://facebook.com/yourpage"></label>
  <label class="ad-f">YouTube channel link<input id="adYt" placeholder="https://youtube.com/@yourchannel"></label>
  <label class="ad-f">About Shastha Guppy Farm (shown when customers tap the name)<textarea id="adAbout" rows="6"></textarea></label>
  <div id="adminList"></div>
  <button id="adAdd" class="ad-add">+ Add new item</button>
</section>
<div class="overlay" id="overlay"></div>
<aside class="drawer" id="drawer">
  <div class="drawer-head"><h2>Your order</h2><button id="drawerClose" aria-label="Close">X</button></div>
  <div class="drawer-items" id="drawerItems"></div>
  <div class="drawer-foot">
    <div class="total-row"><span>Total</span><span id="totalAmt">Rs. 0</span></div>
    <button class="checkout-btn" id="checkoutBtn">Send order on WhatsApp</button>
  </div>
</aside>

<div class="detail-overlay" id="detailOverlay">
  <div class="detail-card" id="detailCard">
    <button class="detail-close" id="detailClose" aria-label="Close">X</button>
    <div class="detail-media" id="detailMedia"></div>
    <div class="detail-body">
      <span class="cat" id="detailCat"></span>
      <h2 id="detailName"></h2>
      <span class="price" id="detailPrice"></span>
      <div class="detail-actions" id="detailActions"></div>
    </div>
  </div>
</div>

<div class="detail-overlay" id="aboutOverlay">
  <div class="detail-card">
    <button class="detail-close" id="aboutClose" aria-label="Close">X</button>
    <div class="about-body">
      <img id="aboutLogo" alt="Shastha Guppy Farm">
      <h2>Shastha Guppy Farm</h2>
      <p class="about-text" id="aboutText"></p>
      <div class="social" id="aboutSocial"></div>
    </div>
  </div>
</div>

<script type="application/json" id="state">{"whatsapp": "918088820799", "products": [{"id": "g1", "name": "Albino Platinum White Guppy (pair)", "cat": "Guppies", "price": 300, "inStock": true}, {"id": "g2", "name": "Albino Redlace Guppy (pair)", "cat": "Guppies", "price": 250, "inStock": true}, {"id": "g3", "name": "Albino Silvarado Red Ear Guppy (pair)", "cat": "Guppies", "price": 240, "inStock": true}, {"id": "g4", "name": "AFR Guppy (pair)", "cat": "Guppies", "price": 230, "inStock": true}, {"id": "g5", "name": "Masco Blue Guppy (pair)", "cat": "Guppies", "price": 220, "inStock": true}, {"id": "g6", "name": "Black Guppy (pair)", "cat": "Guppies", "price": 180, "inStock": true}, {"id": "g7", "name": "Platinum White Dumbo Guppy (pair)", "cat": "Guppies", "price": 450, "inStock": true}, {"id": "g8", "name": "Silvarado Mosaic Guppy (pair)", "cat": "Guppies", "price": 180, "inStock": true}, {"id": "g9", "name": "White Texido Guppy (pair)", "cat": "Guppies", "price": 180, "inStock": true}, {"id": "g10", "name": "Japanese Blue Guppy (pair)", "cat": "Guppies", "price": 250, "inStock": true}, {"id": "g11", "name": "Platinum Big Ear Guppy (pair)", "cat": "Guppies", "price": 250, "inStock": true}, {"id": "g12", "name": "Chilli Mosaic Dumbo Guppy (pair)", "cat": "Guppies", "price": 205, "inStock": true}, {"id": "g13", "name": "Gold Guppy (pair)", "cat": "Guppies", "price": 250, "inStock": true}, {"id": "g14", "name": "Gold Ribbon Guppy (pair)", "cat": "Guppies", "price": 500, "inStock": true}, {"id": "g15", "name": "Red Granite Guppy (pair)", "cat": "Guppies", "price": 215, "inStock": true}, {"id": "g16", "name": "Blue Panda Guppy (pair)", "cat": "Guppies", "price": 230, "inStock": true}, {"id": "g17", "name": "Purple Burry Guppy (pair)", "cat": "Guppies", "price": 250, "inStock": true}, {"id": "g18", "name": "Tiger HM Guppy (pair)", "cat": "Guppies", "price": 180, "inStock": true}, {"id": "g19", "name": "Yellow Pingu Guppy (pair)", "cat": "Guppies", "price": 215, "inStock": true}, {"id": "g20", "name": "Lazuli Blue Guppy (pair)", "cat": "Guppies", "price": 190, "inStock": true}, {"id": "g21", "name": "Black Bar Endler Guppy (pair)", "cat": "Guppies", "price": 200, "inStock": true}, {"id": "g22", "name": "Red Scarlet Endler Guppy (pair)", "cat": "Guppies", "price": 200, "inStock": true}, {"id": "g23", "name": "Ivory Purple Guppy (pair)", "cat": "Guppies", "price": 250, "inStock": true}, {"id": "g24", "name": "Red Coral Endler Guppy (pair)", "cat": "Guppies", "price": 250, "inStock": true}, {"id": "g25", "name": "Zee Through Koi Guppy (pair)", "cat": "Guppies", "price": 250, "inStock": true}, {"id": "g26", "name": "Santha Clause SB Guppy (pair)", "cat": "Guppies", "price": 400, "inStock": true}, {"id": "g27", "name": "Wildred Guppy (pair)", "cat": "Guppies", "price": 210, "inStock": true}, {"id": "g28", "name": "Albino Metal Redlace Guppy (pair)", "cat": "Guppies", "price": 230, "inStock": true}, {"id": "g29", "name": "Red Dragon HM Guppy (pair)", "cat": "Guppies", "price": 250, "inStock": true}, {"id": "f1", "name": "Guppy Flake Food 100g", "cat": "Food", "price": 120, "inStock": true}, {"id": "f2", "name": "Live Daphnia Culture", "cat": "Food", "price": 80, "inStock": true}, {"id": "f3", "name": "Baby Guppy Fry Food", "cat": "Food", "price": 100, "inStock": true}]}</script>
<script>
let state = JSON.parse(document.getElementById('state').textContent);
let PRODUCTS = state.products;
const CATS = ['All','Guppies','Food'];
let cart = {}, activeCat = 'All';
const $ = id => document.getElementById(id);
const money = n => '\u20b9' + Number(n).toLocaleString('en-IN');
const esc = s => String(s).replace(/[&<>"']/g, c => ({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'}[c]));
const find = id => PRODUCTS.find(p => p.id === id);

function renderTabs(){
  $('tabs').innerHTML = '';
  CATS.forEach(c => {
    const b = document.createElement('button');
    b.className = 'tab'; b.textContent = c;
    b.setAttribute('aria-selected', c === activeCat ? 'true' : 'false');
    b.onclick = () => { activeCat = c; renderTabs(); renderGrid(); };
    $('tabs').appendChild(b);
  });
}
function mediaHtml(p){
  if(p.video) return '<div class="media"><video src="'+p.video+'" '+(p.photo?'poster="'+p.photo+'" ':'')+'controls preload="none" playsinline></video></div>';
  if(p.photo) return '<div class="media"><img src="'+p.photo+'" alt="'+esc(p.name)+'" loading="lazy"></div>';
  return '<div class="media">'+(p.cat==='Guppies'?'GUPPY':'FOOD')+'</div>';
}
function renderGrid(){
  const grid = $('grid'); grid.innerHTML = '';
  PRODUCTS.filter(p => activeCat === 'All' || p.cat === activeCat).forEach(p => {
    const q = cart[p.id] || 0;
    const action = !p.inStock ? '<button class="add-btn" disabled>Sold out</button>'
      : q === 0 ? '<button class="add-btn" data-add="'+p.id+'">Add to order</button>'
      : '<div class="qty-row"><button data-dec="'+p.id+'">-</button><span>'+q+'</span><button data-inc="'+p.id+'">+</button></div>';
    const card = document.createElement('div'); card.className = 'card';
    card.innerHTML = mediaHtml(p)+'<div class="card-body"><span class="cat">'+esc(p.cat)+'</span><h3>'+esc(p.name)+'</h3><span class="price">'+money(p.price)+'</span>'+action+'</div>';
    card.addEventListener('click', (ev) => { if(ev.target.closest('button')) return; openDetail(p.id); });
    grid.appendChild(card);
  });
  bind(grid);
}

function openDetail(id){
  const p = find(id); if(!p) return;
  $('detailMedia').innerHTML = mediaHtml(p);
  const vid = $('detailMedia').querySelector('video');
  if(vid){ vid.muted = true; vid.autoplay = true; vid.loop = true; vid.play().catch(()=>{}); }
  $('detailCat').textContent = p.cat;
  $('detailName').textContent = p.name;
  $('detailPrice').textContent = money(p.price);
  const q = cart[p.id] || 0;
  $('detailActions').innerHTML = !p.inStock ? '<button class="add-btn" disabled>Sold out</button>'
    : q === 0 ? '<button class="add-btn" data-add="'+p.id+'">Add to order</button>'
    : '<div class="qty-row"><button data-dec="'+p.id+'">-</button><span>'+q+'</span><button data-inc="'+p.id+'">+</button></div>';
  bind($('detailActions'));
  $('detailOverlay').classList.add('open');
}
function closeDetail(){ $('detailOverlay').classList.remove('open'); }
$('detailClose').onclick = closeDetail;
$('detailOverlay').onclick = (ev) => { if(ev.target === $('detailOverlay')) closeDetail(); };
function bind(root){
  root.querySelectorAll('[data-add]').forEach(b => b.onclick = () => { cart[b.dataset.add] = 1; renderAll(); });
  root.querySelectorAll('[data-inc]').forEach(b => b.onclick = () => { cart[b.dataset.inc]++; renderAll(); });
  root.querySelectorAll('[data-dec]').forEach(b => b.onclick = () => { const id = b.dataset.dec; if(--cart[id] <= 0) delete cart[id]; renderAll(); });
}
const cartTotal = () => Object.entries(cart).reduce((s,[id,q]) => s + (find(id)?.price||0)*q, 0);
const cartCount = () => Object.values(cart).reduce((a,b) => a+b, 0);
function renderDrawer(){
  $('cartCount').textContent = cartCount();
  const w = $('drawerItems'), e = Object.entries(cart).filter(([id]) => find(id));
  w.innerHTML = e.length ? e.map(([id,q]) => { const p = find(id);
    return '<div class="line"><div><div class="line-name">'+esc(p.name)+'</div><div style="font-size:.82rem;opacity:.65">'+money(p.price)+' x '+q+'</div></div><div class="line-qty"><button data-dec="'+id+'">-</button><span>'+q+'</span><button data-inc="'+id+'">+</button></div></div>'; }).join('')
    : '<p class="empty-note">Your order is empty.<br>Add guppies or food from the catalog.</p>';
  bind(w);
  $('totalAmt').textContent = money(cartTotal());
}
function renderAll(){ renderGrid(); renderDrawer(); refreshDetailActions(); }
function refreshDetailActions(){
  if(!$('detailOverlay').classList.contains('open')) return;
  const id = $('detailActions').querySelector('[data-add],[data-inc],[data-dec]');
  if(!id) return;
  const pid = id.dataset.add || id.dataset.inc || id.dataset.dec;
  const p = find(pid); if(!p) return;
  const q = cart[p.id] || 0;
  $('detailActions').innerHTML = !p.inStock ? '<button class="add-btn" disabled>Sold out</button>'
    : q === 0 ? '<button class="add-btn" data-add="'+p.id+'">Add to order</button>'
    : '<div class="qty-row"><button data-dec="'+p.id+'">-</button><span>'+q+'</span><button data-inc="'+p.id+'">+</button></div>';
  bind($('detailActions'));
}
const setDrawer = on => { $('overlay').classList.toggle('open', on); $('drawer').classList.toggle('open', on); };
$('cartOpenBtn').onclick = () => setDrawer(true);
$('drawerClose').onclick = $('overlay').onclick = () => setDrawer(false);

$('checkoutBtn').onclick = () => {
  const e = Object.entries(cart).filter(([id]) => find(id));
  if(!e.length){ alert('Add at least one item to your order first.'); return; }
  let msg = "Hello Shastha Guppy Farm, I'd like to order:\n\n";
  e.forEach(([id,q]) => { const p = find(id); msg += '- '+p.name+' x'+q+' = '+money(p.price*q)+'\n'; });
  msg += '\nTotal: '+money(cartTotal())+'\n\nPlease confirm availability and delivery.';
  window.open('https://wa.me/'+state.whatsapp+'?text='+encodeURIComponent(msg), '_blank');
};

/* ---------- owner-only edit mode ---------- */
let draft;
function buildDoc(s){
  const c = document.documentElement.cloneNode(true);
  ['grid','tabs','drawerItems','adminList','detailMedia','detailActions','socialBar','aboutSocial'].forEach(id => { const e = c.querySelector('#'+id); if(e) e.innerHTML = ''; });
  c.querySelector('#state').textContent = JSON.stringify(s).replace(/</g,'\\u003c');
  c.querySelectorAll('.open').forEach(e => e.classList.remove('open'));
  c.querySelector('#editBtn').setAttribute('hidden','');
  c.querySelector('#aboutText').textContent = '';
  c.querySelector('#aboutLogo').removeAttribute('src');
  c.querySelector('#adminPanel').setAttribute('hidden','');
  c.querySelector('#cartCount').textContent = '0';
  c.querySelector('#totalAmt').textContent = money(0);
  return '<!DOCTYPE html>\n' + c.outerHTML;
}
function readData(f){ return new Promise((res,rej)=>{ const r=new FileReader(); r.onload=()=>res(r.result); r.onerror=rej; r.readAsDataURL(f); }); }
async function shrink(f){
  const img = new Image(); img.src = await readData(f); await img.decode();
  const s = Math.min(1, 640/img.width), c = document.createElement('canvas');
  c.width = Math.round(img.width*s); c.height = Math.round(img.height*s);
  c.getContext('2d').drawImage(img,0,0,c.width,c.height);
  return c.toDataURL('image/jpeg',0.72);
}
function renderAdmin(){
  $('adminList').innerHTML = draft.products.map((p,i) =>
    '<div class="ad-row"><input data-f="name" data-i="'+i+'" value="'+esc(p.name)+'"><input data-f="price" data-i="'+i+'" inputmode="numeric" value="'+p.price+'"><select data-f="cat" data-i="'+i+'"><option'+(p.cat==='Guppies'?' selected':'')+'>Guppies</option><option'+(p.cat==='Food'?' selected':'')+'>Food</option></select>'
    +'<div class="full"><span>Photo: '+(p.photo?'added <button class="del" data-rmp="'+i+'">remove</button>':'<input type="file" accept="image/*" data-photo="'+i+'" style="width:auto">')+'</span></div>'
    +'<div class="full"><span>Video: '+(p.video?'added <button class="del" data-rmv="'+i+'">remove</button>':'<input type="file" accept="video/*" data-video="'+i+'" style="width:auto">')+'</span></div>'
    +'<div class="full"><label><input type="checkbox" style="width:auto" data-f="inStock" data-i="'+i+'"'+(p.inStock?' checked':'')+'> In stock</label><button class="del" data-del="'+i+'">Delete</button></div></div>').join('');
  const L = $('adminList');
  L.querySelectorAll('[data-f]').forEach(el => el.onchange = () => {
    const p = draft.products[el.dataset.i], f = el.dataset.f;
    p[f] = f==='inStock' ? el.checked : f==='price' ? (Number(el.value)||0) : el.value.trim();
  });
  L.querySelectorAll('[data-photo]').forEach(el => el.onchange = async () => { const f = el.files[0]; if(!f) return; draft.products[el.dataset.photo].photo = await shrink(f); renderAdmin(); });
  L.querySelectorAll('[data-video]').forEach(el => el.onchange = async () => {
    const f = el.files[0]; if(!f) return;
    if(f.size > 2*1048576){ alert('This video is '+(f.size/1048576).toFixed(1)+' MB. Please compress it under 2 MB first.'); el.value=''; return; }
    draft.products[el.dataset.video].video = await readData(f); renderAdmin();
  });
  L.querySelectorAll('[data-rmp]').forEach(b => b.onclick = () => { delete draft.products[b.dataset.rmp].photo; renderAdmin(); });
  L.querySelectorAll('[data-rmv]').forEach(b => b.onclick = () => { delete draft.products[b.dataset.rmv].video; renderAdmin(); });
  L.querySelectorAll('[data-del]').forEach(b => b.onclick = () => { if(confirm('Delete this item?')){ draft.products.splice(b.dataset.del,1); renderAdmin(); } });
}
const DEFAULT_ABOUT = 'Shastha Guppy Farm breeds and raises fifty plus varieties of guppies, along with the food that keeps them healthy.\n\nPick your favourites, send the order on WhatsApp, and we will confirm it with you directly.';
const ICONS = {
  whatsapp:'<svg viewBox="0 0 24 24"><path d="M3 21l1.6-4.6A9 9 0 1 1 8 19.6L3 21z"/><path d="M9 8.5c0 3 2.5 5.5 5.5 5.5l1-1.5-2-1-1 .8c-.8-.4-1.5-1.1-1.9-1.9l.8-1-1-2L9 8.5z" style="fill:currentColor;stroke:none"/></svg>',
  instagram:'<svg viewBox="0 0 24 24"><rect x="3" y="3" width="18" height="18" rx="5"/><circle cx="12" cy="12" r="4"/><circle cx="17.5" cy="6.5" r="1" style="fill:currentColor"/></svg>',
  facebook:'<svg viewBox="0 0 24 24"><path d="M14 8h3V4h-3a4 4 0 0 0-4 4v3H7v4h3v6h4v-6h3l1-4h-4V8z"/></svg>',
  youtube:'<svg viewBox="0 0 24 24"><rect x="2" y="5" width="20" height="14" rx="4"/><path d="M10 9l5 3-5 3z" style="fill:currentColor"/></svg>'
};
const normUrl = u => { u = String(u||'').trim(); return !u ? '' : (/^https?:\/\//i.test(u) ? u : 'https://' + u); };
function renderSocial(){
  const s = state.social || {};
  const items = [['whatsapp','https://wa.me/'+state.whatsapp,'WhatsApp'],['instagram',s.instagram,'Instagram'],['facebook',s.facebook,'Facebook'],['youtube',s.youtube,'YouTube']];
  const h = items.filter(x => x[1]).map(x => '<a href="'+esc(x[1])+'" target="_blank" rel="noopener" aria-label="'+x[2]+'">'+ICONS[x[0]]+'</a>').join('');
  $('socialBar').innerHTML = h; $('aboutSocial').innerHTML = h;
  $('aboutText').textContent = state.about || DEFAULT_ABOUT;
}
$('aboutClose').onclick = () => $('aboutOverlay').classList.remove('open');
$('aboutOverlay').onclick = ev => { if(ev.target === $('aboutOverlay')) $('aboutOverlay').classList.remove('open'); };
document.querySelector('.brand').onclick = () => { $('aboutLogo').src = document.querySelector('.brand img').src; $('aboutOverlay').classList.add('open'); };
const isOwnerLink = () => location.hash === '#owner';
window.addEventListener('hashchange', () => { $('editBtn').hidden = !isOwnerLink(); });

const OWNER_PASSWORD = 'shastha2026'; // change this to any password you like

function initAdmin(){
  $('editBtn').hidden = !isOwnerLink();
  $('editBtn').onclick = () => {
    if(!sessionStorage.getItem('ownerOk')){
      const pw = prompt('Enter shop owner password:');
      if(pw !== OWNER_PASSWORD){ if(pw !== null) alert('Wrong password.'); return; }
      sessionStorage.setItem('ownerOk','1');
    }
    draft = JSON.parse(JSON.stringify(state)); $('adWa').value = draft.whatsapp; const sc = draft.social || {}; $('adIg').value = sc.instagram || ''; $('adFb').value = sc.facebook || ''; $('adYt').value = sc.youtube || ''; $('adAbout').value = draft.about || DEFAULT_ABOUT; renderAdmin(); $('adminPanel').hidden = false;
  };
  $('adClose').onclick = () => { $('adminPanel').hidden = true; };
  $('adAdd').onclick = () => { draft.products.unshift({id:'n'+Date.now(), name:'New guppy (pair)', cat:'Guppies', price:0, inStock:true}); renderAdmin(); };
  $('adSave').onclick = () => {
    draft.whatsapp = $('adWa').value.replace(/\D/g,'') || draft.whatsapp;
    draft.social = {instagram: normUrl($('adIg').value), facebook: normUrl($('adFb').value), youtube: normUrl($('adYt').value)};
    draft.about = $('adAbout').value.trim();
    if(JSON.stringify(draft).length > 12e6){ alert('Too much photo/video data for one page (limit about 12 MB). Remove a few videos.'); return; }
    state = draft; PRODUCTS = state.products;
    const blob = new Blob([buildDoc(state)], {type:'text/html'});
    const url = URL.createObjectURL(blob);
    const a = document.createElement('a');
    a.href = url; a.download = 'index.html';
    document.body.appendChild(a); a.click(); a.remove();
    URL.revokeObjectURL(url);
    $('adminPanel').hidden = true;
    renderTabs(); renderAll(); renderSocial();
    alert('Saved! A file was downloaded. On GitHub, upload it, delete the old index.html, and rename the new file to index.html. The live site then updates in a minute or two.');
  };
}
initAdmin();


renderTabs(); renderAll(); renderSocial();
</script>
</body>
</html>

<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Shastha Guppy Farm</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Baloo+2:wght@500;600;700&family=Karla:wght@400;500;700&display=swap" rel="stylesheet">
<style>
  :root{
    --ink:#12324F;         /* deep navy text on white */
    --paper:#FFFFFF;       /* clean white page */
    --panel:#EEF5FF;       /* pale blue panels */
    --violet:#2E7BE0;      /* secondary blue */
    --magenta:#4A90E2;     /* light blue accent */
    --gold:#1E6FD9;        /* main blue accent */
    --teal:#0F4C9A;        /* deep blue, used sparingly */
    --line:#CFE0F5;        /* soft blue hairline */
    --radius:14px;
  }
  *{box-sizing:border-box;}
  html{scroll-behavior:smooth;}
  body{
    margin:0; background:var(--paper); color:var(--ink);
    font-family:'Karla',sans-serif; line-height:1.55;
    padding-bottom:env(safe-area-inset-bottom,0px);
  }
  h1,h2,h3,.brand,.tagline{font-family:'Baloo 2',sans-serif;}

  header{
    position:sticky; top:0; z-index:30; background:var(--paper);
    border-bottom:2px solid var(--line);
    padding:calc(env(safe-area-inset-top,0px) + 12px) 20px 12px;
    display:flex; align-items:center; justify-content:space-between; gap:12px;
  }
  .brand{display:flex; align-items:center; gap:10px; font-size:1.2rem; font-weight:700; color:var(--ink);}
  .brand .fin{
    width:40px;height:40px;border-radius:50%;
    object-fit:cover; flex-shrink:0; background:#000;
  }
  .cart-btn{
    background:var(--ink); color:var(--paper); border:none; border-radius:999px;
    padding:10px 18px; font-family:'Karla'; font-weight:700; font-size:.88rem;
    cursor:pointer; display:flex; align-items:center; gap:8px;
  }
  .cart-count{background:var(--gold); color:#fff; border-radius:999px; padding:1px 9px; font-size:.78rem; font-weight:700;}

  .hero{
    padding:52px 20px 40px; max-width:920px; margin:0 auto;
    display:flex; flex-direction:column; gap:14px;
  }
  .tagline{
    font-size:.85rem; letter-spacing:.02em; color:var(--teal); font-weight:600;
    text-transform:lowercase;
  }
  .hero h1{
    font-size:clamp(2.1rem,6vw,3.2rem); margin:0; font-weight:700; line-height:1.08;
    max-width:16ch;
  }
  .hero h1 .accent{color:var(--magenta);}
  .hero p{max-width:52ch; font-size:1.05rem; margin:2px 0 0; color:#3D5A80;}
  .tail-row{display:flex; gap:10px; margin-top:6px; font-size:1.6rem;}

  main{max-width:1000px; margin:0 auto; padding:0 20px 90px;}
  .tabs{display:flex; gap:10px; overflow-x:auto; padding:4px 0 26px;}
  .tab{
    border:2px solid var(--ink); background:transparent; color:var(--ink);
    padding:9px 18px; border-radius:999px; font-size:.9rem; font-weight:700;
    cursor:pointer; white-space:nowrap; font-family:'Karla';
  }
  .tab[aria-selected="true"]{background:var(--ink); color:var(--paper);}

  .grid{display:grid; grid-template-columns:repeat(auto-fill,minmax(220px,1fr)); gap:20px;}
  .card{
    background:var(--panel); border-radius:var(--radius); overflow:hidden;
    display:flex; flex-direction:column;
    box-shadow:0 1px 0 var(--line);
    border:1px solid var(--line);
  }
  .media{
    width:100%; aspect-ratio:4/3; background:linear-gradient(160deg,#E6F0FC,#D3E4F9);
    display:flex; align-items:center; justify-content:center; font-size:1.1rem; letter-spacing:.08em; color:#6E8FB8; font-weight:700;
    position:relative; overflow:hidden;
  }
  .media img, .media video{width:100%; height:100%; object-fit:cover;}
  .media .play-badge{
    position:absolute; bottom:8px; right:8px; background:rgba(27,16,53,.75); color:#fff;
    font-size:.7rem; padding:3px 8px; border-radius:999px; font-weight:700;
  }
  .card-body{padding:14px 14px 16px; display:flex; flex-direction:column; gap:6px; flex:1;}
  .card-body .cat{font-size:.72rem; font-weight:700; color:var(--violet); text-transform:lowercase;}
  .card-body h3{margin:0; font-size:1.05rem; font-weight:600; color:var(--ink);}
  .card-body .price{font-weight:700; margin-top:auto; font-size:1.05rem;}
  .qty-row{display:flex; align-items:center; gap:10px; margin-top:4px;}
  .qty-row button{
    width:30px; height:30px; border-radius:8px; border:2px solid var(--ink);
    background:var(--paper); color:var(--ink); font-size:1rem; cursor:pointer; font-weight:700;
  }
  .add-btn{
    background:var(--violet); color:#fff; border:none; border-radius:8px;
    padding:10px; font-weight:700; cursor:pointer; font-family:'Karla'; font-size:.92rem;
    margin-top:4px;
  }
  .add-btn:active{background:var(--magenta);}

  .overlay{position:fixed; inset:0; background:rgba(10,30,60,.4); z-index:40; display:none;}
  .overlay.open{display:block;}
  .drawer{
    position:fixed; top:0; right:0; bottom:0; width:min(400px,92vw);
    background:var(--panel); z-index:41; transform:translateX(105%);
    transition:transform .25s ease; display:flex; flex-direction:column;
    padding-top:env(safe-area-inset-top,0px); padding-bottom:env(safe-area-inset-bottom,0px);
  }
  .drawer.open{transform:translateX(0);}
  .drawer-head{padding:18px 20px; border-bottom:2px solid var(--line); display:flex; justify-content:space-between; align-items:center;}
  .drawer-head h2{margin:0; font-size:1.25rem;}
  .drawer-head button{background:none; border:none; font-size:1.3rem; cursor:pointer; color:var(--ink);}
  .drawer-items{flex:1; overflow-y:auto; padding:14px 20px;}
  .line{display:flex; justify-content:space-between; align-items:center; gap:8px; padding:12px 0; border-bottom:1px solid var(--line);}
  .line-name{font-size:.92rem; font-weight:600;}
  .line-qty{display:flex; align-items:center; gap:6px;}
  .line-qty button{width:26px;height:26px;border-radius:6px;border:2px solid var(--ink);background:var(--paper);cursor:pointer;font-weight:700;}
  .drawer-foot{padding:18px 20px; border-top:2px solid var(--line);}
  .total-row{display:flex; justify-content:space-between; font-weight:700; margin-bottom:14px; font-size:1.1rem;}
  .checkout-btn{
    width:100%; background:#25D366; color:#062A16; border:none; border-radius:10px;
    padding:14px; font-weight:700; font-size:1rem; cursor:pointer; font-family:'Karla';
    display:flex; align-items:center; justify-content:center; gap:8px;
  }
  .empty-note{color:var(--violet); opacity:.85; font-size:.92rem; padding:24px 0; text-align:center;}
  footer{text-align:center; padding:26px 20px 40px; font-size:.82rem; opacity:.6;}

  .add-btn[disabled]{background:#DDE6F1;color:#8095AF;cursor:not-allowed;}
  #adminPanel{position:fixed;inset:0;z-index:60;background:var(--paper);overflow-y:auto;padding:calc(env(safe-area-inset-top,0px) + 16px) 16px 60px;}
  #adminPanel[hidden]{display:none;}
  .ad-head{display:flex;justify-content:space-between;align-items:center;gap:8px;flex-wrap:wrap;}
  .ad-head h2{margin:0;}
  .ad-save,.ad-x,.ad-add{border:none;border-radius:8px;padding:10px 14px;font-weight:700;cursor:pointer;font-family:'Karla';}
  .ad-save{background:var(--gold);color:#fff;} .ad-x{background:var(--line);color:var(--ink);}
  .ad-add{background:var(--panel);color:var(--gold);border:2px dashed var(--gold);width:100%;margin-top:14px;}
  .ad-note{font-size:.85rem;opacity:.75;}
  .ad-wa{display:block;font-size:.85rem;margin:8px 0 14px;}
  .ad-wa input,.ad-row input,.ad-row select{background:var(--panel);color:var(--ink);border:1px solid var(--line);border-radius:6px;padding:8px;font-family:'Karla';font-size:.9rem;width:100%;}
  .ad-row{display:grid;grid-template-columns:2fr 1fr 1fr;gap:6px;background:var(--panel);border:1px solid var(--line);border-radius:10px;padding:10px;margin-bottom:8px;}
  .ad-row .full{grid-column:1/-1;display:flex;justify-content:space-between;align-items:center;font-size:.85rem;}
  .ad-row .del{background:none;border:none;color:#e0705a;font-weight:700;cursor:pointer;}

  /* ---------- product detail popup ---------- */
  .card{cursor:pointer;}
  .detail-overlay{
    position:fixed; inset:0; background:rgba(10,30,60,.55); z-index:60;
    display:flex; align-items:flex-end; justify-content:center;
    opacity:0; pointer-events:none; transition:opacity .28s ease;
  }
  .detail-overlay.open{opacity:1; pointer-events:auto;}
  @media (min-width:720px){ .detail-overlay{align-items:center;} }
  .detail-card{
    background:var(--panel); border:2px solid var(--line); border-radius:20px 20px 0 0;
    width:100%; max-width:560px; max-height:88vh; overflow-y:auto;
    padding:0 0 26px; position:relative;
    transform:translateY(28px) scale(.97); opacity:0;
    transition:transform .32s cubic-bezier(.2,.9,.25,1.1), opacity .28s ease;
  }
  .detail-overlay.open .detail-card{transform:translateY(0) scale(1); opacity:1;}
  @media (min-width:720px){ .detail-card{border-radius:20px;} }
  .detail-close{
    position:absolute; top:14px; right:14px; z-index:2;
    background:rgba(255,255,255,.92); color:var(--ink); border:1px solid var(--line);
    border-radius:999px; width:36px; height:36px; font-size:1.1rem; cursor:pointer;
  }
  .detail-media{width:100%; aspect-ratio:1/1; background:#000; overflow:hidden; border-radius:20px 20px 0 0;}
  .detail-media img, .detail-media video{width:100%; height:100%; object-fit:cover; display:block;
    animation:detailZoom .5s ease;}
  @keyframes detailZoom{from{transform:scale(1.08); opacity:.4;} to{transform:scale(1); opacity:1;}}
  .detail-media .media{height:100%; border-radius:0;}
  .detail-body{padding:20px 22px 4px;}
  .detail-body .cat{display:block; margin-bottom:4px;}
  .detail-body h2{margin:2px 0 8px; font-size:1.5rem;}
  .detail-body .price{font-size:1.2rem; font-weight:700; color:var(--gold); display:block; margin-bottom:16px;}
  .detail-actions{display:flex; gap:10px;}

  .brand{cursor:pointer;}
  .social{display:flex;justify-content:center;gap:14px;margin:26px 0 0;}
  .social a{width:44px;height:44px;border:1.5px solid var(--line);border-radius:999px;display:grid;place-items:center;color:var(--gold);transition:transform .2s,background .2s;}
  .social a:hover{transform:translateY(-2px);background:rgba(30,111,217,.10);}
  .social svg{width:22px;height:22px;fill:none;stroke:currentColor;stroke-width:1.8;stroke-linecap:round;stroke-linejoin:round;}
  .about-body{padding:26px 22px 8px;text-align:center;}
  .about-body img{width:84px;height:84px;border-radius:50%;object-fit:cover;margin-bottom:6px;}
  .about-text{white-space:pre-line;line-height:1.6;margin:8px 0 6px;}
  .about-body .social{margin:16px 0 0;}
  .ad-f{display:block;margin:12px 0;font-size:.85rem;}
  .ad-f input,.ad-f textarea{display:block;width:100%;margin-top:4px;padding:10px;border-radius:10px;border:1px solid var(--line);background:var(--paper);color:var(--ink);font:inherit;box-sizing:border-box;}
</style>
</head>
<body>

<header>
  <div class="brand"><img class="fin" src="data:image/jpeg;base64,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" alt="Shastha Guppy Farm logo">Shastha Guppy Farm</div>
  <button class="cart-btn" id="editBtn" hidden style="background:var(--gold);color:#fff;margin-left:auto">Edit shop</button>
  <button class="cart-btn" id="cartOpenBtn">Order <span class="cart-count" id="cartCount">0</span></button>
</header>

<div class="hero">
  <div class="tagline">fifty plus guppy varieties, bred and raised here</div>
  <h1>Colour that <span class="accent">swims</span></h1>
  <p>Live guppies in every colour and tail shape we raise, plus the food that keeps them thriving. Pick your favourites and send the order straight to us on WhatsApp.</p>
</div>

<main>
  <div class="tabs" id="tabs"></div>
  <div class="grid" id="grid"></div>
</main>

<div class="social" id="socialBar"></div>
<footer>Shastha Guppy Farm &mdash; orders confirmed over WhatsApp.</footer>


<section id="adminPanel" hidden>
  <div class="ad-head"><h2>Edit shop</h2><div><button id="adSave" class="ad-save">Save changes</button> <button id="adClose" class="ad-x">Close</button></div></div>
  <p class="ad-note">Only you see this screen. Changes go live for all customers after you press Save.</p>
  <label class="ad-wa">WhatsApp number (country code first, no + or spaces)<input id="adWa" inputmode="numeric"></label>
  <label class="ad-f">Instagram page link<input id="adIg" placeholder="https://instagram.com/yourpage"></label>
  <label class="ad-f">Facebook page link<input id="adFb" placeholder="https://facebook.com/yourpage"></label>
  <label class="ad-f">YouTube channel link<input id="adYt" placeholder="https://youtube.com/@yourchannel"></label>
  <label class="ad-f">About Shastha Guppy Farm (shown when customers tap the name)<textarea id="adAbout" rows="6"></textarea></label>
  <div id="adminList"></div>
  <button id="adAdd" class="ad-add">+ Add new item</button>
</section>
<div class="overlay" id="overlay"></div>
<aside class="drawer" id="drawer">
  <div class="drawer-head"><h2>Your order</h2><button id="drawerClose" aria-label="Close">X</button></div>
  <div class="drawer-items" id="drawerItems"></div>
  <div class="drawer-foot">
    <div class="total-row"><span>Total</span><span id="totalAmt">Rs. 0</span></div>
    <button class="checkout-btn" id="checkoutBtn">Send order on WhatsApp</button>
  </div>
</aside>

<div class="detail-overlay" id="detailOverlay">
  <div class="detail-card" id="detailCard">
    <button class="detail-close" id="detailClose" aria-label="Close">X</button>
    <div class="detail-media" id="detailMedia"></div>
    <div class="detail-body">
      <span class="cat" id="detailCat"></span>
      <h2 id="detailName"></h2>
      <span class="price" id="detailPrice"></span>
      <div class="detail-actions" id="detailActions"></div>
    </div>
  </div>
</div>

<div class="detail-overlay" id="aboutOverlay">
  <div class="detail-card">
    <button class="detail-close" id="aboutClose" aria-label="Close">X</button>
    <div class="about-body">
      <img id="aboutLogo" alt="Shastha Guppy Farm">
      <h2>Shastha Guppy Farm</h2>
      <p class="about-text" id="aboutText"></p>
      <div class="social" id="aboutSocial"></div>
    </div>
  </div>
</div>

<script type="application/json" id="state">{"whatsapp": "918088820799", "products": [{"id": "g1", "name": "Albino Platinum White Guppy (pair)", "cat": "Guppies", "price": 300, "inStock": true}, {"id": "g2", "name": "Albino Redlace Guppy (pair)", "cat": "Guppies", "price": 250, "inStock": true}, {"id": "g3", "name": "Albino Silvarado Red Ear Guppy (pair)", "cat": "Guppies", "price": 240, "inStock": true}, {"id": "g4", "name": "AFR Guppy (pair)", "cat": "Guppies", "price": 230, "inStock": true}, {"id": "g5", "name": "Masco Blue Guppy (pair)", "cat": "Guppies", "price": 220, "inStock": true}, {"id": "g6", "name": "Black Guppy (pair)", "cat": "Guppies", "price": 180, "inStock": true}, {"id": "g7", "name": "Platinum White Dumbo Guppy (pair)", "cat": "Guppies", "price": 450, "inStock": true}, {"id": "g8", "name": "Silvarado Mosaic Guppy (pair)", "cat": "Guppies", "price": 180, "inStock": true}, {"id": "g9", "name": "White Texido Guppy (pair)", "cat": "Guppies", "price": 180, "inStock": true}, {"id": "g10", "name": "Japanese Blue Guppy (pair)", "cat": "Guppies", "price": 250, "inStock": true}, {"id": "g11", "name": "Platinum Big Ear Guppy (pair)", "cat": "Guppies", "price": 250, "inStock": true}, {"id": "g12", "name": "Chilli Mosaic Dumbo Guppy (pair)", "cat": "Guppies", "price": 205, "inStock": true}, {"id": "g13", "name": "Gold Guppy (pair)", "cat": "Guppies", "price": 250, "inStock": true}, {"id": "g14", "name": "Gold Ribbon Guppy (pair)", "cat": "Guppies", "price": 500, "inStock": true}, {"id": "g15", "name": "Red Granite Guppy (pair)", "cat": "Guppies", "price": 215, "inStock": true}, {"id": "g16", "name": "Blue Panda Guppy (pair)", "cat": "Guppies", "price": 230, "inStock": true}, {"id": "g17", "name": "Purple Burry Guppy (pair)", "cat": "Guppies", "price": 250, "inStock": true}, {"id": "g18", "name": "Tiger HM Guppy (pair)", "cat": "Guppies", "price": 180, "inStock": true}, {"id": "g19", "name": "Yellow Pingu Guppy (pair)", "cat": "Guppies", "price": 215, "inStock": true}, {"id": "g20", "name": "Lazuli Blue Guppy (pair)", "cat": "Guppies", "price": 190, "inStock": true}, {"id": "g21", "name": "Black Bar Endler Guppy (pair)", "cat": "Guppies", "price": 200, "inStock": true}, {"id": "g22", "name": "Red Scarlet Endler Guppy (pair)", "cat": "Guppies", "price": 200, "inStock": true}, {"id": "g23", "name": "Ivory Purple Guppy (pair)", "cat": "Guppies", "price": 250, "inStock": true}, {"id": "g24", "name": "Red Coral Endler Guppy (pair)", "cat": "Guppies", "price": 250, "inStock": true}, {"id": "g25", "name": "Zee Through Koi Guppy (pair)", "cat": "Guppies", "price": 250, "inStock": true}, {"id": "g26", "name": "Santha Clause SB Guppy (pair)", "cat": "Guppies", "price": 400, "inStock": true}, {"id": "g27", "name": "Wildred Guppy (pair)", "cat": "Guppies", "price": 210, "inStock": true}, {"id": "g28", "name": "Albino Metal Redlace Guppy (pair)", "cat": "Guppies", "price": 230, "inStock": true}, {"id": "g29", "name": "Red Dragon HM Guppy (pair)", "cat": "Guppies", "price": 250, "inStock": true}, {"id": "f1", "name": "Guppy Flake Food 100g", "cat": "Food", "price": 120, "inStock": true}, {"id": "f2", "name": "Live Daphnia Culture", "cat": "Food", "price": 80, "inStock": true}, {"id": "f3", "name": "Baby Guppy Fry Food", "cat": "Food", "price": 100, "inStock": true}]}</script>
<script>
let state = JSON.parse(document.getElementById('state').textContent);
let PRODUCTS = state.products;
const CATS = ['All','Guppies','Food'];
let cart = {}, activeCat = 'All';
const $ = id => document.getElementById(id);
const money = n => '\u20b9' + Number(n).toLocaleString('en-IN');
const esc = s => String(s).replace(/[&<>"']/g, c => ({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'}[c]));
const find = id => PRODUCTS.find(p => p.id === id);

function renderTabs(){
  $('tabs').innerHTML = '';
  CATS.forEach(c => {
    const b = document.createElement('button');
    b.className = 'tab'; b.textContent = c;
    b.setAttribute('aria-selected', c === activeCat ? 'true' : 'false');
    b.onclick = () => { activeCat = c; renderTabs(); renderGrid(); };
    $('tabs').appendChild(b);
  });
}
function mediaHtml(p){
  if(p.video) return '<div class="media"><video src="'+p.video+'" '+(p.photo?'poster="'+p.photo+'" ':'')+'controls preload="none" playsinline></video></div>';
  if(p.photo) return '<div class="media"><img src="'+p.photo+'" alt="'+esc(p.name)+'" loading="lazy"></div>';
  return '<div class="media">'+(p.cat==='Guppies'?'GUPPY':'FOOD')+'</div>';
}
function renderGrid(){
  const grid = $('grid'); grid.innerHTML = '';
  PRODUCTS.filter(p => activeCat === 'All' || p.cat === activeCat).forEach(p => {
    const q = cart[p.id] || 0;
    const action = !p.inStock ? '<button class="add-btn" disabled>Sold out</button>'
      : q === 0 ? '<button class="add-btn" data-add="'+p.id+'">Add to order</button>'
      : '<div class="qty-row"><button data-dec="'+p.id+'">-</button><span>'+q+'</span><button data-inc="'+p.id+'">+</button></div>';
    const card = document.createElement('div'); card.className = 'card';
    card.innerHTML = mediaHtml(p)+'<div class="card-body"><span class="cat">'+esc(p.cat)+'</span><h3>'+esc(p.name)+'</h3><span class="price">'+money(p.price)+'</span>'+action+'</div>';
    card.addEventListener('click', (ev) => { if(ev.target.closest('button')) return; openDetail(p.id); });
    grid.appendChild(card);
  });
  bind(grid);
}

function openDetail(id){
  const p = find(id); if(!p) return;
  $('detailMedia').innerHTML = mediaHtml(p);
  const vid = $('detailMedia').querySelector('video');
  if(vid){ vid.muted = true; vid.autoplay = true; vid.loop = true; vid.play().catch(()=>{}); }
  $('detailCat').textContent = p.cat;
  $('detailName').textContent = p.name;
  $('detailPrice').textContent = money(p.price);
  const q = cart[p.id] || 0;
  $('detailActions').innerHTML = !p.inStock ? '<button class="add-btn" disabled>Sold out</button>'
    : q === 0 ? '<button class="add-btn" data-add="'+p.id+'">Add to order</button>'
    : '<div class="qty-row"><button data-dec="'+p.id+'">-</button><span>'+q+'</span><button data-inc="'+p.id+'">+</button></div>';
  bind($('detailActions'));
  $('detailOverlay').classList.add('open');
}
function closeDetail(){ $('detailOverlay').classList.remove('open'); }
$('detailClose').onclick = closeDetail;
$('detailOverlay').onclick = (ev) => { if(ev.target === $('detailOverlay')) closeDetail(); };
function bind(root){
  root.querySelectorAll('[data-add]').forEach(b => b.onclick = () => { cart[b.dataset.add] = 1; renderAll(); });
  root.querySelectorAll('[data-inc]').forEach(b => b.onclick = () => { cart[b.dataset.inc]++; renderAll(); });
  root.querySelectorAll('[data-dec]').forEach(b => b.onclick = () => { const id = b.dataset.dec; if(--cart[id] <= 0) delete cart[id]; renderAll(); });
}
const cartTotal = () => Object.entries(cart).reduce((s,[id,q]) => s + (find(id)?.price||0)*q, 0);
const cartCount = () => Object.values(cart).reduce((a,b) => a+b, 0);
function renderDrawer(){
  $('cartCount').textContent = cartCount();
  const w = $('drawerItems'), e = Object.entries(cart).filter(([id]) => find(id));
  w.innerHTML = e.length ? e.map(([id,q]) => { const p = find(id);
    return '<div class="line"><div><div class="line-name">'+esc(p.name)+'</div><div style="font-size:.82rem;opacity:.65">'+money(p.price)+' x '+q+'</div></div><div class="line-qty"><button data-dec="'+id+'">-</button><span>'+q+'</span><button data-inc="'+id+'">+</button></div></div>'; }).join('')
    : '<p class="empty-note">Your order is empty.<br>Add guppies or food from the catalog.</p>';
  bind(w);
  $('totalAmt').textContent = money(cartTotal());
}
function renderAll(){ renderGrid(); renderDrawer(); refreshDetailActions(); }
function refreshDetailActions(){
  if(!$('detailOverlay').classList.contains('open')) return;
  const id = $('detailActions').querySelector('[data-add],[data-inc],[data-dec]');
  if(!id) return;
  const pid = id.dataset.add || id.dataset.inc || id.dataset.dec;
  const p = find(pid); if(!p) return;
  const q = cart[p.id] || 0;
  $('detailActions').innerHTML = !p.inStock ? '<button class="add-btn" disabled>Sold out</button>'
    : q === 0 ? '<button class="add-btn" data-add="'+p.id+'">Add to order</button>'
    : '<div class="qty-row"><button data-dec="'+p.id+'">-</button><span>'+q+'</span><button data-inc="'+p.id+'">+</button></div>';
  bind($('detailActions'));
}
const setDrawer = on => { $('overlay').classList.toggle('open', on); $('drawer').classList.toggle('open', on); };
$('cartOpenBtn').onclick = () => setDrawer(true);
$('drawerClose').onclick = $('overlay').onclick = () => setDrawer(false);

$('checkoutBtn').onclick = () => {
  const e = Object.entries(cart).filter(([id]) => find(id));
  if(!e.length){ alert('Add at least one item to your order first.'); return; }
  let msg = "Hello Shastha Guppy Farm, I'd like to order:\n\n";
  e.forEach(([id,q]) => { const p = find(id); msg += '- '+p.name+' x'+q+' = '+money(p.price*q)+'\n'; });
  msg += '\nTotal: '+money(cartTotal())+'\n\nPlease confirm availability and delivery.';
  window.open('https://wa.me/'+state.whatsapp+'?text='+encodeURIComponent(msg), '_blank');
};

/* ---------- owner-only edit mode ---------- */
let draft;
function buildDoc(s){
  const c = document.documentElement.cloneNode(true);
  ['grid','tabs','drawerItems','adminList','detailMedia','detailActions','socialBar','aboutSocial'].forEach(id => { const e = c.querySelector('#'+id); if(e) e.innerHTML = ''; });
  c.querySelector('#state').textContent = JSON.stringify(s).replace(/</g,'\\u003c');
  c.querySelectorAll('.open').forEach(e => e.classList.remove('open'));
  c.querySelector('#editBtn').setAttribute('hidden','');
  c.querySelector('#aboutText').textContent = '';
  c.querySelector('#aboutLogo').removeAttribute('src');
  c.querySelector('#adminPanel').setAttribute('hidden','');
  c.querySelector('#cartCount').textContent = '0';
  c.querySelector('#totalAmt').textContent = money(0);
  return '<!DOCTYPE html>\n' + c.outerHTML;
}
function readData(f){ return new Promise((res,rej)=>{ const r=new FileReader(); r.onload=()=>res(r.result); r.onerror=rej; r.readAsDataURL(f); }); }
async function shrink(f){
  const img = new Image(); img.src = await readData(f); await img.decode();
  const s = Math.min(1, 640/img.width), c = document.createElement('canvas');
  c.width = Math.round(img.width*s); c.height = Math.round(img.height*s);
  c.getContext('2d').drawImage(img,0,0,c.width,c.height);
  return c.toDataURL('image/jpeg',0.72);
}
function renderAdmin(){
  $('adminList').innerHTML = draft.products.map((p,i) =>
    '<div class="ad-row"><input data-f="name" data-i="'+i+'" value="'+esc(p.name)+'"><input data-f="price" data-i="'+i+'" inputmode="numeric" value="'+p.price+'"><select data-f="cat" data-i="'+i+'"><option'+(p.cat==='Guppies'?' selected':'')+'>Guppies</option><option'+(p.cat==='Food'?' selected':'')+'>Food</option></select>'
    +'<div class="full"><span>Photo: '+(p.photo?'added <button class="del" data-rmp="'+i+'">remove</button>':'<input type="file" accept="image/*" data-photo="'+i+'" style="width:auto">')+'</span></div>'
    +'<div class="full"><span>Video: '+(p.video?'added <button class="del" data-rmv="'+i+'">remove</button>':'<input type="file" accept="video/*" data-video="'+i+'" style="width:auto">')+'</span></div>'
    +'<div class="full"><label><input type="checkbox" style="width:auto" data-f="inStock" data-i="'+i+'"'+(p.inStock?' checked':'')+'> In stock</label><button class="del" data-del="'+i+'">Delete</button></div></div>').join('');
  const L = $('adminList');
  L.querySelectorAll('[data-f]').forEach(el => el.onchange = () => {
    const p = draft.products[el.dataset.i], f = el.dataset.f;
    p[f] = f==='inStock' ? el.checked : f==='price' ? (Number(el.value)||0) : el.value.trim();
  });
  L.querySelectorAll('[data-photo]').forEach(el => el.onchange = async () => { const f = el.files[0]; if(!f) return; draft.products[el.dataset.photo].photo = await shrink(f); renderAdmin(); });
  L.querySelectorAll('[data-video]').forEach(el => el.onchange = async () => {
    const f = el.files[0]; if(!f) return;
    if(f.size > 2*1048576){ alert('This video is '+(f.size/1048576).toFixed(1)+' MB. Please compress it under 2 MB first.'); el.value=''; return; }
    draft.products[el.dataset.video].video = await readData(f); renderAdmin();
  });
  L.querySelectorAll('[data-rmp]').forEach(b => b.onclick = () => { delete draft.products[b.dataset.rmp].photo; renderAdmin(); });
  L.querySelectorAll('[data-rmv]').forEach(b => b.onclick = () => { delete draft.products[b.dataset.rmv].video; renderAdmin(); });
  L.querySelectorAll('[data-del]').forEach(b => b.onclick = () => { if(confirm('Delete this item?')){ draft.products.splice(b.dataset.del,1); renderAdmin(); } });
}
const DEFAULT_ABOUT = 'Shastha Guppy Farm breeds and raises fifty plus varieties of guppies, along with the food that keeps them healthy.\n\nPick your favourites, send the order on WhatsApp, and we will confirm it with you directly.';
const ICONS = {
  whatsapp:'<svg viewBox="0 0 24 24"><path d="M3 21l1.6-4.6A9 9 0 1 1 8 19.6L3 21z"/><path d="M9 8.5c0 3 2.5 5.5 5.5 5.5l1-1.5-2-1-1 .8c-.8-.4-1.5-1.1-1.9-1.9l.8-1-1-2L9 8.5z" style="fill:currentColor;stroke:none"/></svg>',
  instagram:'<svg viewBox="0 0 24 24"><rect x="3" y="3" width="18" height="18" rx="5"/><circle cx="12" cy="12" r="4"/><circle cx="17.5" cy="6.5" r="1" style="fill:currentColor"/></svg>',
  facebook:'<svg viewBox="0 0 24 24"><path d="M14 8h3V4h-3a4 4 0 0 0-4 4v3H7v4h3v6h4v-6h3l1-4h-4V8z"/></svg>',
  youtube:'<svg viewBox="0 0 24 24"><rect x="2" y="5" width="20" height="14" rx="4"/><path d="M10 9l5 3-5 3z" style="fill:currentColor"/></svg>'
};
const normUrl = u => { u = String(u||'').trim(); return !u ? '' : (/^https?:\/\//i.test(u) ? u : 'https://' + u); };
function renderSocial(){
  const s = state.social || {};
  const items = [['whatsapp','https://wa.me/'+state.whatsapp,'WhatsApp'],['instagram',s.instagram,'Instagram'],['facebook',s.facebook,'Facebook'],['youtube',s.youtube,'YouTube']];
  const h = items.filter(x => x[1]).map(x => '<a href="'+esc(x[1])+'" target="_blank" rel="noopener" aria-label="'+x[2]+'">'+ICONS[x[0]]+'</a>').join('');
  $('socialBar').innerHTML = h; $('aboutSocial').innerHTML = h;
  $('aboutText').textContent = state.about || DEFAULT_ABOUT;
}
$('aboutClose').onclick = () => $('aboutOverlay').classList.remove('open');
$('aboutOverlay').onclick = ev => { if(ev.target === $('aboutOverlay')) $('aboutOverlay').classList.remove('open'); };
document.querySelector('.brand').onclick = () => { $('aboutLogo').src = document.querySelector('.brand img').src; $('aboutOverlay').classList.add('open'); };
const isOwnerLink = () => location.hash === '#owner';
window.addEventListener('hashchange', () => { $('editBtn').hidden = !isOwnerLink(); });

const OWNER_PASSWORD = 'shastha2026'; // change this to any password you like

function initAdmin(){
  $('editBtn').hidden = !isOwnerLink();
  $('editBtn').onclick = () => {
    if(!sessionStorage.getItem('ownerOk')){
      const pw = prompt('Enter shop owner password:');
      if(pw !== OWNER_PASSWORD){ if(pw !== null) alert('Wrong password.'); return; }
      sessionStorage.setItem('ownerOk','1');
    }
    draft = JSON.parse(JSON.stringify(state)); $('adWa').value = draft.whatsapp; const sc = draft.social || {}; $('adIg').value = sc.instagram || ''; $('adFb').value = sc.facebook || ''; $('adYt').value = sc.youtube || ''; $('adAbout').value = draft.about || DEFAULT_ABOUT; renderAdmin(); $('adminPanel').hidden = false;
  };
  $('adClose').onclick = () => { $('adminPanel').hidden = true; };
  $('adAdd').onclick = () => { draft.products.unshift({id:'n'+Date.now(), name:'New guppy (pair)', cat:'Guppies', price:0, inStock:true}); renderAdmin(); };
  $('adSave').onclick = () => {
    draft.whatsapp = $('adWa').value.replace(/\D/g,'') || draft.whatsapp;
    draft.social = {instagram: normUrl($('adIg').value), facebook: normUrl($('adFb').value), youtube: normUrl($('adYt').value)};
    draft.about = $('adAbout').value.trim();
    if(JSON.stringify(draft).length > 12e6){ alert('Too much photo/video data for one page (limit about 12 MB). Remove a few videos.'); return; }
    state = draft; PRODUCTS = state.products;
    const blob = new Blob([buildDoc(state)], {type:'text/html'});
    const url = URL.createObjectURL(blob);
    const a = document.createElement('a');
    a.href = url; a.download = 'index.html';
    document.body.appendChild(a); a.click(); a.remove();
    URL.revokeObjectURL(url);
    $('adminPanel').hidden = true;
    renderTabs(); renderAll(); renderSocial();
    alert('Saved! A file was downloaded. On GitHub, upload it, delete the old index.html, and rename the new file to index.html. The live site then updates in a minute or two.');
  };
}
initAdmin();


renderTabs(); renderAll(); renderSocial();
</script>
</body>
</html>

<html lang="en">
<head><!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Shastha Guppy Farm</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Baloo+2:wght@500;600;700&family=Karla:wght@400;500;700&display=swap" rel="stylesheet">
<style>
  :root{
    --ink:#F4E7C9;         /* warm parchment text on dark */
    --paper:#0B0906;       /* near-black, matches logo background */
    --panel:#161209;       /* slightly lifted panel over the black */
    --violet:#C79A3D;      /* muted gold, used for secondary accents */
    --magenta:#E3A83B;     /* warm amber accent */
    --gold:#D4AF37;        /* classic metallic gold, the hero accent */
    --teal:#8C6A2F;        /* deep bronze, used sparingly */
    --line:#2B2313;        /* dark bronze hairline */
    --radius:14px;
  }
  *{box-sizing:border-box;}
  html{scroll-behavior:smooth;}
  body{
    margin:0; background:var(--paper); color:var(--ink);
    font-family:'Karla',sans-serif; line-height:1.55;
    padding-bottom:env(safe-area-inset-bottom,0px);
  }
  h1,h2,h3,.brand,.tagline{font-family:'Baloo 2',sans-serif;}

  header{
    position:sticky; top:0; z-index:30; background:var(--paper);
    border-bottom:2px solid var(--line);
    padding:calc(env(safe-area-inset-top,0px) + 12px) 20px 12px;
    display:flex; align-items:center; justify-content:space-between; gap:12px;
  }
  .brand{display:flex; align-items:center; gap:10px; font-size:1.2rem; font-weight:700; color:var(--ink);}
  .brand .fin{
    width:40px;height:40px;border-radius:50%;
    object-fit:cover; flex-shrink:0; background:#000;
  }
  .cart-btn{
    background:var(--ink); color:var(--paper); border:none; border-radius:999px;
    padding:10px 18px; font-family:'Karla'; font-weight:700; font-size:.88rem;
    cursor:pointer; display:flex; align-items:center; gap:8px;
  }
  .cart-count{background:var(--gold); color:var(--ink); border-radius:999px; padding:1px 9px; font-size:.78rem; font-weight:700;}

  .hero{
    padding:52px 20px 40px; max-width:920px; margin:0 auto;
    display:flex; flex-direction:column; gap:14px;
  }
  .tagline{
    font-size:.85rem; letter-spacing:.02em; color:var(--teal); font-weight:600;
    text-transform:lowercase;
  }
  .hero h1{
    font-size:clamp(2.1rem,6vw,3.2rem); margin:0; font-weight:700; line-height:1.08;
    max-width:16ch;
  }
  .hero h1 .accent{color:var(--magenta);}
  .hero p{max-width:52ch; font-size:1.05rem; margin:2px 0 0; color:#D8C79A;}
  .tail-row{display:flex; gap:10px; margin-top:6px; font-size:1.6rem;}

  main{max-width:1000px; margin:0 auto; padding:0 20px 90px;}
  .tabs{display:flex; gap:10px; overflow-x:auto; padding:4px 0 26px;}
  .tab{
    border:2px solid var(--ink); background:transparent; color:var(--ink);
    padding:9px 18px; border-radius:999px; font-size:.9rem; font-weight:700;
    cursor:pointer; white-space:nowrap; font-family:'Karla';
  }
  .tab[aria-selected="true"]{background:var(--ink); color:var(--paper);}

  .grid{display:grid; grid-template-columns:repeat(auto-fill,minmax(220px,1fr)); gap:20px;}
  .card{
    background:var(--panel); border-radius:var(--radius); overflow:hidden;
    display:flex; flex-direction:column;
    box-shadow:0 1px 0 var(--line);
    border:1px solid var(--line);
  }
  .media{
    width:100%; aspect-ratio:4/3; background:linear-gradient(160deg,#241C0D,#171207);
    display:flex; align-items:center; justify-content:center; font-size:1.1rem; letter-spacing:.08em; color:#7A6636; font-weight:700;
    position:relative; overflow:hidden;
  }
  .media img, .media video{width:100%; height:100%; object-fit:cover;}
  .media .play-badge{
    position:absolute; bottom:8px; right:8px; background:rgba(27,16,53,.75); color:#fff;
    font-size:.7rem; padding:3px 8px; border-radius:999px; font-weight:700;
  }
  .card-body{padding:14px 14px 16px; display:flex; flex-direction:column; gap:6px; flex:1;}
  .card-body .cat{font-size:.72rem; font-weight:700; color:var(--violet); text-transform:lowercase;}
  .card-body h3{margin:0; font-size:1.05rem; font-weight:600; color:var(--ink);}
  .card-body .price{font-weight:700; margin-top:auto; font-size:1.05rem;}
  .qty-row{display:flex; align-items:center; gap:10px; margin-top:4px;}
  .qty-row button{
    width:30px; height:30px; border-radius:8px; border:2px solid var(--ink);
    background:var(--paper); color:var(--ink); font-size:1rem; cursor:pointer; font-weight:700;
  }
  .add-btn{
    background:var(--violet); color:#fff; border:none; border-radius:8px;
    padding:10px; font-weight:700; cursor:pointer; font-family:'Karla'; font-size:.92rem;
    margin-top:4px;
  }
  .add-btn:active{background:var(--magenta);}

  .overlay{position:fixed; inset:0; background:rgba(27,16,53,.45); z-index:40; display:none;}
  .overlay.open{display:block;}
  .drawer{
    position:fixed; top:0; right:0; bottom:0; width:min(400px,92vw);
    background:var(--panel); z-index:41; transform:translateX(105%);
    transition:transform .25s ease; display:flex; flex-direction:column;
    padding-top:env(safe-area-inset-top,0px); padding-bottom:env(safe-area-inset-bottom,0px);
  }
  .drawer.open{transform:translateX(0);}
  .drawer-head{padding:18px 20px; border-bottom:2px solid var(--line); display:flex; justify-content:space-between; align-items:center;}
  .drawer-head h2{margin:0; font-size:1.25rem;}
  .drawer-head button{background:none; border:none; font-size:1.3rem; cursor:pointer; color:var(--ink);}
  .drawer-items{flex:1; overflow-y:auto; padding:14px 20px;}
  .line{display:flex; justify-content:space-between; align-items:center; gap:8px; padding:12px 0; border-bottom:1px solid var(--line);}
  .line-name{font-size:.92rem; font-weight:600;}
  .line-qty{display:flex; align-items:center; gap:6px;}
  .line-qty button{width:26px;height:26px;border-radius:6px;border:2px solid var(--ink);background:var(--paper);cursor:pointer;font-weight:700;}
  .drawer-foot{padding:18px 20px; border-top:2px solid var(--line);}
  .total-row{display:flex; justify-content:space-between; font-weight:700; margin-bottom:14px; font-size:1.1rem;}
  .checkout-btn{
    width:100%; background:#25D366; color:#062A16; border:none; border-radius:10px;
    padding:14px; font-weight:700; font-size:1rem; cursor:pointer; font-family:'Karla';
    display:flex; align-items:center; justify-content:center; gap:8px;
  }
  .empty-note{color:var(--violet); opacity:.85; font-size:.92rem; padding:24px 0; text-align:center;}
  footer{text-align:center; padding:26px 20px 40px; font-size:.82rem; opacity:.6;}

  .add-btn[disabled]{background:#3a3220;color:#8a7a52;cursor:not-allowed;}
  #adminPanel{position:fixed;inset:0;z-index:60;background:var(--paper);overflow-y:auto;padding:calc(env(safe-area-inset-top,0px) + 16px) 16px 60px;}
  #adminPanel[hidden]{display:none;}
  .ad-head{display:flex;justify-content:space-between;align-items:center;gap:8px;flex-wrap:wrap;}
  .ad-head h2{margin:0;}
  .ad-save,.ad-x,.ad-add{border:none;border-radius:8px;padding:10px 14px;font-weight:700;cursor:pointer;font-family:'Karla';}
  .ad-save{background:var(--gold);color:#0B0906;} .ad-x{background:var(--line);color:var(--ink);}
  .ad-add{background:var(--panel);color:var(--gold);border:2px dashed var(--gold);width:100%;margin-top:14px;}
  .ad-note{font-size:.85rem;opacity:.75;}
  .ad-wa{display:block;font-size:.85rem;margin:8px 0 14px;}
  .ad-wa input,.ad-row input,.ad-row select{background:var(--panel);color:var(--ink);border:1px solid var(--line);border-radius:6px;padding:8px;font-family:'Karla';font-size:.9rem;width:100%;}
  .ad-row{display:grid;grid-template-columns:2fr 1fr 1fr;gap:6px;background:var(--panel);border:1px solid var(--line);border-radius:10px;padding:10px;margin-bottom:8px;}
  .ad-row .full{grid-column:1/-1;display:flex;justify-content:space-between;align-items:center;font-size:.85rem;}
  .ad-row .del{background:none;border:none;color:#e0705a;font-weight:700;cursor:pointer;}

  /* ---------- product detail popup ---------- */
  .card{cursor:pointer;}
  .detail-overlay{
    position:fixed; inset:0; background:rgba(0,0,0,.72); z-index:60;
    display:flex; align-items:flex-end; justify-content:center;
    opacity:0; pointer-events:none; transition:opacity .28s ease;
  }
  .detail-overlay.open{opacity:1; pointer-events:auto;}
  @media (min-width:720px){ .detail-overlay{align-items:center;} }
  .detail-card{
    background:var(--panel); border:2px solid var(--line); border-radius:20px 20px 0 0;
    width:100%; max-width:560px; max-height:88vh; overflow-y:auto;
    padding:0 0 26px; position:relative;
    transform:translateY(28px) scale(.97); opacity:0;
    transition:transform .32s cubic-bezier(.2,.9,.25,1.1), opacity .28s ease;
  }
  .detail-overlay.open .detail-card{transform:translateY(0) scale(1); opacity:1;}
  @media (min-width:720px){ .detail-card{border-radius:20px;} }
  .detail-close{
    position:absolute; top:14px; right:14px; z-index:2;
    background:rgba(11,9,6,.75); color:var(--ink); border:1px solid var(--line);
    border-radius:999px; width:36px; height:36px; font-size:1.1rem; cursor:pointer;
  }
  .detail-media{width:100%; aspect-ratio:1/1; background:#000; overflow:hidden; border-radius:20px 20px 0 0;}
  .detail-media img, .detail-media video{width:100%; height:100%; object-fit:cover; display:block;
    animation:detailZoom .5s ease;}
  @keyframes detailZoom{from{transform:scale(1.08); opacity:.4;} to{transform:scale(1); opacity:1;}}
  .detail-media .media{height:100%; border-radius:0;}
  .detail-body{padding:20px 22px 4px;}
  .detail-body .cat{display:block; margin-bottom:4px;}
  .detail-body h2{margin:2px 0 8px; font-size:1.5rem;}
  .detail-body .price{font-size:1.2rem; font-weight:700; color:var(--gold); display:block; margin-bottom:16px;}
  .detail-actions{display:flex; gap:10px;}
</style>
</head>
<body>

<header>
  <div class="brand"><img class="fin" src="data:image/jpeg;base64,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" alt="Shastha Guppy Farm logo">Shastha Guppy Farm</div>
  <button class="cart-btn" id="editBtn" hidden style="background:var(--gold);color:#0B0906;margin-left:auto">Edit shop</button>
  <button class="cart-btn" id="cartOpenBtn">Order <span class="cart-count" id="cartCount">0</span></button>
</header>

<div class="hero">
  <div class="tagline">fifty plus guppy varieties, bred and raised here</div>
  <h1>Colour that <span class="accent">swims</span></h1>
  <p>Live guppies in every colour and tail shape we raise, plus the food that keeps them thriving. Pick your favourites and send the order straight to us on WhatsApp.</p>
</div>

<main>
  <div class="tabs" id="tabs"></div>
  <div class="grid" id="grid"></div>
</main>

<footer>Shastha Guppy Farm &mdash; orders confirmed over WhatsApp.</footer>


<section id="adminPanel" hidden>
  <div class="ad-head"><h2>Edit shop</h2><div><button id="adSave" class="ad-save">Save changes</button> <button id="adClose" class="ad-x">Close</button></div></div>
  <p class="ad-note">Only you see this screen. Changes go live for all customers after you press Save.</p>
  <label class="ad-wa">WhatsApp number (country code first, no + or spaces)<input id="adWa" inputmode="numeric"></label>
  <div id="adminList"></div>
  <button id="adAdd" class="ad-add">+ Add new item</button>
</section>
<div class="overlay" id="overlay"></div>
<aside class="drawer" id="drawer">
  <div class="drawer-head"><h2>Your order</h2><button id="drawerClose" aria-label="Close">X</button></div>
  <div class="drawer-items" id="drawerItems"></div>
  <div class="drawer-foot">
    <div class="total-row"><span>Total</span><span id="totalAmt">Rs. 0</span></div>
    <button class="checkout-btn" id="checkoutBtn">Send order on WhatsApp</button>
  </div>
</aside>

<div class="detail-overlay" id="detailOverlay">
  <div class="detail-card" id="detailCard">
    <button class="detail-close" id="detailClose" aria-label="Close">X</button>
    <div class="detail-media" id="detailMedia"></div>
    <div class="detail-body">
      <span class="cat" id="detailCat"></span>
      <h2 id="detailName"></h2>
      <span class="price" id="detailPrice"></span>
      <div class="detail-actions" id="detailActions"></div>
    </div>
  </div>
</div>

<script type="application/json" id="state">{"whatsapp": "918088820799", "products": [{"id": "g1", "name": "Albino Platinum White Guppy (pair)", "cat": "Guppies", "price": 300, "inStock": true}, {"id": "g2", "name": "Albino Redlace Guppy (pair)", "cat": "Guppies", "price": 250, "inStock": true}, {"id": "g3", "name": "Albino Silvarado Red Ear Guppy (pair)", "cat": "Guppies", "price": 240, "inStock": true}, {"id": "g4", "name": "AFR Guppy (pair)", "cat": "Guppies", "price": 230, "inStock": true}, {"id": "g5", "name": "Masco Blue Guppy (pair)", "cat": "Guppies", "price": 220, "inStock": true}, {"id": "g6", "name": "Black Guppy (pair)", "cat": "Guppies", "price": 180, "inStock": true}, {"id": "g7", "name": "Platinum White Dumbo Guppy (pair)", "cat": "Guppies", "price": 450, "inStock": true}, {"id": "g8", "name": "Silvarado Mosaic Guppy (pair)", "cat": "Guppies", "price": 180, "inStock": true}, {"id": "g9", "name": "White Texido Guppy (pair)", "cat": "Guppies", "price": 180, "inStock": true}, {"id": "g10", "name": "Japanese Blue Guppy (pair)", "cat": "Guppies", "price": 250, "inStock": true}, {"id": "g11", "name": "Platinum Big Ear Guppy (pair)", "cat": "Guppies", "price": 250, "inStock": true}, {"id": "g12", "name": "Chilli Mosaic Dumbo Guppy (pair)", "cat": "Guppies", "price": 205, "inStock": true}, {"id": "g13", "name": "Gold Guppy (pair)", "cat": "Guppies", "price": 250, "inStock": true}, {"id": "g14", "name": "Gold Ribbon Guppy (pair)", "cat": "Guppies", "price": 500, "inStock": true}, {"id": "g15", "name": "Red Granite Guppy (pair)", "cat": "Guppies", "price": 215, "inStock": true}, {"id": "g16", "name": "Blue Panda Guppy (pair)", "cat": "Guppies", "price": 230, "inStock": true}, {"id": "g17", "name": "Purple Burry Guppy (pair)", "cat": "Guppies", "price": 250, "inStock": true}, {"id": "g18", "name": "Tiger HM Guppy (pair)", "cat": "Guppies", "price": 180, "inStock": true}, {"id": "g19", "name": "Yellow Pingu Guppy (pair)", "cat": "Guppies", "price": 215, "inStock": true}, {"id": "g20", "name": "Lazuli Blue Guppy (pair)", "cat": "Guppies", "price": 190, "inStock": true}, {"id": "g21", "name": "Black Bar Endler Guppy (pair)", "cat": "Guppies", "price": 200, "inStock": true}, {"id": "g22", "name": "Red Scarlet Endler Guppy (pair)", "cat": "Guppies", "price": 200, "inStock": true}, {"id": "g23", "name": "Ivory Purple Guppy (pair)", "cat": "Guppies", "price": 250, "inStock": true}, {"id": "g24", "name": "Red Coral Endler Guppy (pair)", "cat": "Guppies", "price": 250, "inStock": true}, {"id": "g25", "name": "Zee Through Koi Guppy (pair)", "cat": "Guppies", "price": 250, "inStock": true}, {"id": "g26", "name": "Santha Clause SB Guppy (pair)", "cat": "Guppies", "price": 400, "inStock": true}, {"id": "g27", "name": "Wildred Guppy (pair)", "cat": "Guppies", "price": 210, "inStock": true}, {"id": "g28", "name": "Albino Metal Redlace Guppy (pair)", "cat": "Guppies", "price": 230, "inStock": true}, {"id": "g29", "name": "Red Dragon HM Guppy (pair)", "cat": "Guppies", "price": 250, "inStock": true}, {"id": "f1", "name": "Guppy Flake Food 100g", "cat": "Food", "price": 120, "inStock": true}, {"id": "f2", "name": "Live Daphnia Culture", "cat": "Food", "price": 80, "inStock": true}, {"id": "f3", "name": "Baby Guppy Fry Food", "cat": "Food", "price": 100, "inStock": true}]}</script>
<script>
let state = JSON.parse(document.getElementById('state').textContent);
let PRODUCTS = state.products;
const CATS = ['All','Guppies','Food'];
let cart = {}, activeCat = 'All';
const $ = id => document.getElementById(id);
const money = n => '\u20b9' + Number(n).toLocaleString('en-IN');
const esc = s => String(s).replace(/[&<>"']/g, c => ({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'}[c]));
const find = id => PRODUCTS.find(p => p.id === id);

function renderTabs(){
  $('tabs').innerHTML = '';
  CATS.forEach(c => {
    const b = document.createElement('button');
    b.className = 'tab'; b.textContent = c;
    b.setAttribute('aria-selected', c === activeCat ? 'true' : 'false');
    b.onclick = () => { activeCat = c; renderTabs(); renderGrid(); };
    $('tabs').appendChild(b);
  });
}
function mediaHtml(p){
  if(p.video) return '<div class="media"><video src="'+p.video+'" '+(p.photo?'poster="'+p.photo+'" ':'')+'controls preload="none" playsinline></video></div>';
  if(p.photo) return '<div class="media"><img src="'+p.photo+'" alt="'+esc(p.name)+'" loading="lazy"></div>';
  return '<div class="media">'+(p.cat==='Guppies'?'GUPPY':'FOOD')+'</div>';
}
function renderGrid(){
  const grid = $('grid'); grid.innerHTML = '';
  PRODUCTS.filter(p => activeCat === 'All' || p.cat === activeCat).forEach(p => {
    const q = cart[p.id] || 0;
    const action = !p.inStock ? '<button class="add-btn" disabled>Sold out</button>'
      : q === 0 ? '<button class="add-btn" data-add="'+p.id+'">Add to order</button>'
      : '<div class="qty-row"><button data-dec="'+p.id+'">-</button><span>'+q+'</span><button data-inc="'+p.id+'">+</button></div>';
    const card = document.createElement('div'); card.className = 'card';
    card.innerHTML = mediaHtml(p)+'<div class="card-body"><span class="cat">'+esc(p.cat)+'</span><h3>'+esc(p.name)+'</h3><span class="price">'+money(p.price)+'</span>'+action+'</div>';
    card.addEventListener('click', (ev) => { if(ev.target.closest('button')) return; openDetail(p.id); });
    grid.appendChild(card);
  });
  bind(grid);
}

function openDetail(id){
  const p = find(id); if(!p) return;
  $('detailMedia').innerHTML = mediaHtml(p);
  const vid = $('detailMedia').querySelector('video');
  if(vid){ vid.muted = true; vid.autoplay = true; vid.loop = true; vid.play().catch(()=>{}); }
  $('detailCat').textContent = p.cat;
  $('detailName').textContent = p.name;
  $('detailPrice').textContent = money(p.price);
  const q = cart[p.id] || 0;
  $('detailActions').innerHTML = !p.inStock ? '<button class="add-btn" disabled>Sold out</button>'
    : q === 0 ? '<button class="add-btn" data-add="'+p.id+'">Add to order</button>'
    : '<div class="qty-row"><button data-dec="'+p.id+'">-</button><span>'+q+'</span><button data-inc="'+p.id+'">+</button></div>';
  bind($('detailActions'));
  $('detailOverlay').classList.add('open');
}
function closeDetail(){ $('detailOverlay').classList.remove('open'); }
$('detailClose').onclick = closeDetail;
$('detailOverlay').onclick = (ev) => { if(ev.target === $('detailOverlay')) closeDetail(); };
function bind(root){
  root.querySelectorAll('[data-add]').forEach(b => b.onclick = () => { cart[b.dataset.add] = 1; renderAll(); });
  root.querySelectorAll('[data-inc]').forEach(b => b.onclick = () => { cart[b.dataset.inc]++; renderAll(); });
  root.querySelectorAll('[data-dec]').forEach(b => b.onclick = () => { const id = b.dataset.dec; if(--cart[id] <= 0) delete cart[id]; renderAll(); });
}
const cartTotal = () => Object.entries(cart).reduce((s,[id,q]) => s + (find(id)?.price||0)*q, 0);
const cartCount = () => Object.values(cart).reduce((a,b) => a+b, 0);
function renderDrawer(){
  $('cartCount').textContent = cartCount();
  const w = $('drawerItems'), e = Object.entries(cart).filter(([id]) => find(id));
  w.innerHTML = e.length ? e.map(([id,q]) => { const p = find(id);
    return '<div class="line"><div><div class="line-name">'+esc(p.name)+'</div><div style="font-size:.82rem;opacity:.65">'+money(p.price)+' x '+q+'</div></div><div class="line-qty"><button data-dec="'+id+'">-</button><span>'+q+'</span><button data-inc="'+id+'">+</button></div></div>'; }).join('')
    : '<p class="empty-note">Your order is empty.<br>Add guppies or food from the catalog.</p>';
  bind(w);
  $('totalAmt').textContent = money(cartTotal());
}
function renderAll(){ renderGrid(); renderDrawer(); refreshDetailActions(); }
function refreshDetailActions(){
  if(!$('detailOverlay').classList.contains('open')) return;
  const id = $('detailActions').querySelector('[data-add],[data-inc],[data-dec]');
  if(!id) return;
  const pid = id.dataset.add || id.dataset.inc || id.dataset.dec;
  const p = find(pid); if(!p) return;
  const q = cart[p.id] || 0;
  $('detailActions').innerHTML = !p.inStock ? '<button class="add-btn" disabled>Sold out</button>'
    : q === 0 ? '<button class="add-btn" data-add="'+p.id+'">Add to order</button>'
    : '<div class="qty-row"><button data-dec="'+p.id+'">-</button><span>'+q+'</span><button data-inc="'+p.id+'">+</button></div>';
  bind($('detailActions'));
}
const setDrawer = on => { $('overlay').classList.toggle('open', on); $('drawer').classList.toggle('open', on); };
$('cartOpenBtn').onclick = () => setDrawer(true);
$('drawerClose').onclick = $('overlay').onclick = () => setDrawer(false);

$('checkoutBtn').onclick = () => {
  const e = Object.entries(cart).filter(([id]) => find(id));
  if(!e.length){ alert('Add at least one item to your order first.'); return; }
  let msg = "Hello Shastha Guppy Farm, I'd like to order:\n\n";
  e.forEach(([id,q]) => { const p = find(id); msg += '- '+p.name+' x'+q+' = '+money(p.price*q)+'\n'; });
  msg += '\nTotal: '+money(cartTotal())+'\n\nPlease confirm availability and delivery.';
  window.open('https://wa.me/'+state.whatsapp+'?text='+encodeURIComponent(msg), '_blank');
};

/* ---------- owner-only edit mode ---------- */
let draft;
function buildDoc(s){
  const c = document.documentElement.cloneNode(true);
  ['grid','tabs','drawerItems','adminList','detailMedia','detailActions'].forEach(id => { const e = c.querySelector('#'+id); if(e) e.innerHTML = ''; });
  c.querySelector('#state').textContent = JSON.stringify(s).replace(/</g,'\\u003c');
  c.querySelectorAll('.open').forEach(e => e.classList.remove('open'));
  c.querySelector('#editBtn').setAttribute('hidden','');
  c.querySelector('#adminPanel').setAttribute('hidden','');
  c.querySelector('#cartCount').textContent = '0';
  c.querySelector('#totalAmt').textContent = money(0);
  return '<!DOCTYPE html>\n' + c.outerHTML;
}
function readData(f){ return new Promise((res,rej)=>{ const r=new FileReader(); r.onload=()=>res(r.result); r.onerror=rej; r.readAsDataURL(f); }); }
async function shrink(f){
  const img = new Image(); img.src = await readData(f); await img.decode();
  const s = Math.min(1, 640/img.width), c = document.createElement('canvas');
  c.width = Math.round(img.width*s); c.height = Math.round(img.height*s);
  c.getContext('2d').drawImage(img,0,0,c.width,c.height);
  return c.toDataURL('image/jpeg',0.72);
}
function renderAdmin(){
  $('adminList').innerHTML = draft.products.map((p,i) =>
    '<div class="ad-row"><input data-f="name" data-i="'+i+'" value="'+esc(p.name)+'"><input data-f="price" data-i="'+i+'" inputmode="numeric" value="'+p.price+'"><select data-f="cat" data-i="'+i+'"><option'+(p.cat==='Guppies'?' selected':'')+'>Guppies</option><option'+(p.cat==='Food'?' selected':'')+'>Food</option></select>'
    +'<div class="full"><span>Photo: '+(p.photo?'added <button class="del" data-rmp="'+i+'">remove</button>':'<input type="file" accept="image/*" data-photo="'+i+'" style="width:auto">')+'</span></div>'
    +'<div class="full"><span>Video: '+(p.video?'added <button class="del" data-rmv="'+i+'">remove</button>':'<input type="file" accept="video/*" data-video="'+i+'" style="width:auto">')+'</span></div>'
    +'<div class="full"><label><input type="checkbox" style="width:auto" data-f="inStock" data-i="'+i+'"'+(p.inStock?' checked':'')+'> In stock</label><button class="del" data-del="'+i+'">Delete</button></div></div>').join('');
  const L = $('adminList');
  L.querySelectorAll('[data-f]').forEach(el => el.onchange = () => {
    const p = draft.products[el.dataset.i], f = el.dataset.f;
    p[f] = f==='inStock' ? el.checked : f==='price' ? (Number(el.value)||0) : el.value.trim();
  });
  L.querySelectorAll('[data-photo]').forEach(el => el.onchange = async () => { const f = el.files[0]; if(!f) return; draft.products[el.dataset.photo].photo = await shrink(f); renderAdmin(); });
  L.querySelectorAll('[data-video]').forEach(el => el.onchange = async () => {
    const f = el.files[0]; if(!f) return;
    if(f.size > 2*1048576){ alert('This video is '+(f.size/1048576).toFixed(1)+' MB. Please compress it under 2 MB first.'); el.value=''; return; }
    draft.products[el.dataset.video].video = await readData(f); renderAdmin();
  });
  L.querySelectorAll('[data-rmp]').forEach(b => b.onclick = () => { delete draft.products[b.dataset.rmp].photo; renderAdmin(); });
  L.querySelectorAll('[data-rmv]').forEach(b => b.onclick = () => { delete draft.products[b.dataset.rmv].video; renderAdmin(); });
  L.querySelectorAll('[data-del]').forEach(b => b.onclick = () => { if(confirm('Delete this item?')){ draft.products.splice(b.dataset.del,1); renderAdmin(); } });
}
const OWNER_PASSWORD = 'shastha2026'; // change this to any password you like

function initAdmin(){
  $('editBtn').hidden = false;
  $('editBtn').onclick = () => {
    if(!sessionStorage.getItem('ownerOk')){
      const pw = prompt('Enter shop owner password:');
      if(pw !== OWNER_PASSWORD){ if(pw !== null) alert('Wrong password.'); return; }
      sessionStorage.setItem('ownerOk','1');
    }
    draft = JSON.parse(JSON.stringify(state)); $('adWa').value = draft.whatsapp; renderAdmin(); $('adminPanel').hidden = false;
  };
  $('adClose').onclick = () => { $('adminPanel').hidden = true; };
  $('adAdd').onclick = () => { draft.products.unshift({id:'n'+Date.now(), name:'New guppy (pair)', cat:'Guppies', price:0, inStock:true}); renderAdmin(); };
  $('adSave').onclick = () => {
    draft.whatsapp = $('adWa').value.replace(/\D/g,'') || draft.whatsapp;
    if(JSON.stringify(draft).length > 12e6){ alert('Too much photo/video data for one page (limit about 12 MB). Remove a few videos.'); return; }
    state = draft;
    localStorage.setItem('shasthaState', JSON.stringify(state));
    const blob = new Blob([buildDoc(state)], {type:'text/html'});
    const url = URL.createObjectURL(blob);
    const a = document.createElement('a');
    a.href = url; a.download = 'index.html';
    document.body.appendChild(a); a.click(); a.remove();
    URL.revokeObjectURL(url);
    $('adminPanel').hidden = true;
    renderTabs(); renderAll();
    alert('Saved! A file named index.html was downloaded. Upload it to your GitHub repository (replacing the old one) to publish these changes live. Your changes are also kept in this browser for now.');
  };
}
initAdmin();

(() => {
  try {
    const saved = localStorage.getItem('shasthaState');
    if(saved){ state = JSON.parse(saved); }
  } catch(e){}
})();

renderTabs(); renderAll();
</script>
</body>
</html>

<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Shastha Guppy Farm</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Baloo+2:wght@500;600;700&family=Karla:wght@400;500;700&display=swap" rel="stylesheet">
<style>
  :root{
    --ink:#F4E7C9;         /* warm parchment text on dark */
    --paper:#0B0906;       /* near-black, matches logo background */
    --panel:#161209;       /* slightly lifted panel over the black */
    --violet:#C79A3D;      /* muted gold, used for secondary accents */
    --magenta:#E3A83B;     /* warm amber accent */
    --gold:#D4AF37;        /* classic metallic gold, the hero accent */
    --teal:#8C6A2F;        /* deep bronze, used sparingly */
    --line:#2B2313;        /* dark bronze hairline */
    --radius:14px;
  }
  *{box-sizing:border-box;}
  html{scroll-behavior:smooth;}
  body{
    margin:0; background:var(--paper); color:var(--ink);
    font-family:'Karla',sans-serif; line-height:1.55;
    padding-bottom:env(safe-area-inset-bottom,0px);
  }
  h1,h2,h3,.brand,.tagline{font-family:'Baloo 2',sans-serif;}

  header{
    position:sticky; top:0; z-index:30; background:var(--paper);
    border-bottom:2px solid var(--line);
    padding:calc(env(safe-area-inset-top,0px) + 12px) 20px 12px;
    display:flex; align-items:center; justify-content:space-between; gap:12px;
  }
  .brand{display:flex; align-items:center; gap:10px; font-size:1.2rem; font-weight:700; color:var(--ink);}
  .brand .fin{
    width:40px;height:40px;border-radius:50%;
    object-fit:cover; flex-shrink:0; background:#000;
  }
  .cart-btn{
    background:var(--ink); color:var(--paper); border:none; border-radius:999px;
    padding:10px 18px; font-family:'Karla'; font-weight:700; font-size:.88rem;
    cursor:pointer; display:flex; align-items:center; gap:8px;
  }
  .cart-count{background:var(--gold); color:var(--ink); border-radius:999px; padding:1px 9px; font-size:.78rem; font-weight:700;}

  .hero{
    padding:52px 20px 40px; max-width:920px; margin:0 auto;
    display:flex; flex-direction:column; gap:14px;
  }
  .tagline{
    font-size:.85rem; letter-spacing:.02em; color:var(--teal); font-weight:600;
    text-transform:lowercase;
  }
  .hero h1{
    font-size:clamp(2.1rem,6vw,3.2rem); margin:0; font-weight:700; line-height:1.08;
    max-width:16ch;
  }
  .hero h1 .accent{color:var(--magenta);}
  .hero p{max-width:52ch; font-size:1.05rem; margin:2px 0 0; color:#D8C79A;}
  .tail-row{display:flex; gap:10px; margin-top:6px; font-size:1.6rem;}

  main{max-width:1000px; margin:0 auto; padding:0 20px 90px;}
  .tabs{display:flex; gap:10px; overflow-x:auto; padding:4px 0 26px;}
  .tab{
    border:2px solid var(--ink); background:transparent; color:var(--ink);
    padding:9px 18px; border-radius:999px; font-size:.9rem; font-weight:700;
    cursor:pointer; white-space:nowrap; font-family:'Karla';
  }
  .tab[aria-selected="true"]{background:var(--ink); color:var(--paper);}

  .grid{display:grid; grid-template-columns:repeat(auto-fill,minmax(220px,1fr)); gap:20px;}
  .card{
    background:var(--panel); border-radius:var(--radius); overflow:hidden;
    display:flex; flex-direction:column;
    box-shadow:0 1px 0 var(--line);
    border:1px solid var(--line);
  }
  .media{
    width:100%; aspect-ratio:4/3; background:linear-gradient(160deg,#241C0D,#171207);
    display:flex; align-items:center; justify-content:center; font-size:1.1rem; letter-spacing:.08em; color:#7A6636; font-weight:700;
    position:relative; overflow:hidden;
  }
  .media img, .media video{width:100%; height:100%; object-fit:cover;}
  .media .play-badge{
    position:absolute; bottom:8px; right:8px; background:rgba(27,16,53,.75); color:#fff;
    font-size:.7rem; padding:3px 8px; border-radius:999px; font-weight:700;
  }
  .card-body{padding:14px 14px 16px; display:flex; flex-direction:column; gap:6px; flex:1;}
  .card-body .cat{font-size:.72rem; font-weight:700; color:var(--violet); text-transform:lowercase;}
  .card-body h3{margin:0; font-size:1.05rem; font-weight:600; color:var(--ink);}
  .card-body .price{font-weight:700; margin-top:auto; font-size:1.05rem;}
  .qty-row{display:flex; align-items:center; gap:10px; margin-top:4px;}
  .qty-row button{
    width:30px; height:30px; border-radius:8px; border:2px solid var(--ink);
    background:var(--paper); color:var(--ink); font-size:1rem; cursor:pointer; font-weight:700;
  }
  .add-btn{
    background:var(--violet); color:#fff; border:none; border-radius:8px;
    padding:10px; font-weight:700; cursor:pointer; font-family:'Karla'; font-size:.92rem;
    margin-top:4px;
  }
  .add-btn:active{background:var(--magenta);}

  .overlay{position:fixed; inset:0; background:rgba(27,16,53,.45); z-index:40; display:none;}
  .overlay.open{display:block;}
  .drawer{
    position:fixed; top:0; right:0; bottom:0; width:min(400px,92vw);
    background:var(--panel); z-index:41; transform:translateX(105%);
    transition:transform .25s ease; display:flex; flex-direction:column;
    padding-top:env(safe-area-inset-top,0px); padding-bottom:env(safe-area-inset-bottom,0px);
  }
  .drawer.open{transform:translateX(0);}
  .drawer-head{padding:18px 20px; border-bottom:2px solid var(--line); display:flex; justify-content:space-between; align-items:center;}
  .drawer-head h2{margin:0; font-size:1.25rem;}
  .drawer-head button{background:none; border:none; font-size:1.3rem; cursor:pointer; color:var(--ink);}
  .drawer-items{flex:1; overflow-y:auto; padding:14px 20px;}
  .line{display:flex; justify-content:space-between; align-items:center; gap:8px; padding:12px 0; border-bottom:1px solid var(--line);}
  .line-name{font-size:.92rem; font-weight:600;}
  .line-qty{display:flex; align-items:center; gap:6px;}
  .line-qty button{width:26px;height:26px;border-radius:6px;border:2px solid var(--ink);background:var(--paper);cursor:pointer;font-weight:700;}
  .drawer-foot{padding:18px 20px; border-top:2px solid var(--line);}
  .total-row{display:flex; justify-content:space-between; font-weight:700; margin-bottom:14px; font-size:1.1rem;}
  .checkout-btn{
    width:100%; background:#25D366; color:#062A16; border:none; border-radius:10px;
    padding:14px; font-weight:700; font-size:1rem; cursor:pointer; font-family:'Karla';
    display:flex; align-items:center; justify-content:center; gap:8px;
  }
  .empty-note{color:var(--violet); opacity:.85; font-size:.92rem; padding:24px 0; text-align:center;}
  footer{text-align:center; padding:26px 20px 40px; font-size:.82rem; opacity:.6;}

  .add-btn[disabled]{background:#3a3220;color:#8a7a52;cursor:not-allowed;}
  #adminPanel{position:fixed;inset:0;z-index:60;background:var(--paper);overflow-y:auto;padding:calc(env(safe-area-inset-top,0px) + 16px) 16px 60px;}
  #adminPanel[hidden]{display:none;}
  .ad-head{display:flex;justify-content:space-between;align-items:center;gap:8px;flex-wrap:wrap;}
  .ad-head h2{margin:0;}
  .ad-save,.ad-x,.ad-add{border:none;border-radius:8px;padding:10px 14px;font-weight:700;cursor:pointer;font-family:'Karla';}
  .ad-save{background:var(--gold);color:#0B0906;} .ad-x{background:var(--line);color:var(--ink);}
  .ad-add{background:var(--panel);color:var(--gold);border:2px dashed var(--gold);width:100%;margin-top:14px;}
  .ad-note{font-size:.85rem;opacity:.75;}
  .ad-wa{display:block;font-size:.85rem;margin:8px 0 14px;}
  .ad-wa input,.ad-row input,.ad-row select{background:var(--panel);color:var(--ink);border:1px solid var(--line);border-radius:6px;padding:8px;font-family:'Karla';font-size:.9rem;width:100%;}
  .ad-row{display:grid;grid-template-columns:2fr 1fr 1fr;gap:6px;background:var(--panel);border:1px solid var(--line);border-radius:10px;padding:10px;margin-bottom:8px;}
  .ad-row .full{grid-column:1/-1;display:flex;justify-content:space-between;align-items:center;font-size:.85rem;}
  .ad-row .del{background:none;border:none;color:#e0705a;font-weight:700;cursor:pointer;}

  /* ---------- product detail popup ---------- */
  .card{cursor:pointer;}
  .detail-overlay{
    position:fixed; inset:0; background:rgba(0,0,0,.72); z-index:60;
    display:flex; align-items:flex-end; justify-content:center;
    opacity:0; pointer-events:none; transition:opacity .28s ease;
  }
  .detail-overlay.open{opacity:1; pointer-events:auto;}
  @media (min-width:720px){ .detail-overlay{align-items:center;} }
  .detail-card{
    background:var(--panel); border:2px solid var(--line); border-radius:20px 20px 0 0;
    width:100%; max-width:560px; max-height:88vh; overflow-y:auto;
    padding:0 0 26px; position:relative;
    transform:translateY(28px) scale(.97); opacity:0;
    transition:transform .32s cubic-bezier(.2,.9,.25,1.1), opacity .28s ease;
  }
  .detail-overlay.open .detail-card{transform:translateY(0) scale(1); opacity:1;}
  @media (min-width:720px){ .detail-card{border-radius:20px;} }
  .detail-close{
    position:absolute; top:14px; right:14px; z-index:2;
    background:rgba(11,9,6,.75); color:var(--ink); border:1px solid var(--line);
    border-radius:999px; width:36px; height:36px; font-size:1.1rem; cursor:pointer;
  }
  .detail-media{width:100%; aspect-ratio:1/1; background:#000; overflow:hidden; border-radius:20px 20px 0 0;}
  .detail-media img, .detail-media video{width:100%; height:100%; object-fit:cover; display:block;
    animation:detailZoom .5s ease;}
  @keyframes detailZoom{from{transform:scale(1.08); opacity:.4;} to{transform:scale(1); opacity:1;}}
  .detail-media .media{height:100%; border-radius:0;}
  .detail-body{padding:20px 22px 4px;}
  .detail-body .cat{display:block; margin-bottom:4px;}
  .detail-body h2{margin:2px 0 8px; font-size:1.5rem;}
  .detail-body .price{font-size:1.2rem; font-weight:700; color:var(--gold); display:block; margin-bottom:16px;}
  .detail-actions{display:flex; gap:10px;}
</style>
</head>
<body>

<header>
  <div class="brand"><img class="fin" src="data:image/jpeg;base64,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" alt="Shastha Guppy Farm logo">Shastha Guppy Farm</div>
  <button class="cart-btn" id="editBtn" hidden style="background:var(--gold);color:#0B0906;margin-left:auto">Edit shop</button>
  <button class="cart-btn" id="cartOpenBtn">Order <span class="cart-count" id="cartCount">0</span></button>
</header>

<div class="hero">
  <div class="tagline">fifty plus guppy varieties, bred and raised here</div>
  <h1>Colour that <span class="accent">swims</span></h1>
  <p>Live guppies in every colour and tail shape we raise, plus the food that keeps them thriving. Pick your favourites and send the order straight to us on WhatsApp.</p>
</div>

<main>
  <div class="tabs" id="tabs"></div>
  <div class="grid" id="grid"></div>
</main>

<footer>Shastha Guppy Farm &mdash; orders confirmed over WhatsApp.</footer>


<section id="adminPanel" hidden>
  <div class="ad-head"><h2>Edit shop</h2><div><button id="adSave" class="ad-save">Save changes</button> <button id="adClose" class="ad-x">Close</button></div></div>
  <p class="ad-note">Only you see this screen. Changes go live for all customers after you press Save.</p>
  <label class="ad-wa">WhatsApp number (country code first, no + or spaces)<input id="adWa" inputmode="numeric"></label>
  <div id="adminList"></div>
  <button id="adAdd" class="ad-add">+ Add new item</button>
</section>
<div class="overlay" id="overlay"></div>
<aside class="drawer" id="drawer">
  <div class="drawer-head"><h2>Your order</h2><button id="drawerClose" aria-label="Close">X</button></div>
  <div class="drawer-items" id="drawerItems"></div>
  <div class="drawer-foot">
    <div class="total-row"><span>Total</span><span id="totalAmt">Rs. 0</span></div>
    <button class="checkout-btn" id="checkoutBtn">Send order on WhatsApp</button>
  </div>
</aside>

<div class="detail-overlay" id="detailOverlay">
  <div class="detail-card" id="detailCard">
    <button class="detail-close" id="detailClose" aria-label="Close">X</button>
    <div class="detail-media" id="detailMedia"></div>
    <div class="detail-body">
      <span class="cat" id="detailCat"></span>
      <h2 id="detailName"></h2>
      <span class="price" id="detailPrice"></span>
      <div class="detail-actions" id="detailActions"></div>
    </div>
  </div>
</div>

<script type="application/json" id="state">{"whatsapp": "919999999999", "products": [{"id": "g1", "name": "Albino Platinum White Guppy (pair)", "cat": "Guppies", "price": 300, "inStock": true}, {"id": "g2", "name": "Albino Redlace Guppy (pair)", "cat": "Guppies", "price": 250, "inStock": true}, {"id": "g3", "name": "Albino Silvarado Red Ear Guppy (pair)", "cat": "Guppies", "price": 240, "inStock": true}, {"id": "g4", "name": "AFR Guppy (pair)", "cat": "Guppies", "price": 230, "inStock": true}, {"id": "g5", "name": "Masco Blue Guppy (pair)", "cat": "Guppies", "price": 220, "inStock": true}, {"id": "g6", "name": "Black Guppy (pair)", "cat": "Guppies", "price": 180, "inStock": true}, {"id": "g7", "name": "Platinum White Dumbo Guppy (pair)", "cat": "Guppies", "price": 450, "inStock": true}, {"id": "g8", "name": "Silvarado Mosaic Guppy (pair)", "cat": "Guppies", "price": 180, "inStock": true}, {"id": "g9", "name": "White Texido Guppy (pair)", "cat": "Guppies", "price": 180, "inStock": true}, {"id": "g10", "name": "Japanese Blue Guppy (pair)", "cat": "Guppies", "price": 250, "inStock": true}, {"id": "g11", "name": "Platinum Big Ear Guppy (pair)", "cat": "Guppies", "price": 250, "inStock": true}, {"id": "g12", "name": "Chilli Mosaic Dumbo Guppy (pair)", "cat": "Guppies", "price": 205, "inStock": true}, {"id": "g13", "name": "Gold Guppy (pair)", "cat": "Guppies", "price": 250, "inStock": true}, {"id": "g14", "name": "Gold Ribbon Guppy (pair)", "cat": "Guppies", "price": 500, "inStock": true}, {"id": "g15", "name": "Red Granite Guppy (pair)", "cat": "Guppies", "price": 215, "inStock": true}, {"id": "g16", "name": "Blue Panda Guppy (pair)", "cat": "Guppies", "price": 230, "inStock": true}, {"id": "g17", "name": "Purple Burry Guppy (pair)", "cat": "Guppies", "price": 250, "inStock": true}, {"id": "g18", "name": "Tiger HM Guppy (pair)", "cat": "Guppies", "price": 180, "inStock": true}, {"id": "g19", "name": "Yellow Pingu Guppy (pair)", "cat": "Guppies", "price": 215, "inStock": true}, {"id": "g20", "name": "Lazuli Blue Guppy (pair)", "cat": "Guppies", "price": 190, "inStock": true}, {"id": "g21", "name": "Black Bar Endler Guppy (pair)", "cat": "Guppies", "price": 200, "inStock": true}, {"id": "g22", "name": "Red Scarlet Endler Guppy (pair)", "cat": "Guppies", "price": 200, "inStock": true}, {"id": "g23", "name": "Ivory Purple Guppy (pair)", "cat": "Guppies", "price": 250, "inStock": true}, {"id": "g24", "name": "Red Coral Endler Guppy (pair)", "cat": "Guppies", "price": 250, "inStock": true}, {"id": "g25", "name": "Zee Through Koi Guppy (pair)", "cat": "Guppies", "price": 250, "inStock": true}, {"id": "g26", "name": "Santha Clause SB Guppy (pair)", "cat": "Guppies", "price": 400, "inStock": true}, {"id": "g27", "name": "Wildred Guppy (pair)", "cat": "Guppies", "price": 210, "inStock": true}, {"id": "g28", "name": "Albino Metal Redlace Guppy (pair)", "cat": "Guppies", "price": 230, "inStock": true}, {"id": "g29", "name": "Red Dragon HM Guppy (pair)", "cat": "Guppies", "price": 250, "inStock": true}, {"id": "f1", "name": "Guppy Flake Food 100g", "cat": "Food", "price": 120, "inStock": true}, {"id": "f2", "name": "Live Daphnia Culture", "cat": "Food", "price": 80, "inStock": true}, {"id": "f3", "name": "Baby Guppy Fry Food", "cat": "Food", "price": 100, "inStock": true}]}</script>
<script>
let state = JSON.parse(document.getElementById('state').textContent);
let PRODUCTS = state.products;
const CATS = ['All','Guppies','Food'];
let cart = {}, activeCat = 'All';
const $ = id => document.getElementById(id);
const money = n => '\u20b9' + Number(n).toLocaleString('en-IN');
const esc = s => String(s).replace(/[&<>"']/g, c => ({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'}[c]));
const find = id => PRODUCTS.find(p => p.id === id);

function renderTabs(){
  $('tabs').innerHTML = '';
  CATS.forEach(c => {
    const b = document.createElement('button');
    b.className = 'tab'; b.textContent = c;
    b.setAttribute('aria-selected', c === activeCat ? 'true' : 'false');
    b.onclick = () => { activeCat = c; renderTabs(); renderGrid(); };
    $('tabs').appendChild(b);
  });
}
function mediaHtml(p){
  if(p.video) return '<div class="media"><video src="'+p.video+'" '+(p.photo?'poster="'+p.photo+'" ':'')+'controls preload="none" playsinline></video></div>';
  if(p.photo) return '<div class="media"><img src="'+p.photo+'" alt="'+esc(p.name)+'" loading="lazy"></div>';
  return '<div class="media">'+(p.cat==='Guppies'?'GUPPY':'FOOD')+'</div>';
}
function renderGrid(){
  const grid = $('grid'); grid.innerHTML = '';
  PRODUCTS.filter(p => activeCat === 'All' || p.cat === activeCat).forEach(p => {
    const q = cart[p.id] || 0;
    const action = !p.inStock ? '<button class="add-btn" disabled>Sold out</button>'
      : q === 0 ? '<button class="add-btn" data-add="'+p.id+'">Add to order</button>'
      : '<div class="qty-row"><button data-dec="'+p.id+'">-</button><span>'+q+'</span><button data-inc="'+p.id+'">+</button></div>';
    const card = document.createElement('div'); card.className = 'card';
    card.innerHTML = mediaHtml(p)+'<div class="card-body"><span class="cat">'+esc(p.cat)+'</span><h3>'+esc(p.name)+'</h3><span class="price">'+money(p.price)+'</span>'+action+'</div>';
    card.addEventListener('click', (ev) => { if(ev.target.closest('button')) return; openDetail(p.id); });
    grid.appendChild(card);
  });
  bind(grid);
}

function openDetail(id){
  const p = find(id); if(!p) return;
  $('detailMedia').innerHTML = mediaHtml(p);
  const vid = $('detailMedia').querySelector('video');
  if(vid){ vid.muted = true; vid.autoplay = true; vid.loop = true; vid.play().catch(()=>{}); }
  $('detailCat').textContent = p.cat;
  $('detailName').textContent = p.name;
  $('detailPrice').textContent = money(p.price);
  const q = cart[p.id] || 0;
  $('detailActions').innerHTML = !p.inStock ? '<button class="add-btn" disabled>Sold out</button>'
    : q === 0 ? '<button class="add-btn" data-add="'+p.id+'">Add to order</button>'
    : '<div class="qty-row"><button data-dec="'+p.id+'">-</button><span>'+q+'</span><button data-inc="'+p.id+'">+</button></div>';
  bind($('detailActions'));
  $('detailOverlay').classList.add('open');
}
function closeDetail(){ $('detailOverlay').classList.remove('open'); }
$('detailClose').onclick = closeDetail;
$('detailOverlay').onclick = (ev) => { if(ev.target === $('detailOverlay')) closeDetail(); };
function bind(root){
  root.querySelectorAll('[data-add]').forEach(b => b.onclick = () => { cart[b.dataset.add] = 1; renderAll(); });
  root.querySelectorAll('[data-inc]').forEach(b => b.onclick = () => { cart[b.dataset.inc]++; renderAll(); });
  root.querySelectorAll('[data-dec]').forEach(b => b.onclick = () => { const id = b.dataset.dec; if(--cart[id] <= 0) delete cart[id]; renderAll(); });
}
const cartTotal = () => Object.entries(cart).reduce((s,[id,q]) => s + (find(id)?.price||0)*q, 0);
const cartCount = () => Object.values(cart).reduce((a,b) => a+b, 0);
function renderDrawer(){
  $('cartCount').textContent = cartCount();
  const w = $('drawerItems'), e = Object.entries(cart).filter(([id]) => find(id));
  w.innerHTML = e.length ? e.map(([id,q]) => { const p = find(id);
    return '<div class="line"><div><div class="line-name">'+esc(p.name)+'</div><div style="font-size:.82rem;opacity:.65">'+money(p.price)+' x '+q+'</div></div><div class="line-qty"><button data-dec="'+id+'">-</button><span>'+q+'</span><button data-inc="'+id+'">+</button></div></div>'; }).join('')
    : '<p class="empty-note">Your order is empty.<br>Add guppies or food from the catalog.</p>';
  bind(w);
  $('totalAmt').textContent = money(cartTotal());
}
function renderAll(){ renderGrid(); renderDrawer(); refreshDetailActions(); }
function refreshDetailActions(){
  if(!$('detailOverlay').classList.contains('open')) return;
  const id = $('detailActions').querySelector('[data-add],[data-inc],[data-dec]');
  if(!id) return;
  const pid = id.dataset.add || id.dataset.inc || id.dataset.dec;
  const p = find(pid); if(!p) return;
  const q = cart[p.id] || 0;
  $('detailActions').innerHTML = !p.inStock ? '<button class="add-btn" disabled>Sold out</button>'
    : q === 0 ? '<button class="add-btn" data-add="'+p.id+'">Add to order</button>'
    : '<div class="qty-row"><button data-dec="'+p.id+'">-</button><span>'+q+'</span><button data-inc="'+p.id+'">+</button></div>';
  bind($('detailActions'));
}
const setDrawer = on => { $('overlay').classList.toggle('open', on); $('drawer').classList.toggle('open', on); };
$('cartOpenBtn').onclick = () => setDrawer(true);
$('drawerClose').onclick = $('overlay').onclick = () => setDrawer(false);

$('checkoutBtn').onclick = () => {
  const e = Object.entries(cart).filter(([id]) => find(id));
  if(!e.length){ alert('Add at least one item to your order first.'); return; }
  let msg = "Hello Shastha Guppy Farm, I'd like to order:\n\n";
  e.forEach(([id,q]) => { const p = find(id); msg += '- '+p.name+' x'+q+' = '+money(p.price*q)+'\n'; });
  msg += '\nTotal: '+money(cartTotal())+'\n\nPlease confirm availability and delivery.';
  window.open('https://wa.me/'+state.whatsapp+'?text='+encodeURIComponent(msg), '_blank');
};

/* ---------- owner-only edit mode ---------- */
let draft;
function buildDoc(s){
  const c = document.documentElement.cloneNode(true);
  ['grid','tabs','drawerItems','adminList','detailMedia','detailActions'].forEach(id => { const e = c.querySelector('#'+id); if(e) e.innerHTML = ''; });
  c.querySelector('#state').textContent = JSON.stringify(s).replace(/</g,'\\u003c');
  c.querySelectorAll('.open').forEach(e => e.classList.remove('open'));
  c.querySelector('#editBtn').setAttribute('hidden','');
  c.querySelector('#adminPanel').setAttribute('hidden','');
  c.querySelector('#cartCount').textContent = '0';
  c.querySelector('#totalAmt').textContent = money(0);
  return '<!DOCTYPE html>\n' + c.outerHTML;
}
function readData(f){ return new Promise((res,rej)=>{ const r=new FileReader(); r.onload=()=>res(r.result); r.onerror=rej; r.readAsDataURL(f); }); }
async function shrink(f){
  const img = new Image(); img.src = await readData(f); await img.decode();
  const s = Math.min(1, 640/img.width), c = document.createElement('canvas');
  c.width = Math.round(img.width*s); c.height = Math.round(img.height*s);
  c.getContext('2d').drawImage(img,0,0,c.width,c.height);
  return c.toDataURL('image/jpeg',0.72);
}
function renderAdmin(){
  $('adminList').innerHTML = draft.products.map((p,i) =>
    '<div class="ad-row"><input data-f="name" data-i="'+i+'" value="'+esc(p.name)+'"><input data-f="price" data-i="'+i+'" inputmode="numeric" value="'+p.price+'"><select data-f="cat" data-i="'+i+'"><option'+(p.cat==='Guppies'?' selected':'')+'>Guppies</option><option'+(p.cat==='Food'?' selected':'')+'>Food</option></select>'
    +'<div class="full"><span>Photo: '+(p.photo?'added <button class="del" data-rmp="'+i+'">remove</button>':'<input type="file" accept="image/*" data-photo="'+i+'" style="width:auto">')+'</span></div>'
    +'<div class="full"><span>Video: '+(p.video?'added <button class="del" data-rmv="'+i+'">remove</button>':'<input type="file" accept="video/*" data-video="'+i+'" style="width:auto">')+'</span></div>'
    +'<div class="full"><label><input type="checkbox" style="width:auto" data-f="inStock" data-i="'+i+'"'+(p.inStock?' checked':'')+'> In stock</label><button class="del" data-del="'+i+'">Delete</button></div></div>').join('');
  const L = $('adminList');
  L.querySelectorAll('[data-f]').forEach(el => el.onchange = () => {
    const p = draft.products[el.dataset.i], f = el.dataset.f;
    p[f] = f==='inStock' ? el.checked : f==='price' ? (Number(el.value)||0) : el.value.trim();
  });
  L.querySelectorAll('[data-photo]').forEach(el => el.onchange = async () => { const f = el.files[0]; if(!f) return; draft.products[el.dataset.photo].photo = await shrink(f); renderAdmin(); });
  L.querySelectorAll('[data-video]').forEach(el => el.onchange = async () => {
    const f = el.files[0]; if(!f) return;
    if(f.size > 2*1048576){ alert('This video is '+(f.size/1048576).toFixed(1)+' MB. Please compress it under 2 MB first.'); el.value=''; return; }
    draft.products[el.dataset.video].video = await readData(f); renderAdmin();
  });
  L.querySelectorAll('[data-rmp]').forEach(b => b.onclick = () => { delete draft.products[b.dataset.rmp].photo; renderAdmin(); });
  L.querySelectorAll('[data-rmv]').forEach(b => b.onclick = () => { delete draft.products[b.dataset.rmv].video; renderAdmin(); });
  L.querySelectorAll('[data-del]').forEach(b => b.onclick = () => { if(confirm('Delete this item?')){ draft.products.splice(b.dataset.del,1); renderAdmin(); } });
}
const OWNER_PASSWORD = 'shastha2026'; // change this to any password you like

function initAdmin(){
  $('editBtn').hidden = false;
  $('editBtn').onclick = () => {
    if(!sessionStorage.getItem('ownerOk')){
      const pw = prompt('Enter shop owner password:');
      if(pw !== OWNER_PASSWORD){ if(pw !== null) alert('Wrong password.'); return; }
      sessionStorage.setItem('ownerOk','1');
    }
    draft = JSON.parse(JSON.stringify(state)); $('adWa').value = draft.whatsapp; renderAdmin(); $('adminPanel').hidden = false;
  };
  $('adClose').onclick = () => { $('adminPanel').hidden = true; };
  $('adAdd').onclick = () => { draft.products.unshift({id:'n'+Date.now(), name:'New guppy (pair)', cat:'Guppies', price:0, inStock:true}); renderAdmin(); };
  $('adSave').onclick = () => {
    draft.whatsapp = $('adWa').value.replace(/\D/g,'') || draft.whatsapp;
    if(JSON.stringify(draft).length > 12e6){ alert('Too much photo/video data for one page (limit about 12 MB). Remove a few videos.'); return; }
    state = draft;
    localStorage.setItem('shasthaState', JSON.stringify(state));
    const blob = new Blob([buildDoc(state)], {type:'text/html'});
    const url = URL.createObjectURL(blob);
    const a = document.createElement('a');
    a.href = url; a.download = 'index.html';
    document.body.appendChild(a); a.click(); a.remove();
    URL.revokeObjectURL(url);
    $('adminPanel').hidden = true;
    renderTabs(); renderAll();
    alert('Saved! A file named index.html was downloaded. Upload it to your GitHub repository (replacing the old one) to publish these changes live. Your changes are also kept in this browser for now.');
  };
}
initAdmin();

(() => {
  try {
    const saved = localStorage.getItem('shasthaState');
    if(saved){ state = JSON.parse(saved); }
  } catch(e){}
})();

renderTabs(); renderAll();
</script>
</body>
</html>
