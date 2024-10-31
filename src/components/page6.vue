<script setup>
import accordion from '../components/accordion.vue'
</script>
<template>
  <section class="page-4">
    <div class="page-4-container">
      <div class="page-4-grid">
        <h2>Any questions? Check out the FAQs</h2>
        <p class="pg-4-p">
          Still have unanswered questions and need to get in touch?
        </p>
        <div class="faq-ctn">
          <div class="faq">
            <img src="/media/faq-1.svg" alt="FAQ" />
            <p>Still have questions?</p>
            <div class="btn-faq-wrapper">
              <button class="btn-faq-1">Contact us</button>
              <img src="/media/faq-1-arrow.svg" alt="FAQ Arrow" />
            </div>
          </div>
          <div class="faq">
            <img src="/media/faq-2.svg" alt="FAQ" />
            <p>Don't like phone calls?</p>
            <div class="btn-faq-wrapper">
              <button class="btn-faq-2">Contact us</button>
              <img src="/media/faq-2-arrow.svg" alt="FAQ Arrow" />
            </div>
          </div>
        </div>
        <div class="accordion-style">
          <accordion />
        </div>
        <div class="btn-con">
          <button>Contact us now</button>
        </div>
      </div>
      <div class="newsletter-cnt">
        <div class="newsletter-header">
          <div class="newsletter-wrapper">
            <img
              src="/media/icons/notification-icon.svg"
              alt="Newsletter Icon"
              class="newsletter-icon"
            />
            <h2 class="newsletter">Subscribe to our newsletter</h2>
            <h2 class="newsletter-d">
              Subscribe to our newsletter to stay informed about the latest
              updates
            </h2>
          </div>
          <form>
            <div class="subscribe">
              <label for="email" class="form-label"></label>
              <input
                type="email"
                placeholder="Enter your email"
                name="email"
                id="email"
                autocomplete="on"
              />
              <button class="btn-subscribe" type="submit" id="button-addon2">
                Subscribe
              </button>
            </div>
          </form>
        </div>
      </div>
    </div>
  </section>
</template>
<style scoped>
.page-4 {
  padding-left: 1rem;
  padding-right: 1rem;

  .newsletter-cnt {
    background: #f3f6ff;
    border-radius: 8px;
    gap: 1rem;

    .newsletter-header {
      display: flex;
      flex-direction: column;
      text-align: left;
      padding: 32px 16px;

      .newsletter-wrapper {
        display: flex;
        flex-direction: row;
        padding: 20px 0px;
      }

      .newsletter {
        display: block;
      }
      .newsletter-d {
        display: none;
      }

      img {
        width: 20%;
        height: auto;
      }

      .subscribe {
        display: flex;
      }
    }
  }

  .btn-con {
    display: flex;
    justify-content: center;
    margin-top: 3rem;
    margin-bottom: 3rem;
    border-radius: 6px;

    button {
      border-radius: 6px;
      border: 1px solid var(--Brand-Primary);
      background: var(--Brand-Primary);
      padding: 10px 28px 16px 28px;
      color: var(--white-color);
      text-align: center;
      font-style: normal;
      font-weight: 600;
    }
  }

  form {
    padding-left: 1rem;
    padding-right: 1rem;
    display: flex;
    justify-content: center;
    align-items: center;
    margin-bottom: 1rem;

    input {
      display: inline-flex;
      height: 50.7px;
      padding: 14.15px 18px 14.95px 48px;
      justify-content: flex-end;
      align-items: center;
      border-radius: 8px 0px 0px 8px;
      border: 1px solid #d4d7e5;
      background: var(--white-color);
    }

    button {
      color: var(--white-color);
      border-radius: 0px 8px 8px 0px;
      border: 1px solid var(--Brand-Primary);
      background: var(--Brand-Primary);
    }
  }

  .faq-ctn {
    display: none;
  }
}

@media (min-width: 768px) {
  .page-4 {
    margin-top: 2rem;

    .page-4-container {
      max-width: 730px;
      margin: 0 auto;
    }
    h2 {
      color: #0b0f19;
      text-align: center;
      font-family: 'manrope';
      font-size: 32px;
      font-style: normal;
      font-weight: 800;
      line-height: 130%;
      /* margin-top: 2rem; */
    }
    .pg-4-p {
      color: #565973;
      text-align: center;
      font-family: 'Manrope';
      font-size: 18px;
      font-style: normal;
      font-weight: 400;
      line-height: 160%;
      margin-bottom: 4rem;
    }

    .faq-ctn {
      display: flex;
      gap: 1rem;
      margin-bottom: 2rem;

      .faq {
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        font-family: 'manrope';
        width: 100%;
        padding: 24px 10px;
        gap: 8px;
        border-radius: 8px;
        border: 1px solid #e2e5f1;
      }

      .btn-faq-wrapper {
        display: flex;

        .btn-faq-1 {
          background-color: var(--white-color);
          text-decoration: none;

          color: var(--Brand-Primary);
          border: 0px;
        }

        .btn-faq-2 {
          background-color: var(--white-color);
          text-decoration: none;
          color: #22c55e;
          border: 0px;
        }
      }
    }

    .newsletter-cnt {
      display: flex;
      justify-content: center;
      align-items: center;
      .newsletter-header {
        flex-direction: row;
        .newsletter-wrapper {
          padding: 0px 0px;
        }
        display: flex;
        justify-content: center;
        align-items: center;
        .newsletter {
          display: block;
        }
      }
    }
  }

  .btn-con {
    display: none;
    button {
      display: none;
    }
  }
}

@media (min-width: 1400px) {
  .page-4 {
    .page-4-container {
      max-width: 1320px;
      margin: 0 auto;
    }
    .page-4-grid {
      display: grid;
      grid-template-columns: repeat(12, minmax(0, 1fr));

      h2 {
        grid-column: 1/4;
        grid-row: 1/2;
        text-align: left;
        margin-top: 0rem;
      }

      p {
        grid-column: 1/6;
        grid-row: 2/3;
        text-align: left;
      }
      .accordion-style {
        grid-column: 6/13;
        grid-row: 1/13;
        margin-bottom: 2rem;
      }

      .faq-ctn {
        grid-column: 1/5;
        grid-row: 3/4;
        margin: 0px 0px;
        padding: 0px 0px;
      }
    }

    .newsletter-cnt {
      padding: 72px 110px;

      .newsletter-header {
        flex-direction: row;

        img {
          width: 78px;
          height: 78px;
        }

        .newsletter {
          display: none;
        }

        .newsletter-d {
          display: block;
        }

        .newsletter-wrapper {
          padding: 0px 0px;
        }
      }
    }
  }
}
</style>
