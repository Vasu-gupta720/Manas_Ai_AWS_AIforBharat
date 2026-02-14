# Manas AI 🧠💙

> An India-first, voice-enabled AI companion supporting student mental well-being through empathetic conversation.


---

## 🌟 Overview

Manas AI is a voice-first AI companion designed specifically for students to provide emotional support and mental wellness assistance through natural conversation. The system creates a safe, judgment-free space where students can express themselves freely and receive empathetic, contextually aware responses.

### Why Manas AI?

Students across India face increasing academic pressure, isolation, and emotional burnout. Despite the availability of mental health resources, many hesitate to seek help due to stigma, fear of judgment, or discomfort with formal systems. Manas AI bridges this gap by offering:

- 🎤 **Voice-First Interaction**: Natural speech-based communication
- 🧠 **Emotional Intelligence**: Real-time emotion detection and sentiment analysis
- 🔒 **Privacy-Centric**: No permanent storage of sensitive voice data
- 🌐 **Multilingual Support**: English and Hindi with extensibility for regional languages
- 🚨 **Crisis Detection**: Identifies high-risk situations and provides appropriate resources

---

## ✨ Key Features

### Core Capabilities
- **Natural Conversations**: Speak freely about academic pressure, stress, loneliness, or emotional burnout
- **Empathetic Responses**: Warm, non-judgmental, human-like voice output
- **Background Emotion Analysis**: Silent sentiment tracking without interrupting the experience
- **Proactive Check-ins**: Gentle engagement based on emotional patterns
- **Monthly Emotional Wrap**: Visual summaries of emotional trends for self-reflection
- **Safety First**: Crisis detection with helpline and resource provision

### User Interface
- Large, centered microphone button with pulse animation
- Optional text transcript display
- Emergency access to crisis resources
- Text input fallback for situations where voice isn't practical
- Mobile-first responsive design

---

## 🏗️ Architecture

```
Student Voice Input
       ↓
Speech-to-Text Module
       ↓
AI Conversation Engine ←→ Emotion Analysis (parallel)
       ↓                          ↓
Response Generation         Safety & Crisis Check
       ↓                          ↓
Text-to-Speech            Insights & Engagement
       ↓
Voice Output to Student
```

### Component Interaction
- **Synchronous Path**: Voice input → STT → Conversation → TTS → Voice output
- **Asynchronous Path**: Emotion analysis → Insights → Proactive engagement
- **Safety Override**: Crisis detection can interrupt normal flow for immediate intervention

---

## 🛠️ Technology Stack

### Frontend
- **Framework**: React.js with TypeScript
- **UI Library**: Material-UI or Chakra UI
- **State Management**: Redux/Zustand
- **Audio**: Web Audio API
- **Visualizations**: Chart.js
- **PWA**: Service workers for offline capability

### Backend
- **Runtime**: Node.js with Express.js
- **Language**: TypeScript
- **APIs**: RESTful with WebSocket for real-time features
- **Authentication**: JWT tokens
- **Rate Limiting**: API abuse prevention

### AI & ML Services
- **Conversational AI**: OpenAI GPT-4 or Anthropic Claude
- **Speech-to-Text**: Browser Web Speech API / OpenAI Whisper
- **Text-to-Speech**: ElevenLabs API
- **Emotion Analysis**: Hugging Face Transformers
- **Language Detection**: FastText

### Data Storage
- **Primary Database**: PostgreSQL
- **Session/Cache**: Redis
- **File Storage**: AWS S3 (temporary audio files)
- **Analytics**: InfluxDB (emotion tracking)

### Infrastructure
- **Hosting**: AWS/GCP/Azure
- **Containerization**: Docker
- **Orchestration**: Kubernetes
- **CDN**: CloudFlare
- **Monitoring**: Sentry, DataDog
- **CI/CD**: GitHub Actions

---

## 📋 Roadmap

### Phase 1: MVP (Months 1-3) ✅
- [x] Basic voice input/output functionality
- [x] Conversational AI with empathetic responses
- [x] Text-based emotion analysis
- [x] Minimal UI with microphone button
- [x] Crisis detection and resource provision
- [x] English language support

### Phase 2: Enhanced Features (Months 4-6) 🚧
- [ ] Hindi language support
- [ ] Improved emotion analysis with pattern tracking
- [ ] Proactive engagement triggers
- [ ] Activity recommendations (breathing, mindfulness)
- [ ] Enhanced UI with conversation history
- [ ] Basic analytics dashboard

