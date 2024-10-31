<script setup></script>
<template>
  <section class="page-6">
    <div class="page-6-container">
      <div class="page-6-grid-1">
        <h2>Make your money transfer simple and clear</h2>
        <div class="statement-container">
          <div class="statement">
            <img src="/media/page-6_check-circle.svg" alt="Check Circle" />
            <p>Banking transactions are free for you</p>
          </div>
          <div class="statement">
            <img src="/media/page-6_check-circle.svg" alt="Check Circle" />
            <p>No monthly cash commissions</p>
          </div>
          <div class="statement">
            <img src="/media/page-6_check-circle.svg" alt="Check Circle" />
            <p>Manage payments and transactions online</p>
          </div>
        </div>
        <div class="btn-market-1">
          <button class="btn-market-1-style">
            Learn more <img src="/media/page-6-arrow.svg" alt="Arrow" />
          </button>
        </div>
        <div class="market-1">
          <img src="/media/page-6_1.svg" alt="Market" />
        </div>
      </div>
      <div class="page-6-grid-2">
        <h2>Receive payment from international bank details</h2>
        <div class="pg6-comm-1">
          <div class="ft-bg-pg2">
            <img src="/media/icons/payments.svg" alt="Easy Payments" />
          </div>
          <p>
            Manage your payments online. Mollis congue egestas egestas fermentum
            fames.
          </p>
        </div>
        <div class="pg6-comm-2">
          <div class="ft-bg-pg2">
            <img src="/media/icons/cashback.svg" alt="Regular Cashback" />
          </div>
          <p>
            A elementur and imperdiet enim, pretium etiam facilisi aenean quam
            mauris.
          </p>
        </div>
        <div class="market-2">
          <img src="/media/page-6_2.svg" alt="Market" />
        </div>
        <div class="btn-market-2">
          <button class="btn-market-2-style">
            Learn more<img src="/media/page-6-arrow.svg" alt="Arrow" />
          </button>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.page-6 {
  display: none;

  .page-6-container {
    display: none;
    max-width: 1320px;
    margin: 0 auto;
  }

  .page-6-grid-1 {
    display: grid;
    grid-template-columns: repeat(12, minmax(0, 1fr));
    gap: 1rem;

    h2 {
      margin-top: 2rem;
      grid-column: 3/7;
      grid-row: 1/2;
      text-align: left;
    }

    .market-1 {
      margin-top: 2rem;
      grid-column: 9/12;
      grid-row: 1/12;

      img {
        width: 410px;
        height: auto;
      }
    }

    .statement-container {
      grid-column: 3/8;
      grid-row: 2/3;
    }

    .statement {
      display: flex;
      flex-direction: row;
      justify-content: start;
      align-items: flex-start;
    }

    .btn-market-1 {
      grid-column: 3/7;
      grid-row: 3/4;
    }
  }
  .page-6-grid-2 {
    display: grid;
    grid-template-columns: repeat(12, minmax(0, 1fr));
    gap: 1rem;

    h2 {
      grid-column: 9/13;
      grid-row: 1/2;
      text-align: left;
    }
    .pg6-comm-1 {
      grid-column: 9/11;
      grid-row: 2/3;
    }

    .pg6-comm-2 {
      grid-column: 11/13;
      grid-row: 2/3;
    }

    .market-2 {
      grid-column: 3/4;
      grid-row: 1/12;

      img {
        width: 410px;
        height: auto;
      }
    }

    .btn-market-2 {
      grid-column: 9/11;
      grid-row: 3/4;
    }
  }

  .btn-market-1-style {
    grid-row: 1;
    grid-column: 6;
    background-color: var(--Brand-Primary);
    color: var(--white-color);
    border-radius: 8px;
    border: 0px;
    padding: 12px 25px;
    display: flex;
    justify-content: center;
    align-items: center;
    text-decoration: none;
    box-shadow:
      0px 4.4px 12px -1px rgba(#6366f1, 0.06),
      0px 2px 6.4px -1px rgba(#6366f1, 0.03);
  }

  .btn-market-2-style {
    grid-row: 1;
    grid-column: 6;
    background-color: var(--Brand-Primary);
    color: var(--white-color);
    border-radius: 8px;
    border: 0px;
    padding: 12px 25px;
    display: flex;
    justify-content: center;
    align-items: center;
    text-decoration: none;
  }
}

@media (min-width: 768px) {
  .page-6 {
    display: none;
  }
}

@media (min-width: 1400px) {
  .page-6 {
    display: block;

    .page-6-container {
      display: block;
    }
  }

  .ft-bg-pg2 {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 60px;
    height: 60.08px;
    margin-top: 1.5rem;
    border-radius: 8px;
    background: var(--Gray-100);
  }
}
</style>
