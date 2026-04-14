# 🚀 Trivia Game - Plaza Cielo Tierra

This repository contains the production-ready source code and assets for the **Plaza Cielo Tierra** science museum interactive trivia game. Designed as a cross-platform simulation, the project integrates **Unity UI Toolkit** with a **Supabase** backend to provide a seamless, real-time competitive experience.

---

## 🔗 Live Deployment
You can access the live version of the game here:
**https://xpedrojfloresx.github.io/pct-build-client-dev/**

---

## 🌐 Deployment Configuration

This repository is optimized for deployment. Key configurations include:

### 1. Backend Integration (Supabase)
The application is pre-configured to communicate with a Supabase instance for data persistence.
* **Real-time Scoring**: Player scores are pushed to the database upon completion.
* **Data Collection**: The system captures user demographics (Name, Surname, Age, Country) alongside performance metrics for museum analytics.
* **Service Setup**: Ensure the `SupabaseService` component in the main scene is updated with the production URL and Anon Key.

### 2. Global UI Theming (Panel Settings)
To ensure visual consistency across different mobile devices and resolutions:
* **Theme Management**: The project utilizes a custom **Theme Style Sheet** assigned to the `Panel Settings` asset.
* **Global Styles**: Critical UI fixes, such as the flicker-free dropdown menus and pixel-art font rendering, are handled through global USS files linked to the Theme.
* **Performance**: UI rendering is optimized via the `Scale With Screen Size` mode, targeting a 1080x1920 reference resolution.

### 3. Mobile Optimization
* **Touch-First Navigation**: Scrollbars are hidden via USS to favor native touch gestures on mobile devices.
* **Dynamic Anchoring**: The country selection dropdown uses a script-based anchoring system (`worldBound`) to ensure the menu always appears correctly aligned with the input field regardless of device aspect ratio.

---

## 👨‍💻 Developer Information

This project was developed as a final thesis for the **Virtual Simulations and Video Games Development** degree at **Colegio Universitario IES 21**.

**Pedro Flores**
* **Role**: Junior Full Stack Developer & Technical Artist
* **Location**: Córdoba, Argentina
* **Specialization**: 3D Web Technologies (Three.js/Babylon.js), Unity Technical Art, and Full Stack Development.

**Connect with me:**
* **LinkedIn**: https://www.linkedin.com/in/pedro-flores-dev/
* **Portfolio**: https://portfolio-pedrojflores.vercel.app/
* **Email**: pflores0213@gmail.com

---

## 📄 License
*This project is part of a technical thesis and is intended for use by the Plaza Cielo Tierra Science Museum.*

---

## 👥 Team & Collaborators

This project was a collaborative effort, and I would like to acknowledge the hard work and contributions of my teammates:

* **Matías Gómez**: Lead Programmer and partner for the degree thesis project.
* **Nicolás Álvarez**: Artist and Game Designer.

Working together, we ensured the technical and artistic success of the trivia system for the museum.
