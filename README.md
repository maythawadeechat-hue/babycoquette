# babycoquette
<!DOCTYPE html><html class="light" lang="th" style=""><head>
<meta charset="utf-8">
<meta content="width=device-width, initial-scale=1.0" name="viewport">
<title>Baby Coquette - Custom Order Calculator</title>
<link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;600;700;800&amp;family=Be+Vietnam+Pro:wght@400;600&amp;family=Mitr:wght@300;400;500&amp;display=swap" rel="stylesheet">
<link href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:wght,FILL@100..700,0..1&amp;display=swap" rel="stylesheet">
<script src="https://cdn.tailwindcss.com?plugins=forms,container-queries"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/html2canvas/1.4.1/html2canvas.min.js"></script>
<script id="tailwind-config">
        tailwind.config = {
            darkMode: "class",
            theme: {
                extend: {
                    "colors": {
                        "navy-luxe": "#1a2b4c",
                        "secondary-fixed": "#d8e2ff",
                        "tertiary": "#645c5f",
                        "surface-container-lowest": "#ffffff",
                        "on-primary-fixed-variant": "#66394a",
                        "on-tertiary-container": "#5f585a",
                        "surface-container-low": "#f3f3f4",
                        "secondary": "#4e5e82",
                        "on-secondary-container": "#4b5b7f",
                        "inverse-on-surface": "#f0f1f1",
                        "surface-dim": "#dadada",
                        "error": "#ba1a1a",
                        "secondary-fixed-dim": "#b6c6f0",
                        "on-primary-container": "#7b4c5e",
                        "surface-variant": "#e2e2e2",
                        "surface": "#f9f9f9",
                        "inverse-primary": "#f3b6cb",
                        "on-error": "#ffffff",
                        "surface-container-highest": "#e2e2e2",
                        "secondary-container": "#c4d4fe",
                        "on-primary-fixed": "#330f1f",
                        "on-secondary-fixed-variant": "#364669",
                        "surface-container": "#eeeeee",
                        "primary-container": "#ffc1d6",
                        "outline-variant": "#d4c2c6",
                        "primary-fixed": "#ffd9e4",
                        "on-tertiary": "#ffffff",
                        "surface-container-high": "#e8e8e8",
                        "surface-bright": "#f9f9f9",
                        "primary-fixed-dim": "#f3b6cb",
                        "on-primary": "#ffffff",
                        "outline": "#827377",
                        "on-secondary": "#ffffff",
                        "on-tertiary-fixed-variant": "#4b4548",
                        "background": "#f9f9f9",
                        "tertiary-container": "#d9cfd2",
                        "on-secondary-fixed": "#071b3b",
                        "error-container": "#ffdad6",
                        "on-background": "#1a1c1c",
                        "primary": "#805062",
                        "surface-tint": "#805062",
                        "on-error-container": "#93000a",
                        "on-surface-variant": "#504447",
                        "tertiary-fixed-dim": "#cec4c7",
                        "on-surface": "#1a1c1c",
                        "on-tertiary-fixed": "#1f1a1d",
                        "tertiary-fixed": "#eae0e3",
                        "inverse-surface": "#2f3131"
                    },
                    "borderRadius": {
                        "DEFAULT": "0.25rem",
                        "lg": "0.5rem",
                        "xl": "0.75rem",
                        "full": "9999px"
                    },
                    "spacing": {
                        "xl": "80px",
                        "gutter": "20px",
                        "lg": "48px",
                        "margin-desktop": "64px",
                        "xs": "4px",
                        "sm": "12px",
                        "base": "8px",
                        "md": "24px",
                        "margin-mobile": "16px"
                    },
                    "fontFamily": {
                        "body-md": ["Plus Jakarta Sans", "Mitr"],
                        "headline-md": ["Plus Jakarta Sans", "Mitr"],
                        "body-lg": ["Plus Jakarta Sans", "Mitr"],
                        "headline-lg": ["Plus Jakarta Sans", "Mitr"],
                        "headline-lg-mobile": ["Plus Jakarta Sans", "Mitr"],
                        "label-sm": ["Be Vietnam Pro"]
                    },
                    "fontSize": {
                        "body-md": ["16px", {"lineHeight": "1.6", "fontWeight": "400"}],
                        "headline-md": ["24px", {"lineHeight": "1.4", "fontWeight": "600"}],
                        "body-lg": ["18px", {"lineHeight": "1.6", "fontWeight": "400"}],
                        "headline-lg": ["40px", {"lineHeight": "1.2", "letterSpacing": "-0.02em", "fontWeight": "700"}],
                        "headline-lg-mobile": ["32px", {"lineHeight": "1.2", "fontWeight": "700"}],
                        "label-sm": ["13px", {"lineHeight": "1.2", "letterSpacing": "0.05em", "fontWeight": "600"}]
                    }
                },
            },
        }
    </script>
<style>body { font-family: 'Plus Jakarta Sans', 'Mitr', sans-serif; }
        .material-symbols-outlined {
            font-variation-settings: 'FILL' 0, 'wght' 400, 'GRAD' 0, 'opsz' 24;
            display: inline-block;
            vertical-align: middle;
        }
        .ribbon-divider {
            position: relative;
            height: 1px;
            background: #d4c2c6;
            margin: 40px 0;
        }
        .ribbon-divider::after {
            content: 'ȦɀȠ';
            position: absolute;
            left: 50%;
            top: 50%;
            transform: translate(-50%, -50%);
            background: #ffc1d6;
            padding: 0 10px;
        }
        .custom-card {
            background: #ffffff;
            border: 1px solid #ffc1d6;
            transition: all 0.3s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        }
        .squishy-btn {
            transition: transform 0.2s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        }
        .squishy-btn:active {
            transform: scale(0.92);
        }
        .custom-scrollbar {
            scrollbar-width: thin;
            scrollbar-color: #ffc1d6 transparent;
        }
        .custom-scrollbar::-webkit-scrollbar {
            width: 4px;
        }
        .custom-scrollbar::-webkit-scrollbar-thumb {
            background: #ffc1d6;
            border-radius: 10px;
        }</style>
