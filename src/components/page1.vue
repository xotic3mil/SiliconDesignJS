<script setup></script>
<template>
  <section class="page-1 background-gradient">
    <div class="page-1-container">
      <div class="pg1-grid">
        <h1>Manage All Your Money in One App</h1>
        <p class="pg-1-p">
          We offer you a new generation of mobile banking. Save, spend & manage
          money in your pocket.
        </p>
        <div class="btn-stores">
          <div class="btn-store-wrapper">
            <button class="btn-store">
              <img
                src="/media/appstore-light.svg"
                alt="Google Logo"
                class="store-light"
              />
              <img
                src="/media/appstore-dark.svg"
                alt="Google Logo"
                class="store-dark"
              />
            </button>
            <button class="btn-store">
              <img
                src="/media/googleplay-light.svg"
                alt="Google Logo"
                class="store-light"
              />
              <img
                src="/media/googleplay-dark.svg"
                alt="Google Logo"
                class="store-dark"
              />
            </button>
          </div>
        </div>
        <div class="discover-grid">
          <div class="discover-wrapper">
            <div class="btn-discover">
              <img src="/media/button_Icon.svg" alt="Discover Arrow" />
            </div>
            <span class="space">Discover more</span>
          </div>
        </div>
        <div class="iphone">
          <img src="/media/Iphone/hero-iphone.png" alt="Iphone" />
        </div>
      </div>
    </div>
  </section>
</template>
<script></script>

<style scoped>
.background-gradient {
  background: radial-gradient(
    circle at center bottom,
    rgba(99, 102, 241, 0.1) 0%,
    rgba(218, 70, 239, 0.05) 41%,
    rgba(241, 244, 253, 0.07) 65%
  );
}

h1 {
  animation: fade 2s;
  color: #131022;
  font-family: 'manrope';
  font-style: normal;
  text-align: center;
  font-weight: 800;
  padding: 26px 100px 56px 100px;
}

.page-1 {
  .iphone {
    display: none;
  }

  .pg-1-p {
    text-align: center;
  }

  .btn-store-wrapper {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    margin-top: 5rem;
    margin-bottom: 5rem;
    gap: 1rem;

    .btn-store {
      height: 3.25rem;
      width: 90%;
      border-radius: 8px;
      background-color: #131022;
      display: flex;
      justify-content: center;
      align-items: center;

      img {
        padding: 10px 10px;
        object-fit: contain;
        height: auto;

        &:hover {
          animation: shake 0.5s;
          animation-iteration-count: infinite;
        }
      }
    }
  }

  .discover-wrapper {
    display: flex;
    justify-content: center;
    align-items: center;
    color: var(--secondary-color);
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 14px;
    font-style: normal;
    font-weight: 400;
    line-height: 22px;
    gap: 1rem;
  }

  .btn-discover {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 44px;
    height: 44px;
    padding: 12px 0px;
    border-radius: 22px;
    border: 1px solid var(--white-color);
    background: var(--white-color);
    margin-bottom: 2rem;
  }
  .space {
    margin-bottom: 2rem;
  }
}

@media (min-width: 768px) {
  .page-1-container {
    max-width: 768px;
    margin: 0 auto;
  }

  .pg1-grid {
    display: grid;
    grid-template-columns: repeat(12, minmax(0, 1fr));
    padding-left: 1rem;
    padding-right: 1rem;

    h1 {
      padding: 0px 0px 0px 0px;
      margin: 0px 140px;
      grid-column: 1 / 13;
      margin-bottom: 1rem;
      color: #131022;
      text-align: center;
      font-size: 44px;
      font-weight: 800;
      font-style: normal;
      line-height: 57px;
    }

    .pg-1-p {
      padding-left: 1rem;
      padding-right: 1rem;
      grid-column: 1 / 7;
      grid-row: 4 / 10;
      text-align: left;
      color: var(--secondary-color);
      font-size: 18px;
      font-style: normal;
      font-weight: 400;
      line-height: 28px;
    }

    .btn-store-wrapper {
      display: flex;
      flex-direction: row;
    }

    .btn-stores {
      grid-column: 1 / 6;
      grid-row: 5 / 11;

      .btn-store {
        img {
          padding: 10px 10px;
          width: 100%;
          height: auto;
        }
      }
    }

    .discover-grid {
      grid-column: 1 / 6;
      grid-row: 6 / 11;

      .discover-wrapper {
        padding-left: 1rem;
        padding-right: 1rem;
        display: flex;
        flex-direction: row;
        justify-content: flex-start;

        .btn-discover {
          margin-bottom: 0rem;
        }

        .space {
          margin-bottom: 0rem;
        }
      }
    }

    .iphone {
      display: grid;
      grid-column: 6 / 8;
      grid-row: 2 / 12;

      img {
        display: flex;
        justify-content: flex-end;
        align-self: flex-end;
        object-fit: contain;
        width: 440px;
      }
    }
  }
}

@media (min-width: 1400px) {
  .page-1-container {
    max-width: 1320px;
    margin: 0 auto;
  }

  .pg1-grid {
    h1 {
      margin: 10px 0px;
      width: 450px;
      text-align: left;
      grid-column: 1 / 7;
      grid-row: 5 / 7;
    }

    .pg-1-p {
      padding-left: 0px;
      grid-column: 1 / 5;
      grid-row: 7 / 8;
    }

    .btn-stores {
      grid-column: 1 / 5;
      grid-row: 7 / 8;

      .btn-store {
        display: flex;
        color: white;

        img {
          padding: 10px 10px;
          width: 85%;
          height: auto;
        }
      }
    }

    .discover-grid {
      grid-column: 1 / 4;
      grid-row: 9 / 10;
    }

    .iphone {
      display: grid;
      grid-column: 5 / 13;
      grid-row: 2 / 12;

      img {
        object-fit: cover;
        width: 100%;
        height: auto;
      }
    }
  }
}

@keyframes fade {
  from {
    transform: translateX(-900px);
  }
  to {
    transform: translateX(0px);
  }
}

@keyframes shake {
  0% {
    transform: translate(1px, 1px) rotate(0deg);
  }
  10% {
    transform: translate(-1px, -2px) rotate(-1deg);
  }
  20% {
    transform: translate(-3px, 0px) rotate(1deg);
  }
  30% {
    transform: translate(3px, 2px) rotate(0deg);
  }
  40% {
    transform: translate(1px, -1px) rotate(1deg);
  }
  50% {
    transform: translate(-1px, 2px) rotate(-1deg);
  }
  60% {
    transform: translate(-3px, 1px) rotate(0deg);
  }
  70% {
    transform: translate(3px, 1px) rotate(-1deg);
  }
  80% {
    transform: translate(-1px, -1px) rotate(1deg);
  }
  90% {
    transform: translate(1px, 2px) rotate(0deg);
  }
  100% {
    transform: translate(1px, -2px) rotate(-1deg);
  }
}
</style>
