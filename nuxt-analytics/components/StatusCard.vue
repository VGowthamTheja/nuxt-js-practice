<template>
  <section class="grid gap-5 md:grid-cols-2">
    <!-- Revenue card -->
    <div class="rounded-lg border bg-card p-6">
      <div class="flex items-center justify-between">
        <p class="text-sm font-medium">
          Total Revenue
        </p>
        <span class="shrink-0">
          <Icon name="heroicons:banknotes" class="h-6 w-6 text-muted-foreground" />
        </span>
      </div>
      <p class="mt-1.5 text-xl font-extrabold">$432,576</p>
      <p class="text-xs text-muted-foreground">20% more than last month</p>
    </div>

    <!-- Sales card -->
    <div class="rounded-lg border bg-card p-6">
      <div class="flex items-center justify-between">
        <p class="text-sm font-medium">
          Total Sales
        </p>
        <span class="shrink-0">
          <Icon name="heroicons:credit-card" class="h-6 w-6 text-muted-foreground" />
        </span>
      </div>
      <p class="mt-1.5 text-xl font-extrabold">$12,576</p>
      <p class="text-xs text-muted-foreground">13.2% more than last month</p>
    </div>
  </section>
</template>

<script lang="ts" setup>

</script>

<style></style>

