<script setup>
import navmenu from '../components/navmenu.vue'
import contactForm from './contactForm.vue'
</script>
<template>
  <div class="bg">
    <navmenu />
    <div class="contact-grid">
      <h2 class="contact-title">Contact Us</h2>
      <div class="box-grid-1 contact-box-md">
        <div class="box-container-1 box-container-sm">
          <div class="icon-bg">
            <img src="\src\images/icons-bx-envelope.svg" />
          </div>
          <div class="box-text">
            <h4>Email us</h4>
            <p>
              Please feel free to drop us a line. We will respond as soon as
              possible.
            </p>
            <button class="btn-text">Leave a message -></button>
          </div>
        </div>

        <div class="box-grid-2">
          <div class="box-container-2 box-container-sm">
            <div class="icon-bg">
              <img src="\src\images/add-group.svg" />
            </div>
            <div class="box-text box-sm">
              <h4>Careers</h4>
              <p>
                We are looking for talented to join our team. Please check our
                current job openings and apply.
              </p>
              <button class="btn-text">Send an application -></button>
            </div>
          </div>
        </div>
      </div>
      <div class="contactForm">
        <contactForm class="contactStyle" />
      </div>
    </div>
  </div>
  <h2 class="contact-title-btm">Locations</h2>

  <div class="bottom-container">
    <div class="map">
      <img src="\src\images/image.svg" />
    </div>
    <div class="center-container">
      <div class="center-1 center-sm">
        <h4>Medical Center 1</h4>
        <div class="center-style center-style-sm">
          <img src="\src\images/icons-bx-map.svg" />
          <p>4517 Washington Ave. Manchester, Kentucky 39495</p>
        </div>
        <div class="center-style center-style-sm">
          <img src="\src\images/icons-bx-phone-call.svg" />
          <p>(406) 555-0120</p>
        </div>
        <div class="center-style center-style-sm">
          <img src="\src\images/icons-bx-time-five.svg" alt="time" />
          <p><strong>Mon – Fri:</strong> 9:00 am – 22:00 am</p>
          <p><strong>Sat – Sun:</strong> 9:00 am – 20:00 am</p>
        </div>
      </div>

      <div class="center-2 center-sm">
        <h4>Medical Center 2</h4>
        <div class="center-style center-style-sm center-style-md">
          <img src="\src\images/icons-bx-map.svg" />
          <p>2464 Royal Ln. Mesa,New Jersey 45463</p>
        </div>
        <div class="center-style center-style-sm center-style-md">
          <img src="\src\images/icons-bx-phone-call.svg" />
          <p>(406) 544-0123</p>
        </div>
        <div class="center-style center-style-sm center-style-md">
          <img src="\src\images/icons-bx-time-five.svg" />
          <p><strong>Mon – Fri:</strong> 9:00 am – 22:00 am</p>
          <p><strong>Sat – Sun:</strong> 9:00 am – 20:00 am</p>
        </div>
      </div>
    </div>

    <div class="social-grid">
      <div class="social-container">
        <div class="social-bg">
          <img src="\src\images\social-btn-icons-bxl-facebook-square.svg " />
        </div>
        <div class="social-bg">
          <img src="\src\images\social-btn-icons-bxl-twitter.svg" />
        </div>
        <div class="social-bg">
          <img src="\src\images\social-btn-icons-bxl-instagram-alt.svg" />
        </div>
        <div class="social-bg">
          <img src="\src\images\social-btn-icons-bxl-youtube.svg" />
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.bg {
  width: 100%;
  height: 1000px;
  position: relative;
  background-color: var(--Gray-200);
}

.contact-title {
  text-align: center;
}

.map {
  display: none;
}

.contact-title {
  margin-bottom: 2rem;
}

.contact-title-btm {
  text-align: center;
  margin-top: 200px;
  margin-bottom: 2rem;
}

.box-container-1,
.box-container-2 {
  background-color: var(--white-color);
}

.btn-text {
  all: unset;
  color: var(--Brand-Primary);
  text-align: center;
  font-weight: 600;
  line-height: 160%;
}

.btn:hover {
  background: var(--Brand-Secondary);
}

.box-container-sm {
  box-shadow:
    0px 4.8px 24.4px -6px rgba(19, 16, 34, 0.1),
    0px 4px 13px -2px rgba(19, 16, 34, 0.06);
  border-radius: 8px;
  padding: 20px 25px;
  margin: 0px 15px;
  display: flex;
  gap: 10px;
  margin-bottom: 2rem;
}

