<template>
  <div class="flex flex-col w-content mx-auto pt-9">
    <div class="header h-16 flex justify-between items-center">
      <div class="flex items-center space-x-3">
        <h1 class="text-4xl font-bold">data I</h1>
      </div>
      <div class="links flex items-center space-x-5 text-black-1 dark:text-white font-['Poppins'] text-[17px]">
        <!--<a v-for="link in links" :key="link" class="group relative h-7 flex items-center cursor-pointer">
          <span>{{ link }}</span>
        </a>-->
        <div class="flex justify-center ml-2" @click="toggleColorMode">
          <input type="checkbox" name="light-switch" class="light-switch sr-only" />
          <label
            class="relative h-[30px] p-[3px] bg-[#F0F2F5] dark:bg-[#2C2C2C] rounded-full after:content-[''] after:transition-transform after:duration-500 after:absolute after:dark:translate-x-full after:w-6 after:h-6 after:p-[6px] after:rounded-full after:bg-gradient-to-r after:from-[#439DFF] after:to-[#6052FF] flex items-center cursor-pointer select-none"
            for="light-switch">
            <img class="m-[6px] z-20 w-3 h-3" src="~/assets/svg/light-mode.svg" alt="light-mode">
            <img class="m-[6px] z-20 w-3 h-3" src="~/assets/svg/dark-mode.svg" alt="dark-mode">
            <span class="sr-only">Switch to light / dark version</span>
          </label>
        </div>
      </div>
    </div>
    <div class="slogon mt-12 flex justify-between items-center">
      <div class="flex flex-col space-y-12">
        <div class="texts flex flex-col space-y-6">
          <div class="titles flex flex-col space-y-9">
            <div class="flex flex-col space-y-4 text-black-1 dark:text-white">
              <h1 class="text-6xl font-bold">data I</h1>
              <!--<span class="w-[450px] text-[50px] leading-none font-['Poppins'] font-medium tracking-[0.6px]"><b>Move Game
                Kit</b></span>-->
              <span class="w-[700px] text-[20px] leading-tight font-['Poppins']">AI Tool Kit preparing for the NEXT Generation.</span>
              <span class="w-[700px] text-[20px] leading-tight font-['Poppins']">AI should collaborate with human 🤝, not fight against human ⚔️.</span>
            </div>
          </div>
          <div class="flex items-center space-x-2 text-third-gray dark:text-gray-4 text-[20px]">
            <span class="leading-8">
              Powered by <a href="https://x.com/intent/follow?screen_name=0xleeduckgo" target="_blank" rel="noopener noreferrer"
                class="text-blue-500 underline">0xleeduckgo</a>
            </span>
            &nbsp;and other NonceGeekDAO members
            <img class="w-8 h-8" src="/img/logo-ng.jpg" alt="noncegeek">
          </div>
        </div>
        <div class="buttons flex items-center space-x-8">
          <template v-for="button in buttons" :key="button.text">
            <TheButton :text="button.text" :uppercase="true" :high="true" :colored-border="button.coloredBorder"
              :change-text="true" :href="button.href" />
          </template>
        </div>
      </div>
      <div id="robot-container" class="w-[400px] h-[400px]">
        <svg width="400" height="400"></svg>
      </div>
      <!-- Try SVG Animation in this homepage. -->
    </div>
    <div class="mt-40 mx-auto w-[1160px] flex flex-col items-center space-y-[142px]">

      <!-- A Block Begin -->
      <div class="w-full flex justify-start items-center space-x-60">
        <div class="w-[555px] flex flex-col space-y-6 items-start">
          <div class="w-full flex flex-col space-y-2 text-[20px] text-second-gray dark:text-white font-['Poppins']">
            <div class="flex items-center">
              Lego-style FaaS System based on Blockchain, 
              <br>
              the hand✋🏻 of AI Agents. 
            </div>
          </div>
          <TheButton text="Launch App" :colored-border="true" href="https://faas.movespace.xyz" />
        </div>

        <div class="title text-black-2 dark:text-white text-[40px] font-['Poppins'] font-semibold flex items-center">
          <span>dataI FaaS 🦔</span>
        </div>

      </div>
      <div class="w-[575px] p-2.5">
        <LinearLine />
      </div>
      <!-- A Block End -->

      <!-- B Block Begin -->
      <div class="w-full flex justify-start items-center space-x-60">
        <div class="title text-black-2 dark:text-white text-[30px] font-['Poppins'] font-semibold flex items-center">
          <span>dataI Dataset Service 🐘</span>
        </div>
        <div class="w-[555px] flex flex-col space-y-6 items-start">
          <div class="w-full flex flex-col space-y-2 text-[20px] text-second-gray dark:text-white font-['Poppins']">
            <div class="flex items-center">
              Multimodal Dataset Service based on VectorDB, 
              <br>
              including Text, Image, Audio, Video, etc.
              <br><br>
              Supporting search, retrieval, combination and analysis across multiple datasets.
            </div>
          </div>

          <TheButton text="An Search Example" :colored-border="true" href="https://bodhi.movespace.xyz" />
        </div>
      </div>
      <div class="w-[575px] p-2.5">
        <LinearLine />
      </div>
      <!-- B Block End -->

      <!-- A Block Begin -->
      <div class="w-full flex justify-start items-center space-x-60">
        <div class="w-[555px] flex flex-col space-y-6 items-start">
          <div class="w-full flex flex-col space-y-2 text-[20px] text-second-gray dark:text-white font-['Poppins']">
            <div class="flex items-center">
              Tagger Data Item based on Web3 & AI.
            </div>
          </div>

          <TheButton text="Contact Us" :colored-border="true" href="https://t.me/leeduckgo" />
        </div>

        <div class="title text-black-2 dark:text-white text-[30px] font-['Poppins'] font-semibold flex items-center">
          <span>dataI Tagger Service 🔖</span>

        </div>

      </div>
      <div class="w-[575px] p-2.5">
        <LinearLine />
      </div>
      <!-- A Block End -->

      <!-- A Block Begin -->
      <div class="w-full flex justify-start items-center space-x-60">
        <div class="title text-black-2 dark:text-white text-[30px] font-['Poppins'] font-semibold flex items-center">
          <span>dataI LLM Service 💭</span>

        </div>
        <div class="w-[555px] flex flex-col space-y-6 items-start">
          <div class="w-full flex flex-col space-y-2 text-[20px] text-second-gray dark:text-white font-['Poppins']">
            <div class="flex items-center">
              Not only the General LLM like GPT, 
              <br>
              but also the c00l quick-response micro LLM.
            </div>
          </div>

          <TheButton text="Contact Us" :colored-border="true" href="https://t.me/leeduckgo" />
        </div>



      </div>
      <div class="w-[575px] p-2.5">
        <LinearLine />
      </div>
      <!-- A Block End -->

      <!-- A Block Begin -->
      <div class="w-full flex justify-start items-center space-x-60">
        <div class="w-[555px] flex flex-col space-y-6 items-start">
          <div class="w-full flex flex-col space-y-2 text-[20px] text-second-gray dark:text-white font-['Poppins']">
            <div class="flex items-center">
              Generate Apps lightning fast ⚡.
            </div>
          </div>

          <TheButton text="Launch App" :colored-border="true" href="https://d1v.ai" />
          <TheButton text="Author" :colored-border="true" href="https://x.com/aboutdreamfly" />
        </div>

        <div class="title text-black-2 dark:text-white text-[30px] font-['Poppins'] font-semibold flex items-center">
          <span>dataI App Generator 📦</span>

        </div>

      </div>


    </div>




    <!-- Footer -->
    <div class="footer mt-60 pb-24 flex flex-col space-y-3">
      <LinearLine />
      <div class="flex justify-between items-center text-third-gray dark:text-white font-['Montserrat']">
        <span v-for="text in footerTexts" :key="text">{{ text }}</span>
      </div>
    </div>
  </div>