<style>body { font-family: 'Plus Jakarta Sans', 'Mitr', sans-serif; }
        .material-symbols-outlined {
            font-variation-settings: 'FILL' 0, 'wght' 400, 'GRAD' 0, 'opsz' 24;
            display: inline-block;
            vertical-align: middle;
        }
        .ribbon-divider {
            position: relative;
            height: 1px;
            background: #d4c2c6;
            margin: 40px 0;
        }
        .ribbon-divider::after {
            content: 'ȦɀȠ';
            position: absolute;
            left: 50%;
            top: 50%;
            transform: translate(-50%, -50%);
            background: #ffc1d6;
            padding: 0 10px;
        }
        .custom-card {
            background: #ffffff;
            border: 1px solid #ffc1d6;
            transition: all 0.3s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        }
        .squishy-btn {
            transition: transform 0.2s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        }
        .squishy-btn:active {
            transform: scale(0.92);
        }
        .custom-scrollbar {
            scrollbar-width: thin;
            scrollbar-color: #ffc1d6 transparent;
        }
        .custom-scrollbar::-webkit-scrollbar {
            width: 4px;
        }
        .custom-scrollbar::-webkit-scrollbar-thumb {
            background: #ffc1d6;
            border-radius: 10px;
        }</style></head>
<body class="text-on-background min-h-screen bg-primary-container">
<nav class="w-full top-0 sticky z-50 bg-surface dark:bg-surface-dim shadow-[0_4px_15px_rgba(26,43,76,0.1)] flex justify-between items-center px-6 md:px-margin-desktop py-4 max-w-7xl mx-auto">
<div class="flex items-center gap-2">
<span class="material-symbols-outlined text-navy-luxe" style="font-variation-settings: 'FILL' 1;">temp_preferences_custom</span>
<span class="text-headline-md font-headline-lg text-navy-luxe">Baby Coquette</span>
</div>
<div class="hidden md:flex gap-md">
<a class="text-secondary font-body-md hover:text-navy-luxe transition-colors duration-200" href="#">หน้าแรก</a>
<a class="text-navy-luxe font-bold border-b-2 border-navy-luxe pb-1 transition-colors duration-200" href="#">เครื่องคำนวณ</a>
<a class="text-secondary font-body-md hover:text-navy-luxe transition-colors duration-200" href="#">สินค้า</a>
<a class="text-secondary font-body-md hover:text-navy-luxe transition-colors duration-200" href="#">รีวิว</a>
</div>
<div class="flex items-center gap-sm">
<button class="material-symbols-outlined text-navy-luxe hover:scale-110 transition-transform">favorite</button>
<button class="material-symbols-outlined text-navy-luxe hover:scale-110 transition-transform">shopping_bag</button>
</div>
</nav>
<main class="max-w-6xl mx-auto px-margin-mobile md:px-margin-desktop py-xl">
<header class="text-center mb-xl">
<div class="inline-block p-4 bg-navy-luxe rounded-full mb-md animate-bounce">
<span class="material-symbols-outlined text-white text-4xl" style="font-variation-settings: 'FILL' 1;">auto_awesome</span>
</div>
<h1 class="font-headline-lg-mobile md:font-headline-lg text-navy-luxe mb-sm uppercase tracking-wider">Custom Shop Calculator</h1>
<p class="font-body-lg text-on-surface-variant max-w-lg mx-auto">ออกแบบความน่ารักในสไตล์พรีเมียม คำนวณราคง่ายๆ แค่ไม่กี่คลิก 🎀</p>
</header>
<div class="ribbon-divider"></div>
<div class="grid grid-cols-1 lg:grid-cols-3 gap-md items-start">
<div class="lg:col-span-2 space-y-md">
<!-- Step 1: Global Quantity -->
<section class="bg-white p-md rounded-xl border border-primary-fixed shadow-sm">
<h2 class="font-headline-md text-navy-luxe mb-md flex items-center gap-2">
<span class="material-symbols-outlined">filter_1</span>
                    จำนวนสินค้าทั้งหมด
                </h2>
