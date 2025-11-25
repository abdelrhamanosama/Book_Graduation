# INTRODUCTION
Learning the Qur’an with correct recitation (Tajweed) and memorization (Hifz) has always required direct, continuous supervision from a qualified Sheikh or Sheikha. In traditional Muslim societies, this supervision occurs through mosque-based “Halaqat al-Qur’an” where students sit in circles around a teacher who listens, corrects pronunciation, Tashkeel, and Tajweed rules in real time. This method has proven highly effective for centuries.

However, millions of Muslims living in Europe, North America, Australia, East Asia, and other non-Arab or minority-Muslim regions face severe obstacles in accessing such qualified teachers. Even in many Arab and Muslim-majority countries, the demand for skilled Sheikhs far exceeds supply, especially for female students who often require female teachers for cultural or religious reasons.

At the same time, thousands of highly qualified male and female Huffaz and Tajweed experts remain under-utilized because they lack a structured, global platform to offer their services and earn a respectable income from their knowledge.


## 1.1. Problem Statement
The core problems that this project addresses can be summarized as follows:

1. Geographical and Temporal Barriers Students living far from qualified Sheikhs cannot receive regular, personalized correction of recitation mistakes.
2. Severe Shortage of Qualified Female Sheikhs Many female students and parents refuse mixed-gender sessions, yet female Tajweed teachers are extremely scarce outside certain countries.
3. High Cost and Inflexibility of Traditional Online One-to-One Lessons Existing platforms (when available) are expensive, lack transparent rating systems, and do not guarantee Tajweed specialization.
4. Absence of Objective, Instant Feedback During Independent Practice When a live Sheikh is not available (e.g., late at night), students have no reliable way to know whether they are making linguistic, Tashkeel, or Tajweed mistakes.
5. Under-Utilization of Qualified Human Resources Thousands of certified Sheikhs and Sheikhas worldwide possess excellent recitation skills but have no easy, trustworthy way to reach students globally and monetize their expertise fairly.
6. Lack of Measurable Long-Term Progress Tracking Students and teachers currently rely on subjective memory rather than data-driven reports showing improvement over months and years.
7. Limited scalability (one teacher cannot evaluate many students).
8. Slow review cycles and high workload on teachers.
9. Difficulty pinpointing exact time-based errors.
10. Lack of structured data to track student improvement over time.
11. No instant feedback for the student after recitation.
12. Students require the ability to practice recitation repeatedly at any time.

## 1.2. Suggested Solution – “Qur’anConnect” Platform

Qur’anConnect is a full-stack interactive platform that combines human expertise with artificial intelligence to deliver an experience as close as possible to traditional Halaqat while making it globally accessible 24/7.

The platform consists of two tightly integrated layers:

### Layer 1: Human-to-Human Layer (Live Supervised Sessions)

- Students browse and filter verified Sheikhs by accent (Hafs, Warsh, etc.), gender, hourly rate, ratings, years of experience, mother tongue, and real-time availability.
- Secure booking, escrow-based payment, high-quality WebRTC audio/video calls.
- Automatic session recording (optional), real-time mistake logging, post-session progress reports, and rating system.
- Wallet system and automated payouts to Sheikhs (platform retains a small fair commission).

### Layer 2: Human-to-AI Layer (Autonomous Practice & Assessment)

- This repository contains an AI-powered pipeline for analyzing Qur’an recitation.
It processes an audio file, extracts the spoken text, compares it with the correct Qur’anic verse, and generates a full evaluation report.
- Real-time or post-recitation visual feedback highlighting exact mistake locations in the verse.
- Long-term progress dashboard with statistics and improvement trends.
- AI Pipeline for Handling Recitation:
  - Layer 1 → Audio Separation (Model)
  - Layer 2 → Audio Filtering (Python DSP)
  - Layer 3 → ASR — Speech Recognition
  - Layer 4 → Text & Acoustic Comparison
  - Layer 5 → Report Generation
 
  
By merging verified human teachers with always-available AI correction, the platform offers the best of both worlds: the spiritual and motivational impact of a real Sheikh when possible, and accurate, tireless practice and correction at any hour.


