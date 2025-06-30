<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hiasan Aesthetic</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;500;600&family=Poppins:wght@300;400;500&display=swap');
        
        body {
            font-family: 'Poppins', sans-serif;
            background-color: #f9f5f0;
            color: #5c3a21;
        }
        
        .title-font {
            font-family: 'Playfair Display', serif;
        }
        
        .product-card {
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            background-color: #fffdfa;
        }
        
        .product-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(92, 58, 33, 0.1);
        }
        
        .cart-item {
            transition: background-color 0.2s ease;
        }
        
        .cart-item:hover {
            background-color: #f5ebe0;
        }
        
        .modal-overlay {
            animation: fadeIn 0.3s ease-out;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
    </style>
</head>
<body class="min-h-screen">
    <div class="container mx-auto px-4 py-8">
        <!-- Header -->
        <header class="flex flex-col md:flex-row justify-between items-center mb-12">
            <h1 class="title-font text-4xl md:text-5xl font-semibold text-[#5c3a21] mb-4 md:mb-0">Hiasan Aesthetic</h1>
            <div class="flex items-center space-x-4">
                <button id="viewCartBtn" class="relative px-4 py-2 bg-[#5c3a21] text-white rounded-lg hover:bg-[#4a2f1a] transition">
                    Keranjang
                    <span id="cartCount" class="absolute -top-2 -right-2 bg-[#8b5e33] text-white text-xs font-bold rounded-full h-6 w-6 flex items-center justify-center">0</span>
                </button>
            </div>
        </header>

        <!-- Products Grid -->
        <section class="mb-16">
            <h2 class="title-font text-2xl md:text-3xl font-medium mb-8 text-[#5c3a21]">Produk Kami</h2>
            
            <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-8">
                <!-- Product 1 -->
                <div class="product-card rounded-lg overflow-hidden shadow-md border border-[#e8d6c5]">
                    <div class="h-64 overflow-hidden">
                        <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/ac6d9212-39f1-45b5-9bcc-d557170de6f7.png" alt="Minimalist ceramic vase with earth tones on a wooden table with dried flowers" class="w-full h-full object-cover"/>
                    </div>
                    <div class="p-6">
                        <h3 class="title-font text-xl font-semibold mb-2">Vase Keramik</h3>
                        <p class="text-[#8b5e33] mb-4">Vase minimalis dengan sentuhan modern untuk rumah aesthetic Anda.</p>
                        <div class="flex justify-between items-center">
                            <span class="text-lg font-medium text-[#5c3a21]">Rp 250.000</span>
                            <button class="add-to-cart-btn px-4 py-2 bg-[#8b5e33] hover:bg-[#5c3a21] text-white rounded transition" data-id="1" data-name="Vase Keramik" data-price="250000" data-image="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/e262e155-8d6b-41b2-8ed8-7b89320974a4.png">
                                + Keranjang
                            </button>
                        </div>
                    </div>
                </div>
                
                <!-- Product 2 -->
                <div class="product-card rounded-lg overflow-hidden shadow-md border border-[#e8d6c5]">
                    <div class="h-64 overflow-hidden">
                        <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/511deb66-db9e-424d-92e3-14c459931190.png" alt="Handcrafted wooden photo frame displayed on a rustic shelf with neutral background" class="w-full h-full object-cover"/>
                    </div>
                    <div class="p-6">
                        <h3 class="title-font text-xl font-semibold mb-2">Bingkai Kayu</h3>
                        <p class="text-[#8b5e33] mb-4">Bingkai foto kayu handmade dengan finishing natural.</p>
                        <div class="flex justify-between items-center">
                            <span class="text-lg font-medium text-[#5c3a21]">Rp 180.000</span>
                            <button class="add-to-cart-btn px-4 py-2 bg-[#8b5e33] hover:bg-[#5c3a21] text-white rounded transition" data-id="2" data-name="Bingkai Kayu" data-price="180000" data-image="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/94b20a03-34fe-458f-a383-5f497d2265f9.png">
                                + Keranjang
                            </button>
                        </div>
                    </div>
                </div>
                
                <!-- Product 3 -->
                <div class="product-card rounded-lg overflow-hidden shadow-md border border-[#e8d6c5]">
                    <div class="h-64 overflow-hidden">
                        <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/a3fe1e4c-8ba6-4dd2-afc7-5ce4102dec77.png" alt="Artisan coffee set with ceramic cups and wooden tray on marble countertop" class="w-full h-full object-cover"/>
                    </div>
                    <div class="p-6">
                        <h3 class="title-font text-xl font-semibold mb-2">Set Kopi</h3>
                        <p class="text-[#8b5e33] mb-4">Set kopi berkualitas dengan gelas keramik dan kayu.</p>
                        <div class="flex justify-between items-center">
                            <span class="text-lg font-medium text-[#5c3a21]">Rp 350.000</span>
                            <button class="add-to-cart-btn px-4 py-2 bg-[#8b5e33] hover:bg-[#5c3a21] text-white rounded transition" data-id="3" data-name="Set Kopi" data-price="350000" data-image="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/40528189-152a-4d9d-b514-a615810e7634.png">
                                + Keranjang
                            </button>
                        </div>
                    </div>
                </div>

                <!-- Product 4 -->
                <div class="product-card rounded-lg overflow-hidden shadow-md border border-[#e8d6c5]">
                    <div class="h-64 overflow-hidden">
                        <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/dd1681ba-ebea-4bb6-973d-50aaf075c9d1.png" alt="Elegant decorative candle with wooden wick in neutral tones" class="w-full h-full object-cover"/>
                    </div>
                    <div class="p-6">
                        <h3 class="title-font text-xl font-semibold mb-2">Lilin Dekorasi</h3>
                        <p class="text-[#8b5e33] mb-4">Lilin aesthetic dengan aroma lembut untuk menciptakan suasana cozy.</p>
                        <div class="flex justify-between items-center">
                            <span class="text-lg font-medium text-[#5c3a21]">Rp 120.000</span>
                            <button class="add-to-cart-btn px-4 py-2 bg-[#8b5e33] hover:bg-[#5c3a21] text-white rounded transition" data-id="4" data-name="Lilin Dekorasi" data-price="120000" data-image="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/5f256ae8-ca8a-42c1-bd0c-df19035df8d4.png">
                                + Keranjang
                            </button>
                        </div>
                    </div>
                </div>

                <!-- Product 5 -->
                <div class="product-card rounded-lg overflow-hidden shadow-md border border-[#e8d6c5]">
                    <div class="h-64 overflow-hidden">
                        <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/ac2558ad-68e0-4c14-bc68-d0dd4076f994.png" alt="Handmade macrame wall hanging in natural beige tones" class="w-full h-full object-cover"/>
                    </div>
                    <div class="p-6">
                        <h3 class="title-font text-xl font-semibold mb-2">Hiasan Dinding Makrame</h3>
                        <p class="text-[#8b5e33] mb-4">Dekorasi dinding handmade dengan teknik makrame tradisional.</p>
                        <div class="flex justify-between items-center">
                            <span class="text-lg font-medium text-[#5c3a21]">Rp 290.000</span>
                            <button class="add-to-cart-btn px-4 py-2 bg-[#8b5e33] hover:bg-[#5c3a21] text-white rounded transition" data-id="5" data-name="Hiasan Dinding Makrame" data-price="290000" data-image="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/2a60f187-5360-4678-850b-102a6254a985.png">
                                + Keranjang
                            </button>
                        </div>
                    </div>
                </div>

                <!-- Product 6 -->
                <div class="product-card rounded-lg overflow-hidden shadow-md border border-[#e8d6c5]">
                    <div class="h-64 overflow-hidden">
                        <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/aebf2f99-d959-4cbb-83bc-7432a930ba1d.png" alt="Natural jute woven rug with organic texture in earthy tones" class="w-full h-full object-cover"/>
                    </div>
                    <div class="p-6">
                        <h3 class="title-font text-xl font-semibold mb-2">Karpet Jute</h3>
                        <p class="text-[#8b5e33] mb-4">Karpet anyaman jute alami untuk menambahkan kesan natural di rumah.</p>
                        <div class="flex justify-between items-center">
                            <span class="text-lg font-medium text-[#5c3a21]">Rp 420.000</span>
                            <button class="add-to-cart-btn px-4 py-2 bg-[#8b5e33] hover:bg-[#5c3a21] text-white rounded transition" data-id="6" data-name="Karpet Jute" data-price="420000" data-image="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/0051af1f-9578-4cba-9fe5-5af97602249c.png">
                                + Keranjang
                            </button>
                        </div>
                    </div>
                </div>
            </div>
        </section>
    </div>

    <!-- Shopping Cart Modal -->
    <div id="cartModal" class="fixed inset-0 bg-black bg-opacity-50 z-50 flex items-center justify-center p-4 hidden modal-overlay">
        <div class="bg-white rounded-lg shadow-xl w-full max-w-md max-h-[90vh] overflow-hidden flex flex-col">
            <!-- Modal Header -->
            <div class="bg-[#5c3a21] text-white p-4 flex justify-between items-center">
                <h3 class="title-font text-xl font-semibold">Keranjang Belanja</h3>
                <button id="closeCartBtn" class="text-white hover:text-[#e8d6c5] text-2xl">&times;</button>
            </div>
            
            <!-- Cart Items -->
            <div id="cartItems" class="flex-1 overflow-y-auto p-4">
                <!-- Items will be added here dynamically -->
                <div id="emptyCartMessage" class="text-center py-8">
                    <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/04d081d2-90d5-4c6c-a69a-f468bd446d8f.png" alt="Illustration of an empty shopping basket with text 'Keranjang Kosong'" class="mx-auto mb-4 w-32 h-32 object-contain"/>
                    <p class="text-[#8b5e33]">Keranjang belanja Anda masih kosong</p>
                </div>
            </div>
            
            <!-- Cart Summary -->
            <div id="cartSummary" class="border-t border-[#e8d6c5] p-4 hidden">
                <div class="flex justify-between mb-2">
                    <span class="font-medium">Subtotal</span>
                    <span id="subtotal">Rp 0</span>
                </div>
                
                <!-- Payment Method -->
                <div class="mb-4">
                    <label class="block text-sm font-medium text-[#5c3a21] mb-2">Metode Pembayaran</label>
                    <select id="paymentMethod" class="w-full px-3 py-2 border border-[#e8d6c5] rounded-md focus:outline-none focus:ring-1 focus:ring-[#8b5e33]">
                        <option value="bank">Transfer Bank</option>
                        <option value="ewallet">E-Wallet</option>
                        <option value="cod">COD (Bayar di Tempat)</option>
                    </select>
                </div>
                
                <!-- Checkout Button -->
                <button id="checkoutBtn" class="w-full py-3 bg-[#8b5e33] hover:bg-[#5c3a21] text-white rounded-lg transition font-medium">
                    Checkout (Rp <span id="checkoutTotal">0</span>)
                </button>
            </div>
        </div>
    </div>

    <!-- Payment Modal -->
    <div id="paymentModal" class="fixed inset-0 bg-black bg-opacity-50 z-50 flex items-center justify-center p-4 hidden modal-overlay">
        <div class="bg-white rounded-lg shadow-xl w-full max-w-md max-h-[90vh] overflow-hidden">
            <!-- Modal Header -->
            <div class="bg-[#5c3a21] text-white p-4 flex justify-between items-center">
                <h3 class="title-font text-xl font-semibold">Pembayaran</h3>
                <button id="closePaymentBtn" class="text-white hover:text-[#e8d6c5] text-2xl">&times;</button>
            </div>
            
            <!-- Payment Content -->
            <div class="p-6">
                <div id="bankPayment" class="payment-method">
                    
                    <p class="mb-4 text-[#5c3a21]">Silakan transfer ke rekening berikut:</p>
                    <div class="bg-[#f5ebe0] p-4 rounded mb-4">
                        <div class="mb-3 pb-2 border-b border-[#e8d6c5]">
                            <div class="flex justify-between mb-1">
                                <span>Bank:</span>
                                <span class="font-medium">BCA</span>
                            </div>
                            <div class="flex justify-between mb-1">
                                <span>No. Rekening:</span>
                                <span class="font-medium">123 4567 890</span>
                            </div>
                            <div class="flex justify-between">
                                <span>Atas Nama:</span>
                                <span class="font-medium">Aesthetic Brown Shop</span>
                            </div>
                        </div>
                        
                        <div class="mb-3 pb-2 border-b border-[#e8d6c5]">
                            <div class="flex justify-between mb-1">
                                <span>Bank:</span>
                                <span class="font-medium">BNI</span>
                            </div>
                            <div class="flex justify-between mb-1">
                                <span>No. Rekening:</span>
                                <span class="font-medium">987 6543 210</span>
                            </div>
                            <div class="flex justify-between">
                                <span>Atas Nama:</span>
                                <span class="font-medium">Aesthetic Brown Shop</span>
                            </div>
                        </div>

                        <div>
                            <div class="flex justify-between mb-1">
                                <span>Bank:</span>
                                <span class="font-medium">Mandiri</span>
                            </div>
                            <div class="flex justify-between mb-1">
                                <span>No. Rekening:</span>
                                <span class="font-medium">456 7890 123</span>
                            </div>
                            <div class="flex justify-between">
                                <span>Atas Nama:</span>
                                <span class="font-medium">Aesthetic Brown Shop</span>
                            </div>
                        </div>
                    </div>
                    <p class="mb-4 text-sm text-[#8b5e33]">Jumlah yang harus dibayar: <span id="bankAmount" class="font-medium">Rp 0</span></p>
                </div>
                
                <div id="ewalletPayment" class="payment-method hidden">
                  
                    <p class="mb-4 text-[#5c3a21]">Scan QR code berikut untuk pembayaran:</p>
                    <div class="flex justify-center mb-4">
                        <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/b3725468-0d90-47d1-9020-1f1eb56b843f.png" alt="Payment QR code for e-wallet transactions" class="border border-[#e8d6c5] p-2 rounded"/>
                    </div>
                    <p class="mb-4 text-sm text-[#8b5e33]">Jumlah yang harus dibayar: <span id="ewalletAmount" class="font-medium">Rp 0</span></p>
                </div>
                
                <div id="codPayment" class="payment-method hidden">
                    <img src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/f0b5ff67-6357-4091-b698-36996b81c619.png" alt="Illustration of package delivery with cash payment interaction between courier and customer" class="w-full mb-4 rounded"/>
                    <p class="mb-4 text-[#5c3a21]">Anda akan membayar saat barang diterima.</p>
                    <p class="text-sm text-[#8b5e33]">Total pembayaran: <span id="codAmount" class="font-medium">Rp 0</span></p>
                </div>
                
                <!-- Payment Success Button -->
                <button id="completePaymentBtn" class="w-full mt-6 py-3 bg-[#8b5e33] hover:bg-[#5c3a21] text-white rounded-lg transition font-medium">
                    Selesai Pembayaran
                </button>
            </div>
        </div>
    </div>

    <!-- Order Complete Modal -->
    <div id="completeModal" class="fixed inset-0 bg-black bg-opacity-50 z-50 flex items-center justify-center p-4 hidden modal-overlay">
        <div class="bg-white rounded-lg shadow-xl w-full max-w-md overflow-hidden">
            <div class="p-8 text-center">
               
                <h3 class="title-font text-2xl font-semibold text-[#5c3a21] mb-4">Pembayaran Berhasil!</h3>
                <p class="mb-6 text-[#8b5e33]">Terima kasih telah berbelanja dengan kami. Pesanan Anda akan segera diproses.</p>
                <button id="closeCompleteBtn" class="px-6 py-2 bg-[#8b5e33] hover:bg-[#5c3a21] text-white rounded-lg transition">
                    Tutup
                </button>
            </div>
        </div>
    </div>

    <script>
        // Cart data
        let cart = [];
        
        // DOM Elements
        const viewCartBtn = document.getElementById('viewCartBtn');
        const closeCartBtn = document.getElementById('closeCartBtn');
        const cartModal = document.getElementById('cartModal');
        const cartItems = document.getElementById('cartItems');
        const emptyCartMessage = document.getElementById('emptyCartMessage');
        const cartSummary = document.getElementById('cartSummary');
        const subtotalEl = document.getElementById('subtotal');
        const checkoutTotalEl = document.getElementById('checkoutTotal');
        const cartCount = document.getElementById('cartCount');
        const paymentMethod = document.getElementById('paymentMethod');
        const checkoutBtn = document.getElementById('checkoutBtn');
        
        // Payment modal elements
        const paymentModal = document.getElementById('paymentModal');
        const closePaymentBtn = document.getElementById('closePaymentBtn');
        const bankPayment = document.getElementById('bankPayment');
        const ewalletPayment = document.getElementById('ewalletPayment');
        const codPayment = document.getElementById('codPayment');
        const bankAmount = document.getElementById('bankAmount');
        const ewalletAmount = document.getElementById('ewalletAmount');
        const codAmount = document.getElementById('codAmount');
        const completePaymentBtn = document.getElementById('completePaymentBtn');
        
        // Complete modal elements
        const completeModal = document.getElementById('completeModal');
        const closeCompleteBtn = document.getElementById('closeCompleteBtn');
        
        // Product buttons
        const addToCartBtns = document.querySelectorAll('.add-to-cart-btn');
        
        // Event Listeners
        viewCartBtn.addEventListener('click', openCartModal);
        closeCartBtn.addEventListener('click', closeCartModal);
        checkoutBtn.addEventListener('click', openPaymentModal);
        closePaymentBtn.addEventListener('click', closePaymentModal);
        completePaymentBtn.addEventListener('click', completePayment);
        closeCompleteBtn.addEventListener('click', closeCompleteModal);
        
        paymentMethod.addEventListener('change', updatePaymentMethodDisplay);
        
        // Add to cart buttons event listeners
        addToCartBtns.forEach(btn => {
            btn.addEventListener('click', addToCart);
        });
        
        // Functions
        function openCartModal() {
            renderCartItems();
            cartModal.classList.remove('hidden');
            document.body.style.overflow = 'hidden';
        }
        
        function closeCartModal() {
            cartModal.classList.add('hidden');
            document.body.style.overflow = 'auto';
        }
        
        function openPaymentModal() {
            const total = calculateTotal();
            bankAmount.textContent = `Rp ${formatNumber(total)}`;
            ewalletAmount.textContent = `Rp ${formatNumber(total)}`;
            codAmount.textContent = `Rp ${formatNumber(total)}`;
            updatePaymentMethodDisplay();
            
            paymentModal.classList.remove('hidden');
            cartModal.classList.add('hidden');
        }
        
        function closePaymentModal() {
            paymentModal.classList.add('hidden');
            openCartModal();
        }
        
        function completePayment() {
            paymentModal.classList.add('hidden');
            completeModal.classList.remove('hidden');
            
            // Clear cart after payment complete
            cart = [];
            updateCartCount();
            renderCartItems();
        }
        
        function closeCompleteModal() {
            completeModal.classList.add('hidden');
            document.body.style.overflow = 'auto';
        }
        
        function updatePaymentMethodDisplay() {
            const method = paymentMethod.value;
            
            bankPayment.classList.add('hidden');
            ewalletPayment.classList.add('hidden');
            codPayment.classList.add('hidden');
            
            if (method === 'bank') {
                bankPayment.classList.remove('hidden');
            } else if (method === 'ewallet') {
                ewalletPayment.classList.remove('hidden');
            } else if (method === 'cod') {
                codPayment.classList.remove('hidden');
            }
        }
        
        function addToCart(e) {
            const button = e.currentTarget;
            const product = {
                id: button.dataset.id,
                name: button.dataset.name,
                price: parseInt(button.dataset.price),
                image: button.dataset.image,
                quantity: 1
            };
            
            // Check if product already in cart
            const existingItem = cart.find(item => item.id === product.id);
            
            if (existingItem) {
                existingItem.quantity += 1;
            } else {
                cart.push(product);
            }
            
            updateCartCount();
            
            // Button animation feedback
            button.textContent = '✓ Ditambahkan';
            button.classList.remove('bg-[#8b5e33]', 'hover:bg-[#5c3a21]');
            button.classList.add('bg-green-600', 'hover:bg-green-700');
            
            setTimeout(() => {
                button.textContent = '+ Keranjang';
                button.classList.remove('bg-green-600', 'hover:bg-green-700');
                button.classList.add('bg-[#8b5e33]', 'hover:bg-[#5c3a21]');
            }, 1500);
        }
        
        function updateCartCount() {
            const count = cart.reduce((total, item) => total + item.quantity, 0);
            cartCount.textContent = count;
        }
        
        function renderCartItems() {
            cartItems.innerHTML = '';
            
            if (cart.length === 0) {
                emptyCartMessage.classList.remove('hidden');
                cartSummary.classList.add('hidden');
                return;
            }
            
            emptyCartMessage.classList.add('hidden');
            cartSummary.classList.remove('hidden');
            
            cart.forEach(item => {
                const itemElement = document.createElement('div');
                itemElement.className = 'cart-item flex items-center py-3 border-b border-[#e8d6c5] last:border-0';
                itemElement.innerHTML = `
                    <div class="flex-shrink-0 w-16 h-16 overflow-hidden rounded-lg border border-[#e8d6c5]">
                        <img src="${item.image}" alt="${item.name}" class="w-full h-full object-cover" />
                    </div>
                    <div class="ml-4 flex-1">
                        <h4 class="font-medium text-[#5c3a21]">${item.name}</h4>
                        <div class="flex justify-between items-center mt-1">
                            <div class="flex items-center">
                                <button class="decrease-quantity px-2 py-1 bg-[#f5ebe0] rounded" data-id="${item.id}">-</button>
                                <span class="mx-2">${item.quantity}</span>
                                <button class="increase-quantity px-2 py-1 bg-[#f5ebe0] rounded" data-id="${item.id}">+</button>
                            </div>
                            <span class="text-[#8b5e33] font-medium">Rp ${formatNumber(item.price * item.quantity)}</span>
                        </div>
                    </div>
                    <button class="remove-item ml-4 text-red-500 hover:text-red-700" data-id="${item.id}">
                        Hapus
                    </button>
                `;
                cartItems.appendChild(itemElement);
            });
            
            // Update quantity buttons event listeners
            document.querySelectorAll('.increase-quantity').forEach(btn => {
                btn.addEventListener('click', increaseQuantity);
            });
            
            document.querySelectorAll('.decrease-quantity').forEach(btn => {
                btn.addEventListener('click', decreaseQuantity);
            });
            
            document.querySelectorAll('.remove-item').forEach(btn => {
                btn.addEventListener('click', removeItem);
            });
            
            // Update summary
            const total = calculateTotal();
            subtotalEl.textContent = `Rp ${formatNumber(total)}`;
            checkoutTotalEl.textContent = formatNumber(total);
        }
        
        function calculateTotal() {
            return cart.reduce((total, item) => total + (item.price * item.quantity), 0);
        }
        
        function increaseQuantity(e) {
            const id = e.currentTarget.dataset.id;
            const item = cart.find(item => item.id === id);
            
            if (item) {
                item.quantity += 1;
                updateCartCount();
                renderCartItems();
            }
        }
        
        function decreaseQuantity(e) {
            const id = e.currentTarget.dataset.id;
            const item = cart.find(item => item.id === id);
            
            if (item && item.quantity > 1) {
                item.quantity -= 1;
                updateCartCount();
                renderCartItems();
            }
        }
        
        function removeItem(e) {
            const id = e.currentTarget.dataset.id;
            cart = cart.filter(item => item.id !== id);
            updateCartCount();
            renderCartItems();
        }
        
        function formatNumber(num) {
            return num.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ".");
        }
    </script>
</body>
</html>