</template>

<script setup>
const links = [
  'Twitter',
]
const buttons = [
  {
    text: 'Github',
    coloredBorder: false,
    href: 'https://github.com/NonceGeek/data-i',
  },
  {
    text: 'Whitepaper-EN',
    coloredBorder: false,
    href: '/',
  },
  {
    text: 'Whitepaper-CN',
    coloredBorder: false,
    href: '/',
  },
  {
    text: 'Full Video',
    coloredBorder: false,
    href: '/',
  },
]
const footerTexts = [
  '𑖌𑖼Copyright © 2024 NonceGeekDAO & rootMUD DAO. All rights reserved.𑖌𑖼',
  'Terms of Use & Privacy Policy',
]

const colorMode = useColorMode('dark');
const toggleColorMode = () => {
  if (colorMode.preference === 'dark') {
    colorMode.preference = 'light'
  } else {
    colorMode.preference = 'dark'
  }
}

const scrollToTop = () => {
  window.scrollTo({
    top: 0,
    behavior: 'smooth',
  })
}

// Add this array of hexagrams before initRobot function
const hexagrams = [
  '111111', '000000', '100010', '010001', '111010', '010111', '010000', '000010',
  '111011', '110111', '111000', '000111', '101111', '111101', '001000', '000100',
  '100110', '011001', '110000', '000011', '100101', '101001', '000001', '100000',
  '100111', '111001', '100001', '011110', '010010', '101101', '011100', '001110',
  '001111', '111100', '001010', '010100', '101000', '000101', '001101', '101100',
  '110001', '100011', '111110', '011111', '000110', '011000', '010110', '011010',
  '011101', '101110', '101011', '110101', '001001', '100100', '110100', '001011',
  '110110', '011011', '110010', '010011', '110011', '001100', '101010', '010101'
];