## 1.3. Project Aim and Objectives

### Aim

To design and implement a scalable, secure, and user-friendly web and mobile platform that connects Quran students worldwide with qualified Sheikhs while providing state-of-the-art AI-powered recitation assessment, thereby democratizing access to high-quality Tajweed education.

### Specific Objectives

1. Develop a robust user management and Sheikh verification workflow.
2. Implement an intelligent Sheikh discovery and filtering system.
3. Build a complete session lifecycle system (booking → payment → live call → feedback → payout).
4. Integrate a high-quality WebRTC audio/video communication layer.
5. Develop or fine-tune an AI model capable of detecting and classifying the three categories of recitation mistakes with high accuracy.
6. Create detailed progress tracking and reporting dashboards for students and Sheikhs.
7. Ensure all financial transactions are secure, transparent, and Shariah-compliant (escrow model).
8. Design a responsive interface usable on desktop, tablets, and smartphones.
9. Achieve at least 85% accuracy on the AI Tajweed assessment engine (measured against human expert annotations).
10. Deploy a production-ready MVP by the graduation project deadline.

## 1.4. Project Scope

### In-Scope (MVP – Graduation Project Deliverables)

- Full user registration/login (Student, Sheikh, Admin roles)
- Sheikh application → document upload → manual admin approval workflow
- Advanced search & filters for Sheikhs
- Wallet system + integration with Stripe Connect (or local gateway)
- Session booking with calendar and pending-approval mechanism
- WebRTC live audio/video sessions with recording option
- Post-session rating, notes, and mistake reports
- AI recitation assessment (real-time or upload-based) with three-level mistake classification
- Progress dashboard and history
- Responsive web interface (PWA-ready)
- Complete backend APIs, and PostgreSQL database
- Basic admin panel for user management, dispute handling, and analytics

### Out-of-Scope (Post-Graduation / Future Phases)

- Native iOS & Android apps (will be PWAs in MVP)
- Group Halaqat (many-to-one sessions)
- Subscription plans
- Automated bank transfers to Sheikhs in 100+ countries
- Advanced gamification and certification system
- Integration with physical Quran institutes


## 1.5. Project Milestones

| Sprint # | Finish Date | Sprint Goal & Key Deliverables                                                                                                                                                                                      |
| -------- | ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1        | 30/01/2025  | **Learning & Setup Sprint**<br>• Team training (React, Spring, Docker) <br>• Project repo + CI/CD setup <br>• Initial UI/UX mockups in Figma <br>• Basic ERD draft                                                  |
| 2        | 28/02/2025  | **Authentication & Profiles** <br>• Complete user auth (JWT + Refresh) <br>• Student & Sheikh profiles <br>• Sheikh application form + file upload <br>• Admin panel basics                                         |
| 3        | 31/03/2025  | **Sheikh Verification & Search** <br>• Admin approval workflow <br>• Advanced search & filters (accent, gender, price, rating, etc.) <br>• Sheikh public profile page                                               |
| 4        | 30/04/2025  | **Wallet & Payment System** <br>• Wallet top-up (Stripe/Paymob/Fawry) <br>• Session price calculation & escrow logic <br>• Transaction history                                                                      |
| 5        | 31/05/2025  | **Session Booking & Calendar** <br>• Availability calendar (Sheikh side) <br>• Session request → approval/refusal flow <br>• Payment release after session ends                                                     |
| 6        | 05/07/2025  | **Live Session Core (WebRTC)** <br>• Audio/video call using Agora or Vonage <br>• Session timer, recording toggle, notes <br>• End-session flow + rating                                                            |
| 7        | 10/08/2025  | **AI Recitation Assessment – Phase 1** <br>• Recording upload + real-time microphone access <br>• Integration with AI backend (Whisper + Tajweed classifier) <br>• Display mistakes (linguistic, tashkeel, tajweed) |
| 8        | 31/08/2025  | **Progress Dashboard & History** <br>• Student dashboard (past sessions, AI reports, progress charts) <br>• Sheikh dashboard (earnings, ratings, upcoming sessions)                                                 |
| 9        | 20/09/2025  | **Final Polish & Testing** <br>• Full testing (unit, integration, E2E) <br>• Bug fixes & performance optimization                                                                                                   |
| 10       | 15/10/2025  | **Documentation & Defense Preparation** <br>• Final report writing & diagrams <br>• Presentation & demo video <br>• Deployment to production server                                                                 |

