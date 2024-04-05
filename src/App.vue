<script setup>
import Lockup from './components/Lockup.vue'
import FeaturePill from './components/FeaturePill.vue'
import CallToAction from './components/CallToAction.vue'
import { Application } from '@splinetool/runtime'
import { ref, onMounted } from 'vue'
const canvas = ref(null)
onMounted(() => {
  const app = new Application(canvas.value)
  app.load('https://prod.spline.design/X8R5nCnSa6zzFPWy/scene.splinecode')
})
</script>

<template>
  <div class="app-container">
    <header>
      <Lockup />
      <FeaturePill>
        <canvas ref="canvas"></canvas>
      </FeaturePill>
    </header>

    <main>
      <CallToAction variant="large">
        <template #heading>
          <h1>We’re a collective of digital makers and engineers</h1>
        </template>
        <template #text>
          <p>Based in Canberra, Australia — we’re a collective of good people who do good work.</p>
          <p>
            Our multi-disciplinary collective consists of software engineers, digital designers,
            product managers and everything in-between.
          </p>
          <p>We are an empowering home for colleagues that you want to work with everyday.</p>
        </template>
      </CallToAction>

      <CallToAction variant="default">
        <template #heading>
          <h1>We make good products, services and intentions real</h1>
        </template>
        <template #text>
          <p>
            We work in the Public Service, making accessible and user-centred products and services
            for all Australians.
          </p>
          <p>
            Partnering with Commonwealth, State and Territory agencies, we create good teams to
            solve meaningful problems.
          </p>
        </template>
      </CallToAction>

      <FeaturePill>
        <CallToAction variant="small">
          <template #heading>
            <h1>We have a lot more to say and show, there will be a new website coming soon.</h1>
          </template>
          <template #text>
            <p>
              While not exactly in stealth mode, we've been quietly flying under the radar and
              working hard for our clients since we were founded in 2021.
            </p>
            <p>
              We're excited to share more of these stories and what we've learned on our various
              journeys in 2024.
            </p>
            <p>Stay tuned.</p>
          </template>
        </CallToAction>
      </FeaturePill>
    </main>
  </div>
</template>

<style scoped>
.app-container {
  max-width: 1680px;
  margin: 0 auto;
}
</style>
