# Margarita Kachalko - CV

## Contacts

**Location:** Belarus, Grodno.

**Email:** margarita.kachalko@gmail.com

**GitHub:** [https://github.com/mkachalko](https://github.com/mkachalko)

**Telegram:** [https://t.me/mkachalko](https://t.me/mkachalko)

## About me

I decided to change my profession at the age of 29. I consider myself a responsible and efficient person. I like to study and to gain new knowledge. The world of web development is very interesting to me. I want to improve my hard and soft skills to work as a junior front-end developer in a successful company.

## Skills

- HTML;
- CSS;
- препроцессор SASS;
- JS;
- Webpack
- Git & GitHub
- Методология БЭМ

## Code example

1. *Написать скрипт модального окна*

2. *Написать анимацию появления модального окна*

   - *Использовать JS анимацию. Использовать нативный JavaScript. Использование сторонних библиотек запрещено!*

3. *Если пользователь заходит на сайт с устройства, у которого ширина экрана меньше 768px (мобильного устройства) - анимация отключается.*
``` 
const modal = () => {
  const popupBtn = document.querySelectorAll(".popup-btn");
  const modal = document.querySelector(".popup");

  let count = 0;
  let idAnimationOpen;
  let idAnimationClose;

  const animationOpen = () => {
    count += 0.04;

    idAnimationOpen = requestAnimationFrame(animationOpen);
    if (count < 1) {
      modal.style.opacity = count;
    } else {
      modal.style.opacity = 1;
      cancelAnimationFrame(idAnimationOpen);
    }
  };

  const animationClose = () => {
    count -= 0.04;

    idAnimationClose = requestAnimationFrame(animationClose);
    if (count > 0) {
      modal.style.opacity = count;
    } else {
      modal.style.opacity = "";
      modal.style.display = "none";
      cancelAnimationFrame(idAnimationClose);
    }
  };

  popupBtn.forEach((button) => {
    button.addEventListener("click", () => {
      modal.style.display = "block";
      if (screen.width > 768) {
        animationOpen();
      }
    });
  });

  modal.addEventListener("click", (e) => {
    if (e.target.classList.contains("popup-close") || !e.target.closest(".popup-content")) {
      if (screen.width > 768) {
        animationClose();
      } else {
        modal.style.display = "none";
      }
    }
  });
};
```
## Experience

I have only study projects as an experience yet.

- [Universal](https://mkachalko.github.io/Universal)
- [Tour-Plan](https://mkachalko.github.io/tour-plan/)

## Education

- **The Academy of Public Administration under the President of the Republic of Belarus**  
  Qualification: Economist-Manager / 2010-2015;

## Courses

- **Glo Academy**:
  - *Web-start* / 2021;
  - *JS (in progress)*;
- **RS-School**
  - *JS/Front-end. Stage 0 (in progress)*;

## Languages
- Belorussian - native;
- Russian - native;
- Deutsch - B1;
- English - A2;
