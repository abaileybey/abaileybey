
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
        anchor.addEventListener('click', function (e) {
            e.preventDefault();
            document.querySelector(this.getAttribute('href')).scrollIntoView({
                behavior: 'smooth'
            });
        });
    });

    // Typewriter effect for "Welcome to My Portfolio"
    let i = 0;
    const text = "Welcome to My Portfolio";
    const speed = 100;

    function typeWriter() {
        if (i < text.length) {
            document.getElementById("headline").innerHTML += text.charAt(i);
            i++;
            setTimeout(typeWriter, speed);
        }
    }
    typeWriter();
});