### Phase 3: Insights & Personalization (Months 7-9) 📅
- [ ] Monthly emotional wrap module
- [ ] Personalized response tuning
- [ ] Advanced pattern recognition
- [ ] Goal setting and tracking
- [ ] Improved crisis intervention protocols
- [ ] User feedback integration

### Phase 4: Scale & Expand (Months 10-12) 🔮
- [ ] Additional Indian languages (Tamil, Telugu, Bengali, Marathi)
- [ ] Native mobile apps (iOS/Android)
- [ ] Campus integration pilots
- [ ] Advanced analytics and reporting
- [ ] Community features
- [ ] Performance optimization for scale

---

## 🔒 Privacy & Ethics

### Our Commitments
- **No Permanent Voice Storage**: Raw audio deleted immediately after transcription
- **Data Minimization**: Collect only essential information
- **Anonymization**: No personally identifiable information collected
- **User Control**: Easy access to view, download, or delete data
- **Transparency**: Clear communication about data practices
- **No Diagnosis**: System never provides medical or psychological diagnoses
- **Professional Referral**: Encourage professional help when appropriate

### Compliance
- GDPR compliance for European users
- Indian data protection laws
- WCAG 2.1 AA accessibility standards
- COPPA considerations for younger users

---

## ⚠️ Limitations

### Important Disclaimers
- **Not a Replacement for Therapy**: Manas AI cannot provide professional mental health treatment
- **No Emergency Response**: Cannot dispatch emergency services
- **Limited Crisis Intervention**: Basic support only, not comprehensive crisis care
- **No Medical Diagnosis**: Cannot diagnose or treat mental health conditions
- **Context Limitations**: May misunderstand complex or nuanced situations

### Technical Limitations
- Prototype-level accuracy initially
- API free-tier constraints
- Network-dependent latency
- Limited to English and Hindi initially
- Requires internet connection for core functionality

---

## 📊 Success Metrics

### User Engagement
- Daily/Monthly Active Users (DAU/MAU)
- Average session duration and frequency
- Conversation completion rates
- 7-day return user rate

### Technical Performance
- Speech-to-text accuracy (target: >90%)
- Response latency (target: <3 seconds)
- System uptime (target: 99.5%)

### User Satisfaction
- User satisfaction surveys (target: >4/5)
- Net Promoter Score (NPS)
- User retention (30-day, 90-day)

### Impact Indicators
- Self-reported stress reduction
- Emotional awareness improvement
- Help-seeking behavior increase
- Crisis resource utilization

---

## 🤝 Contributing

We welcome contributions from the community! Please read our [Contributing Guidelines](CONTRIBUTING.md) before submitting pull requests.

### Development Workflow
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Code of Conduct
Please note that this project is released with a [Contributor Code of Conduct](CODE_OF_CONDUCT.md). By participating in this project you agree to abide by its terms.

---

## 📄 Documentation

- [Requirements Document](requirements.md) - Detailed functional and non-functional requirements
- [Design Document](design.md) - Comprehensive system architecture and design specifications
- [API Documentation](docs/API.md) - RESTful API endpoints and WebSocket events
- [Deployment Guide](docs/DEPLOYMENT.md) - Production deployment instructions

---

## 🆘 Crisis Resources

If you or someone you know is in crisis, please reach out to these resources immediately:

### India
- **AASRA**: 91-22-27546669 (24x7)
- **Vandrevala Foundation**: 1860-2662-345 / 1800-2333-330 (24x7)
- **iCall**: 022-25521111 (Mon-Sat, 8am-10pm)
- **NIMHANS**: 080-46110007 (Mon-Sat, 9am-5:30pm)

### International
- **International Association for Suicide Prevention**: https://www.iasp.info/resources/Crisis_Centres/

---

## 📧 Contact

- **Project Lead**: Aastha Suhani
- **GitHub**: [@Vasu-gupta720](https://github.com/Vasu-gupta720)
- **Project Link**: [https://github.com/Vasu-gupta720/Manas_Ai_AWS_AIforBharat](https://github.com/Vasu-gupta720/Manas_Ai_AWS_AIforBharat)



---

## 🙏 Acknowledgments

- OpenAI for GPT-4 API
- ElevenLabs for natural voice synthesis
- Hugging Face for emotion analysis models
- All contributors and supporters of mental health awareness
- The student community for inspiring this project

---

<div align="center">

**Made with ❤️ for student mental well-being**

*Manas AI - Your companion in the journey of emotional wellness*

</div>
