<script setup></script>
<template>
  <section class="page-3">
    <div class="page-3-container">
      <br />
      <h2>How Does It Work?</h2>
      <div
        id="carouselExampleSlidesOnly"
        class="carousel slide carousel-fade"
        data-bs-ride="carousel"
        data-bs-interval="3000"
      >
        <div class="carousel-inner">
          <div class="carousel-item active">
            <img
              src="/media/Iphone/pg3_iphone_1.svg"
              class="d-block w-500 h-auto m-auto"
              alt="Iphone-1"
            />
          </div>
          <div class="carousel-item">
            <img
              src="/media/Iphone/pg3_iphone_2.svg"
              class="d-block w-500 h-auto m-auto"
              alt="Iphone-2"
            />
          </div>
          <div class="carousel-item">
            <img
              src="/media/Iphone/pg3_iphone_3.svg"
              class="d-block w-500 h-auto m-auto"
              alt="Iphone-3"
            />
          </div>
        </div>
      </div>

      <h3>Transfers to people from your contact list</h3>
      <div class="pg3-p-ctn">
        <p class="pg3-p">
          straight from your contact list! With our app, you can transfer funds
          to people you know directly from your saved contacts, making
          transactions faster and simpler than ever before.
        </p>
      </div>
      <br />
    </div>
  </section>
</template>
<style scoped>
.page-3 {
  background-color: var(--Gray-100);
  width: 100%;
  align-items: center;
  text-align: center;

  .page-3-container {
    padding-left: 1rem;
    padding-right: 1rem;
  }

  .pg3-p {
    text-align: center;
    font-size: 1rem;
    font-style: normal;
    font-weight: 400;
    line-height: 26px;
  }
}

@media (min-width: 768px) {
  .page-3 {
    .page-3-container {
      max-width: 755px;
      margin: 0 auto;
    }

    h2 {
      margin-top: 2rem;
    }
    h3 {
      margin-top: 2rem;
    }

    .pg3-p-ctn {
      .pg3-p {
        width: 700px;
        height: 77px;
        margin: 30px 0px;
        color: var(--secondary-color);
        text-align: center;
        font-size: 20px;
        font-style: normal;
        font-weight: 400;
        line-height: 25.6px;
      }
    }
  }
}

@media (min-width: 1400px) {
  .page-3 {
    .page-3-container {
      margin: 0 auto;
    }
  }
}
</style>
