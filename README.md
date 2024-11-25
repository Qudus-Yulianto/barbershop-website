HTML
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Barbershop Anda</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header class="header">
        <div class="container">
            <h1>Barbershop Anda</h1>
            <p>Gaya rambut terbaik untuk Anda</p>
        </div>
    </header>
    
    <nav class="navbar">
        <ul>
            <li><a href="#services">Layanan</a></li>
            <li><a href="#gallery">Galeri</a></li>
            <li><a href="#contact">Kontak</a></li>
        </ul>
    </nav>
    
    <section id="services" class="section">
        <h2>Layanan Kami</h2>
        <div class="services">
            <div class="service">
                <h3>Potong Rambut</h3>
                <p>Layanan potong rambut profesional untuk segala gaya.</p>
            </div>
            <div class="service">
                <h3>Cukur Jenggot</h3>
                <p>Perawatan jenggot yang rapi dan bersih.</p>
            </div>
            <div class="service">
                <h3>Hair Styling</h3>
                <p>Gaya rambut sesuai tren terbaru.</p>
            </div>
        </div>
    </section>
    
    <section id="gallery" class="section">
        <h2>Galeri</h2>
        <div class="gallery">
            <img src="gallery1.jpg" alt="Gaya Rambut 1">
            <img src="gallery2.jpg" alt="Gaya Rambut 2">
            <img src="gallery3.jpg" alt="Gaya Rambut 3">
        </div>
    </section>
    
    <section id="contact" class="section">
        <h2>Hubungi Kami</h2>
        <p>Alamat: Jalan Contoh No. 123, Kota Anda</p>
        <p>Telepon: 0812-3456-7890</p>
        <p>Email: info@barbershopanda.com</p>
    </section>
    
    <footer class="footer">
        <p>&copy; 2024 Barbershop Anda. Semua hak dilindungi.</p>
    </footer>
</body>
</html>

 
CSS
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    color: #333;
}

.header {
    background-color: #2c3e50;
    color: #fff;
    padding: 20px;
    text-align: center;
}

.navbar {
    background-color: #34495e;
    overflow: hidden;
}

.navbar ul {
    list-style-type: none;
    margin: 0;
    padding: 0;
}

.navbar li {
    float: left;
}

.navbar a {
    display: block;
    color: white;
    text-align: center;
    padding: 14px 20px;
    text-decoration: none;
}

.navbar a:hover {
    background-color: #1abc9c;
}

.section {
    padding: 20px;
    text-align: center;
}

.services, .gallery {
    display: flex;
    justify-content: center;
    gap: 20px;
    flex-wrap: wrap;
}

.service, .gallery img {
    flex: 1 1 calc(30% - 20px);
    box-sizing: border-box;
    padding: 10px;
    background: #f4f4f4;
    border: 1px solid #ddd;
    border-radius: 5px;
}

.gallery img {
    max-width: 100%;
    height: auto;
    border-radius: 5px;
}

.footer {
    background-color: #2c3e50;
    color: #fff;
    text-align: center;
    padding: 10px;
}
JAVA SCRIPT
document.querySelectorAll('.navbar a').forEach(link => {
    link.addEventListener('click', event => {
        event.preventDefault();
        document.querySelector(event.target.getAttribute('href')).scrollIntoView({ behavior: 'smooth' });
    });
});
