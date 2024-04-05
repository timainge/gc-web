<script setup>
import Lockup from './components/Lockup.vue'
import FeaturePill from './components/FeaturePill.vue'
import CallToAction from './components/CallToAction.vue'
import Footer from './components/Footer.vue'
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
      <FeaturePill type="blue">
        <canvas ref="canvas"></canvas>
      </FeaturePill>
    </header>

    <main>
      <CallToAction variant="large">
        <template #heading>
          <h2>We’re a collective of digital makers and engineers</h2>
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

      <FeaturePill type="pink">
        <img
          alt="A mockup of a website designed by The Good Collective"
          src="../public/yourcareer.png"
          style="height: 100%"
        />
      </FeaturePill>

      <CallToAction variant="default">
        <template #heading>
          <h2>We make good products, services and intentions real</h2>
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

      <FeaturePill type="black">
        <CallToAction variant="small">
          <template #heading>
            <h1>More to show, soon.</h1>
          </template>
          <template #text>
            <!--<p>
              While not exactly in stealth mode, we've been quietly flying under the radar and
              working hard for our clients since we were founded in 2021.
            </p>-->
            <p>We've been working with our partners under the radar since 2021.</p>
            <p>We're excited to share more this year.</p>
          </template>
        </CallToAction>
      </FeaturePill>

      <Footer />
    </main>
  </div>
</template>

<style scoped>
.app-container {
  max-width: 1680px;
  margin: 0 auto;
}
</style>
