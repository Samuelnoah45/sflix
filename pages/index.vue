<script setup>
import homeDetail from "@/assets/json/Info.json";
useHead({
  title: "SFlix | watch HD movies",
  meta: [{ name: "description", content: "SFlix movie site" }],
  link: [
    { rel: "icon", type: "image/png", href: "@/assets/images/sfilx-logo.png" },
  ],
});
</script>

<template>
  <NavBar></NavBar>
  <div class="bg-primary2 min-h-screen flex flex-col items-center space-y-20 pb-10">
    <div class="w-1/2 flex flex-col items-center pt-24 space-y-10">
      <img class="w-24" src="@/assets/images/sfilx-logo.png" alt="sflix-log" />
      <span class="text-white text-2xl font-bold">SFlix</span>
      <div class="w-full flex space-x-0">
        <input
          class="h-12 rounded-l p-2 pl-4 outline-none w-full"
          placeholder="Enter keywords"
          type="text"
        />
        <div class="w-14 h-12 p-2 rounded-r bg-secondary">
          <svg class="text-white" width="32" height="32" viewBox="0 0 24 24">
            <path
              fill="currentColor"
              d="m19.6 21l-6.3-6.3q-.75.6-1.725.95Q10.6 16 9.5 16q-2.725 0-4.612-1.887Q3 12.225 3 9.5q0-2.725 1.888-4.613Q6.775 3 9.5 3t4.613 1.887Q16 6.775 16 9.5q0 1.1-.35 2.075q-.35.975-.95 1.725l6.3 6.3ZM9.5 14q1.875 0 3.188-1.312Q14 11.375 14 9.5q0-1.875-1.312-3.188Q11.375 5 9.5 5Q7.625 5 6.312 6.312Q5 7.625 5 9.5q0 1.875 1.312 3.188Q7.625 14 9.5 14Z"
            />
          </svg>
        </div>
      </div>
      <div>
        <BasicButton
          title="view full site"
          classStyle="h-14 bg-secondary text-white text-xl "
        >
          <template v-slot:default>
            <div>
              <svg width="32" height="32" viewBox="0 0 24 24">
                <path
                  fill="currentColor"
                  d="m12 16l4-4l-4-4l-1.4 1.4l1.6 1.6H8v2h4.2l-1.6 1.6Zm0 6q-2.075 0-3.9-.788q-1.825-.787-3.175-2.137q-1.35-1.35-2.137-3.175Q2 14.075 2 12t.788-3.9q.787-1.825 2.137-3.175q1.35-1.35 3.175-2.138Q9.925 2 12 2t3.9.787q1.825.788 3.175 2.138q1.35 1.35 2.137 3.175Q22 9.925 22 12t-.788 3.9q-.787 1.825-2.137 3.175q-1.35 1.35-3.175 2.137Q14.075 22 12 22Zm0-2q3.35 0 5.675-2.325Q20 15.35 20 12q0-3.35-2.325-5.675Q15.35 4 12 4Q8.65 4 6.325 6.325Q4 8.65 4 12q0 3.35 2.325 5.675Q8.65 20 12 20Zm0-8Z"
                />
              </svg>
            </div>
          </template>
        </BasicButton>
      </div>
      <div class="w-full space-y-10">
        <div class="space-y-2" v-for="info in homeDetail" :key="info.title">
          <div class="text-white text-xl font-bold">{{ info.title }}</div>
          <div class="text-gray-200">{{ info.description }}</div>
        </div>
      </div>
      <div>
        <BasicButton
          title="Go to sflix"
          classStyle="h-14 bg-secondary text-white text-xl "
        >
          <template v-slot:default>
            <div>
              <svg width="32" height="32" viewBox="0 0 24 24">
                <path
                  fill="currentColor"
                  d="m12 16l4-4l-4-4l-1.4 1.4l1.6 1.6H8v2h4.2l-1.6 1.6Zm0 6q-2.075 0-3.9-.788q-1.825-.787-3.175-2.137q-1.35-1.35-2.137-3.175Q2 14.075 2 12t.788-3.9q.787-1.825 2.137-3.175q1.35-1.35 3.175-2.138Q9.925 2 12 2t3.9.787q1.825.788 3.175 2.138q1.35 1.35 2.137 3.175Q22 9.925 22 12t-.788 3.9q-.787 1.825-2.137 3.175q-1.35 1.35-3.175 2.137Q14.075 22 12 22Zm0-2q3.35 0 5.675-2.325Q20 15.35 20 12q0-3.35-2.325-5.675Q15.35 4 12 4Q8.65 4 6.325 6.325Q4 8.65 4 12q0 3.35 2.325 5.675Q8.65 20 12 20Zm0-8Z"
                />
              </svg>
            </div>
          </template>
        </BasicButton>
      </div>
      <div class="flex flex-col items-center space-y-4">
        <div class="text-white space-x-4">
          <span>Android App</span>
          <span>Terms of service</span>
          <span>Contact</span>
          <span>Sitemap</span>
          <span>9anime</span>
          <span>Fmovies</span>
        </div>
        <div class="text-gray-600 text-sm">
          SFlix is a Free Movies streaming site with zero ads. We let you watch
          movies online without having to register or paying, with over 10000
          movies and TV-Series. You can also Download full movies from
          MoviesCloud and watch it later if you want.
        </div>
        <div class="text-gray-500 text-sm">
          © SFlix
        </div>
      </div>
    </div>
  </div>
</template>
