<template>
  <div class="min-h-screen bg-slate-50">
    <div class="mx-auto max-w-4xl px-4 py-8">
      <header class="mb-8 flex items-center justify-between border-b border-slate-200 pb-4">
        <p class="text-lg font-semibold text-slate-900">animate-js</p>
        <nav class="flex gap-4 text-sm font-medium">
          <RouterLink class="text-slate-600 hover:text-slate-900" to="/">Home</RouterLink>
          <RouterLink class="text-slate-600 hover:text-slate-900" to="/about">About</RouterLink>
        </nav>
      </header>

      <main>
        <RouterView />
      </main>
    </div>
  </div>
</template>
