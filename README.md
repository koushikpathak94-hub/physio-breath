physio-breath

  "name": "physio-breath",
  "private": true,
  "version": "1.0.0",
  "scripts": {
    "dev": "vite",
    "build": "vite build",
    "preview": "vite preview"
  },
  "dependencies": {
    "framer-motion": "^11.0.0",
    "react": "^19.0.0",
    "react-dom": "^19.0.0",
    "react-icons": "^5.2.1",
    "react-router-dom": "^7.0.0"
  },
  "devDependencies": {
    "@vitejs/plugin-react": "^4.3.1",
    "autoprefixer": "^10.4.20",
    "postcss": "^8.4.49",
    "tailwindcss": "^3.4.17",
    "vite": "^6.0.0"
  }
}LOGO

PHYSIO BREATH

Home
About
Services
Testimonials
Contact

[ Book Home Visit ]
Primary: #2563EB
Secondary: #10B981
Background: #F8FAFC
Text: #1F2937
PHYSIO BREATH

Move Better • Heal Faster

📞 9365633019

📧 breathphysio@gmail.com

📍 Guwahati, Assam

Instagram
import React from "react";
import ReactDOM from "react-dom/client";
import App from "./App";
import "./index.css";

ReactDOM.createRoot(document.getElementById("root")).render(
  <React.StrictMode>
    <App />
  </React.StrictMode>
);
import Navbar from "./components/Navbar";
import Hero from "./components/Hero";
import Footer from "./components/Footer";

export default function App() {
  return (
    <>
      <Navbar />
      <Hero />
      <Footer />
    </>
  );
}
import { FaWhatsapp } from "react-icons/fa";

export default function Navbar() {
  return (
    <nav className="bg-white shadow-lg sticky top-0 z-50">
      <div className="max-w-7xl mx-auto flex justify-between items-center px-6 py-4">

        <div className="flex items-center gap-3">
          <img
            src="/logo.png"
            alt="Physio Breath"
            className="w-12 h-12"
          />

          <div>
            <h1 className="text-2xl font-bold text-blue-700">
              PHYSIO BREATH
            </h1>

            <p className="text-sm text-gray-500">
              Move Better • Heal Faster
            </p>
          </div>

        </div>

        <div className="hidden md:flex gap-8">

          <a href="#">Home</a>
          <a href="#">About</a>
          <a href="#">Services</a>
          <a href="#">Contact</a>

        </div>

        <a
          href="https://wa.me/919365633019"
          className="bg-green-500 text-white px-5 py-3 rounded-full flex items-center gap-2 hover:bg-green-600 transition"
        >
          <FaWhatsapp />
          WhatsApp
        </a>

      </div>
    </nav>
  );
}
import { FaPhoneAlt } from "react-icons/fa";

export default function Hero() {
  return (
    <section className="bg-gradient-to-r from-blue-50 to-green-50 min-h-screen flex items-center">

      <div className="max-w-7xl mx-auto px-6 grid md:grid-cols-2 gap-12 items-center">

        <div>

          <h1 className="text-5xl font-bold leading-tight">

            Home Physiotherapy
            <span className="text-blue-700">
              {" "}in Guwahati
            </span>

          </h1>

          <p className="mt-6 text-lg text-gray-600">

            Professional physiotherapy treatment at your doorstep.

            Recover comfortably from your home with personalized care.

          </p>

          <div className="flex gap-5 mt-8">

            <button className="bg-blue-700 text-white px-7 py-4 rounded-full">
              Book Home Visit
            </button>

            <a
              href="tel:9365633019"
              className="border border-blue-700 px-7 py-4 rounded-full flex items-center gap-2"
            >
              <FaPhoneAlt />
              Call Now
            </a>

          </div>

        </div>

        <div>

          <img
            src="/hero-image.jpg"
            className="rounded-3xl shadow-2xl"
            alt="Physiotherapy"
          />

        </div>

      </div>

    </section>
  );
}
export default function Footer() {
  return (
    <footer className="bg-blue-900 text-white py-12">

      <div className="max-w-7xl mx-auto text-center">

        <h2 className="text-3xl font-bold">
          PHYSIO BREATH
        </h2>

        <p className="mt-3">
          Move Better • Heal Faster
        </p>

        <p className="mt-6">
          📞 9365633019
        </p>

        <p>
          📧 breathphysio@gmail.com
        </p>

        <p>
          📍 Guwahati, Assam
        </p>

      </div>

    </footer>
  );
}
@tailwind base;
@tailwind components;
@tailwind utilities;

