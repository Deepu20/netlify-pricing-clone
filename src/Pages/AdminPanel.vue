<template>
  <AdminLayout>
    <div class="bg-white border shadow-sm flex justify-between items-center sticky">
      <div class="relative blue-svg">
        <!-- Seach Input Container -->
        <svg
          class="absolute top-6 left-6 w-5 h-5 text-gray-400 hover:text-blue-300"
          fill="none"
          stroke-linecap="round"
          stroke-linejoin="round"
          stroke-width="2"
          viewBox="0 0 24 24"
          stroke="currentColor"
        ><path d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z" /></svg>
        <input
          id="search"
          class="focus:border-blue-500 focus:outline-none focus:shadow-outline text-black font-normal text-base ml-4 my-3 py-2 px-8 bg-gray-100 rounded-md focus:text-black focus:bg-white outline-none border border-transparent focus:border focus:border-gray-200 hover:border-gray-100 hover:bg-white transition duration-200 ease-in-out"
          type="text"
          name="search"
          placeholder="Search"
          autocomplete="off"
        >
      </div>
            
      <div class="mr-5 flex items-center justify-between space-x-2">
        <!-- Profile Avatar Section -->
        <div 
          class="relative rounded-full w-10 h-10 text-gray-400 hover:text-blue-500 cursor-pointer inline-flex items-center justify-center hover:bg-blue-50 transition duration-200 ease-in-out"
          @mouseover="isVisible = true"
          @mouseleave="isVisible = false"
        >
          <svg
            class="w-7 h-7"
            fill="none"
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            viewBox="0 0 24 24"
            stroke="currentColor"
          ><path d="M15 17h5l-1.405-1.405A2.032 2.032 0 0118 14.158V11a6.002 6.002 0 00-4-5.659V5a2 2 0 10-4 0v.341C7.67 6.165 6 8.388 6 11v3.159c0 .538-.214 1.055-.595 1.436L4 17h5m6 0v1a3 3 0 11-6 0v-1m6 0H9" /></svg>
          <transition name="fade">
            <div
              v-if="isVisible"
              class="absolute bg-white right-0 top-12 rounded-md shadow-3xl w-80 cursor-default"
            >
              <div class="py-3 border-b font-medium uppercase text-gray-400 tracking-wide">
                <div class="mx-4 flex items-center justify-between">
                  <span>Notifications</span>
                  <span class="text-xs bg-blue-200 text-blue-500 px-2 rounded-full">3 new</span>
                </div>
              </div>
              <div class="text-gray-400">
                <div class="flex flex-col mb-10 items-center justify-center">
                  <svg
                    class="w-20 h-20 my-5"
                    fill="none"
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="2"
                    viewBox="0 0 24 24"
                    stroke="currentColor"
                  ><path d="M4 5a1 1 0 011-1h14a1 1 0 011 1v2a1 1 0 01-1 1H5a1 1 0 01-1-1V5zM4 13a1 1 0 011-1h6a1 1 0 011 1v6a1 1 0 01-1 1H5a1 1 0 01-1-1v-6zM16 13a1 1 0 011-1h2a1 1 0 011 1v6a1 1 0 01-1 1h-2a1 1 0 01-1-1v-6z" /></svg>
                  <span class="font-semibold text-base">
                    You do not have any Notifications!
                  </span>
                </div>
                <ul
                  v-if="false"
                  class="mt-6 mb-10"
                >
                  <li class="px-10 py-2 font-bold text-base cursor-pointer hover:bg-gray-100">
                    A new order has been placed!
                  </li>
                </ul>
              </div>
            </div>
          </transition>
        </div>

        <a
          href="#"
          class="border-2 border-gray-200 hover:border-gray-400 rounded-full"
        >
          <img
            class="w-9 h-w-9 object-cover rounded-full"
            src="https://pbs.twimg.com/profile_images/1239889016431861760/jmP-jjik_400x400.jpg"
            alt="Nitin Kaware"
          >
        </a>
      </div>
    </div>
    <div class="overflow-y-auto">
      <div class="mx-4 my-4">
        <CandidateInformation />
      </div>
      <div class="bg-white rounded-md shadow-md mx-4 p-5">
        <div class="max-w-4xl bg-orange-100 p-4 rounded flex space-x-2">
          <div class="w-7 h-7 bg-orange-50 rounded-full inline-flex items-center justify-center">
            <svg
              class="w-5 h-5 text-orange-400"
              fill="none"
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              viewBox="0 0 24 24"
              stroke="currentColor"
            ><path d="M12 9v2m0 4h.01m-6.938 4h13.856c1.54 0 2.502-1.667 1.732-3L13.732 4c-.77-1.333-2.694-1.333-3.464 0L3.34 16c-.77 1.333.192 3 1.732 3z"></path></svg>
          </div>
          <div>
            <h1 class="text-orange-800 font-semibold text-sm">
              Attention Required
            </h1>
            <p class="text-orange-800 font-normal text-sm">
              Your account will be de-activated if you do not verify your email address.
            </p>
          </div>
        </div>
      </div>
      <div class="bg-white rounded-md shadow-md m-4 p-5">
        <div class="max-w-4xl bg-red-100 p-4 rounded flex items-start space-x-2">
          <svg
            class="w-6 h-6 text-red-400"
            fill="none"
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            viewBox="0 0 24 24"
            stroke="currentColor"
          ><path d="M10 14l2-2m0 0l2-2m-2 2l-2-2m2 2l2 2m7-2a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>
          <div class="flex flex-col w-full items-start justify-center space-y-2">
            <h1 class="text-red-800 font-semibold text-sm">
              There were 2 errors with your submission.
            </h1>
            <ul class="list-disc list-inside text-red-800 font-normal text-sm">
              <li>Your password must be at least 8 characters</li>
              <li>This email address is alreadu associated with anather account.</li>
            </ul>
          </div>
        </div>
      </div>
      <div class="bg-gray-500 rounded-md shadow-md m-4 p-5">
        <div class="shadow-2xl bg-white rounded-md max-w-lg overflow-hidden p-6">
          <div class="flex flex-col justify-center items-center space-y-2">
            <span class="w-10 h-10 bg-green-100 flex items-center justify-center rounded-full mb-3">
              <svg
                class="w-6 h-6 text-green-700"
                fill="none"
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                viewBox="0 0 24 24"
                stroke="currentColor"
              ><path d="M5 13l4 4L19 7"></path></svg>
            </span>
            <span class="font-semibold text-lg">Payment Successfull</span>
            <span class="text-sm text-gray-500 font-medium text-center">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Natus voluptates nam alias necessitatibus repellat! Itaque quod omnis quaerat distinctio, doloremque sunt odit facere inventore dolores autem obcaecati molestias minus et?</span>
          </div>
          <div class="flex items-center justify-center mt-6 space-x-2">
            <button class="px-20 py-1.5 rounded-md border border-gray-300 text-gray-900">
              Cancel
            </button>
            <button class="px-20 py-1.5 rounded-md bg-blue-500 text-white font-medium hover:bg-blue-600">
              Deactivate
            </button>
          </div>
        </div>
      </div> 
    </div>
    <div class="bg-gray-500 rounded-md shadow-md m-4 p-5">
      <div class="shadow-2xl bg-white rounded-md max-w-lg overflow-hidden">
        <div class="p-4 flex space-x-4">
          <div class="bg-red-100 w-10 h-10 rounded-full inline-flex flex-shrink-0 items-center justify-center mx-auto">
            <svg
              class="w-6 h-6 text-red-500"
              fill="none"
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              viewBox="0 0 24 24"
              stroke="currentColor"
            ><path d="M12 9v2m0 4h.01m-6.938 4h13.856c1.54 0 2.502-1.667 1.732-3L13.732 4c-.77-1.333-2.694-1.333-3.464 0L3.34 16c-.77 1.333.192 3 1.732 3z"></path></svg>
          </div>
          <div>
            <h1 class="font-medium">
              Deactivate Account
            </h1>
            <p class="font-medium text-sm text-gray-500">
              Are you sure you want to deactivate your account? All of your data will be permanantly removed. This action can not be undone?
            </p>
          </div>
        </div>
        <div class="bg-gray-50 flex items-center justify-end space-x-4 px-6 py-2">
          <button class="font-normal px-4 py-1.5 bg-white rounded-md border border-gray-200 text-gray-900 focus:outline-none">
            Cancel
          </button>
          <button class="font-medium px-4 py-1.5 rounded-md bg-red-600 text-white hover:bg-red-500 focus:outline-none">
            Deactivate
          </button>
        </div>
      </div> 
    </div>
  </AdminLayout>
</template>

<script>
import AdminLayout from '../Layouts/AdminLayouts.vue'
import CandidateInformation from '../components/AdminPanel/CandidateInformation.vue'
export default {
    components: { CandidateInformation, AdminLayout },
    data () {
        return {
            isVisible: false
        }
    }
}
</script>