<div class="flex items-center gap-4">
<button class="w-12 h-12 rounded-full border-2 border-navy-luxe text-navy-luxe flex items-center justify-center hover:bg-navy-luxe hover:text-white transition-all font-bold text-xl" onclick="changeQty(-1)">-</button>
<input class="w-24 text-center border-outline-variant rounded-lg font-headline-md text-navy-luxe text-2xl" id="global-qty" max="10" min="1" onchange="generateItemForms()" type="number" value="1">
<button class="w-12 h-12 rounded-full border-2 border-navy-luxe text-navy-luxe flex items-center justify-center hover:bg-navy-luxe hover:text-white transition-all font-bold text-xl" onclick="changeQty(1)">+</button>
<span class="text-on-surface-variant font-body-md ml-2">ชิ้น</span>
</div>
</section>
<!-- Dynamic Items Container -->
<div class="space-y-md" id="items-container">
        <section class="bg-white p-md rounded-xl border border-primary-fixed shadow-sm item-form" data-id="1">
            <header class="flex items-center justify-between mb-md border-b border-surface-variant pb-base">
                <h2 class="font-headline-md text-navy-luxe flex items-center gap-2">
                    <span class="material-symbols-outlined text-secondary">shopping_basket</span>
                    ชิ้นที่ 1
                </h2>
                <span class="text-xs uppercase font-bold text-outline-variant">การตั้งค่า</span>
            </header>
            
            <div class="grid grid-cols-3 gap-2 mb-md">
                
                    <label class="cursor-pointer group">
                        <input type="radio" name="type_1" value="iphone" checked="" onchange="updateAllUI()" class="hidden peer">
                        <div class="peer-checked:bg-navy-luxe peer-checked:text-white peer-checked:border-navy-luxe p-3 border border-outline-variant rounded-lg text-center transition-all hover:border-navy-luxe">
                            <span class="material-symbols-outlined block text-xl mb-1">smartphone</span>
                            <span class="text-[10px] uppercase font-bold leading-none">iPhone</span>
                        </div>
                    </label>
                
                    <label class="cursor-pointer group">
                        <input type="radio" name="type_1" value="ipad" onchange="updateAllUI()" class="hidden peer">
                        <div class="peer-checked:bg-navy-luxe peer-checked:text-white peer-checked:border-navy-luxe p-3 border border-outline-variant rounded-lg text-center transition-all hover:border-navy-luxe">
                            <span class="material-symbols-outlined block text-xl mb-1">tablet_mac</span>
                            <span class="text-[10px] uppercase font-bold leading-none">iPad</span>
                        </div>
                    </label>
                
                    <label class="cursor-pointer group">
                        <input type="radio" name="type_1" value="film" onchange="updateAllUI()" class="hidden peer">
                        <div class="peer-checked:bg-navy-luxe peer-checked:text-white peer-checked:border-navy-luxe p-3 border border-outline-variant rounded-lg text-center transition-all hover:border-navy-luxe">
                            <span class="material-symbols-outlined block text-xl mb-1">photo_camera</span>
                            <span class="text-[10px] uppercase font-bold leading-none">Film</span>
                        </div>
                    </label>
                
            </div>

            <div id="details_1" class="space-y-md">
                    <div class="grid grid-cols-2 gap-md">
                        <div>
                            <label class="block text-xs font-bold mb-1 uppercase text-outline">รุ่นสินค้า</label>
                            <select id="model_1" onchange="updateAllUI()" class="w-full rounded-lg border-outline-variant text-sm py-2 focus:ring-navy-luxe focus:border-navy-luxe">
                                <option value="XR" selected="">XR</option><option value="11">11</option><option value="11 Pro">11 Pro</option><option value="11 Pro Max">11 Pro Max</option><option value="12">12</option><option value="12 Pro">12 Pro</option><option value="12 Pro Max">12 Pro Max</option><option value="13">13</option><option value="13 Pro">13 Pro</option><option value="13 Pro Max">13 Pro Max</option><option value="14">14</option><option value="14 Pro">14 Pro</option><option value="14 Pro Max">14 Pro Max</option><option value="15">15</option><option value="15 Pro">15 Pro</option><option value="15 Pro Max">15 Pro Max</option><option value="16">16</option><option value="16 Pro">16 Pro</option><option value="16 Pro Max">16 Pro Max</option><option value="17">17</option><option value="17 Pro">17 Pro</option><option value="17 Pro Max">17 Pro Max</option>
                            </select>
                        </div>
                        
                    </div>
                    <div>
                        <label class="block text-xs font-bold mb-1 uppercase text-outline">ข้อความ (6 ตัวแรกฟรี, ต่อไป +5 THB)</label>
                        <input type="text" id="text_1" value="" oninput="updateAllUI()" placeholder="ใส่ข้อความ..." class="w-full rounded-lg border-outline-variant text-sm py-2 focus:ring-navy-luxe focus:border-navy-luxe">
                    </div>
                
                    <div class="pt-2">
                        <p class="text-xs font-bold mb-3 uppercase text-navy-luxe border-l-4 border-navy-luxe pl-2">ของตกแต่ง (iPad ราคา x2)</p>
                        <div class="flex flex-wrap gap-x-2 gap-y-3">
                
                            <div class="flex flex-col gap-1 min-w-[80px]">
                                <label class="flex items-center gap-1.5 bg-surface-container px-3 py-2 rounded-full cursor-pointer hover:bg-navy-luxe hover:text-white transition-all border border-transparent has-[:checked]:border-navy-luxe has-[:checked]:bg-navy-luxe has-[:checked]:text-white">
                                    <input type="checkbox" id="decor_1_โบว์" onchange="updateAllUI()" class="hidden">
                                    <span class="text-[11px] font-medium leading-none">โบว์</span>
                                    <span class="text-[9px] opacity-60 leading-none">+5</span>
                                </label>
                                
                            </div>
                        
                            <div class="flex flex-col gap-1 min-w-[80px]">
                                <label class="flex items-center gap-1.5 bg-surface-container px-3 py-2 rounded-full cursor-pointer hover:bg-navy-luxe hover:text-white transition-all border border-transparent has-[:checked]:border-navy-luxe has-[:checked]:bg-navy-luxe has-[:checked]:text-white">
                                    <input type="checkbox" id="decor_1_หัวใจ" onchange="updateAllUI()" class="hidden">
                                    <span class="text-[11px] font-medium leading-none">หัวใจ</span>
                                    <span class="text-[9px] opacity-60 leading-none">+5</span>
                                </label>
                                
                            </div>
                        
                            <div class="flex flex-col gap-1 min-w-[80px]">
                                <label class="flex items-center gap-1.5 bg-surface-container px-3 py-2 rounded-full cursor-pointer hover:bg-navy-luxe hover:text-white transition-all border border-transparent has-[:checked]:border-navy-luxe has-[:checked]:bg-navy-luxe has-[:checked]:text-white">
                                    <input type="checkbox" id="decor_1_จุด" onchange="updateAllUI()" class="hidden">
                                    <span class="text-[11px] font-medium leading-none">จุด</span>
                                    <span class="text-[9px] opacity-60 leading-none">+5</span>
                                </label>
                                
                            </div>
                        
                            <div class="flex flex-col gap-1 min-w-[80px]">
                                <label class="flex items-center gap-1.5 bg-surface-container px-3 py-2 rounded-full cursor-pointer hover:bg-navy-luxe hover:text-white transition-all border border-transparent has-[:checked]:border-navy-luxe has-[:checked]:bg-navy-luxe has-[:checked]:text-white">
                                    <input type="checkbox" id="decor_1_วิ้ง" onchange="updateAllUI()" class="hidden">
                                    <span class="text-[11px] font-medium leading-none">วิ้ง</span>
                                    <span class="text-[9px] opacity-60 leading-none">+5</span>
                                </label>
                                
                            </div>
                        
                            <div class="flex flex-col gap-1 min-w-[80px]">
                                <label class="flex items-center gap-1.5 bg-surface-container px-3 py-2 rounded-full cursor-pointer hover:bg-navy-luxe hover:text-white transition-all border border-transparent has-[:checked]:border-navy-luxe has-[:checked]:bg-navy-luxe has-[:checked]:text-white">
                                    <input type="checkbox" id="decor_1_ดาว" onchange="updateAllUI()" class="hidden">
                                    <span class="text-[11px] font-medium leading-none">ดาว</span>
                                    <span class="text-[9px] opacity-60 leading-none">+5</span>
                                </label>
                                
                            </div>
                        
                            <div class="flex flex-col gap-1 min-w-[80px]">
                                <label class="flex items-center gap-1.5 bg-surface-container px-3 py-2 rounded-full cursor-pointer hover:bg-navy-luxe hover:text-white transition-all border border-transparent has-[:checked]:border-navy-luxe has-[:checked]:bg-navy-luxe has-[:checked]:text-white">
                                    <input type="checkbox" id="decor_1_ปีกนางฟ้า_1_ข้าง" onchange="updateAllUI()" class="hidden">
                                    <span class="text-[11px] font-medium leading-none">ปีกนางฟ้า 1 ข้าง</span>
                                    <span class="text-[9px] opacity-60 leading-none">+5</span>
                                </label>
                                
                            </div>
                        
                            <div class="flex flex-col gap-1 min-w-[80px]">
                                <label class="flex items-center gap-1.5 bg-surface-container px-3 py-2 rounded-full cursor-pointer hover:bg-navy-luxe hover:text-white transition-all border border-transparent has-[:checked]:border-navy-luxe has-[:checked]:bg-navy-luxe has-[:checked]:text-white">
                                    <input type="checkbox" id="decor_1_ผีเสื้อ_1" onchange="updateAllUI()" class="hidden">
                                    <span class="text-[11px] font-medium leading-none">ผีเสื้อ 1</span>
                                    <span class="text-[9px] opacity-60 leading-none">+10</span>
                                </label>
                                
                            </div>
                        
                            <div class="flex flex-col gap-1 min-w-[80px]">
                                <label class="flex items-center gap-1.5 bg-surface-container px-3 py-2 rounded-full cursor-pointer hover:bg-navy-luxe hover:text-white transition-all border border-transparent has-[:checked]:border-navy-luxe has-[:checked]:bg-navy-luxe has-[:checked]:text-white">
                                    <input type="checkbox" id="decor_1_ผีเสื้อ_2" onchange="updateAllUI()" class="hidden">
                                    <span class="text-[11px] font-medium leading-none">ผีเสื้อ 2</span>
                                    <span class="text-[9px] opacity-60 leading-none">+10</span>
                                </label>
                                
                            </div>
                        
                            <div class="flex flex-col gap-1 min-w-[80px]">
                                <label class="flex items-center gap-1.5 bg-surface-container px-3 py-2 rounded-full cursor-pointer hover:bg-navy-luxe hover:text-white transition-all border border-transparent has-[:checked]:border-navy-luxe has-[:checked]:bg-navy-luxe has-[:checked]:text-white">
                                    <input type="checkbox" id="decor_1_ดอกไม้" onchange="updateAllUI()" class="hidden">
                                    <span class="text-[11px] font-medium leading-none">ดอกไม้</span>
                                    <span class="text-[9px] opacity-60 leading-none">+10</span>
                                </label>
                                
                            </div>
                        
                            <div class="flex flex-col gap-1 min-w-[80px]">
                                <label class="flex items-center gap-1.5 bg-surface-container px-3 py-2 rounded-full cursor-pointer hover:bg-navy-luxe hover:text-white transition-all border border-transparent has-[:checked]:border-navy-luxe has-[:checked]:bg-navy-luxe has-[:checked]:text-white">
                                    <input type="checkbox" id="decor_1_ไม้กางเขน" onchange="updateAllUI()" class="hidden">
                                    <span class="text-[11px] font-medium leading-none">ไม้กางเขน</span>
                                    <span class="text-[9px] opacity-60 leading-none">+10</span>
                                </label>
                                
                            </div>
                        
                            <div class="flex flex-col gap-1 min-w-[80px]">
                                <label class="flex items-center gap-1.5 bg-surface-container px-3 py-2 rounded-full cursor-pointer hover:bg-navy-luxe hover:text-white transition-all border border-transparent has-[:checked]:border-navy-luxe has-[:checked]:bg-navy-luxe has-[:checked]:text-white">
                                    <input type="checkbox" id="decor_1_เชอร์รี่" onchange="updateAllUI()" class="hidden">
                                    <span class="text-[11px] font-medium leading-none">เชอร์รี่</span>
                                    <span class="text-[9px] opacity-60 leading-none">+10</span>
                                </label>
                                
                            </div>
                        
                            <div class="flex flex-col gap-1 min-w-[80px]">
                                <label class="flex items-center gap-1.5 bg-surface-container px-3 py-2 rounded-full cursor-pointer hover:bg-navy-luxe hover:text-white transition-all border border-transparent has-[:checked]:border-navy-luxe has-[:checked]:bg-navy-luxe has-[:checked]:text-white">
                                    <input type="checkbox" id="decor_1_กระต่าย" onchange="updateAllUI()" class="hidden">
                                    <span class="text-[11px] font-medium leading-none">กระต่าย</span>
                                    <span class="text-[9px] opacity-60 leading-none">+10</span>
                                </label>
                                
                            </div>
                        
                            <div class="flex flex-col gap-1 min-w-[80px]">
                                <label class="flex items-center gap-1.5 bg-surface-container px-3 py-2 rounded-full cursor-pointer hover:bg-navy-luxe hover:text-white transition-all border border-transparent has-[:checked]:border-navy-luxe has-[:checked]:bg-navy-luxe has-[:checked]:text-white">
                                    <input type="checkbox" id="decor_1_ปีกนางฟ้า_2_ข้าง" onchange="updateAllUI()" class="hidden">
                                    <span class="text-[11px] font-medium leading-none">ปีกนางฟ้า 2 ข้าง</span>
                                    <span class="text-[9px] opacity-60 leading-none">+10</span>
                                </label>
                                
                            </div>
                        
                            <div class="flex flex-col gap-1 min-w-[80px]">
                                <label class="flex items-center gap-1.5 bg-surface-container px-3 py-2 rounded-full cursor-pointer hover:bg-navy-luxe hover:text-white transition-all border border-transparent has-[:checked]:border-navy-luxe has-[:checked]:bg-navy-luxe has-[:checked]:text-white">
                                    <input type="checkbox" id="decor_1_มายเมโลดี้" onchange="updateAllUI()" class="hidden">
                                    <span class="text-[11px] font-medium leading-none">มายเมโลดี้</span>
                                    <span class="text-[9px] opacity-60 leading-none">+30</span>
                                </label>
                                
                            </div>
                        
                            <div class="flex flex-col gap-1 min-w-[80px]">
                                <label class="flex items-center gap-1.5 bg-surface-container px-3 py-2 rounded-full cursor-pointer hover:bg-navy-luxe hover:text-white transition-all border border-transparent has-[:checked]:border-navy-luxe has-[:checked]:bg-navy-luxe has-[:checked]:text-white">
                                    <input type="checkbox" id="decor_1_ชบา" onchange="updateAllUI()" class="hidden">
                                    <span class="text-[11px] font-medium leading-none">ชบา</span>
                                    <span class="text-[9px] opacity-60 leading-none">+30</span>
                                </label>
                                
                            </div>
                        
                            <div class="flex flex-col gap-1 min-w-[80px]">
                                <label class="flex items-center gap-1.5 bg-surface-container px-3 py-2 rounded-full cursor-pointer hover:bg-navy-luxe hover:text-white transition-all border border-transparent has-[:checked]:border-navy-luxe has-[:checked]:bg-navy-luxe has-[:checked]:text-white">
                                    <input type="checkbox" id="decor_1_คิตตี้" onchange="updateAllUI()" class="hidden">
                                    <span class="text-[11px] font-medium leading-none">คิตตี้</span>
                                    <span class="text-[9px] opacity-60 leading-none">+30</span>
                                </label>
                                
                            </div>
                        
                            <div class="flex flex-col gap-1 min-w-[80px]">
                                <label class="flex items-center gap-1.5 bg-surface-container px-3 py-2 rounded-full cursor-pointer hover:bg-navy-luxe hover:text-white transition-all border border-transparent has-[:checked]:border-navy-luxe has-[:checked]:bg-navy-luxe has-[:checked]:text-white">
                                    <input type="checkbox" id="decor_1_จุด/วิ้ง" onchange="updateAllUI()" class="hidden">
                                    <span class="text-[11px] font-medium leading-none">จุด/วิ้ง</span>
                                    <span class="text-[9px] opacity-60 leading-none">+5</span>
                                </label>
                                
                            </div>
                        </div></div>
                    <div class="pt-4 border-t border-dashed border-primary-container">
                        <label class="block text-xs font-bold mb-2 uppercase text-outline">การเคลือบ (Coating)</label>
                        <div class="flex gap-6">
                            <label class="flex items-center gap-2 cursor-pointer group">
                                <input type="radio" name="coating_1" value="0" checked="" onchange="updateAllUI()" class="text-navy-luxe focus:ring-navy-luxe w-4 h-4">
                                <span class="text-sm font-medium group-hover:text-navy-luxe transition-colors">ไม่เคลือบ (+0)</span>
                            </label>
                            <label class="flex items-center gap-2 cursor-pointer group">
                                <input type="radio" name="coating_1" value="20" onchange="updateAllUI()" class="text-navy-luxe focus:ring-navy-luxe w-4 h-4">
                                <span class="text-sm font-medium group-hover:text-navy-luxe transition-colors">เคลือบ (+20 THB)</span>
                            </label>
                        </div>
                    </div>
                </div>
        </section>
        </div>
