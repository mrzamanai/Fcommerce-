
<!DOCTYPE html>

<html class="light" lang="en"><head>
<meta charset="utf-8"/>
<meta content="width=device-width, initial-scale=1.0" name="viewport"/>
<title>F-Com Auto Dashboard</title>
<script src="https://cdn.tailwindcss.com?plugins=forms,container-queries"></script>
<link href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:wght,FILL@100..700,0..1&amp;display=swap" rel="stylesheet"/>
<link href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:wght,FILL@100..700,0..1&amp;display=swap" rel="stylesheet"/>
<script id="tailwind-config">
        tailwind.config = {
            darkMode: "class",
            theme: {
                extend: {
                    colors: {
                        "primary": "#137fec",
                        "background-light": "#f6f7f8",
                        "background-dark": "#101922",
                    },
                    fontFamily: {
                        "display": ["Manrope", "Noto Sans", "sans-serif"]
                    },
                    borderRadius: {"DEFAULT": "0.25rem", "lg": "0.5rem", "xl": "0.75rem", "full": "9999px"},
                },
            },
        }
    </script>
<style>
        /* Custom scrollbar for better aesthetics */
        ::-webkit-scrollbar {
            width: 8px;
            height: 8px;
        }
        ::-webkit-scrollbar-track {
            background: transparent; 
        }
        ::-webkit-scrollbar-thumb {
            background: #cbd5e1; 
            border-radius: 4px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #94a3b8; 
        }
    </style>
