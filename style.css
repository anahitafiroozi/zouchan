// Mobile menu
const menuToggle = document.querySelector('.menu-toggle');
const nav = document.querySelector('.main-nav');

if (menuToggle && nav) {
  menuToggle.addEventListener('click', () => {
    nav.classList.toggle('open');
  });

  nav.querySelectorAll('a').forEach(link => {
    link.addEventListener('click', () => {
      nav.classList.remove('open');
    });
  });
}


// Language button
const langButton = document.querySelector('[data-language]');

if (langButton) {
  langButton.addEventListener('click', () => {
    alert('نسخه انگلیسی سایت در حال آماده‌سازی است.');
  });
}


// Smooth scrolling
document.querySelectorAll('a[href^="#"]').forEach(anchor => {
  anchor.addEventListener('click', function (event) {

    const target = document.querySelector(this.getAttribute('href'));

    if (!target) return;

    event.preventDefault();

    target.scrollIntoView({
      behavior: 'smooth',
      block: 'start'
    });

  });
});


// 3D tilt effect for product cards
document.querySelectorAll('.product-card').forEach(card => {

  card.addEventListener('pointermove', (event) => {

    const rect = card.getBoundingClientRect();

    const x = event.clientX - rect.left;
    const y = event.clientY - rect.top;

    const rotateY = ((x / rect.width) - 0.5) * 12;
    const rotateX = ((y / rect.height) - 0.5) * -12;

    card.style.transform =
      `perspective(900px) rotateX(${rotateX}deg) rotateY(${rotateY}deg) translateY(-6px)`;

  });


  card.addEventListener('pointerleave', () => {

    card.style.transform =
      'perspective(900px) rotateX(0deg) rotateY(0deg) translateY(0)';

  });

});


// Reveal animation when sections enter the viewport
const revealItems = document.querySelectorAll(
  '.section, .product-card, .news-card, .certificate-card'
);


const observer = new IntersectionObserver(
  (entries) => {

    entries.forEach(entry => {

      if (entry.isIntersecting) {

        entry.target.classList.add('visible');

        observer.unobserve(entry.target);

      }

    });

  },
  {
    threshold: 0.12
  }
);


revealItems.forEach(item => {

  item.classList.add('reveal');

  observer.observe(item);

});


// Demo contact form
const contactForm = document.querySelector('#contact-form');


if (contactForm) {

  contactForm.addEventListener('submit', (event) => {

    event.preventDefault();

    alert(
      'پیام شما با موفقیت ثبت شد. این فرم در نسخه نهایی به سیستم ارسال پیام متصل می‌شود.'
    );

    contactForm.reset();

  });

}