function drawHexagram(snap, hexagram) {
    const lineWidth = 200;
    const lineHeight = 20;
    const lineGap = 10;
    const startX = 100;
    const startY = 100;
    
    hexagram.split('').forEach((bit, index) => {
      const y = startY + (index * (lineHeight + lineGap));
      
      if (bit === '1') {
        snap.line(startX, y, startX + lineWidth, y)
          .attr({
            stroke: colorMode.preference === 'dark' ? '#fff' : '#000',
            strokeWidth: lineHeight,
            strokeLinecap: 'round'
          });
      } else {
        const gap = 60;
        const segmentWidth = (lineWidth - gap) / 2;
        snap.line(startX, y, startX + segmentWidth, y)
          .attr({
            stroke: colorMode.preference === 'dark' ? '#fff' : '#000',
            strokeWidth: lineHeight,
            strokeLinecap: 'round'
          });
        snap.line(startX + segmentWidth + gap, y, startX + lineWidth, y)
          .attr({
            stroke: colorMode.preference === 'dark' ? '#fff' : '#000',
            strokeWidth: lineHeight,
            strokeLinecap: 'round'
          });
      }
    });
  }

const initRobot = () => {
  const container = document.getElementById('robot-container');
  if (!container) {
    console.error('Robot container not found');
    return;
  }

  const s = Snap(container.querySelector('svg'));
  let currentHexagram = hexagrams[Math.floor(Math.random() * hexagrams.length)];
  let intervalId = null;
  const svg = container.querySelector('svg');
  
  // 保存初始的六爻图案
  const initialHexagram = currentHexagram;
  
  // Draw initial hexagram
  drawHexagram(s, currentHexagram);
  
  svg.addEventListener('mouseenter', () => {
    if (intervalId) return; // 防止多次启动interval
    
    intervalId = setInterval(() => {
      s.clear();
      currentHexagram = hexagrams[Math.floor(Math.random() * hexagrams.length)];
      drawHexagram(s, currentHexagram);
    }, 500);
  });

  svg.addEventListener('mouseleave', () => {
    if (intervalId) {
      clearInterval(intervalId);
      intervalId = null;
    }
    
    s.clear();
    // 恢复到初始状态
    currentHexagram = initialHexagram;
    drawHexagram(s, currentHexagram);
  });
};

// Initialize robot when component is mounted
onMounted(() => {
  // Add Snap.svg script dynamically
  const script = document.createElement('script');
  script.src = 'https://cdnjs.cloudflare.com/ajax/libs/snap.svg/0.5.1/snap.svg-min.js';
  script.onload = () => {
    // Add a small delay to ensure Snap is fully loaded
    setTimeout(() => {
      initRobot();
      // Draw initial random hexagram
      const container = document.getElementById('robot-container');
      if (container) {
        const s = Snap(container.querySelector('svg'));
        const randomHexagram = hexagrams[Math.floor(Math.random() * hexagrams.length)];
        drawHexagram(s, randomHexagram);
      }
    }, 100);
  };
  document.head.appendChild(script);
});
</script>

<style scoped></style>
