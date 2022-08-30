<script>
  import { page } from '$app/stores';
  import "../app.css";
</script>

<nav class="">
  <div class="absolute top-4 left-6 flex gap-6">
    <a href="/" class="font-300 {!$page.data.onDark ? 'text-slate-900' : 'text-gray-50'}">
      <svg class="w-8 svg-standalone-icon" preserveAspectRatio="none" viewBox="203.26 115 143.47 143.47" xmlns="http://www.w3.org/2000/svg">
        <g fill-rule="evenodd">
          <!-- <path d="m275 115c-9.729 0-19.037 1.879-27.924 5.638-0.816 0.345-1.623 0.704-2.422 1.076h7.887c7.2054-2.498 14.692-3.747 22.459-3.747 7.767 0 15.254 1.249 22.459 3.747h7.887c-0.798-0.372-1.606-0.731-2.422-1.076-8.887-3.759-18.195-5.638-27.924-5.638z" fill="#0086bf"/> -->
          <path d="m329.72 131.24c-3.81-3.982-11.775-5.887-23.724-5.887h-65.975c-9.697 0-16.451 2.078-20.433 6.407-3.637 3.809-5.542 10.39-5.542 19.567v69.266c0 7.965 2.252 14.372 6.407 18.875 4.503 4.675 11.083 7.099 19.568 7.099h69.265c10.91 0 18.01-1.558 21.126-4.848 3.291-3.464 4.849-10.39 4.849-21.126l-31.862-40.001 31.862-29.265c0-9.697-1.732-16.45-5.541-20.087zm-32.901 20.087-56.798 52.123v-52.123zm5.195 69.266h-42.252l24.416-22.338z" fill="#ffc72c"/>
          <!-- <path d="m346.74 186.74c0-9.729-1.879-19.037-5.638-27.924-0.82-1.94-1.717-3.83-2.691-5.67l-0.185 0.292-0.236 0.297-0.266 0.271-0.616 0.567-0.88 0.807c0.766 1.497 1.479 3.028 2.141 4.592 3.603 8.517 5.404 17.44 5.404 26.768s-1.801 18.251-5.404 26.768c-0.47 1.111-0.965 2.204-1.487 3.28l1.226 1.54 0.34 0.509 0.25 0.559 0.067 0.261c0.838-1.6253 1.617-3.2897 2.337-4.993 3.759-8.887 5.638-18.194 5.638-27.924z" fill="#0086bf"/> -->
          <!-- <path d="m203.26 186.74c0 9.73 1.879 19.037 5.638 27.924 0.477 1.129 0.98 2.24 1.509 3.334v-7.587c-2.787-7.577-4.18-15.467-4.18-23.671s1.393-16.094 4.18-23.671v-7.586c-0.529 1.094-1.032 2.205-1.509 3.333-3.759 8.887-5.638 18.195-5.638 27.924z" fill="#0086bf"/> -->
          <!-- <path d="m302.92 252.84c-8.887 3.758-18.195 5.637-27.924 5.637s-19.037-1.879-27.924-5.637c-1.903-0.805-3.757-1.684-5.563-2.635h6.953c8.447 3.537 17.291 5.305 26.534 5.305 9.2427 0 18.087-1.7683 26.534-5.305h6.954c-1.807 0.951-3.661 1.83-5.564 2.635z" fill="#0086bf"/> -->
        </g>
      </svg>
    </a>
  </div>

  <div class="absolute top-5 right-6 flex gap-6">
    <a href="login" class="font-300 {!$page.data.onDark ? 'text-slate-500' : 'text-gray-400'}">login</a>
    <a href="sign-up" class="font-300 {!$page.data.onDark ? 'text-slate-500' : 'text-gray-400'}">sign up</a>
  </div>
</nav>

<main class="{$page.data.onDark ? 'bg-slate-900' : 'bg-gray-50'}">
  <div class="container mx-auto px-10 h-screen font-sans flex items-center max-w-7xl gap-8">
    <div class="flex flex-{ $page.data.layout } { $page.data.layout === 'col' ? 'items-start justify-center' : 'justify-start items-start' }">
      <h1 class="w-full max-w-md font-heading font-semibold text-10xl leading-tighter mb-2 { $page.data.onDark ? 'text-gray-50' : 'text-slate-700' }">
        { @html $page.data.title }
      </h1>
      <div class="w-full flex flex-{ $page.data.layout }">
        <slot />
      </div>
    </div>
  </div>
</main>