html{
scroll-behavior:smooth;
}

body{
margin:0;
font-family:Inter,sans-serif;
background:#F8FAFC;
}
import {
  FaWalking,
  FaBone,
  FaHeartbeat,
  FaWheelchair,
  FaHandsHelping,
  FaDumbbell,
} from "react-icons/fa";

const services = [
  {
    icon: <FaBone size={40} />,
    title: "Back & Neck Pain",
    desc: "Personalized treatment for spine and posture problems."
  },
  {
    icon: <FaWalking size={40} />,
    title: "Sports Injury",
    desc: "Fast recovery with modern rehabilitation techniques."
  },
  {
    icon: <FaHeartbeat size={40} />,
    title: "Chest Physiotherapy",
    desc: "Breathing exercises and respiratory rehabilitation."
  },
  {
    icon: <FaWheelchair size={40} />,
    title: "Stroke Rehabilitation",
    desc: "Improve mobility, balance and independence."
  },
  {
    icon: <FaHandsHelping size={40} />,
    title: "Home Visits",
    desc: "Professional physiotherapy at your doorstep."
  },
  {
    icon: <FaDumbbell size={40} />,
    title: "Post Surgery Rehab",
    desc: "Safe recovery after joint replacement and surgery."
  },
];

export default function Services() {
  return (
    <section className="py-24 bg-white">
      <div className="max-w-7xl mx-auto px-6">

        <h2 className="text-4xl font-bold text-center">
          Our Services
        </h2>

        <p className="text-center text-gray-500 mt-3">
          Expert home physiotherapy across Guwahati.
        </p>

        <div className="grid md:grid-cols-3 gap-8 mt-14">

          {services.map((item, index) => (
            <div
              key={index}
              className="rounded-3xl bg-white shadow-xl p-8 hover:-translate-y-3 transition duration-300"
            >
              <div className="text-blue-700">
                {item.icon}
              </div>

              <h3 className="text-2xl font-semibold mt-6">
                {item.title}
              </h3>

              <p className="mt-3 text-gray-600">
                {item.desc}
              </p>
            </div>
          ))}

        </div>
      </div>
    </section>
  );
}
export default function About() {
  return (
    <section className="py-24 bg-slate-50">

      <div className="max-w-7xl mx-auto px-6 grid md:grid-cols-2 gap-16 items-center">

        <img
          src="/about.jpg"
          className="rounded-3xl shadow-2xl"
          alt="About Physio Breath"
        />

        <div>

          <h2 className="text-4xl font-bold">
            About Physio Breath
          </h2>

          <p className="mt-6 text-gray-600 leading-8">

            Physio Breath provides professional home physiotherapy
            services throughout Guwahati.

            We believe every patient deserves personalized care in
            the comfort of their own home.

          </p>

          <button className="mt-8 bg-blue-700 text-white px-8 py-4 rounded-full">
            Learn More
          </button>

        </div>

      </div>

    </section>
  );
}
const features = [
  "Experienced Physiotherapist",
  "100% Home Visit Service",
  "Personalized Exercise Plans",
  "Affordable Treatment",
  "Flexible Appointment Timing",
  "Evidence-Based Practice"
];

export default function WhyChooseUs() {
  return (
    <section className="py-24 bg-gradient-to-r from-blue-700 to-green-500 text-white">

      <div className="max-w-6xl mx-auto px-6">

        <h2 className="text-4xl font-bold text-center">
          Why Choose Physio Breath?
        </h2>

        <div className="grid md:grid-cols-2 gap-8 mt-12">

          {features.map((item, i) => (
            <div
              key={i}
              className="bg-white/10 backdrop-blur-md rounded-2xl p-6"
            >
              ✔ {item}
            </div>
          ))}

        </div>

      </div>

    </section>
  );
}
import Navbar from "./components/Navbar";
import Hero from "./components/Hero";
import About from "./components/About";
import Services from "./components/Services";
import WhyChooseUs from "./components/WhyChooseUs";
import Footer from "./components/Footer";

