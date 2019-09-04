<template>
  <footer class="AppFooter px-5 md:px-10 flex-col lg:flex-row">
    <div class="mb-4 lg:mb-0 text-center md:text-left">
      <span class="block md:inline-block mb-4 md:mb-0 text-center">&copy; <a
        href="https://www.creatory.network"
        target="_blank"
      >Creatory.network</a> | {{ year }}. {{ $t('FOOTER.ALL_RIGHTS_RESERVED') }}</span> <div class="block md:inline-block">
        <span class="hidden md:inline-block"> | </span> <span>{{ $t('FOOTER.VERSION') }}: <a
          :href="versionLink"
          target="_blank"
        >{{ version }}</a> | {{ $t('FOOTER.DATE') }}: {{ date }}</span>
      </div>
    </div>
    <div class="text-center">
      <a
        href="https://www.facebook.com/creatorynetwork"
        target="_blank"
      >
        <svg
          class="m-1"
          xmlns="http://www.w3.org/2000/svg"
          xmlns:xlink="http://www.w3.org/1999/xlink"
          width="10px"
          height="16px"
          viewBox="0 0 320 512"
        >
          <path
            fill="currentColor"
            d="M279.14 288l14.22-92.66h-88.91v-60.13c0-25.35 12.42-50.06 52.24-50.06h40.42V6.26S260.43 0 225.36 0c-73.22 0-121.08 44$
          />
        </svg>
      </a>

      <a
        href="https://twitter.com/CreatoryNetwork"
        target="_blank"
      >
        <svg
          class="m-1"
          xmlns="http://www.w3.org/2000/svg"
          xmlns:xlink="http://www.w3.org/1999/xlink"
          width="16px"
          height="16px"
          viewBox="0 0 512 512"
        >
          <path
            fill="currentColor"
            d="M459.37 151.716c.325 4.548.325 9.097.325 13.645 0 138.72-105.583 298.558-298.558 298.558-59.452 0-114.68-17.219-161.1$
          />
        </svg>
      </a>
      <a
        href="mailto:hello@creatory.network"
        target="_blank"
      >
        <svg
          class="m-1"
          xmlns="http://www.w3.org/2000/svg"
          xmlns:xlink="http://www.w3.org/1999/xlink"
          width="16px"
          height="16px"
          viewBox="0 0 24 24"
        >
          <path
            fill-rule="evenodd"
            fill="currentColor"
            d="M12,0C5.4,0,0,5.4,0,12c0,6.6,5.4,12,12,12c2.3,0,4.6-0.7,6.6-1.9c0.6-0.4,0.7-1.2,0.3-1.7l-0.5-0.6c-0.4-0.5-1-0.6-1.5-0$
          />
        </svg>
      </a>

      <a
        href="https://t.me/creatorynetworkchat"
        target="_blank"
      >
        <svg
          class="m-1"
          xmlns="http://www.w3.org/2000/svg"
          xmlns:xlink="http://www.w3.org/1999/xlink"
          width="14px"
          height="16px"
          viewBox="0 0 448 512"
        >
          <path
            fill="currentColor"
            d="M446.7 98.6l-67.6 318.8c-5.1 22.5-18.4 28.1-37.3 17.5l-103-75.9-49.7 47.8c-5.5 5.5-10.1 10.1-20.7 10.1l7.4-104.9 190.$
          />
        </svg>
      </a>

      <a
        href="https://www.reddit.com/user/CreatoryNetwork"
        target="_blank"
      >
        <svg
          class="m-1"
          xmlns="http://www.w3.org/2000/svg"
          xmlns:xlink="http://www.w3.org/1999/xlink"
          width="16px"
          height="16px"
          viewBox="0 0 512 512"
        >
          <path
            fill="currentColor"
            d="M440.3 203.5c-15 0-28.2 6.2-37.9 15.9-35.7-24.7-83.8-40.6-137.1-42.3L293 52.3l88.2 19.8c0 21.6 17.6 39.2 39.2 39.2 22$
          />
        </svg>
      </a>
      <a
        href="https://www.reddit.com/user/CreatoryNetwork"
        target="_blank"
      >
        <svg
          class="m-1"
          xmlns="http://www.w3.org/2000/svg"
          xmlns:xlink="http://www.w3.org/1999/xlink"
          width="16px"
          height="16px"
          viewBox="0 0 512 512"
        >
          <path
            fill="currentColor"
            d="M440.3 203.5c-15 0-28.2 6.2-37.9 15.9-35.7-24.7-83.8-40.6-137.1-42.3L293 52.3l88.2 19.8c0 21.6 17.6 39.2 39.2 39.2 22$
          />
        </svg>
      </a>

      <a
        href="https://github.com/creatorynetwork"
        target="_blank"
      >
        <svg
          class="m-1"
          xmlns="http://www.w3.org/2000/svg"
          xmlns:xlink="http://www.w3.org/1999/xlink"
          width="16px"
          height="16px"
          viewBox="0 0 496 512"
        >
          <path
            fill="currentColor"
            d="M165.9 397.4c0 2-2.3 3.6-5.2 3.6-3.3.3-5.6-1.3-5.6-3.6 0-2 2.3-3.6 5.2-3.6 3-.3 5.6 1.3 5.6 3.6zm-31.1-4.5c-.7 2 1.3 $
          />
        </svg>
      </a>

    </div>
  </footer>
</template>

<script type="text/ecmascript-6">
import moment from 'moment'

export default {
  name: 'AppFooter',

  computed: {
    year () {
      return moment().format('Y')
    },
    version () {
      return GIT_VERSION
    },
    versionLink () {
      return `https://github.com/creatorynetwork/explorer/commit/${GIT_VERSION}`
    },
    date () {
      return GIT_DATE
    }
  }
}
</script>

<style>
.AppFooter {
  @apply .flex .flex-wrap .max-w-2xl .mx-auto .py-8 .text-theme-text-tertiary .justify-between .items-center;
}

.AppFooter svg {
  @apply .inline;
}
</style>
