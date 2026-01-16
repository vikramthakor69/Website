 Mobile menu
const menuBtn = document.getElementById(menuBtn);
const navLinks = document.getElementById(navLinks);

menuBtn.addEventListener(click, () = {
  const isOpen = navLinks.classList.toggle(open);
  menuBtn.setAttribute(aria-expanded, String(isOpen));
});

 Close menu after clicking a link (mobile)
navLinks.querySelectorAll(a).forEach(a = {
  a.addEventListener(click, () = navLinks.classList.remove(open));
});

 Footer year
document.getElementById(year).textContent = new Date().getFullYear();

 Download Resume button
document.getElementById(downloadBtn).addEventListener(click, () = {
   Replace resume.pdf with your actual file name if you add it to the same folder
  const fileName = resume.pdf;
  window.open(fileName, _blank);
});

 Contact form → opens email client (no backend)
document.getElementById(contactForm).addEventListener(submit, (e) = {
  e.preventDefault();
  const data = new FormData(e.target);
  const name = encodeURIComponent(data.get(name));
  const email = encodeURIComponent(data.get(email));
  const message = encodeURIComponent(data.get(message));

  const subject = encodeURIComponent(`Website Contact - ${decodeURIComponent(name)}`);
  const body =
    `Name ${decodeURIComponent(name)}n` +
    `Email ${decodeURIComponent(email)}nn` +
    `Messagen${decodeURIComponent(message)}`;

  window.location.href = `mailtoVikramthakor760065@gmail.comsubject=${subject}&body=${encodeURIComponent(body)}`;
});
