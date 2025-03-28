<script setup lang="ts">
import {
  SelectContent,
  SelectItem,
  SelectItemText,
  SelectRoot,
  SelectTrigger,
  SelectValue,
  SelectViewport,
} from "reka-ui";

const options = [
  {
    name: "Frank Morris",
    avatar: "/avatar-20-01.jpg",
  },
  {
    name: "Xavier Guerra",
    avatar: "/avatar-20-02.jpg",
  },
  {
    name: "Anne Kelley",
    avatar: "/avatar-20-03.jpg",
  },
  {
    name: "John Doe",
    avatar: "/avatar-20-04.jpg",
  },
  {
    name: "Jane Smith",
    avatar: "/avatar-20-05.jpg",
  },
];
</script>

<template>
  <div class="space-y-2">
    <label for="select-35">Select using Reka UI</label>
    <SelectRoot>
      <SelectTrigger
        id="select-39"
        class="ps-2 flex h-9 w-full items-center justify-between gap-2 rounded-lg border border-input bg-background px-3 py-2 text-start text-sm text-foreground shadow-sm shadow-black/5 ring-offset-background focus:border-ring focus:outline-none focus:ring-2 focus:ring-ring/30 focus:ring-offset-2 disabled:cursor-not-allowed disabled:opacity-50 data-[placeholder]:text-muted-foreground/70 [&>span]:min-w-0 [&>span]:flex [&>span]:items-center [&>span]:gap-2 [&>span_[data-square]]:shrink-0"
      >
        <SelectValue placeholder="Select user" />
      </SelectTrigger>
      <SelectPortal>
        <SelectContent
          class="[&_*[role=option]>span]:end-2 relative z-50 max-h-[min(24rem,var(--radix-select-content-available-height))] min-w-[8rem] overflow-hidden rounded-lg border border-input bg-popover text-popover-foreground shadow-lg shadow-black/5 data-[state=open]:animate-in data-[state=closed]:animate-out data-[state=closed]:fade-out-0 data-[state=open]:fade-in-0 data-[state=closed]:zoom-out-95 data-[state=open]:zoom-in-95 data-[side=bottom]:slide-in-from-top-2 data-[side=left]:slide-in-from-right-2 data-[side=right]:slide-in-from-left-2 data-[side=top]:slide-in-from-bottom-2 [&_[role=group]]:py-1 [&_*[role=option]>span]:start-auto [&_*[role=option]>span]:flex [&_*[role=option]>span]:items-center [&_*[role=option]>span]:gap-2 [&_*[role=option]]:pe-8 [&_*[role=option]]:ps-2 bg-white"
        >
          <SelectLabel
            class="ps-2 py-1.5 pe-2 text-xs font-medium text-muted-foreground"
            >Impersonate user</SelectLabel
          >
          <SelectViewport>
            <SelectGroup>
              <SelectItem
                v-for="option in options"
                :key="option.name"
                :value="option.name"
                class="relative gap-2 flex w-full cursor-default select-none items-center rounded-md py-1.5 pe-2 ps-8 text-sm outline-none focus:bg-accent focus:text-accent-foreground data-[disabled]:pointer-events-none data-[disabled]:opacity-50"
              >
                <SelectItemText class="flex items-center gap-2">
                  <div
                    class="rounded bg-indigo-400/20 size-5 justify-center flex items-center text-center text-indigo-500"
                  >
                    {{ option.name.charAt(0) }}
                  </div>
                  <span class="truncate">{{ option.name }}</span>
                  <img
                    :src="option.avatar"
                    class="rounded-full size-5"
                    alt="avatar"
                  />
                </SelectItemText>
              </SelectItem>
            </SelectGroup>
          </SelectViewport>
        </SelectContent>
      </SelectPortal>
    </SelectRoot>
  </div>
</template>
