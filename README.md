<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Corsa Nocturne - Las Vegas Car Meets</title>
    <style>
        body {
            margin: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #000;
            color: #fff;
        }
        header {
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 20px;
            background-color: #111;
        }
        header .logo {
            height: 80px;
        }
        nav ul {
            list-style: none;
            display: flex;
            gap: 20px;
            margin: 0;
            padding: 0;
        }
        nav a {
            color: gold;
            text-decoration: none;
            font-weight: bold;
        }
        .hero {
            text-align: center;
            padding: 100px 20px;
            background: url('images/logo.png') center/contain no-repeat;
            background-color: #111;
        }
        .hero h1 {
            font-size: 48px;
            margin-bottom: 10px;
        }
        .hero p {
            font-size: 20px;
            margin-bottom: 20px;
        }
        .cta-button {
            background-color: gold;
            color: #000;
            padding: 12px 24px;
            text-decoration: none;
            border-radius: 5px;
            font-weight: bold;
        }
        section {
            padding: 60px 20px;
            max-width: 800px;
            margin: auto;
        }
        .events-list {
            list-style: none;
            padding: 0;
        }
        .events-list li {
            margin-bottom: 15px;
            font-size: 18px;
        }
        form {
            display: flex;
            flex-direction: column;
        }
        form input, form textarea, form select {
            margin-bottom: 15px;
            padding: 10px;
            border: none;
            border-radius: 4px;
        }
        form button {
            background-color: gold;
            color: #000;
            border: none;
            padding: 12px;
            font-size: 16px;
            cursor: pointer;
        }
        .gallery {
            display: flex;
            gap: 10px;
            justify-content: center;
            flex-wrap: wrap;
        }
        .gallery img {
            width: 30%;
            border-radius: 10px;
        }
        footer {
            text-align: center;
            padding: 20px;
            background-color: #111;
            font-size: 14px;
        }
        .modal {
            display: none;
            position: fixed;
            z-index: 999;
            left: 0; top: 0;
            width: 100%; height: 100%;
            background: rgba(0,0,0,0.8);
            justify-content: center;
            align-items: center;
        }
        .modal-content {
            background: #111;
            padding: 20px;
            border-radius: 10px;
            width: 300px;
            color: #fff;
            position: relative;
        }
        .close {
            position: absolute;
            right: 10px; top: 10px;
            cursor: pointer;
            font-size: 24px;
            color: gold;
        }
        .modal-content form input, .modal-content form button {
            width: 100%;
            margin: 8px 0;
            padding: 10px;
        }
    </style>
</head>
<body>
    <header>
        <img src="images/logo.png" alt="Corsa Nocturne Logo" class="logo">
        <nav>
            <ul>
                <li><a href="#about">About</a></li>
                <li><a href="#events">Events</a></li>
                <li><a href="#gallery">Gallery</a></li>
                <li><a href="#tickets">Tickets</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <section class="hero">
        <h1>Corsa Nocturne - Las Vegas</h1>
        <p>The ultimate night car meets experience in Las Vegas</p>
        <a href="#events" class="cta-button">View Upcoming Vegas Events</a>
    </section>

    <section id="about">
        <h2>About Us</h2>
        <p>Corsa Nocturne brings together car enthusiasts under the neon lights of Las Vegas. Our meets feature exotic cars, classic rides, and high-performance machines in exclusive Sin City locations.</p>
    </section>

    <section id="events">
        <h2>Upcoming Events - Las Vegas, NV</h2>
        <ul class="events-list">
            <li>
                <strong>May 15, 2025:</strong> Rooftop Meet - Downtown Garage (Las Vegas, NV)
                <button onclick="openRSVP('May 15, 2025 - Rooftop Meet, Las Vegas')">RSVP</button>
            </li>
            <li>
                <strong>June 20, 2025:</strong> Highway Midnight Cruise (Las Vegas Strip)
                <button onclick="openRSVP('June 20, 2025 - Highway Cruise, Las Vegas')">RSVP</button>
            </li>
            <li>
                <strong>July 12, 2025:</strong> Beachfront Night Rally (Lake Las Vegas)
                <button onclick="openRSVP('July 12, 2025 - Beachfront Rally, Las Vegas')">RSVP</button>
            </li>
        </ul>
    </section>

    <section id="gallery">
        <h2>Gallery</h2>
        <div class="gallery">
            <img src="images/gallery1.jpg" alt="Car Meet Photo 1">
            <img src="images/gallery2.jpg" alt="Car Meet Photo 2">
            <img src="images/gallery3.jpg" alt="Car Meet Photo 3">
        </div>
    </section>

    <section id="tickets">
        <h2>Book Tickets</h2>
        <form id="ticketForm">
            <label for="ticketName">Name:</label><input type="text" id="ticketName" name="ticketName" required>
            <label for="ticketEmail">Email:</label><input type="email" id="ticketEmail" name="ticketEmail" required>
            <label for="ticketEvent">Select Event:</label>
            <select id="ticketEvent" name="ticketEvent" required>
                <option value="">--Choose a Las Vegas Event--</option>
                <option>May 15, 2025 - Rooftop Meet (Las Vegas, NV)</option>
                <option>June 20, 2025 - Highway Midnight Cruise (Las Vegas Strip)</option>
                <option>July 12, 2025 - Beachfront Night Rally (Lake Las Vegas)</option>
            </select>
            <label for="ticketQty">Tickets:</label><input type="number" id="ticketQty" name="ticketQty" min="1" max="10" value="1" required>
            <button type="submit">Book Now</button>
        </form>
    </section>

    <section id="contact">
        <h2>Contact Us</h2>
        <form id="contactForm">
            <label for="name">Name:</label><input type="text" id="name" name="name" required>
            <label for="email">Email:</label><input type="email" id="email" name="email" required>
            <label for="message">Message:</label><textarea id="message" name="message" required></textarea>
            <button type="submit">Send</button>
        </form>
    </section>

    <footer>
        <p>&copy; 2025 Corsa Nocturne. All rights reserved.</p>
    </footer>

    <!-- RSVP Modal -->
    <div id="rsvpModal" class="modal">
        <div class="modal-content">
            <span class="close" onclick="closeRSVP()">&times;</span>
            <h2>RSVP</h2>
            <form id="rsvpForm">
                <input type="hidden" id="rsvpEvent" name="rsvpEvent">
                <p id="rsvpEventText"></p>
                <label for="rsvpName">Your Name:</label><input type="text" id="rsvpName" name="rsvpName" required>
                <label for="rsvpEmail">Your Email:</label><input type="email" id="rsvpEmail" name="rsvpEmail" required>
                <button type="submit">Submit RSVP</button>
            </form>
        </div>
    </div>

    <script>
        document.getElementById('contactForm').addEventListener('submit', function(e) {
            e.preventDefault();
            alert('Thank you for contacting us! We will get back to you.');
            this.reset();
        });

        document.getElementById('ticketForm').addEventListener('submit', function(e) {
            e.preventDefault();
            alert('Your tickets have been booked! Check your email for details.');
            this.reset();
        });

        document.getElementById('rsvpForm').addEventListener('submit', function(e) {
            e.preventDefault();
            alert('RSVP submitted! See you at the event.');
            closeRSVP();
            this.reset();
        });

        function openRSVP(eventName) {
            document.getElementById('rsvpModal').style.display = 'flex';
            document.getElementById('rsvpEventText').textContent = `Event: ${eventName}`;
            document.getElementById('rsvpEvent').value = eventName;
        }

        function closeRSVP() {
            document.getElementById('rsvpModal').style.display = 'none';
        }
    </script>
</body>
</html># e.g.corsanocturne