.center-sm {
  box-shadow:
    0px 4.8px 24.4px -6px rgba(19, 16, 34, 0.1),
    0px 4px 13px -2px rgba(19, 16, 34, 0.06);
  border-radius: 8px;
  padding: 20px 25px;
  margin: 0px 15px;
  gap: 10px;
  margin-bottom: 2rem;
}

.center-1 {
  margin-top: 40px;
}

.center-style-sm {
  display: flex;
  align-items: start;
  margin: 10px 15px;
}

.icon-bg {
  display: flex;
  width: 60px;
  height: 60px;
  padding: 16px;
  justify-content: center;
  align-items: center;
  flex-shrink: 0;
  border-radius: 100px;
  background: var(--Gray-200);
  margin-right: 10px;
}

.social-container {
  display: flex;
  justify-content: center;
  gap: 16px;
  margin: 10px 0px;
  padding: 10px 10px;
}

.social-bg {
  border-radius: 6px;
  background: var(--Gray-200);
  padding: 12px;
}

@media (min-width: 768px) {
  .contact-title-btm {
    text-align: center;
    margin-top: 25px;
    margin-bottom: 2rem;
  }

  .contact-box-md {
    display: flex;
    flex-direction: row;
    width: 100%;
  }

  .box-grid-1 {
    max-width: 768px;
    margin: 0 auto;
  }

  .box-grid-2 {
    max-width: 768px;
    margin: 0 auto;
  }

  .bottom-container {
    display: flex;
    margin-top: 2rem;
  }

  .center-container {
    display: flex;
    flex-direction: row;
    justify-content: center;
    margin: 0 auto;
  }

  .center-1 {
    margin-top: 0px;
  }

  .center-sm {
    max-width: 350px;
    border-radius: 8px;
    padding: 20px 15px;
    margin: 0px 15px;
    margin-bottom: 2rem;
  }

  .social-grid {
    display: none;
  }
}

@media (min-width: 1400px) {
  .center-sm {
    box-shadow: none;
    border-radius: 0px;
    padding: 0px 0px;
    margin: 0px 0px;
    gap: 0px;
    margin-bottom: 0rem;
  }

  h1 {
    color: var(--Gray-900);
    font-feature-settings:
      'liga' off,
      'clig' off;
    font-family: Manrope;
    font-size: 40px;
    font-style: normal;
    font-weight: 800;
    line-height: 130%;
  }

  h4 {
    color: var(--Gray-900);
    font-feature-settings:
      'liga' off,
      'clig' off;
    font-size: 24px;
    font-style: normal;
    font-weight: 800;
    line-height: 130%;
  }

  .bg {
    width: 100%;
    height: 777px;
    background-color: var(--Gray-200);
  }

  .paper-1 {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 32px;
    padding: 32px;
    background: var(--Brand-Primary);
    border-radius: 8px;
    box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.1);
  }

  .bottom-container {
    max-width: 1920px;
    display: grid;
    grid-template-columns: repeat(12, minmax(0, 1fr));
    background: var(--white-color);
    margin-top: 200px;
    margin-bottom: 50px;
  }

  .map {
    display: grid;
    grid-column: 5/9;
    grid-row: 1/12;

    img {
      border-radius: 8px;
    }
  }

  .center-container {
    display: grid;
    grid-column: 9/13;
    grid-row: 2/4;
  }

  .social-container {
    display: flex;
    justify-content: none;
    gap: none;
    margin: none;
    padding: none;
    margin-left: 40px;
  }

  .social-grid {
    display: block;
    grid-column: 9/12;
    grid-row: 11/12;
  }

  .center-style {
    gap: 5px;

    img {
      width: 20px;
      height: 20px;
    }
  }

  .box-container-1,
  .box-container-2 {
    display: flex;
    width: 400px;
    flex-direction: row;
    align-items: flex-start;
    gap: 12px;
    background: none;
    box-shadow: none;
  }

  .contact-box-md {
    display: block;
    width: none;
  }

  .icon-bg {
    background: var(--Gray-100);
  }

  .contact-grid {
    display: grid;
    grid-template-columns: repeat(12, minmax(0, 1fr));
  }

  .contact-title {
    grid-column: 4/5;
    grid-row: 1/12;
  }

  .contact-title-btm {
    display: none;
  }

  .box-grid-1 {
    grid-column: 4/6;
    grid-row: 4;
  }
  .box-grid-2 {
    grid-column: 4/6;
    grid-row: 7;
  }

  .contactForm {
    display: block;
    max-width: 1920px;

    grid-column: 5/13;
    grid-row: 1/12;
  }
}
</style>