</head>
<body class="bg-background-light dark:bg-background-dark font-display text-slate-900 dark:text-slate-100 overflow-hidden">
<div class="flex h-screen w-full">
<!-- Sidebar -->
<div class="w-64 flex-shrink-0 border-r border-slate-200 dark:border-slate-800 bg-white dark:bg-slate-900 flex flex-col justify-between p-4 h-full overflow-y-auto">
<div class="flex flex-col gap-6">
<!-- Branding / Profile -->
<div class="flex gap-3 items-center px-2">
<div class="bg-center bg-no-repeat bg-cover rounded-full size-10 border border-slate-200 dark:border-slate-700 shadow-sm" data-alt="Small business logo showing abstract shopping cart" style='background-image: url("https://lh3.googleusercontent.com/aida-public/AB6AXuBNamdmpGzSriAmso6hx3_sikT32njHvGy1DzhPBbtthzdjjjLtv5oeolEt4YD-tiBlILsns5Nfm9n1iOiLjNLxj8eXqdVjYPkqaj3FFPthXIjFBRepQoIrpexBU4EQ2Bot38BFi6WrH99-3oV5lImQUGPQcKXRJ-_CkBstt2WQ9nPrv29dptTmwFsIumpXWxM0Jj8vngTEGoE15cWUu4IIE8bKn4JCdmphOkbfNSh2BpZhlS2X7MaBAWzFicnz6ZPYWh0s2HTo6L2a");'></div>
<div class="flex flex-col">
<h1 class="text-slate-900 dark:text-white text-base font-bold leading-normal">F-Com Auto</h1>
<p class="text-slate-500 dark:text-slate-400 text-xs font-normal leading-normal">Business Pro</p>
</div>
</div>
<!-- Navigation -->
<nav class="flex flex-col gap-2">
<a class="flex items-center gap-3 px-3 py-2 rounded-lg bg-primary/10 text-primary dark:text-primary dark:bg-primary/20 group transition-colors" href="#">
<span class="material-symbols-outlined filled text-[24px]">dashboard</span>
<span class="text-sm font-semibold">Dashboard</span>
</a>
<a class="flex items-center gap-3 px-3 py-2 rounded-lg text-slate-700 dark:text-slate-300 hover:bg-slate-100 dark:hover:bg-slate-800 transition-colors" href="#">
<span class="material-symbols-outlined text-[24px]">shopping_bag</span>
<span class="text-sm font-medium">Orders</span>
</a>
<a class="flex items-center gap-3 px-3 py-2 rounded-lg text-slate-700 dark:text-slate-300 hover:bg-slate-100 dark:hover:bg-slate-800 transition-colors" href="#">
<span class="material-symbols-outlined text-[24px]">description</span>
<span class="text-sm font-medium">Invoices</span>
</a>
<a class="flex items-center gap-3 px-3 py-2 rounded-lg text-slate-700 dark:text-slate-300 hover:bg-slate-100 dark:hover:bg-slate-800 transition-colors" href="#">
<span class="material-symbols-outlined text-[24px]">group</span>
<span class="text-sm font-medium">Customers</span>
</a>
<a class="flex items-center gap-3 px-3 py-2 rounded-lg text-slate-700 dark:text-slate-300 hover:bg-slate-100 dark:hover:bg-slate-800 transition-colors" href="#">
<span class="material-symbols-outlined text-[24px]">inventory_2</span>
<span class="text-sm font-medium">Inventory</span>
</a>
<a class="flex items-center gap-3 px-3 py-2 rounded-lg text-slate-700 dark:text-slate-300 hover:bg-slate-100 dark:hover:bg-slate-800 transition-colors" href="#">
<span class="material-symbols-outlined text-[24px]">settings</span>
<span class="text-sm font-medium">Settings</span>
</a>
</nav>
</div>
<div class="flex flex-col gap-1 border-t border-slate-200 dark:border-slate-800 pt-4">
<a class="flex items-center gap-3 px-3 py-2 rounded-lg text-slate-700 dark:text-slate-300 hover:bg-slate-100 dark:hover:bg-slate-800 transition-colors" href="#">
<span class="material-symbols-outlined text-[24px]">logout</span>
<span class="text-sm font-medium">Log Out</span>
</a>
</div>
</div>
<!-- Main Content Area -->
<div class="flex-1 flex flex-col h-full overflow-hidden relative">
<!-- Header -->
<header class="h-16 border-b border-slate-200 dark:border-slate-800 bg-white dark:bg-slate-900 flex items-center justify-between px-6 lg:px-10 shrink-0 z-10">
<div class="flex items-center gap-4">
<!-- Mobile Toggle (Hidden on Desktop) -->
<button class="lg:hidden text-slate-500 hover:text-primary">
<span class="material-symbols-outlined">menu</span>
</button>
<!-- Search Bar -->
<div class="hidden md:flex items-center bg-slate-100 dark:bg-slate-800 rounded-lg px-3 py-2 w-64 lg:w-96 focus-within:ring-2 ring-primary/20">
<span class="material-symbols-outlined text-slate-400 text-[20px]">search</span>
<input class="bg-transparent border-none text-sm w-full focus:ring-0 text-slate-700 dark:text-slate-200 placeholder-slate-400" placeholder="Search orders, customers..." type="text"/>
</div>
</div>
<div class="flex items-center gap-4">
<button class="relative p-2 text-slate-500 dark:text-slate-400 hover:bg-slate-100 dark:hover:bg-slate-800 rounded-full transition-colors">
<span class="material-symbols-outlined text-[24px]">notifications</span>
<span class="absolute top-2 right-2 size-2 bg-red-500 rounded-full border-2 border-white dark:border-slate-900"></span>
</button>
<div class="h-8 w-px bg-slate-200 dark:bg-slate-700 mx-1"></div>
<div class="flex items-center gap-3 cursor-pointer hover:bg-slate-50 dark:hover:bg-slate-800 py-1 px-2 rounded-lg transition-colors">
<div class="size-8 rounded-full bg-slate-200 bg-cover bg-center" data-alt="User avatar profile picture" style='background-image: url("https://lh3.googleusercontent.com/aida-public/AB6AXuDUsZ7YGiZISjpjui9_uYyBSUMjO9eSI1UIL7NJ0-WpEra6DKR8YyK1l46rpvAKK_Kmi1FF1CO8fKCFhWax6eMc20jesZ7JzmKCQpssIgojqVQuOnEksF8FeGlISUFeYXv0BNCyE286FrmCbq90sRB_LUHH6mcRmThExywYYscyWKwkIayGSyJlL31920U9-JHvGMIoxUmw43TYkrQicYmUv1eMJt2c--jaWu6c5tATDl_XQyI62kRI1uGDzX4jGE1QzEGkHE3IIl65");'></div>
<div class="hidden lg:block text-sm">
<p class="font-medium text-slate-700 dark:text-slate-200">Rahim Store</p>
<p class="text-xs text-slate-500 dark:text-slate-400">Admin</p>
</div>
<span class="material-symbols-outlined text-slate-400 text-[20px] hidden lg:block">expand_more</span>
</div>
</div>
</header>
<!-- Scrollable Content -->
<main class="flex-1 overflow-y-auto bg-background-light dark:bg-background-dark p-6 lg:p-10">
<div class="max-w-[1280px] mx-auto flex flex-col gap-8">
<!-- Page Heading & Actions -->
<div class="flex flex-col sm:flex-row sm:items-end justify-between gap-4">
<div class="flex flex-col gap-1">
<h2 class="text-3xl font-bold text-slate-900 dark:text-white tracking-tight">Dashboard Overview</h2>
<p class="text-slate-500 dark:text-slate-400 text-base">Welcome back, here's what's happening today.</p>
</div>
<button class="bg-primary hover:bg-blue-600 text-white font-bold py-2.5 px-5 rounded-lg shadow-sm shadow-blue-200 dark:shadow-none flex items-center gap-2 transition-all active:scale-95 w-full sm:w-auto justify-center">
<span class="material-symbols-outlined text-[20px]">add</span>
<span>Create New Order</span>
</button>
</div>
<!-- Stats Grid -->
<div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-4">
<!-- Stat Card 1 -->
<div class="bg-white dark:bg-slate-800 rounded-xl p-5 border border-slate-200 dark:border-slate-700 shadow-sm flex flex-col gap-2 relative overflow-hidden group">
<div class="flex justify-between items-start z-10">
<div>
<p class="text-slate-500 dark:text-slate-400 text-sm font-medium">Total Sales Today</p>
<p class="text-slate-900 dark:text-white text-2xl font-bold mt-1">৳12,500</p>
</div>
<div class="bg-blue-50 dark:bg-slate-700 p-2 rounded-lg text-primary">
<span class="material-symbols-outlined">payments</span>
</div>
</div>
<div class="flex items-center gap-1 mt-2 z-10">
<span class="material-symbols-outlined text-green-600 text-[16px]">trending_up</span>
<span class="text-green-600 text-sm font-medium">+12%</span>
<span class="text-slate-400 text-xs ml-1">vs yesterday</span>
</div>
</div>
<!-- Stat Card 2 -->
<div class="bg-white dark:bg-slate-800 rounded-xl p-5 border border-slate-200 dark:border-slate-700 shadow-sm flex flex-col gap-2">
<div class="flex justify-between items-start">
<div>
<p class="text-slate-500 dark:text-slate-400 text-sm font-medium">Pending Confirmation</p>
<p class="text-slate-900 dark:text-white text-2xl font-bold mt-1">5</p>
</div>
<div class="bg-orange-50 dark:bg-slate-700 p-2 rounded-lg text-orange-500">
<span class="material-symbols-outlined">pending_actions</span>
</div>
</div>
<div class="flex items-center gap-1 mt-2">
<span class="material-symbols-outlined text-green-600 text-[16px]">trending_up</span>
<span class="text-green-600 text-sm font-medium">+2%</span>
<span class="text-slate-400 text-xs ml-1">new inquiries</span>
</div>
</div>
<!-- Stat Card 3 -->
<div class="bg-white dark:bg-slate-800 rounded-xl p-5 border border-slate-200 dark:border-slate-700 shadow-sm flex flex-col gap-2">
<div class="flex justify-between items-start">
<div>
<p class="text-slate-500 dark:text-slate-400 text-sm font-medium">To Be Shipped</p>
<p class="text-slate-900 dark:text-white text-2xl font-bold mt-1">12</p>
</div>
<div class="bg-purple-50 dark:bg-slate-700 p-2 rounded-lg text-purple-500">
<span class="material-symbols-outlined">local_shipping</span>
</div>
</div>
<div class="flex items-center gap-1 mt-2">
<span class="material-symbols-outlined text-red-500 text-[16px]">trending_down</span>
<span class="text-red-500 text-sm font-medium">-5%</span>
<span class="text-slate-400 text-xs ml-1">processing delay</span>
</div>
</div>
<!-- Stat Card 4 -->
<div class="bg-white dark:bg-slate-800 rounded-xl p-5 border border-slate-200 dark:border-slate-700 shadow-sm flex flex-col gap-2">
<div class="flex justify-between items-start">
<div>
<p class="text-slate-500 dark:text-slate-400 text-sm font-medium">Total Revenue</p>
<p class="text-slate-900 dark:text-white text-2xl font-bold mt-1">৳45,200</p>
</div>
<div class="bg-green-50 dark:bg-slate-700 p-2 rounded-lg text-green-600">
<span class="material-symbols-outlined">account_balance_wallet</span>
</div>
</div>
<div class="flex items-center gap-1 mt-2">
<span class="material-symbols-outlined text-green-600 text-[16px]">trending_up</span>
<span class="text-green-600 text-sm font-medium">+8%</span>
<span class="text-slate-400 text-xs ml-1">this week</span>
</div>
</div>
</div>
<!-- Quick Actions & Widgets -->
<div class="grid grid-cols-1 lg:grid-cols-3 gap-6">
<!-- Quick Actions -->
<div class="lg:col-span-2 flex flex-col gap-4">
<h3 class="text-lg font-bold text-slate-900 dark:text-white flex items-center gap-2">
<span class="material-symbols-outlined text-primary">bolt</span> Quick Actions
                            </h3>
