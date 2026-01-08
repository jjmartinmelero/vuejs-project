<script setup lang="ts">
import { TresCanvas } from '@tresjs/core'
import { OrbitControls } from '@tresjs/cientos';
</script>

<template>
  <main class="relative mx-auto h-screen flex items-center">
    <div class="w-full h-screen flex">
      <!-- <section class="min-h-400px w-2/3"> -->
        <!-- <TresCanvas alpha>
          <TheExperience />
        </TresCanvas> -->
        <TresCanvas clear-color="#82dbc8">
          <TresPerspectiveCamera :position="[0, 0, 5]" />
          <OrbitControls />
          <TresMesh 
            :position="[0.5,1,-1]" 
            :rotation="[-Math.PI / 4,0,0]"
            :scale="[0.5,0.5,0.5]">
            <!-- <TresBoxGeometry :args="[1,2,3]" /> -->
            <TresBoxGeometry/>
            <TresMeshNormalMaterial />
          </TresMesh>
          <TresAxesHelper />
        </TresCanvas>
      <!-- </section> -->
      <aside class="bg-dark text-gray shadow-md w-1/3">
        <header class="p-8 bg-dark-700">
          <h1>
            Configurador de escritorio
          </h1>
        </header>
        <div class="p-8">
        </div>
      </aside>
    </div>
  </main>
</template>
