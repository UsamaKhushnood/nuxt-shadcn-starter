<template>
  <header
    class="sticky top-0 flex h-16 items-center gap-4 border-b bg-background px-4 md:px-6 z-10"
  >
    <div class="container flex items-center">
      <nav
        class="hidden flex-col gap-6 text-lg font-medium md:flex md:flex-row md:items-center md:gap-5 md:text-sm lg:gap-6"
      >
        <a
          href="#"
          class="flex items-center gap-2 text-lg font-semibold md:text-base whitespace-nowrap"
        >
          Acme Inc
        </a>
        <a
          href="#"
          class="text-muted-foreground transition-colors hover:text-foreground"
        >
          Dashboard
        </a>
        <a
          href="#"
          class="text-muted-foreground transition-colors hover:text-foreground"
        >
          Orders
        </a>
        <a
          href="#"
          class="text-muted-foreground transition-colors hover:text-foreground"
        >
          Products
        </a>
        <a
          href="#"
          class="text-muted-foreground transition-colors hover:text-foreground"
        >
          Customers
        </a>
        <a
          href="#"
          class="text-foreground transition-colors hover:text-foreground"
        >
          Settings
        </a>
      </nav>
      <Sheet>
        <SheetTrigger as-child>
          <Button variant="outline" size="icon" class="shrink-0 md:hidden">
            <Icon
              icon="radix-icons:hamburger-menu"
              class="h-[1.2rem] w-[1.2rem]"
            />
            <span class="sr-only">Toggle navigation menu</span>
          </Button>
        </SheetTrigger>
        <SheetContent side="left">
          <nav class="grid gap-6 text-lg font-medium">
            <a href="#" class="flex items-center gap-2 text-lg font-semibold">
              <span class="sr-only">Acme Inc</span>
            </a>
            <a href="#" class="text-muted-foreground hover:text-foreground">
              Dashboard
            </a>
            <a href="#" class="text-muted-foreground hover:text-foreground">
              Orders
            </a>
            <a href="#" class="text-muted-foreground hover:text-foreground">
              Products
            </a>
            <a href="#" class="text-muted-foreground hover:text-foreground">
              Customers
            </a>
            <a href="#" class="hover:text-foreground"> Settings </a>
          </nav>
        </SheetContent>
      </Sheet>
      <div class="flex w-full items-center gap-4 md:ml-auto md:gap-2 lg:gap-4">
        <form class="ml-auto flex-1 sm:flex-initial">
          <div class="relative">
            <Input
              type="search"
              placeholder="Search products..."
              class="sm:w-[300px] md:w-[200px] lg:w-[300px]"
            />
          </div>
        </form>
        <div>
          <DropdownMenu>
            <DropdownMenuTrigger as-child>
              <Button variant="outline" size="icon" class="border-0">
                <Icon icon="radix-icons:person" class="h-[1.2rem] w-[1.2rem]" />
                <span class="sr-only">Toggle user menu</span>
              </Button>
            </DropdownMenuTrigger>
            <DropdownMenuContent align="end">
              <DropdownMenuLabel>My Account</DropdownMenuLabel>
              <DropdownMenuSeparator />
              <DropdownMenuItem>Settings</DropdownMenuItem>
              <DropdownMenuItem>Support</DropdownMenuItem>
              <DropdownMenuSeparator />
              <DropdownMenuItem>Logout</DropdownMenuItem>
            </DropdownMenuContent>
          </DropdownMenu>
          <ThemeToggler />
        </div>
      </div>
    </div>
  </header>
</template>
<script setup>
import { Icon } from "@iconify/vue";
import ThemeToggler from "~/components/common/ThemeToggler.vue";
</script>