<div class="grid grid-cols-1 sm:grid-cols-3 gap-4">
<button class="group bg-white dark:bg-slate-800 p-4 rounded-xl border border-slate-200 dark:border-slate-700 shadow-sm hover:border-primary/50 hover:shadow-md transition-all text-left">
<div class="bg-blue-50 dark:bg-slate-700 size-10 rounded-lg flex items-center justify-center text-primary mb-3 group-hover:scale-110 transition-transform">
<span class="material-symbols-outlined">content_paste</span>
</div>
<h4 class="font-bold text-slate-900 dark:text-white mb-1">Paste Order Details</h4>
<p class="text-sm text-slate-500 dark:text-slate-400">Parse text from Messenger directly</p>
</button>
<button class="group bg-white dark:bg-slate-800 p-4 rounded-xl border border-slate-200 dark:border-slate-700 shadow-sm hover:border-primary/50 hover:shadow-md transition-all text-left">
<div class="bg-green-50 dark:bg-slate-700 size-10 rounded-lg flex items-center justify-center text-green-600 mb-3 group-hover:scale-110 transition-transform">
<span class="material-symbols-outlined">add_shopping_cart</span>
</div>
<h4 class="font-bold text-slate-900 dark:text-white mb-1">Manual Order</h4>
<p class="text-sm text-slate-500 dark:text-slate-400">Create a fresh order form</p>
</button>
<button class="group bg-white dark:bg-slate-800 p-4 rounded-xl border border-slate-200 dark:border-slate-700 shadow-sm hover:border-primary/50 hover:shadow-md transition-all text-left">
<div class="bg-indigo-50 dark:bg-slate-700 size-10 rounded-lg flex items-center justify-center text-indigo-500 mb-3 group-hover:scale-110 transition-transform">
<span class="material-symbols-outlined">forum</span>
</div>
<h4 class="font-bold text-slate-900 dark:text-white mb-1">Unread Messages</h4>
<p class="text-sm text-slate-500 dark:text-slate-400">3 new inquiries waiting</p>
</button>
</div>
</div>
<!-- Pending Invoices Widget -->
<div class="lg:col-span-1 flex flex-col gap-4">
<div class="flex items-center justify-between">
<h3 class="text-lg font-bold text-slate-900 dark:text-white">Pending Invoices</h3>
<a class="text-sm text-primary font-medium hover:underline" href="#">View All</a>
</div>
<div class="bg-white dark:bg-slate-800 rounded-xl border border-slate-200 dark:border-slate-700 shadow-sm overflow-hidden flex flex-col divide-y divide-slate-100 dark:divide-slate-700">
<div class="p-4 flex items-center justify-between hover:bg-slate-50 dark:hover:bg-slate-700/50 transition-colors">
<div class="flex items-center gap-3">
<div class="bg-red-50 dark:bg-slate-700 p-2 rounded-lg text-red-500">
<span class="material-symbols-outlined text-[20px]">receipt_long</span>
</div>
<div>
<p class="font-semibold text-sm text-slate-900 dark:text-white">Inv #2024-91</p>
<p class="text-xs text-slate-500 dark:text-slate-400">Karim Khan</p>
</div>
</div>
<div class="text-right">
<p class="font-bold text-sm text-slate-900 dark:text-white">৳2,450</p>
<p class="text-[10px] text-red-500 font-medium">Overdue</p>
</div>
</div>
<div class="p-4 flex items-center justify-between hover:bg-slate-50 dark:hover:bg-slate-700/50 transition-colors">
<div class="flex items-center gap-3">
<div class="bg-orange-50 dark:bg-slate-700 p-2 rounded-lg text-orange-500">
<span class="material-symbols-outlined text-[20px]">receipt_long</span>
</div>
<div>
<p class="font-semibold text-sm text-slate-900 dark:text-white">Inv #2024-95</p>
<p class="text-xs text-slate-500 dark:text-slate-400">Sumaiya Akter</p>
</div>
</div>
<div class="text-right">
<p class="font-bold text-sm text-slate-900 dark:text-white">৳1,200</p>
<p class="text-[10px] text-orange-500 font-medium">Unpaid</p>
</div>
</div>
<div class="p-4 flex items-center justify-between hover:bg-slate-50 dark:hover:bg-slate-700/50 transition-colors">
<div class="flex items-center gap-3">
<div class="bg-orange-50 dark:bg-slate-700 p-2 rounded-lg text-orange-500">
<span class="material-symbols-outlined text-[20px]">receipt_long</span>
</div>
<div>
<p class="font-semibold text-sm text-slate-900 dark:text-white">Inv #2024-98</p>
<p class="text-xs text-slate-500 dark:text-slate-400">Rafiqul Islam</p>
</div>
</div>
<div class="text-right">
<p class="font-bold text-sm text-slate-900 dark:text-white">৳5,600</p>
<p class="text-[10px] text-orange-500 font-medium">Unpaid</p>
</div>
</div>
</div>
</div>
</div>
<!-- Recent Orders Table -->
<div class="flex flex-col gap-4">
<div class="flex items-center justify-between">
<h3 class="text-xl font-bold text-slate-900 dark:text-white">Recent Orders</h3>
<div class="flex gap-2">
<button class="px-3 py-1.5 text-sm font-medium text-slate-600 dark:text-slate-300 bg-white dark:bg-slate-800 border border-slate-200 dark:border-slate-700 rounded-lg shadow-sm hover:bg-slate-50 dark:hover:bg-slate-700 flex items-center gap-2">
<span class="material-symbols-outlined text-[18px]">filter_list</span> Filter
                                </button>