export default function App() {
  return (
    <>
      <Navbar />
      <Hero />
      <About />
      <Services />
      <WhyChooseUs />
      <Footer />
    </>
  );
}
import Navbar from "./components/Navbar";
import Hero from "./components/Hero";
import About from "./components/About";
import Services from "./components/Services";
import WhyChooseUs from "./components/WhyChooseUs";
import Footer from "./components/Footer";

export default function App() {
  return (
    <>
      <Navbar />
      <Hero />
      <About />
      <Services />
      <WhyChooseUs />
      <Footer />
    </>
  );
}
import Navbar from "./components/Navbar";
import Hero from "./components/Hero";
import About from "./components/About";
import Services from "./components/Services";
import WhyChooseUs from "./components/WhyChooseUs";
import Footer from "./components/Footer";

export default function App() {
  return (
    <>
      <Navbar />
      <Hero />
      <About />
      <Services />
      <WhyChooseUs />
      <Footer />
    </>
  );
}
import { FaWhatsapp } from "react-icons/fa";

export default function WhatsAppButton() {
  return (
    <a
      href="https://wa.me/919365633019"
      target="_blank"
      rel="noreferrer"
      className="fixed bottom-6 right-6 bg-green-500 text-white p-5 rounded-full shadow-2xl hover:scale-110 transition"
    >
      <FaWhatsapp size={32} />
    </a>
  );
}
export default function Booking() {
  return (
    <section className="py-24 bg-white">
      <div className="max-w-4xl mx-auto px-6">

        <h2 className="text-4xl font-bold text-center">
          Book a Home Visit
        </h2>

        <form className="mt-12 grid gap-5">

          <input
            placeholder="Full Name"
            className="border rounded-xl p-4"
          />

          <input
            placeholder="Phone Number"
            className="border rounded-xl p-4"
          />

          <input
            placeholder="Address"
            className="border rounded-xl p-4"
          />

          <textarea
            rows="5"
            placeholder="Describe your condition"
            className="border rounded-xl p-4"
          ></textarea>

          <button className="bg-blue-700 text-white py-4 rounded-xl">
            Book Appointment
          </button>

        </form>

      </div>
    </section>
  );
}
import Navbar from "./components/Navbar";
import Hero from "./components/Hero";
import About from "./components/About";
import Services from "./components/Services";
import WhyChooseUs from "./components/WhyChooseUs";
import Stats from "./components/Stats";
import Testimonials from "./components/Testimonials";
import Booking from "./components/Booking";
import WhatsAppButton from "./components/WhatsAppButton";
import Footer from "./components/Footer";

export default function App() {
  return (
    <>
      <Navbar />
      <Hero />
      <About />
      <Services />
      <WhyChooseUs />
      <Stats />
      <Testimonials />
      <Booking />
      <WhatsAppButton />
      <Footer />
    </>
  );
}
npm install framer-motion react-icons react-router-dom emailjs-com
import { motion } from "framer-motion";

<motion.div
 initial={{opacity:0,y:50}}
 animate={{opacity:1,y:0}}
 transition={{duration:1}}
>

<h1 className="text-6xl font-bold">
Home Physiotherapy
<span className="text-blue-600">
 in Guwahati
</span>
</h1>

</motion.div>
const [dark,setDark]=useState(false);

<button onClick={()=>setDark(!dark)}>
🌙
</button>
<iframe
src="https://www.google.com/maps?q=Guwahati&output=embed"
width="100%"
height="450"
style="border:0;"
loading="lazy">
</iframe>
<title>
Physio Breath | Home Physiotherapy in Guwahati
</title>

<meta
name="description"
content="Professional Home Physiotherapy Service in Guwahati."
/>
Loading...

(Your Logo)

PHYSIO BREATH
Navbar

↓

Hero

↓

Statistics

↓

About

↓

Services

↓

Why Choose Us

↓

Treatment Process

↓

Testimonials

↓

Book Appointment

↓

FAQ

↓

Contact

↓

Google Map

↓

Footer
git add .

git commit -m "Initial Release"

git push origin main
npm run build