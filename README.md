# LoLLabs Studio - AI Voice Creator

A modern, responsive web application for AI-powered text-to-speech generation and voice cloning using the ElevenLabs API. Transform text into lifelike speech and create custom voices with advanced AI technology.

![LoLLabs Studio Interface](https://img.shields.io/badge/Interface-Modern%20UI-blue)
![API](https://img.shields.io/badge/API-ElevenLabs-green)
![License](https://img.shields.io/badge/License-MIT-yellow)

## ✨ Features

### 🎙️ Text-to-Speech
- **Voice Library**: Access to premium AI voices with categorized selection (Male, Female, AI/Neutral)
- **Advanced Settings**: Fine-tune stability, clarity, and style parameters
- **Real-time Audio Player**: Built-in player with progress tracking and controls
- **Download & Share**: Save generated audio files or share them instantly
- **Keyboard Shortcuts**: Quick generation with Ctrl+Enter and spacebar playback

### 🧬 Voice Cloning
- **Custom Voice Creation**: Upload audio samples to create personalized voices
- **Smart Gender Detection**: Automatic voice categorization with manual override
- **File Support**: Multiple audio formats (MP3, WAV, M4A, FLAC)
- **Quality Validation**: File size and format validation for optimal results

### 🎨 Modern UI/UX
- **Glass Morphism Design**: Beautiful translucent interface with blur effects
- **Dark Theme**: Eye-friendly dark mode with gradient backgrounds
- **Responsive Layout**: Works perfectly on desktop, tablet, and mobile devices
- **Smooth Animations**: Engaging micro-interactions and hover effects
- **Accessibility**: Keyboard navigation and screen reader support

## 🚀 Quick Start

### Prerequisites
- Modern web browser (Chrome, Firefox, Safari, Edge)
- ElevenLabs API key
- Internet connection

### Installation

1. **Clone or Download**
   ```bash
   git clone https://github.com/yourusername/lollabs-studio.git
   cd lollabs-studio
   ```

2. **Setup API Key**
   Open the HTML file and replace the API key:
   ```javascript
   const apiKey = "your_elevenlabs_api_key_here";
   ```

3. **Launch Application**
   ```bash
   # Option 1: Open directly in browser
   open index.html
   
   # Option 2: Use a local server
   python -m http.server 8000
   # or
   npx serve .
   ```

### Getting Your ElevenLabs API Key

1. Visit [ElevenLabs](https://elevenlabs.io)
2. Create an account or log in
3. Navigate to your profile settings
4. Generate an API key
5. Copy the key and paste it in the application

## 📱 Usage

### Text-to-Speech Generation

1. **Select a Voice**
   - Click the voice dropdown
   - Browse categorized voices (Female 👩, Male 👨, AI/Neutral 🤖)
   - Select your preferred voice

2. **Enter Your Text**
   - Type or paste text (up to 5,000 characters)
   - Use the provided sample text or create your own

3. **Adjust Voice Settings**
   - **Stability** (0-1): Controls consistency vs. expressiveness
   - **Clarity** (0-1): Adjusts similarity to original voice
   - **Style** (0-1): Adds stylistic variation

4. **Generate & Play**
   - Click "Generate Speech" or press Ctrl+Enter
   - Use the built-in player to preview
   - Download or share your audio

### Voice Cloning

1. **Prepare Audio Sample**
   - Record at least 1 minute of clear, high-quality audio
   - Supported formats: MP3, WAV, M4A, FLAC
   - Maximum file size: 25MB

2. **Create Custom Voice**
   - Enter a descriptive name
   - Add optional description
   - Upload your audio file
   - Select gender (or let AI auto-detect)

3. **Generate & Use**
   - Click "Create Voice"
   - Wait for processing (usually 1-2 minutes)
   - Your new voice will appear in the voice library

## ⚙️ Configuration

### Voice Settings Explained

| Setting | Range | Description |
|---------|-------|-------------|
| **Stability** | 0.0 - 1.0 | Higher values = more consistent, Lower values = more expressive |
| **Clarity** | 0.0 - 1.0 | Higher values = closer to original voice |
| **Style** | 0.0 - 1.0 | Adds stylistic variation and emotion |

### Recommended Settings

| Use Case | Stability | Clarity | Style |
|----------|-----------|---------|-------|
| **Audiobooks** | 0.7 | 0.8 | 0.2 |
| **Podcasts** | 0.5 | 0.7 | 0.3 |
| **Character Voices** | 0.3 | 0.6 | 0.8 |
| **Professional** | 0.8 | 0.9 | 0.1 |

## 🎹 Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| `Ctrl + Enter` | Generate speech |
| `Spacebar` | Play/pause audio |
| `Escape` | Close dropdowns |

## 🔧 Technical Details

### Technologies Used
- **Frontend**: HTML5, CSS3, Vanilla JavaScript
- **Styling**: CSS Grid, Flexbox, CSS Variables
- **Audio**: Web Audio API, HTML5 Audio
- **File Handling**: FormData API, FileReader API
- **API**: ElevenLabs REST API v1

### Browser Compatibility
- ✅ Chrome 80+
- ✅ Firefox 75+
- ✅ Safari 13+
- ✅ Edge 80+

### Performance Features
- Lazy loading of voice library
- Optimized audio streaming
- Efficient DOM updates
- Memory management for audio files

## 🛠️ Customization

### Adding New Voice Categories
```javascript
const categories = {
    female: [],
    male: [],
    neutral: [],
    celebrity: [], // Add new category
    // Add more categories
};
```

### Customizing Theme Colors
```css
:root {
    --primary: #667eea;      /* Primary brand color */
    --secondary: #764ba2;    /* Secondary brand color */
    --accent: #f093fb;       /* Accent color */
    --bg-primary: #0f0f23;   /* Background color */
    /* Modify other variables */
}
```

### Adding Custom Voice Settings
```javascript
// Add new sliders in the voice-settings section
<div class="slider-group">
    <div class="slider-label">
        <span>Speed</span>
        <span class="slider-value" id="speedValue">1.0</span>
    </div>
    <input type="range" class="slider" id="speed" min="0.5" max="2.0" step="0.1" value="1.0">
</div>
```

## 🐛 Troubleshooting

### Common Issues

**Audio Not Playing**
- Check browser audio permissions
- Ensure audio files are properly loaded
- Try refreshing the page

**Voice Generation Fails**
- Verify API key is correct and active
- Check internet connection
- Ensure text length is under 5,000 characters

**Voice Cloning Issues**
- Verify audio file format (MP3, WAV, M4A, FLAC)
- Check file size (must be under 25MB)
- Ensure audio quality is high (clear speech, minimal background noise)

**Dropdown Not Working**
- Check JavaScript console for errors
- Ensure voices are loaded successfully
- Try refreshing the page

### Error Codes

| Code | Description | Solution |
|------|-------------|----------|
| 401 | Invalid API key | Check and update your API key |
| 429 | Rate limit exceeded | Wait before making more requests |
| 422 | Invalid request data | Check text length and voice settings |

## 📊 API Limits

### ElevenLabs Free Tier
- 10,000 characters per month
- 3 custom voices
- Standard voice library access

### ElevenLabs Paid Tiers
- Starter: 30,000 characters/month
- Creator: 100,000 characters/month
- Pro: 500,000 characters/month
- Scale: Custom limits

## 🔒 Security & Privacy

- API keys are stored client-side only
- Audio files are processed securely through ElevenLabs
- No personal data is stored on external servers
- Generated audio can be downloaded and deleted locally

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feature-name`
3. Commit changes: `git commit -am 'Add feature'`
4. Push to branch: `git push origin feature-name`
5. Submit a pull request

### Development Guidelines
- Follow existing code style
- Add comments for complex functionality
- Test on multiple browsers
- Update documentation as needed

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [ElevenLabs](https://elevenlabs.io) for the amazing AI voice technology
- [Font Awesome](https://fontawesome.com) for the beautiful icons
- [Google Fonts](https://fonts.google.com) for the Inter font family

## 📞 Support

For support and questions:
- 📧 Email: support@lollabs.com
- 🐛 Issues: [GitHub Issues](https://github.com/yourusername/lollabs-studio/issues)
- 💬 Discussions: [GitHub Discussions](https://github.com/yourusername/lollabs-studio/discussions)

## 🚀 Future Roadmap

- [ ] Voice emotion control
- [ ] Batch text processing
- [ ] Voice comparison tool
- [ ] Audio effects and filters
- [ ] Multi-language support
- [ ] Voice analytics dashboard
- [ ] Cloud storage integration
- [ ] Collaboration features

---

**Made with ❤️ by Nitesh** | Powered by ElevenLabs AI