<button class="px-3 py-1.5 text-sm font-medium text-slate-600 dark:text-slate-300 bg-white dark:bg-slate-800 border border-slate-200 dark:border-slate-700 rounded-lg shadow-sm hover:bg-slate-50 dark:hover:bg-slate-700 flex items-center gap-2">
<span class="material-symbols-outlined text-[18px]">download</span> Export
                                </button>
</div>
</div>
<div class="bg-white dark:bg-slate-800 rounded-xl border border-slate-200 dark:border-slate-700 shadow-sm overflow-hidden">
<div class="overflow-x-auto">
<table class="w-full text-left text-sm text-slate-600 dark:text-slate-400">
<thead class="bg-slate-50 dark:bg-slate-900 text-xs uppercase font-semibold text-slate-500 dark:text-slate-400 border-b border-slate-200 dark:border-slate-700">
<tr>
<th class="px-6 py-4">Order ID</th>
<th class="px-6 py-4">Customer</th>
<th class="px-6 py-4">Date</th>
<th class="px-6 py-4">Payment Status</th>
<th class="px-6 py-4">Delivery Status</th>
<th class="px-6 py-4 text-right">Amount</th>
<th class="px-6 py-4 text-center">Action</th>
</tr>
</thead>
<tbody class="divide-y divide-slate-100 dark:divide-slate-700">
<tr class="hover:bg-slate-50 dark:hover:bg-slate-700/50 transition-colors group">
<td class="px-6 py-4 font-medium text-slate-900 dark:text-white whitespace-nowrap">#ORD-001</td>
<td class="px-6 py-4">
<div class="flex items-center gap-2">
<span class="font-medium text-slate-900 dark:text-white">Tanvir Ahmed</span>
<a class="text-blue-500 hover:text-blue-700 opacity-0 group-hover:opacity-100 transition-opacity" href="#" title="Open Messenger">
<span class="material-symbols-outlined text-[16px]">chat</span>
</a>
</div>
<div class="text-xs text-slate-400">Dhaka, Mirpur</div>
</td>
<td class="px-6 py-4 whitespace-nowrap">Oct 24, 2023</td>
<td class="px-6 py-4">
<span class="inline-flex items-center gap-1.5 px-2.5 py-1 rounded-full text-xs font-medium bg-green-100 text-green-700 dark:bg-green-900/30 dark:text-green-400">
<span class="size-1.5 rounded-full bg-green-500"></span> Paid
                                                </span>
