<script setup lang="ts">
import ContentTable from '@/components/ContentTable.vue'
import DraggableUpload from '@/components/DraggableUpload.vue'
</script>

<template>
  <main class="bg-gray-100 h-full px-2 lg:px-4">

    <!-- Breadcrum Component-->
    <div class="w-full bg-white my-4 py-4 px-2 lg:px-4">
      <span>File Manager / Home</span>
    </div>

    <!-- Main Page Layout-->
    <div class="flex flex-col lg:flex-row space-y-8 lg:space-y-0 lg:space-x-8">

      <!-- Upload and file navigation-->
      <div class="w-full flex flex-col justify-between lg:w-1/4 bg-white">
      <div>
        <button type="button" class="bg-blue-600 text-white w-full py-2 uppercase text-sm tracking-widest font-medium">Upload File</button>
        <div class="flex flex-row items-center justify-evenly">
          <button class="w-full bg-gray-100 py-2 text-sm">All</button>
          <button class="w-full py-2 text-sm">Documents</button>
          <button class="w-full py-2 text-sm">Audio</button>
          <button class="w-full py-2 text-sm">Images</button>
        </div>
      </div>

      <div>
        <div class="bg-blue-50 flex flex-row justify-center py-2">
          <span class="uppercase text-blue-700 text-sm font-semibold">you are using 0.0GB / 512 GB</span>
        </div>
      </div>
      
      </div>

      <!-- Files browser-->
      <div class="w-full lg:w-3/4 bg-white px-4 py-4">
        <h2>Your Recent Files</h2>
        <div class="flex flex-row justify-evenly flex-wrap pt-4">
          <button type="button" class="mb-2 flex flex-row items-center space-x-2 border border-slate-400 rounded-md px-5 py-1.5 uppercase text-xs font-semibold">
            <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 7l-.867 12.142A2 2 0 0116.138 21H7.862a2 2 0 01-1.995-1.858L5 7m5 4v6m4-6v6m1-10V4a1 1 0 00-1-1h-4a1 1 0 00-1 1v3M4 7h16"></path></svg>
            <span>Delete</span>
          </button>

          <button type="button" class="mb-2 flex flex-row items-center space-x-2 border border-slate-400 rounded-md px-5 py-1.5 uppercase text-xs font-semibold">
            <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 9l4-4 4 4m0 6l-4 4-4-4"></path></svg>            
            <span>Move</span>
          </button>

          <button type="button" class="mb-2 flex flex-row items-center space-x-2 border border-slate-400 rounded-md px-5 py-1.5 uppercase text-xs font-semibold">
            <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 7v8a2 2 0 002 2h6M8 7V5a2 2 0 012-2h4.586a1 1 0 01.707.293l4.414 4.414a1 1 0 01.293.707V15a2 2 0 01-2 2h-2M8 7H6a2 2 0 00-2 2v10a2 2 0 002 2h8a2 2 0 002-2v-2"></path></svg>
            <span>Copy</span>
          </button>

          <button type="button" class="mb-2 flex flex-row items-center space-x-2 border border-slate-400 rounded-md px-5 py-1.5 uppercase text-xs font-semibold">
            <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13.828 10.172a4 4 0 00-5.656 0l-4 4a4 4 0 105.656 5.656l1.102-1.101m-.758-4.899a4 4 0 005.656 0l4-4a4 4 0 00-5.656-5.656l-1.1 1.1"></path></svg>
            <span>Copy Link</span>
          </button>

          <button type="button" class="mb-2 flex flex-row items-center space-x-2 border border-slate-400 rounded-md px-5 py-1.5 uppercase text-xs font-semibold">
            <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15.232 5.232l3.536 3.536m-2.036-5.036a2.5 2.5 0 113.536 3.536L6.5 21.036H3v-3.572L16.732 3.732z"></path></svg>
            <span>Rename</span>
          </button>

          <button type="button" class="mb-2 flex flex-row items-center space-x-2 border border-slate-400 rounded-md px-5 py-1.5 uppercase text-xs font-semibold">
            <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 13h6m-3-3v6m-9 1V7a2 2 0 012-2h6l2 2h6a2 2 0 012 2v8a2 2 0 01-2 2H5a2 2 0 01-2-2z"></path></svg>
            <span>New Folder</span>
          </button>

        </div>

        <div class="mt-2 max-h-72 overflow-auto">
          <ContentTable/>
        </div>

        <DraggableUpload/>

      </div>
    </div>

  </main>
</template>