</div>
<!-- Right Side: Summary Sticky -->
<aside class="lg:sticky lg:top-[100px]">
<div class="p-md rounded-2xl shadow-xl border-2 relative overflow-hidden bg-primary-fixed text-on-primary-fixed border-navy-luxe" id="bill-card">
<div class="absolute -top-4 -right-4 opacity-10 rotate-12 pointer-events-none">
<span class="material-symbols-outlined text-9xl text-navy-luxe">shopping_cart</span>
</div>
<h3 class="font-headline-md mb-md flex items-center gap-2 text-navy-luxe">
<span class="material-symbols-outlined">receipt_long</span>
                    บิลของคุณ
                </h3>
<div class="space-y-sm mb-md border-b pb-md max-h-[50vh] overflow-y-auto pr-2 custom-scrollbar border-navy-luxe/20" id="summary-items">
<!-- Dynamic Summary Lines -->
</div>
<div class="space-y-xs mb-md">
<div class="flex justify-between font-body-md text-navy-luxe/80">
<span class="">ค่าจัดส่ง (เหมาจ่าย)</span>
<span class="">50 THB</span>
</div>
</div>
<div class="flex justify-between items-center bg-white p-4 rounded-xl border border-navy-luxe/10">
<span class="font-headline-md text-navy-luxe">ยอดรวม</span>
<div class="text-right">
<span class="font-headline-lg text-navy-luxe leading-tight block" id="total-price">0</span>
<span class="text-[10px] uppercase font-bold text-outline">THB (Net)</span>
</div>
</div>
<div class="mt-md space-y-3">
<button class="w-full font-bold py-3 rounded-xl shadow-sm hover:bg-navy-luxe/5 transition-all flex items-center justify-center gap-2 bg-navy-luxe text-white" onclick="saveBillImage()">
<span class="material-symbols-outlined">download</span>
                        บันทึกรูปบิล
                    </button>
