<script setup></script>
<template>
  <section class="page-2">
    <div class="page-2-container">
      <div class="sponsors">
        <div class="sp4">
          <img src="/media/logo/logo1.svg" alt="Sponsor 1" />
        </div>
        <div class="sp4">
          <img src="/media/logo/logo2.svg" alt="Sponsor 2" />
        </div>
        <div class="sp4">
          <img src="/media/logo/logo3.svg" alt="Sponsor 3" />
        </div>
        <div class="sp4">
          <img src="/media/logo/logo4.svg" alt="Sponsor 4" />
        </div>
        <div class="desk">
          <img src="/media/logo/logo5.svg" alt="Sponsor 5" />
        </div>
        <div class="desk">
          <img src="/media/logo/logo6.svg" alt="Sponsor 6" />
        </div>
      </div>
      <div class="ft-grid">
        <h2 class="ft-grid-obj-1 app-ft-intro">App Features</h2>
        <p class="ft-grid-obj-2 app-ft-intro">
          Our app offers 24/7 account access and allows you to download
          transaction history in PDF, CSV, or Excel. Schedule future transfers,
          create secure yet memorable passwords, and easily recover them if
          needed.
        </p>
      </div>
      <div class="app-ft">
        <div class="app-ft-grid-2">
          <img
            src="/media/Iphone/app_ft_iphone.svg"
            alt="Iphone"
            class="app-ft-iphone"
            style="width: 100%; object-fit: cover"
          />
        </div>
        <div class="app-ft-grid-1">
          <div class="app-ft-icon">
            <div class="ft-bg-pg2">
              <img src="/media/icons/payments.svg" alt="Easy Payments" />
            </div>
          </div>
          <div class="ft-text">
            <h3>Easy Payments</h3>
            <p>
              Payments in our app make managing transactions effortless and
              efficient.
            </p>
          </div>
        </div>
        <div class="app-ft-grid-1">
          <div class="ft-bg-pg2">
            <img src="/media/icons/security.svg" alt="Data Security" />
          </div>
          <div class="ft-text">
            <h3>Data Security</h3>
            <p>
              Top priority for our app, ensuring that your personal and
              financial information is protected.
            </p>
          </div>
        </div>
        <div class="app-ft-grid-1">
          <div class="ft-bg-pg2">
            <img src="/media/icons/statistics.svg" alt="Cost Statistics" />
          </div>
          <div class="ft-text">
            <h3>Cost Statistics</h3>
            <p>
              in our app provide you with valuable insights into your spending
              patterns and financial habits.
            </p>
          </div>
        </div>
        <div class="app-ft-grid-1">
          <div class="ft-bg-pg2">
            <img
              src="/media//icons/support.svg"
              alt="Support 24/7"
              class="box"
            />
          </div>
          <div class="ft-text">
            <h3>Support 24/7</h3>
            <p>
              We ensure that you receive help and assistance whenever you need
              it, around the clock.
            </p>
          </div>
        </div>
        <div class="app-ft-grid-1">
          <div class="ft-bg-pg2">
            <img src="/media/icons/cashback.svg" alt="Regular Cashback" />
          </div>
          <div class="ft-text">
            <h3>Regular Cashback</h3>
            <p>
              This is a rewarding feature of our app designed to give you money
              back.
            </p>
          </div>
        </div>
        <div class="app-ft-grid-1">
          <div class="ft-bg-pg2">
            <img src="/media/icons/happy.svg" alt="Top Standards" />
          </div>
          <div class="ft-text">
            <h3>Top Standards</h3>
            <p>
              in our app ensure that you receive a high-quality, reliable, and
              secure experience.
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
<style scoped>
.page-2 {
  .app-ft-intro {
    margin-top: 1rem;
    margin-bottom: 1rem;
    padding-left: 1rem;
    padding-right: 1rem;
  }

  .ft-text {
    font-size: 1rem;
    font-style: normal;
    font-weight: 400;
    line-height: 25px;
  }

  .app-ft-grid-1 {
    padding-left: 1rem;
    padding-right: 1rem;
    display: flex;
    flex-direction: row;
  }
}

.ft-bg-pg2 {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;

  width: 60px;
  height: 60.08px;
  padding: 16px 16px 16px 16px;
  margin-top: 1.5rem;
  border-radius: 8px;
  background: var(--Gray-100);
}

.sponsors {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 5rem;

  .sp4 {
    display: none;
  }
  .desk {
    display: none;
  }
}

.app-ft {
  display: grid;
  grid-template-columns: repeat(1, minmax(0, 1fr));

  .app-ft-grid-2 {
    display: none;
  }

  .app-ft-iphone {
    display: none;
  }

  .ft-bg-pg2 {
    display: flex;
    margin-right: 30px;
    align-items: center;
  }
}

@media (min-width: 768px) {
  .page-2 {
    .app-ft {
      display: grid;
      grid-template-columns: repeat(2, minmax(0, 1fr));
    }

    .sponsors {
      display: flex;
      justify-content: center;
      align-items: center;
      gap: 24px;
      margin-top: 2rem;
      margin-bottom: 2rem;

      .sp4 {
        width: 159px;
        height: 99px;
        border-radius: 8px;
        padding: 32px 9px;
        border-radius: 8px;
        border: 1px solid #e2e5f1;
        display: block;

        img {
          width: 100%;
          height: 100%;
        }
      }

      .desk {
        display: none;
      }
    }
  }

  .app-ft-iphone {
    display: none;
  }
}

@media (min-width: 1400px) {
  .page-2 {
    .page-2-container {
      max-width: 1320px;
      margin: 0 auto;
    }

    .ft-grid {
      display: grid;
      grid-template-columns: repeat(12, minmax(0, 1fr));

      .ft-grid-obj-1 {
        grid-column: 6/9;
        grid-row: 1/2;
        margin: 0px 0px;
        padding: 0px 10px;
        text-align: left;
        margin-bottom: 1rem;
      }
      .ft-grid-obj-2 {
        grid-column: 6/13;
        grid-row: 2/3;
        margin: 0px 0px;
        padding: 0px 10px;
        text-align: left;
        margin-bottom: 3rem;
      }
    }
    .app-ft {
      display: grid;
      grid-template-columns: repeat(12, minmax(0, 1fr));
      gap: 1rem;
    }

    .app-ft-grid-1:nth-child(even) {
      grid-column: 6/9;
      margin: 0px 0px;
      padding: 0px 0px;
    }

    .app-ft-grid-1:nth-child(odd) {
      grid-column: 9/12;
      margin: 0px 0px;
      padding: 0px 0px;
    }

    .app-ft-grid-2 {
      grid-column: 3/5;
      grid-row: 1/4;
      display: block;
      width: 265px;
      height: 651px;
    }

    .app-ft-iphone {
      animation: fadescroll linear both;
      animation-timeline: view();
      animation-range: entry 50% cover 50%;
      width: 100%;
      object-fit: cover;
      display: block;
    }

    .sponsors {
      display: flex;
      height: 100px;
      justify-content: center;
      align-items: center;
      gap: 24px;

      .sp4 {
        display: flex;
        width: 196px;
        height: 100px;
        padding: 34px 36px;
        justify-content: center;
        align-items: center;
      }

      .desk {
        display: flex;
        width: 196px;
        height: 100px;
        padding: 34px 36px;
        border-radius: 8px;
        border: 1px solid #e2e5f1;
        justify-content: center;
        align-items: center;
      }
    }
  }
}

@keyframes fadescroll {
  from {
    opacity: 0;
    scale: 0.7;
  }
  to {
    opacity: 1;
    scale: 1;
  }
}
</style>
