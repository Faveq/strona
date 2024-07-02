<template>
  <nav class="h-screen p-2 border-r border-solid border-accent absolute">
    <div
      class="px-2 my-1.1"
      v-for="category in categories"
      :key="category.mainCategory"
    >
      <p class=" pt-6 pb-2 text-xs w-full text-gray-600" v-if="category.isHeading">
        {{ category.heading }}
      </p>
      <a class="navLink text-sm flex items-center my-1" v-else-if="category.subCategories.length === 0">
        <component :is="category.icon" class="h-3 w-3 m-1" />
        {{ category.mainCategory }}</a
      >
      <Collapsible
        class="text-sm my-1"
        v-else
        v-model:open="categoryOpenStates[category.mainCategory]"
      >
        <CollapsibleTrigger class="collapsibleTrigger flex items-center w-full">
          <ChevronRight v-if="!categoryOpenStates[category.mainCategory]" class="h-4 w-4" />
          <ChevronDown v-else class="h-4 w-4" />
          <component :is="category.icon" class="h-3 w-3 m-1" />
          {{ category.mainCategory }}
        </CollapsibleTrigger>

        <CollapsibleContent
          class=" collapsibleContent p-1 px-3 w-full"
          v-for="subCategory in category.subCategories"
        >
          {{ subCategory }}
        </CollapsibleContent>
      </Collapsible>
    </div>
  </nav>
</template>

<script setup lang="ts">
import { ref } from "vue";
import {
  Collapsible,
  CollapsibleContent,
  CollapsibleTrigger,
} from "@/components/ui/collapsible";import {
  ChevronRight,
  ChevronDown,
  House,
  ShoppingCart,
  Phone,
  ClipboardList,
  Luggage,
  MessageSquare,
  Mail,
  Bookmark,
  DollarSign,
  Bell,
  Users,
  Clock,
  Lock,
  FileText,
  Star,
  Table,
  BarChart2,
  Layers,
  Grid,
  List,
  PlayCircle,
  Settings,
  Layout,
  Droplet,
  File,
  RefreshCw,
  Eye,
} from "lucide-vue-next";
import { DefineComponent } from "vue";
import { LucideProps } from "lucide-vue-next";

interface Category {
  mainCategory: string;
  subCategories: string[];
  isOpen?: boolean;
  heading?: string;
  isHeading: boolean;
  icon?: DefineComponent<LucideProps>;
}

