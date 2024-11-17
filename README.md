<!doctype html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <script src="https://cdn.tailwindcss.com"></script>
  <script>
    tailwind.config = {
      theme: {
        extend: {
          colors: {
            clifford: '#da373d',
          }
        }
      }
    }
  </script>
</head>
<body class="bg-gray-100 transition-all duration-300" id="body">
  <nav class="bg-gray-800">
    <div class="mx-auto max-w-7xl px-2 sm:px-6 lg:px-8">
      <div class="relative flex h-16 items-center justify-between">
        <div class="absolute inset-y-0 left-0 flex items-center sm:hidden">
          <!-- Mobile menu button-->
          <button id="mobile-menu-button" type="button" class="relative inline-flex items-center justify-center rounded-md p-2 text-gray-400 hover:bg-gray-700 hover:text-white focus:outline-none focus:ring-2 focus:ring-inset focus:ring-white" aria-controls="mobile-menu" aria-expanded="false">
            <span class="sr-only">Open main menu</span>
            <svg class="h-6 w-6" id="hamburger-icon" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" aria-hidden="true">
              <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
            </svg>
            <svg class="hidden h-6 w-6" id="close-icon" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" aria-hidden="true">
              <path stroke-linecap="round" stroke-linejoin="round" d="M6 18 18 6M6 6l12 12" />
            </svg>
          </button>
        </div>

        <!-- Dark Mode Toggle Button -->
        <div class="flex items-center ml-4 sm:ml-6">
          <button id="mode-toggle" class="text-gray-300 hover:text-white p-2 rounded-md focus:outline-none">
            <svg class="h-6 w-6 dark:hidden" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" aria-hidden="true">
              <path stroke-linecap="round" stroke-linejoin="round" d="M12 3v1m0 16v1m9-9h1M3 12H2m16.243 5.657l.707.707M5.757 5.757l.707-.707m12.728 0l-.707.707M5.757 18.243l-.707-.707M12 8a4 4 0 1 1 0 8 4 4 0 0 1 0-8z"/>
            </svg>
            <svg class="hidden h-6 w-6 dark:block" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" aria-hidden="true">
              <path stroke-linecap="round" stroke-linejoin="round" d="M12 3c1.308 0 2.588.278 3.717.786a9.978 9.978 0 0 1 2.622 2.622A9.986 9.986 0 0 1 21 12a9.978 9.978 0 0 1-2.661 6.592 9.978 9.978 0 0 1-2.622 2.622A9.986 9.986 0 0 1 12 21a9.978 9.978 0 0 1-6.592-2.661 9.978 9.978 0 0 1-2.622-2.622A9.986 9.986 0 0 1 3 12a9.978 9.978 0 0 1 2.661-6.592A9.978 9.978 0 0 1 8.283 3.786C9.412 3.278 10.692 3 12 3z"/>
            </svg>
          </button>
        </div>

        <div class="flex flex-1 items-center justify-center sm:items-stretch sm:justify-start">
          <div class="flex shrink-0 items-center">
            <img class="h-8 w-auto" src="https://tailwindui.com/plus/img/logos/mark.svg?color=indigo&shade=500" alt="Your Company">
          </div>
          <div class="hidden sm:ml-6 sm:block">
            <div class="flex space-x-4">
              <a href="#" class="rounded-md bg-gray-900 px-3 py-2 text-sm font-medium text-white" aria-current="page">Dashboard</a>
              <a href="#" class="rounded-md px-3 py-2 text-sm font-medium text-gray-300 hover:bg-gray-700 hover:text-white">Team</a>
              <a href="#" class="rounded-md px-3 py-2 text-sm font-medium text-gray-300 hover:bg-gray-700 hover:text-white">Projects</a>
              <a href="#" class="rounded-md px-3 py-2 text-sm font-medium text-gray-300 hover:bg-gray-700 hover:text-white">Calendar</a>
            </div>
          </div>
        </div>

        <div class="absolute inset-y-0 right-0 flex items-center pr-2 sm:static sm:inset-auto sm:ml-6 sm:pr-0">
          <button type="button" class="relative rounded-full bg-gray-800 p-1 text-gray-400 hover:text-white focus:outline-none focus:ring-2 focus:ring-white focus:ring-offset-2 focus:ring-offset-gray-800">
            <span class="absolute -inset-1.5"></span>
            <span class="sr-only">View notifications</span>
            <svg class="size-6" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" aria-hidden="true" data-slot="icon">
              <path stroke-linecap="round" stroke-linejoin="round" d="M14.857 17.082a23.848 23.848 0 0 0 5.454-1.31A8.967 8.967 0 0 1 18 9.75V9A6 6 0 0 0 6 9v.75a8.967 8.967 0 0 1-2.312 6.022c1.733.64 3.56 1.085 5.455 1.31m5.714 0a24.255 24.255 0 0 1-5.714 0m5.714 0a3 3 0 1 1-5.714 0" />
            </svg>
          </button>
  
          <!-- Profile dropdown -->
          <div class="relative ml-3">
            <div>
              <button type="button" class="relative flex rounded-full bg-gray-800 text-sm focus:outline-none focus:ring-2 focus:ring-white focus:ring-offset-2 focus:ring-offset-gray-800" id="user-menu-button" aria-expanded="false" aria-haspopup="true">
                <span class="absolute -inset-1.5"></span>
                <span class="sr-only">Open user menu</span>
                <img class="size-8 rounded-full" src="https://images.unsplash.com/photo-1472099645785-5658abf4ff4e?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80" alt="">
              </button>
            </div>
            <div id="user-menu" class="absolute right-0 z-10 mt-2 w-48 origin-top-right rounded-md bg-white py-1 shadow-lg ring-1 ring-black/5 focus:outline-none hidden" role="menu" aria-orientation="vertical" aria-labelledby="user-menu-button" tabindex="-1">
              <a href="#" class="block px-4 py-2 text-sm text-gray-700" role="menuitem" tabindex="-1" id="user-menu-item-0">Your Profile</a>
              <a href="#" class="block px-4 py-2 text-sm text-gray-700" role="menuitem" tabindex="-1" id="user-menu-item-1">Settings</a>
              <a href="#" class="block px-4 py-2 text-sm text-gray-700" role="menuitem" tabindex="-1" id="user-menu-item-2">Sign out</a>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Mobile menu, show/hide based on menu state. -->
    <div id="mobile-menu" class="hidden ">
      <div class="space-y-1 px-2 pb-3 pt-2">
        <a href="#" class="block rounded-md bg-gray-900 px-3 py-2 text-base font-medium text-white" aria-current="page">Dashboard</a>
        <a href="#" class="block rounded-md px-3 py-2 text-base font-medium text-gray-300 hover:bg-gray-700 hover:text-white">Team</a>
        <a href="#" class="block rounded-md px-3 py-2 text-base font-medium text-gray-300 hover:bg-gray-700 hover:text-white">Projects</a>
        <a href="#" class="block rounded-md px-3 py-2 text-base font-medium text-gray-300 hover:bg-gray-700 hover:text-white">Calendar</a>
      </div>
    </div>
  </nav>

  <script>
    // Toggle mobile menu visibility
    const menuButton = document.getElementById('mobile-menu-button');
    const mobileMenu = document.getElementById('mobile-menu');
    const menuIcon = menuButton.querySelector('#hamburger-icon');
    const closeIcon = menuButton.querySelector('#close-icon');
    const userButton = document.getElementById('user-menu-button');
    const userMenu = document.getElementById('user-menu');

    menuButton.addEventListener('click', () => {
      mobileMenu.classList.toggle('hidden');
      menuIcon.classList.toggle('hidden');
      closeIcon.classList.toggle('hidden');
      
      // Ensure profile menu is hidden when mobile menu is toggled
      userMenu.classList.add('hidden');
    });

    userButton.addEventListener('click', () => {
      userMenu.classList.toggle('hidden');
      // Hide mobile menu when profile menu is toggled
      mobileMenu.classList.add('hidden');
      menuIcon.classList.remove('hidden');
      closeIcon.classList.add('hidden');
    });

    // Dark mode toggle
    const modeToggle = document.getElementById('mode-toggle');
    const body = document.getElementById('body');

    modeToggle.addEventListener('click', () => {
      body.classList.toggle('dark');
    });
  </script>
</body>
</html>