## 1.6. Detailed Project Plan (Gantt-style Table)
| Phase / Sprint                       | Task Name                                 | Duration | Start Date | End Date   |
| ------------------------------------ | ----------------------------------------- | -------- | ---------- | ---------- |
| **Learning & Setup Sprint 1**        | Learning React + NestJS + TypeScript      | 20 days  | 02/01/2025 | 21/01/2025 |
|                                      | Setup GitHub repo, Docker, CI/CD          | 7 days   | 22/01/2025 | 28/01/2025 |
|                                      | Initial Figma wireframes & UI mockups     | 10 days  | 10/01/2025 | 19/01/2025 |
|                                      | Draft ERD & database schema               | 8 days   | 20/01/2025 | 27/01/2025 |
| **Sprint 2 – Auth & Profiles**       | User authentication & roles               | 18 days  | 01/02/2025 | 18/02/2025 |
|                                      | Student & Sheikh profile management       | 15 days  | 10/02/2025 | 24/02/2025 |
|                                      | Sheikh application form + document upload | 12 days  | 15/02/2025 | 26/02/2025 |
|                                      | Basic Admin panel                         | 10 days  | 19/02/2025 | 28/02/2025 |
| **Sprint 3 – Search & Verification** | Admin approval workflow                   | 14 days  | 01/03/2025 | 14/03/2025 |
|                                      | Advanced Sheikh search & filters          | 18 days  | 08/03/2025 | 25/03/2025 |
|                                      | Sheikh public profile page                | 10 days  | 20/03/2025 | 29/03/2025 |
| **Sprint 4 – Payment**               | Wallet system & top-up (Stripe/Paymob)    | 20 days  | 01/04/2025 | 20/04/2025 |
|                                      | Session pricing & escrow logic            | 15 days  | 10/04/2025 | 24/04/2025 |
|                                      | Transaction history & receipts            | 8 days   | 22/04/2025 | 29/04/2025 |
| **Sprint 5 – Booking**               | Sheikh availability calendar              | 18 days  | 01/05/2025 | 18/05/2025 |
|                                      | Session booking flow + notifications      | 16 days  | 10/05/2025 | 25/05/2025 |
|                                      | Payment release after session             | 8 days   | 24/05/2025 | 31/05/2025 |
| **Sprint 6 – Live Session**          | WebRTC integration (Agora/Vonage)         | 25 days  | 01/06/2025 | 25/06/2025 |
|                                      | Session timer, recording, notes, rating   | 20 days  | 15/06/2025 | 04/07/2025 |
| **Sprint 7 – AI Assessment**         | Real-time/upload recitation recording     | 18 days  | 06/07/2025 | 23/07/2025 |
|                                      | AI backend API integration                | 25 days  | 15/07/2025 | 08/08/2025 |
|                                      | Mistake visualization (3 categories)      | 20 days  | 25/07/2025 | 13/08/2025 |
| **Sprint 8 – Dashboards**            | Student & Sheikh dashboards               | 25 days  | 14/08/2025 | 07/09/2025 |
|                                      | Progress reports & charts                 | 15 days  | 01/09/2025 | 15/09/2025 |
| **Sprint 9 – Testing & Polish**      | Full testing (unit + integration + E2E)   | 20 days  | 08/09/2025 | 27/09/2025 |
|                                      | Bug fixing & performance optimization     | 15 days  | 20/09/2025 | 04/10/2025 |
|                                      | Mobile PWA optimization                   | 10 days  | 01/10/2025 | 10/10/2025 |
| **Sprint 10 – Final**                | Production deployment                     | 7 days   | 05/10/2025 | 11/10/2025 |
|                                      | Final documentation & report              | 20 days  | 20/09/2025 | 09/10/2025 |
|                                      | Presentation & demo preparation           | 10 days  | 05/10/2025 | 14/10/2025 |