const categories: Category[] = [
  {
    mainCategory: "Home",
    subCategories: [
      "E commerce",
      "Project management",
      "CRM",
      "Travel agency",
      "Social feed",
    ],
    isOpen: false,
    isHeading: false,
    icon: House as unknown as DefineComponent<LucideProps>,
  },
  {
    mainCategory: "",
    subCategories: [],
    isOpen: false,
    heading: "APPS",
    isHeading: true,
  },
  {
    mainCategory: "E commerce",
    subCategories: [
      "Admin",
      "Products",
      "Customers",
      "Customer details",
      "Orders",
      "Order details",
      "Refund",
    ],
    isOpen: false,
    isHeading: false,
    icon: ShoppingCart as unknown as DefineComponent<LucideProps>,
  },
  {
    mainCategory: "CRM",
    subCategories: ["Analytics", "Deals", "Deal details"],
    isOpen: false,
    isHeading: false,
    icon: Phone as unknown as DefineComponent<LucideProps>,
  },
  {
    mainCategory: "Travel agency",
    subCategories: ["Landing", "Flight", "Trip"],
    isOpen: false,
    isHeading: false,
    icon: Luggage as unknown as DefineComponent<LucideProps>,
  },
  {
    mainCategory: "Chat",
    subCategories: [],
    isHeading: false,
    icon: MessageSquare as unknown as DefineComponent<LucideProps>,
  },
  {
    mainCategory: "Email",
    subCategories: ["Inbox", "Email detail", "Compose"],
    isOpen: false,
    isHeading: false,
    icon: Mail as unknown as DefineComponent<LucideProps>,
  },
  {
    mainCategory: "Events",
    subCategories: ["Create an event", "Event detail"],
    isOpen: false,
    isHeading: false,
    icon: ClipboardList as unknown as DefineComponent<LucideProps>,
  },
  {
    mainCategory: "Social",
    subCategories: ["Profile", "Settings"],
    isOpen: false,
    isHeading: false,
    icon: Bookmark as unknown as DefineComponent<LucideProps>,
  },
  {
    mainCategory: "",
    subCategories: [],
    isOpen: false,
    heading: "PAGES",
    isHeading: true,
    icon: ClipboardList as unknown as DefineComponent<LucideProps>,
  },
  {
    mainCategory: "Starter",
    subCategories: [],
    isOpen: false,
    isHeading: false,
    icon: ClipboardList as unknown as DefineComponent<LucideProps>,
  },
  {
    mainCategory: "Faq",
    subCategories: ["Faq accordion", "Faq tab"],
    isOpen: false,
    isHeading: false,
    icon: Bookmark as unknown as DefineComponent<LucideProps>,
  },
  {
    mainCategory: "Landing",
    subCategories: ["Default", "Alternate"],
    isOpen: false,
    isHeading: false,
    icon: House as unknown as DefineComponent<LucideProps>,
  },
  {
    mainCategory: "Pricing",
    subCategories: ["Pricing column", "Pricing grid"],
    isOpen: false,
    isHeading: false,
    icon: DollarSign as unknown as DefineComponent<LucideProps>,
  },
  {
    mainCategory: "Notifications",
    subCategories: [],
    isOpen: false,
    isHeading: false,
    icon: Bell as unknown as DefineComponent<LucideProps>,
  },
  {
    mainCategory: "Members",
    subCategories: [],
    isOpen: false,
    isHeading: false,
    icon: Users as unknown as DefineComponent<LucideProps>,
  },
  {
    mainCategory: "Timeline",
    subCategories: [],
    isOpen: false,
    isHeading: false,
    icon: Clock as unknown as DefineComponent<LucideProps>,
  },
  {
    mainCategory: "Authentication",
    subCategories: ["Simple", "Split", "Card"],
    isOpen: false,
    isHeading: false,
    icon: Lock as unknown as DefineComponent<LucideProps>,
  },
  {
    mainCategory: "",
    subCategories: [],
    isOpen: false,
    heading: "MODULES",
    isHeading: true,
  },
  {
    mainCategory: "Forms",
    subCategories: ["Basic", "Advance"],
    isOpen: false,
    isHeading: false,
    icon: FileText as unknown as DefineComponent<LucideProps>,
  },
  {
    mainCategory: "Icons",
    subCategories: ["Feather", "Font awesome"],
    isOpen: false,
    isHeading: false,
    icon: Star as unknown as DefineComponent<LucideProps>,
  },
  {
    mainCategory: "Tables",
    subCategories: ["Basic tables", "Advance tables", "Bulk select"],
    isOpen: false,
    isHeading: false,
    icon: Table as unknown as DefineComponent<LucideProps>,
  },
  {
    mainCategory: "ECharts",
    subCategories: [
      "Line charts",
      "Bar charts",
      "Geo map",
      "Pie charts",
      "Gauge chart",
    ],
    isOpen: false,
    isHeading: false,
    icon: BarChart2 as unknown as DefineComponent<LucideProps>,
  },
  {
    mainCategory: "Components",
    subCategories: ["Avatar", "Accordion", "Alerts", "Badge"],
    isOpen: false,
    isHeading: false,
    icon: Layers as unknown as DefineComponent<LucideProps>,
  },
  {
    mainCategory: "Widgets",
    subCategories: [],
    isOpen: false,
    isHeading: false,
    icon: Grid as unknown as DefineComponent<LucideProps>,
  },
  {
    mainCategory: "Multi level",
    subCategories: ["Level two", "Level three", "Level four"],
    isOpen: false,
    isHeading: false,
    icon: List as unknown as DefineComponent<LucideProps>,
  },
  {
    mainCategory: "",
    subCategories: [],
    isOpen: false,
    heading: "DOCUMENTATION",
    isHeading: true,
  },
  {
    mainCategory: "Getting started",
    subCategories: [],
    isOpen: false,
    isHeading: false,
    icon: PlayCircle as unknown as DefineComponent<LucideProps>,
  },
  {
    mainCategory: "Customization",
    subCategories: ["Configuration", "Styling", "Color"],
    isOpen: false,
    isHeading: false,
    icon: Settings as unknown as DefineComponent<LucideProps>,
  },
  {
    mainCategory: "Layouts doc",
    subCategories: [
      "Vertical navbar",
      "Horizontal navbar",
      "Combo navbar",
      "Dual navbar",
    ],
    isOpen: false,
    isHeading: false,
    icon: Layout as unknown as DefineComponent<LucideProps>,
  },
  {
    mainCategory: "Gulp",
    subCategories: [],
    isOpen: false,
    isHeading: false,
    icon: Droplet as unknown as DefineComponent<LucideProps>,
  },
  {
    mainCategory: "Design file",
    subCategories: [],
    isOpen: false,
    isHeading: false,
    icon: File as unknown as DefineComponent<LucideProps>,
  },
  {
    mainCategory: "Changelog",
    subCategories: [],
    isOpen: false,
    isHeading: false,
    icon: RefreshCw as unknown as DefineComponent<LucideProps>,
  },
  {
    mainCategory: "Showcase",
    subCategories: [],
    isOpen: false,
    isHeading: false,
    icon: Eye as unknown as DefineComponent<LucideProps>,
  },
];

const categoryOpenStates = ref(
  categories.reduce((acc, category) => {
    acc[category.mainCategory] = false;
    return acc;
  }, {} as Record<string, boolean>)
);
</script>

<style scoped>
nav{
  overflow-y: auto;
  width: 150pt;
}
.collapsibleContent, .collapsibleTrigger:hover, .navLink{
  transition: all .3s ease;
}
.collapsibleContent:hover, .collapsibleTrigger:hover, .navLink:hover{
  background: #e0e0e0;
  border-radius: 10px;
  cursor: pointer;
}

</style>
