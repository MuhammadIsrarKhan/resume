<script setup>
import { Tooltip, TooltipContent, TooltipProvider, TooltipTrigger } from '@/components/ui/tooltip'
</script>
<template>
  <TooltipProvider>
    <Tooltip>
      <TooltipTrigger>
        <slot></slot>
      </TooltipTrigger>
      <TooltipContent>
        <slot name="tooltipContent"></slot>
      </TooltipContent>
    </Tooltip>
  </TooltipProvider>
</template>
