<template>
    <div class="isolate bg-white px-6 py-24 sm:py-32 lg:px-8" id="Cont">
      <div class="mx-auto max-w-2xl text-center">
        <h2 class="text-3xl font-bold tracking-tight text-gray-900 sm:text-4xl">
          Contactos
        </h2>
        <p class="mt-2 text-lg leading-8 text-gray-600">
          Puede escribir para mayor informacion o dudas
        </p>
      </div>
      <form
        @submit.prevent="handleSubmit"
        class="mx-auto mt-16 max-w-xl sm:mt-20"
      >
        <div class="grid grid-cols-1 gap-x-8 gap-y-6 sm:grid-cols-2">
          <div>
            <label
              for="first-name"
              class="block text-sm font-semibold leading-6 text-gray-900 not null"
              >Nombre</label
            >
            <div class="mt-2.5">
              <input
                type="text"
                name="firstname"
                id="first-name"
                autocomplete="given-name"
                class="block w-full rounded-md border-0 px-3.5 py-2 text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-indigo-600 sm:text-sm sm:leading-6"
                ref="firstName"
              />
            </div>
          </div>
          <div>
            <label
              for="last-name"
              class="block text-sm font-semibold leading-6 text-gray-900"
              >Apellido</label
            >
            <div class="mt-2.5">
              <input
                type="text"
                name="last-name"
                id="last-name"
                autocomplete="family-name"
                class="block w-full rounded-md border-0 px-3.5 py-2 text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-indigo-600 sm:text-sm sm:leading-6"
                ref="lastName"
              />
            </div>
          </div>
          <div class="sm:col-span-2">
            <label class="block">
              <span
                class="after:content-['*'] after:ml-0.5 after:text-red-500 block text-sm font-medium text-slate-700"
              >
                Compañia
              </span>
              <input
                type="comun"
                name="email"
                class="mt-1 px-3 py-2 bg-white border shadow-sm border-slate-300 placeholder-slate-400 focus:outline-none focus:border-sky-500 focus:ring-sky-500 block w-full rounded-md sm:text-sm focus:ring-1"
                placeholder="exemplo: Selectos"
              />
            </label>
          </div>
          <div class="sm:col-span-2">
            <label class="block">
              <span
                class="after:content-['*'] after:ml-0.5 after:text-red-500 block text-sm font-medium text-slate-700"
              >
                Email
              </span>
              <input
                type="email"
                name="email"
                class="mt-1 px-3 py-2 bg-white border shadow-sm border-slate-300 placeholder-slate-400 focus:outline-none focus:border-sky-500 focus:ring-sky-500 block w-full rounded-md sm:text-sm focus:ring-1"
                placeholder="you@example.com"
              />
            </label>
          </div>
          <div class="sm:col-span-2">
            <label
              for="phone-number"
              class="block text-sm font-semibold leading-6 text-gray-900"
              >Numero de telefono</label
            >

            <div class="relative mt-2.5">
              <div class="absolute inset-y-0 left-0 flex items-center">
                <label for="country" class="sr-only">Country</label>
                <select
                  id="country"
                  name="country"
                  class="h-full rounded-md border-0 bg-transparent bg-none py-0 pl-4 pr-9 text-gray-400 focus:ring-2 focus:ring-inset focus:ring-indigo-600 sm:text-sm"
                >
                  <option>ES</option>
                  <option>CA</option>
                  <option>USA</option>
                </select>
                <ChevronDownIcon
                  class="pointer-events-none absolute right-3 top-0 h-full w-5 text-gray-400"
                  aria-hidden="true"
                />
              </div>
              <input
                type="tel"
                name="phone-number"
                id="phone-number"
                autocomplete="tel"
                class="block w-full rounded-md border-0 px-3.5 py-2 pl-20 text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-indigo-600 sm:text-sm sm:leading-6"
              />
            </div>
          </div>
          <div class="sm:col-span-2">
            <label
              for="message"
              class="block text-sm font-semibold leading-6 text-gray-900"
              >Message</label
            >
            <div class="mt-2.5">
              <textarea
                name="message"
                id="message"
                rows="4"
                class="block w-full rounded-md border-0 px-3.5 py-2 text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-indigo-600 sm:text-sm sm:leading-6"
              />
            </div>
          </div>
          <SwitchGroup as="div" class="flex gap-x-4 sm:col-span-2">
            <div class="flex h-6 items-center"></div>
            <SwitchLabel class="text-sm text-center leading-6 text-gray-600">
              Al seleccionar esto, usted acepta nuestra
              {{ " " }}
              <a href="" class="font-semibold text-indigo-600"
                >privacy&nbsp;policy</a
              >.
            </SwitchLabel>
          </SwitchGroup>
        </div>
        <div class="mt-10">
          <button
            type="submit"
            class="block w-full rounded-md bg-indigo-600 px-3.5 py-2.5 text-center text-sm font-semibold text-white shadow-sm hover:bg-indigo-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600"
          >
            Enviar Informacion
          </button>
        </div>
      </form>
    </div>
</template>

<script lang="ts">
import Swal from "sweetalert2";

export default {
  methods: {
    handleSubmit() {
      Swal.fire({
        title: "¡Nos pondremos en contacto!",
        text: `Gracias, .`,
        icon: "success",
      });
    },
  },
};
</script>
