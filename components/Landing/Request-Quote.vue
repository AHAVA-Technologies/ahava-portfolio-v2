<template>
  <section
    id="request-quote"
    class="grid min-h-[90vh] grid-cols-1 md:grid-cols-7 gap-x-10 items-center"
  >
    <div class="col-span-1 md:col-span-4">
      <div class="pb-3 mb-5 animated_underline">
        <h5 class="text-lg font-bold uppercase sm:text-xl text-primary-600">
          Request a Quote
        </h5>
        <h1
          class="mt-3 mb-0 text-2xl font-extrabold sm:text-3xl md:text-4xl text-midnight-950"
        >
          Need A Free Quote? Please Feel Free to Contact Us
        </h1>
      </div>
      <div class="mb-3">
        <div class="grid grid-cols-2 zoomIn">
          <h5 class="mb-3 text-base sm:text-lg font-[500] sm:gap-x-3 gap-x-2">
            <Icon
              name="fa-solid:reply"
              class="text-xl font-extrabold sm:text-2xl text-primary-600"
            />
            <span> Reply within 24 hours </span>
          </h5>
          <h5 class="mb-3 text-base sm:text-lg font-[500] gap-x-3">
            <Icon
              name="ic:round-phone"
              class="text-xl font-extrabold sm:text-2xl text-primary-600"
            />
            <span> 24 hrs telephone support </span>
          </h5>
        </div>
      </div>
      <p class="mb-4 text-secondary-600">
        Whether you're seeking a custom product, specialized service, or
        comprehensive solution package, our form allows you to easily
        communicate your requirements. Our experienced team will carefully
        review your details and prepare a comprehensive quote with transparent
        pricing, terms, and additional relevant information. We value your time
        and strive to provide prompt responses, delivering exceptional customer
        service at every step.
      </p>
      <div class="flex mb-4 align-center wow fadeIn" data-wow-delay="0.6s">
        <div
          class="flex items-center justify-center w-16 h-16 rounded bg-primary-600"
        >
          <Icon name="ic:round-phone" class="text-2xl text-white" />
        </div>
        <div class="ps-4">
          <h5 class="mb-2 text-xl">Call to ask any question</h5>
          <h4 class="mb-0 text-primary-600 font-[700] text-2xl">
            +251 939 064 200
          </h4>
        </div>
      </div>
    </div>
    <div class="col-span-1 md:col-span-3">
      <Landing-QuoteForm />
    </div>
  </section>
</template>