</td>
<td class="px-6 py-4">
<span class="inline-flex items-center gap-1.5 px-2.5 py-1 rounded-full text-xs font-medium bg-blue-100 text-blue-700 dark:bg-blue-900/30 dark:text-blue-400">
                                                    Processing
                                                </span>
</td>
<td class="px-6 py-4 text-right font-bold text-slate-900 dark:text-white">৳1,500</td>
<td class="px-6 py-4 text-center">
<button class="text-slate-400 hover:text-slate-600 dark:hover:text-slate-200">
<span class="material-symbols-outlined">more_vert</span>
</button>
</td>
</tr>
<tr class="hover:bg-slate-50 dark:hover:bg-slate-700/50 transition-colors group">
<td class="px-6 py-4 font-medium text-slate-900 dark:text-white whitespace-nowrap">#ORD-002</td>
<td class="px-6 py-4">
<div class="flex items-center gap-2">
<span class="font-medium text-slate-900 dark:text-white">Sadia Islam</span>
<a class="text-blue-500 hover:text-blue-700 opacity-0 group-hover:opacity-100 transition-opacity" href="#" title="Open Messenger">
<span class="material-symbols-outlined text-[16px]">chat</span>
</a>
</div>
<div class="text-xs text-slate-400">Chittagong, GEC</div>
</td>
<td class="px-6 py-4 whitespace-nowrap">Oct 24, 202
