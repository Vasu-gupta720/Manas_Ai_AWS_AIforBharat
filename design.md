# Manas AI – Design Document

## 1. System Overview

Manas AI is a voice-first AI companion for students providing emotional support through natural conversation. The system creates a safe, judgment-free space for students to express themselves and receive empathetic, contextually aware responses.

### Core Philosophy
- Supportive friend rather than clinical tool
- Active listening with emotional intelligence
- Student safety and privacy prioritized
- Non-judgmental, warm communication

### Key Capabilities
- Voice-first natural speech interaction
- Real-time emotion detection and sentiment analysis
- Contextual awareness across sessions
- Crisis detection with appropriate resource provision
- Multilingual support (English and Hindi)
- Privacy-centric design with no permanent voice storage

---

## 2. Architecture

### System Flow
```
Student Voice → Speech-to-Text → AI Conversation Engine → Response Generation → Text-to-Speech → Voice Output
                                          ↓
                                  Emotion Analysis (parallel)
                                          ↓
                                  Safety & Crisis Check
                                          ↓
                                  Insights & Engagement
```

### Component Interaction
- **Synchronous**: Voice input → STT → Conversation → TTS → Voice output
- **Asynchronous**: Emotion analysis → Insights → Proactive engagement
- **Safety Override**: Crisis detection interrupts normal flow

---

## 3. Core Components

### 3.1 User Interface
**Design Principles**: Minimalist, accessible, calming aesthetics, voice-first

**Key Elements**:
- Large centered microphone button with pulse animation
- Optional text transcript display
- Status indicators (connection, processing, emotion detection)
- Settings panel (language, voice speed, privacy)
- Emergency access to crisis resources
- Text input fallback

**Responsive**: Mobile-first, tablet/desktop support, offline indicators, low-bandwidth optimization

### 3.2 Speech-to-Text Module
**Audio Processing**:
- High-quality capture with noise cancellation
- Voice activity detection for auto start/stop
- Streaming transcription for real-time feedback

**Transcription**:
- Primary: Browser Web Speech API (low-latency)
- Fallback: OpenAI Whisper API (higher accuracy)
- Automatic language detection (English/Hindi)
- Code-switching support for mixed languages
- Confidence scoring and error handling

### 3.3 AI Conversation Engine
**Model**: GPT-4 or similar LLM fine-tuned for student support

**Personality**: Warm, empathetic, non-judgmental, casual yet supportive

**Intent Recognition**:
- Emotional expression and sharing
- Information seeking (stress management, study tips)
- Crisis signals (self-harm, severe distress)
- Casual conversation
- Activity requests (breathing exercises, meditation)

**Context Management**:
- Session context and emotional trajectory
- Anonymized interaction history
- Current and recent emotional patterns
- Topic tracking for coherence

**Response Strategy**:
- Empathy first, acknowledge emotions
- Open-ended questions for self-reflection
- Validation and normalization
- Gentle guidance without prescription
- Regular wellness check-ins

### 3.4 Emotion & Sentiment Analysis
**Analysis Dimensions**:
- Primary emotions: joy, sadness, anger, fear, surprise, disgust
- Emotional intensity (mild to severe)
- Sentiment polarity (positive, neutral, negative)
- Stress and anxiety indicators
- Crisis markers

**Methods**:
- NLP models on transcribed speech
- Pattern recognition over time
- Contextual analysis with conversation history
- Parallel processing to avoid delays

**Privacy**: Emotion data stored separately, aggregated/anonymized, user control, automatic deletion

### 3.5 Insights & Engagement Layer
**Pattern Detection**:
- Emotional trends over days/weeks
- Trigger identification
- Engagement patterns (time, frequency, duration)
- Coping effectiveness tracking

**Proactive Engagement**:
- Check-ins after negative emotion periods
- Celebration of positive shifts
- Self-care activity reminders
- Timely resource suggestions

**Activity Recommendations**:
- Breathing exercises
- Mindfulness and grounding
- Journaling prompts
- Physical movement breaks
- Social connection encouragement

### 3.6 Monthly Emotional Wrap
**Data Aggregation**: 30-day emotion data, dominant states, interaction frequency/duration

**Visualizations**:
- Emotion timeline
- Mood distribution charts
- Interaction pattern heatmaps
- Progress indicators
- Reflection prompts

**Insights**: Patterns, triggers, effective coping strategies, growth recognition

**Privacy**: User control to view/download/delete, optional sharing, opt-out available

### 3.7 Safety & Crisis Module
**Risk Detection**:
- Explicit crisis language (self-harm, suicide)
- Implicit indicators (hopelessness, isolation)
- Extreme emotional distress
- Sudden behavioral changes