<a class="w-full bg-navy-luxe text-white font-headline-md py-4 rounded-xl shadow-lg hover:brightness-110 squishy-btn flex items-center justify-center gap-2 decoration-none no-underline" href="https://lin.ee/vtj36AZ" target="_blank">
                        สั่งซื้อเลย 🎀
                    </a>
</div><div class="mt-4 p-3 bg-white/40 rounded-xl border border-navy-luxe/20 text-center">
<p class="text-sm text-navy-luxe font-bold leading-relaxed">
        กดบันทึกรูปบิลแล้วกดสั่งซื้อสินค้า <br>
        แล้วให้ลูกค้าส่งรูปบิลที่เซฟให้กับร้าน 🎀
    </p>
</div>
</div>
<!-- Ad/Visual Card -->
<a class="mt-md bg-white border border-primary-fixed p-4 rounded-xl flex items-center gap-4 group cursor-pointer overflow-hidden shadow-sm hover:shadow-md transition-shadow" href="https://www.tiktok.com/@babycoquettie" target="_blank">
<div class="w-16 h-16 rounded-full bg-navy-luxe overflow-hidden shrink-0 flex items-center justify-center">
<img alt="Review" class="w-full h-full object-cover group-hover:scale-110 transition-transform" src="https://lh3.googleusercontent.com/aida-public/AB6AXuCB_6EwRP-je1Iz0kcHaJm9FbWbzyzg0Sm2U7fNN0bDlhQVPTJZrPyfdiY37oAzSzGLPMRhYw87Wc2EmvI8YZLww1XYo4LyhRj_VLI8A131UnUnz3V35GVdb0TauufjhIAVmw1M7hWO952lXZRQSkoaBeM5Jz3od3Mzd7qY3Ku1gx66Jb8gvgB5iIJeSOc-sFwC1BvFhU_QlAjnyWIhq4TRVxLZQDOTAeVxomqJGrwzZ-0YSKeocYZaAUlgQoukVuYeKYmhoc08KAs">
</div>
<div>
<p class="font-bold text-navy-luxe">รีวิวสินค้า</p>
<p class="text-xs text-outline">TikTok: @babycoquettie</p>
</div>
</a>
</aside>
</div>
</main>
<footer class="w-full mt-xl bg-navy-luxe text-white flex flex-col md:flex-row justify-between items-center px-margin-desktop py-lg gap-base">
<div class="flex flex-col items-center md:items-start gap-1">
<span class="text-primary-fixed font-headline-md">Baby Coquette</span>
<span class="text-primary-fixed/60 text-body-md">© 2024 Baby Coquette Shop - Crafted with Luxe &amp; Love</span>
</div>
<div class="flex gap-md">
<a class="text-primary-fixed/60 hover:text-white transition-colors" href="#">นโยบายความเป็นส่วนตัว</a>
</div>
</footer>
<script>
    const CONFIG = {
        iphone: {
            label: "iPhone",
            basePrice: 199,
            coatingPrice: 20,
            models: ["XR", "11", "11 Pro", "11 Pro Max", "12", "12 Pro", "12 Pro Max", "13", "13 Pro", "13 Pro Max", "14", "14 Pro", "14 Pro Max", "15", "15 Pro", "15 Pro Max", "16", "16 Pro", "16 Pro Max", "17", "17 Pro", "17 Pro Max"],
            decorPriceMult: 1
        },
        ipad: {
            label: "iPad",
            basePrice: 289,
            coatingPrice: 30,
            models: ["mini 6", "mini 7", "Air 4", "Air 5", "Air 6", "Air 7", "Gen 7", "Gen 8", "Gen 9", "Gen 10", "Gen 11", "Pro 11", "Pro 12.9"],
            caseColors: ["Black", "White", "Pink", "Blue", "Purple", "Grey"],
            decorPriceMult: 2
        },
        film: {
            label: "Film",
            basePrice: 150,
            models: ["Fuji Simple Ace", "Kodak FunSaver", "Custom Film 1", "Custom Film 2"]
        },
        decorations: {
            cat_a: { name: "หมวด A", items: ["โบว์", "หัวใจ", "จุด", "วิ้ง", "ดาว", "ปีกนางฟ้า 1 ข้าง"], price: 5, colors: ["Clear", "Pink", "Black"] },
            cat_b: { name: "หมวด B", items: ["ผีเสื้อ 1", "ผีเสื้อ 2", "ดอกไม้", "ไม้กางเขน", "เชอร์รี่", "กระต่าย", "ปีกนางฟ้า 2 ข้าง"], price: 10, colors: ["Clear", "Pink", "Black"] },
            cat_c: { name: "หมวด C", items: ["มายเมโลดี้", "ชบา", "คิตตี้"], price: 30, 
                specialColors: {
                    "คิตตี้": ["Clear Bow Pink", "Clear", "Pink", "Black"],
                    "มายเมโลดี้": ["Pink Head White Face", "Pink", "White", "Black"],
                    "ชบา": ["Clear", "Pink", "Black"]
                }
            },
            cat_special: { name: "ลวดลาย", items: ["จุด/วิ้ง"], price: 5, colors: ["Clear", "Pink", "Black", "Mixed White Pink"] }
        }
    };

    let states = {};

    function saveState() {
        const forms = document.querySelectorAll('.item-form');
        forms.forEach(form => {
            const id = form.dataset.id;
            const typeInput = form.querySelector(`input[name="type_${id}"]:checked`);
            const type = typeInput ? typeInput.value : 'iphone';
            const model = document.getElementById(`model_${id}`)?.value;
            const color = document.getElementById(`color_${id}`)?.value;
            const text = document.getElementById(`text_${id}`)?.value;
            const coatingInput = form.querySelector(`input[name="coating_${id}"]:checked`);
            const coating = coatingInput ? coatingInput.value : "0";
            
            const decors = {};
            Object.keys(CONFIG.decorations).forEach(catKey => {
                CONFIG.decorations[catKey].items.forEach(item => {
                    const itemKey = item.replace(/\s+/g, '_');
                    const checkbox = document.getElementById(`decor_${id}_${itemKey}`);
                    const colorSelect = document.getElementById(`color_pick_${id}_${itemKey}`);
                    if (checkbox) {
                        decors[itemKey] = {
                            checked: checkbox.checked,
                            color: colorSelect ? colorSelect.value : null
                        };
                    }
                });
            });

            states[id] = { type, model, color, text, coating, decors };
        });
    }

    function changeQty(delta) {
        const input = document.getElementById('global-qty');
        let val = parseInt(input.value) + delta;
        if (val < 1) val = 1;
        if (val > 10) val = 10;
        input.value = val;
        generateItemForms();
    }

    function generateItemForms() {
        saveState();
        const qty = parseInt(document.getElementById('global-qty').value);
        const container = document.getElementById('items-container');
        
        container.innerHTML = '';
        for (let i = 1; i <= qty; i++) {
            const data = states[i] || { type: 'iphone' };
            container.innerHTML += createItemHTML(i, data);
        }
        updateAllUI();
    }

    function createItemHTML(id, data) {
        return `
        <section class="bg-white p-md rounded-xl border border-primary-fixed shadow-sm item-form" data-id="${id}">
            <header class="flex items-center justify-between mb-md border-b border-surface-variant pb-base">
                <h2 class="font-headline-md text-navy-luxe flex items-center gap-2">
                    <span class="material-symbols-outlined text-secondary">shopping_basket</span>
                    ชิ้นที่ ${id}
                </h2>
                <span class="text-xs uppercase font-bold text-outline-variant">การตั้งค่า</span>
            </header>
            
            <div class="grid grid-cols-3 gap-2 mb-md">
                ${['iphone', 'ipad', 'film'].map(t => `
                    <label class="cursor-pointer group">
                        <input type="radio" name="type_${id}" value="${t}" ${data.type === t ? 'checked' : ''} onchange="updateAllUI()" class="hidden peer">
                        <div class="peer-checked:bg-navy-luxe peer-checked:text-white peer-checked:border-navy-luxe p-3 border border-outline-variant rounded-lg text-center transition-all hover:border-navy-luxe">
                            <span class="material-symbols-outlined block text-xl mb-1">${t === 'iphone' ? 'smartphone' : t === 'ipad' ? 'tablet_mac' : 'photo_camera'}</span>
                            <span class="text-[10px] uppercase font-bold leading-none">${CONFIG[t].label}</span>
                        </div>
                    </label>
                `).join('')}
            </div>

            <div id="details_${id}" class="space-y-md">
                <!-- Dynamic Content -->
            </div>
        </section>
        `;
    }

    function updateAllUI() {
        const forms = document.querySelectorAll('.item-form');
        let total = 50; 
        let summaryHtml = '';

        forms.forEach(form => {
            const id = form.dataset.id;
            const typeInput = form.querySelector(`input[name="type_${id}"]:checked`);
            if (!typeInput) return;
            const type = typeInput.value;
            const details = form.querySelector(`#details_${id}`);
            const state = states[id] || {};
            
            let itemTotal = 0;
            let itemSummary = `
                <div class="p-3 bg-white/40 rounded-xl mb-3 border border-navy-luxe/10 shadow-sm">
                    <div class="flex justify-between font-bold text-navy-luxe mb-1 border-b border-navy-luxe/5 pb-1">
                        <span class="flex items-center gap-1">
                            <span class="material-symbols-outlined text-sm">label</span>
                            ชิ้นที่ ${id}: ${CONFIG[type].label}
                        </span>
                        <span id="price_val_${id}">0 THB</span>
                    </div>`;

            if (type === 'film') {
                itemTotal = CONFIG.film.basePrice;
                const currentModel = state.model || CONFIG.film.models[0];
                details.innerHTML = `
                    <div class="grid grid-cols-1 gap-md">
                        <div>
                            <label class="block text-xs font-bold mb-1 uppercase text-outline">เลือกรุ่นกล้อง</label>
                            <select id="model_${id}" onchange="updateAllUI()" class="w-full rounded-lg border-outline-variant text-sm py-2 focus:ring-navy-luxe focus:border-navy-luxe">
                                ${CONFIG.film.models.map(m => `<option value="${m}" ${m === currentModel ? 'selected' : ''}>${m}</option>`).join('')}
                            </select>
                        </div>
                    </div>
                `;
                itemSummary += `<div class="text-[11px] text-navy-luxe/70 flex justify-between"><span>ราคาเริ่มต้น</span><span>${itemTotal} THB</span></div>`;
            } else {
                const config = CONFIG[type];
                itemTotal = config.basePrice;
                
                const currentModel = (states[id]?.type === type) ? (states[id]?.model || config.models[0]) : config.models[0];
                const currentColor = (states[id]?.type === type) ? (states[id]?.color || (type === 'ipad' ? config.caseColors[0] : '')) : (type === 'ipad' ? config.caseColors[0] : '');
                const currentText = (states[id]?.type === type) ? (states[id]?.text || '') : '';
                
                let fieldsHtml = `
                    <div class="grid grid-cols-2 gap-md">
                        <div>
                            <label class="block text-xs font-bold mb-1 uppercase text-outline">รุ่นสินค้า</label>
                            <select id="model_${id}" onchange="updateAllUI()" class="w-full rounded-lg border-outline-variant text-sm py-2 focus:ring-navy-luxe focus:border-navy-luxe">
                                ${config.models.map(m => `<option value="${m}" ${m === currentModel ? 'selected' : ''}>${m}</option>`).join('')}
                            </select>
                        </div>
                        ${type === 'ipad' ? `
                            <div>
                                <label class="block text-xs font-bold mb-1 uppercase text-outline">สีเคส</label>
                                <select id="color_${id}" onchange="updateAllUI()" class="w-full rounded-lg border-outline-variant text-sm py-2 focus:ring-navy-luxe focus:border-navy-luxe">
                                    ${config.caseColors.map(c => `<option value="${c}" ${c === currentColor ? 'selected' : ''}>${c}</option>`).join('')}
                                </select>
                            </div>
                        ` : ''}
                    </div>
                    <div>
                        <label class="block text-xs font-bold mb-1 uppercase text-outline">ข้อความ (6 ตัวแรกฟรี, ต่อไป +5 THB)</label>
                        <input type="text" id="text_${id}" value="${currentText}" oninput="updateAllUI()" placeholder="ใส่ข้อความ..." class="w-full rounded-lg border-outline-variant text-sm py-2 focus:ring-navy-luxe focus:border-navy-luxe">
                    </div>
                `;

                itemSummary += `<div class="text-[11px] text-navy-luxe/70 flex justify-between"><span>ราคาเริ่มต้น: ${currentModel} ${currentColor ? '('+currentColor+')' : ''}</span><span>${config.basePrice} THB</span></div>`;

                if(currentText.length > 6) {
                    const extraChars = currentText.length - 6;
                    const extraPrice = extraChars * 5;
                    itemTotal += extraPrice;
                    itemSummary += `<div class="text-[11px] text-navy-luxe/70 flex justify-between"><span>ข้อความส่วนเกิน (+${extraChars})</span><span>+${extraPrice} THB</span></div>`;
                }

                fieldsHtml += `
                    <div class="pt-2">
                        <p class="text-xs font-bold mb-3 uppercase text-navy-luxe border-l-4 border-navy-luxe pl-2">ของตกแต่ง (iPad ราคา x2)</p>
                        <div class="flex flex-wrap gap-x-2 gap-y-3">
                `;

                Object.keys(CONFIG.decorations).forEach(catKey => {
                    const cat = CONFIG.decorations[catKey];
                    cat.items.forEach(item => {
                        const itemKey = item.replace(/\s+/g, '_');
                        const isChecked = (states[id]?.type === type) ? (states[id]?.decors?.[itemKey]?.checked) : false;
                        const price = cat.price * config.decorPriceMult;
                        
                        fieldsHtml += `
                            <div class="flex flex-col gap-1 min-w-[80px]">
                                <label class="flex items-center gap-1.5 bg-surface-container px-3 py-2 rounded-full cursor-pointer hover:bg-navy-luxe hover:text-white transition-all border border-transparent has-[:checked]:border-navy-luxe has-[:checked]:bg-navy-luxe has-[:checked]:text-white">
                                    <input type="checkbox" id="decor_${id}_${itemKey}" onchange="updateAllUI()" ${isChecked ? 'checked' : ''} class="hidden">
                                    <span class="text-[11px] font-medium leading-none">${item}</span>
                                    <span class="text-[9px] opacity-60 leading-none">+${price}</span>
                                </label>
                                ${isChecked ? createColorPicker(id, item, catKey) : ''}
                            </div>
                        `;

                        if (isChecked) {
                            itemTotal += price;
                            const colorSelect = document.getElementById(`color_pick_${id}_${itemKey}`);
                            const selectedColor = colorSelect ? colorSelect.value : (cat.colors ? cat.colors[0] : 'Default');
                            itemSummary += `<div class="text-[11px] text-navy-luxe/70 flex justify-between"><span>• ${item} (${selectedColor})</span><span>+${price} THB</span></div>`;
                        }
                    });
                });

                fieldsHtml += `</div></div>`;

                const currentCoating = (states[id]?.type === type) ? (states[id]?.coating || "0") : "0";
                fieldsHtml += `
                    <div class="pt-4 border-t border-dashed border-primary-container">
                        <label class="block text-xs font-bold mb-2 uppercase text-outline">การเคลือบ (Coating)</label>
                        <div class="flex gap-6">
                            <label class="flex items-center gap-2 cursor-pointer group">
                                <input type="radio" name="coating_${id}" value="0" ${currentCoating === "0" ? 'checked' : ''} onchange="updateAllUI()" class="text-navy-luxe focus:ring-navy-luxe w-4 h-4">
                                <span class="text-sm font-medium group-hover:text-navy-luxe transition-colors">ไม่เคลือบ (+0)</span>
                            </label>
                            <label class="flex items-center gap-2 cursor-pointer group">
                                <input type="radio" name="coating_${id}" value="${config.coatingPrice}" ${currentCoating == config.coatingPrice ? 'checked' : ''} onchange="updateAllUI()" class="text-navy-luxe focus:ring-navy-luxe w-4 h-4">
                                <span class="text-sm font-medium group-hover:text-navy-luxe transition-colors">เคลือบ (+${config.coatingPrice} THB)</span>
                            </label>
                        </div>
                    </div>
                `;

                const coatingRadio = form.querySelector(`input[name="coating_${id}"]:checked`);
                const coatingValue = coatingRadio ? parseInt(coatingRadio.value) : 0;
                if(coatingValue > 0) {
                    itemTotal += coatingValue;
                    itemSummary += `<div class="text-[11px] text-navy-luxe/70 flex justify-between"><span>การเคลือบ (Coating)</span><span>+${coatingValue} THB</span></div>`;
                }

                details.innerHTML = fieldsHtml;
            }

            itemSummary += `</div>`;
            summaryHtml += itemSummary;
            total += itemTotal;
            document.getElementById(`price_val_${id}`).innerText = `${itemTotal} THB`;
        });

        document.getElementById('summary-items').innerHTML = summaryHtml;
        document.getElementById('total-price').innerText = total;
        
        saveState();
    }

    function createColorPicker(id, item, catKey) {
        const itemKey = item.replace(/\s+/g, '_');
        const cat = CONFIG.decorations[catKey];
        let options = cat.colors || [];
        
        if (cat.specialColors && cat.specialColors[item]) {
            options = cat.specialColors[item];
        }

        if (options.length === 0) return '';

        const savedColor = (states[id] && states[id].decors && states[id].decors[itemKey]) ? states[id].decors[itemKey].color : options[0];

        return `
            <select id="color_pick_${id}_${itemKey}" onchange="updateAllUI()" class="text-[10px] p-1 h-7 rounded border-outline-variant bg-white w-full outline-none focus:border-navy-luxe transition-colors">
                ${options.map(o => `<option value="${o}" ${o === savedColor ? 'selected' : ''}>${o}</option>`).join('')}
            </select>
        `;
    }

    async function saveBillImage() {
        const element = document.getElementById('bill-card');
        const buttons = element.querySelectorAll('button, a');
        buttons.forEach(b => b.style.opacity = '0');
        
        const canvas = await html2canvas(element, {
            backgroundColor: '#ffffff',
            scale: 2,
            logging: false,
            useCORS: true
        });

        buttons.forEach(b => b.style.opacity = '1');

        const link = document.createElement('a');
        link.download = `BabyCoquette_Bill_${Date.now()}.png`;
        link.href = canvas.toDataURL('image/png');
        link.click();
    }

    document.addEventListener('DOMContentLoaded', () => {
        generateItemForms();
    });
</script>




</body></html>
