<template>
  <div class="border-t-[1px]">
    <div
      class="container md:grid grid-rows-1 grid-cols-3 gap-4 px-4 md:px-6 md:py-[8rem] py-[4rem]"
    >
      <div class="col-span-1 flex flex-col md:pb-0 pb-[2rem]">
        <a href="#" class="flex gap-2 font-semibold pb-2"> Acme Inc </a>
        <p class="pb-4">
          Making the world a better place through constructing elegant
          hierarchies.
        </p>
        <div class="flex gap-4 text-xs font-light text-muted-foreground">
          <Icon
            icon="ic:baseline-facebook"
            class="h-[1.2rem] w-[1.2rem] hover:text-primary cursor-pointer"
          />
          <Icon
            icon="hugeicons:instagram"
            class="h-[1.2rem] w-[1.2rem] hover:text-primary cursor-pointer"
          />
          <Icon
            icon="pajamas:twitter"
            class="h-[1.2rem] w-[1.2rem] hover:text-primary cursor-pointer"
          />
          <Icon
            icon="mdi:github"
            class="h-[1.2rem] w-[1.2rem] hover:text-primary cursor-pointer"
          />
          <Icon
            icon="mdi:youtube"
            class="h-[1.2rem] w-[1.2rem] hover:text-primary cursor-pointer"
          />
        </div>
      </div>

      <div class="col-span-2 md:grid grid-cols-4">
        <div
          class="md:py-0 py-4"
          v-for="(solution, index) in Solutions"
          :key="index"
        >
          <h6 class="text-sm pb-4">{{ solution.heading }}</h6>
          <div class="grid gap-4">
            <p
              class="text-xs font-light text-muted-foreground hover:text-primary cursor-pointer"
              v-for="(link, i) in solution.links"
              :key="i"
            >
              {{ link }}
            </p>
          </div>
        </div>
      </div>
    </div>
    <div
      class="grid border-t-[1px] px-4 md:p-4 py-3 text-sm font-thin items-center justify-center"
    >
      © 2020 Your Company, Inc. All rights reserved.
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";
import { Icon } from "@iconify/vue";

const Solutions = ref([
  {
    heading: "Solution",
    links: ["Marketing", "Analytics", "Common", "Insight"],
  },
  {
    heading: "Support",
    links: ["Pricing", "Documentation", "Guides", "API Status"],
  },
  {
    heading: "Company",
    links: ["About", "Blog", "Job", "Press", "Partners"],
  },
  {
    heading: "Legal",
    links: ["Claim", "Privacy", "Terms"],
  },
]);
</script>
