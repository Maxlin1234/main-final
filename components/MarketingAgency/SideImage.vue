<template>
  <section class="sideimg-numbers section-padding sub-bg">
    <div class="container">
      <div class="row">
        <div class="col-lg-6 offset-lg-6">
          <div class="cont">
            <div>
              <h6 class="sub-title mb-15">Who we are ?</h6>
              <h2 class="fz-50">We want to bring business & the digital world together.</h2>
              <div class="underline">
                <NuxtLink to="/dark/page-about" class="arrow mt-30">
                  <span class="sub-title">Explore about us</span>
                  <span class="circle">
                    <svg width="18" height="18" viewBox="0 0 18 18" fill="none" xmlns="http://www.w3.org/2000/svg">
                      <path
                        d="M13.922 4.5V11.8125C13.922 11.9244 13.8776 12.0317 13.7985 12.1108C13.7193 12.1899 13.612 12.2344 13.5002 12.2344C13.3883 12.2344 13.281 12.1899 13.2018 12.1108C13.1227 12.0317 13.0783 11.9244 13.0783 11.8125V5.51953L4.79547 13.7953C4.71715 13.8736 4.61092 13.9176 4.50015 13.9176C4.38939 13.9176 4.28316 13.8736 4.20484 13.7953C4.12652 13.717 4.08252 13.6108 4.08252 13.5C4.08252 13.3892 4.12652 13.283 4.20484 13.2047L12.4806 4.92188H6.18765C6.07577 4.92188 5.96846 4.87743 5.88934 4.79831C5.81023 4.71919 5.76578 4.61189 5.76578 4.5C5.76578 4.38811 5.81023 4.28081 5.88934 4.20169C5.96846 4.12257 6.07577 4.07813 6.18765 4.07812H13.5002C13.612 4.07813 13.7193 4.12257 13.7985 4.20169C13.8776 4.28081 13.922 4.38811 13.922 4.5Z"
                        fill="currentColor"></path>
                    </svg>
                  </span>
                </NuxtLink>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="bg-img bg-left parallaxie d-flex align-items-center justify-content-center"
      data-background="/dark/assets/imgs/background/3.jpg">
      <div class="vid-circle bg-white text-dark">
        <a href="https://youtu.be/AzwC6umvd1s" class="vid" @click="openVideo">
          <span class="icon">
            <svg class="default" width="13" height="20" viewBox="0 0 13 20" fill="currentColor"
              xmlns="http://www.w3.org/2000/svg">
              <path d="M0 20L13 10L0 0V20Z"></path>
            </svg>
          </span>
        </a>
      </div>
    </div>
    <div class="container-fluid mt-100">
      <div class="row">
        <div class="col-12">
          <div class="main-marq xlrg">
            <div class="slide-har st1 strok">
              <div class="box">
                <div class="item">
                  <h4 class="stroke opacity-4">Amazing Services</h4>
                </div>
                <div class="item">
                  <h4 class="stroke opacity-4">Amazing Services</h4>
                </div>
                <div class="item">
                  <h4 class="stroke opacity-4">Amazing Services</h4>
                </div>
                <div class="item">
                  <h4 class="stroke opacity-4">Amazing Services</h4>
                </div>
                <div class="item">
                  <h4 class="stroke opacity-4">Amazing Services</h4>
                </div>
              </div>
              <div class="box">
                <div class="item">
                  <h4 class="stroke opacity-4">Amazing Services</h4>
                </div>
                <div class="item">
                  <h4 class="stroke opacity-4">Amazing Services</h4>
                </div>
                <div class="item">
                  <h4 class="stroke opacity-4">Amazing Services</h4>
                </div>
                <div class="item">
                  <h4 class="stroke opacity-4">Amazing Services</h4>
                </div>
                <div class="item">
                  <h4 class="stroke opacity-4">Amazing Services</h4>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <ModalVideo channel="youtube" videoId="pGbIOC83-So" :isOpen="isOpen" :onClose="closeVideo" />
  </section>
</template>
  
<script setup>
import { onMounted } from 'vue';
//= Components
import ModalVideo from '../Common/ModalVideo';
//= Scripts
import parallaxie from '@/common/parallaxie';

onMounted(() => {
  parallaxie(`.bg-img.parallaxie`, 0.4);
});

const isOpen = useState('isOpen', () => false);

function openVideo(event) {
  event.preventDefault();
  isOpen.value = true;
}

function closeVideo() {
  isOpen.value = false;
}
</script>