**Crisis Response Protocol**:
1. Immediate validation without judgment
2. Safety assessment questions
3. Crisis helpline and emergency contact provision
4. Tone shift to serious, supportive mode
5. Follow-up in subsequent interactions

**Resources**: National helplines, campus counseling, local services, online support, emergency services

**Disclaimers**: Clear communication about limitations, not a replacement for professional help

---

## 4. Technology Stack

### Frontend
- React.js with TypeScript
- Material-UI or Chakra UI
- Redux/Zustand for state management
- Web Audio API
- Chart.js for visualizations
- PWA with service workers

### Backend
- Node.js with Express.js
- TypeScript
- RESTful APIs with WebSocket
- JWT authentication
- Rate limiting

### AI & ML
- Conversational AI: OpenAI GPT-4 or Anthropic Claude
- STT: Browser Web Speech API / OpenAI Whisper
- TTS: ElevenLabs API
- Emotion Analysis: Hugging Face Transformers
- Language Detection: FastText

### Data Storage
- PostgreSQL (primary database)
- Redis (session/cache)
- AWS S3 (temporary audio files)
- InfluxDB (emotion tracking)

### Infrastructure
- Cloud hosting (AWS/GCP/Azure)
- Docker containerization
- Kubernetes for scaling
- CloudFlare CDN
- Sentry error tracking
- GitHub Actions CI/CD

---

## 5. Privacy & Ethics

### Data Privacy
- Data minimization and purpose limitation
- Automatic deletion after retention period
- Transparent communication
- User control over data

### Voice Data
- No permanent storage, immediate deletion after transcription
- Encrypted transmission
- No voice biometrics
- Explicit user consent

### Conversation Data
- Anonymized, no PII collected
- Encrypted at rest
- 90-day retention (configurable)
- Export rights for users

### Ethical Guidelines
- No diagnosis or therapy claims
- Professional referral when appropriate
- Informed consent about capabilities
- Cultural sensitivity
- Mandatory crisis resources

### Compliance
- GDPR, COPPA considerations
- Indian data protection laws
- WCAG 2.1 AA accessibility

---

## 6. Scalability & Future Scope

### Technical Scalability
- Horizontal scaling with stateless services
- Load balancing and caching
- Database optimization
- Async processing queues

### Language Expansion
- Phase 1: English and Hindi
- Phase 2: Tamil, Telugu, Bengali, Marathi
- Phase 3: Regional languages

### Feature Enhancements
- Voice journaling
- Peer support groups
- Goal tracking
- Wearable integration
- Campus system integration

### Platform Expansion
- Native mobile apps (iOS/Android)
- Voice-only low-bandwidth mode
- Smart speaker integration
- Offline mode

---

## 7. Limitations

### Technical
- Prototype-level accuracy initially
- API free-tier constraints
- Network-dependent latency
- Limited language support initially

### Functional
- Not a replacement for therapy
- Cannot dispatch emergency services
- Limited crisis intervention capability
- No medical diagnosis
- Context understanding limitations

### Scope
- Awareness-focused, not clinical intervention
- Optimized for college-age students
- Best for stress, anxiety, loneliness
- Initially designed for Indian context

### Mitigation
- Clear communication of limitations
- Regular updates based on feedback
- Partnerships with mental health services
- Continuous monitoring and improvement

---

## 8. Implementation Roadmap

### Phase 1: MVP (Months 1-3)
- Basic voice input/output
- Conversational AI with empathetic responses
- Text-based emotion analysis
- Minimal UI with microphone button
- Crisis detection and resources
- English support

### Phase 2: Enhanced Features (Months 4-6)
- Hindi language support
- Improved emotion analysis with patterns
- Proactive engagement triggers
- Activity recommendations
- Enhanced UI with history

### Phase 3: Insights & Personalization (Months 7-9)
- Monthly emotional wrap
- Personalized response tuning
- Advanced pattern recognition
- Goal setting and tracking

### Phase 4: Scale & Expand (Months 10-12)
- Additional Indian languages
- Native mobile apps
- Campus integration pilots
- Advanced analytics
- Performance optimization

---

## 9. Success Metrics

### User Engagement
- DAU/MAU, session duration, frequency
- Conversation completion rates
- Return user rate (7-day)

### Technical Performance
- STT accuracy (>90%)
- Response latency (<3 seconds)
- System uptime (99.5%)

### User Satisfaction
- Satisfaction surveys (>4/5)
- Net Promoter Score
- User retention (30-day, 90-day)

### Impact
- Self-reported stress reduction
- Emotional awareness improvement
- Help-seeking behavior increase
