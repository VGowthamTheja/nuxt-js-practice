<template>
  <div>
    <!-- Header -->
    <Header />
    <div class="container lg:grid lg:grid-cols-12 lg:gap-10">
      <!-- Sidebar -->
      <Sidebar class="hidden lg:block lg:col-span-3" />

      <!-- Main Section -->
      <main class="py-5 lg:col-span-6">
        <!-- Status Card -->
        <StatusCard />
        <!-- Customer List -->
        <NewCustomers />
        <!-- Sales Chart -->
        <SalesChart />
        <!-- Recent Orders -->
        <RecentOrder />
      </main>

      <div class="hidden py-5 lg:col-span-3 lg:block">
        <!-- Profile info to the side -->
        <ProfileInfo />
        <hr class="my-5" />
        <!-- Reminders to the side -->
        <Remainders />
      </div>
    </div>
  </div>
</template>
