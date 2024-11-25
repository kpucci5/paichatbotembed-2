# Personal AI Chatbot Integration Guide

## Overview
A customizable chat widget that integrates with the Personal AI API to create an interactive chatbot experience on any website. Features include user authentication, customizable UI, responsive design, and real-time message handling.

## Features
- Customizable chat interface
- User authentication with intake form
- Real-time message processing
- Responsive design for all devices
- Session management
- Typing indicators
- Message history
- Fullscreen mode
- URL detection and link conversion
- Custom styling options

## Installation

1. Add the script to your HTML:
```html
<script>
document.addEventListener('DOMContentLoaded', function() {
    initPersonalAIChatbot({
        apiKey: 'your-api-key',
        domainName: 'your-domain-name',
        // ... other config options
    });
});
</script>
```

2. Include the main chatbot script file in your HTML

## Configuration Options

| Option | Type | Description | Default |
|--------|------|-------------|---------|
| `apiKey` | string | Personal AI API key | Required |
| `domainName` | string | Your domain name | Required |
| `initialMessage` | string | First message shown to user | "Hi, welcome to our website. Chat now?" |
| `aiAvatarUrl` | string | URL for AI avatar image | Required |
| `userAvatarUrl` | string | URL for user avatar image | Required |
| `chatbotName` | string | Name of the chatbot | "AI Chatbot" |
| `sendButtonColor` | string | Color for send button | "#6656FF" |
| `messageIconColor` | string | Color for message icon | "#6656FF" |
| `startChatButtonColor` | string | Color for start chat button | "#6656FF" |
| `initiatorPosition` | string | Position of chat widget | "bottom-right" |
| `initialQuestion` | string | First question from AI | Optional |
| `requireIntake` | boolean | Enable/disable intake form | true |
| `defaultUserEmail` | string | Default email when intake disabled | "anonymous@user.com" |
| `intakeFormTitle` | string | Title for intake form | "Before we start chatting" |
| `intakeFormSubtitle` | string | Subtitle for intake form | "Please fill out your information" |

## Positioning Options
The chat widget can be positioned in four corners:
- `"top-left"`
- `"top-right"`
- `"bottom-left"`
- `"bottom-right"` (default)

## Intake Form Fields
When enabled, the intake form collects:
- First Name
- Last Name
- Email Address
- Phone Number

## API Integration
The chatbot integrates with Personal AI's API endpoints:
```javascript
POST https://api.personal.ai/v1/message
Headers: {
    'Content-Type': 'application/json',
    'x-api-key': config.apiKey
}
```

## Customization
### CSS Classes
Major CSS classes for styling:
- `.pai-chat-window`: Main chat window
- `.pai-chat-messages`: Messages container
- `.pai-chat-message`: Individual message
- `.pai-chat-input`: Input field
- `.pai-chat-header`: Chat header

### Mobile Responsiveness
The widget automatically adjusts for mobile devices:
- Full-width display on small screens
- Optimized touch targets
- Responsive font sizes
- Bottom-right positioning

## Browser Support
- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers

## Error Handling
- API connection errors
- Form validation
- Session management
- Network issues

## Security Features
- HTTPS endpoint usage
- Input sanitization
- Session validation
- Secure data transmission

## Performance
- Lazy loading of resources
- Optimized animations
- Efficient DOM updates
- Memory leak prevention

## Troubleshooting
Common issues and solutions:
1. API Key Issues: Verify API key is correct
2. Loading Problems: Check script inclusion
3. Styling Conflicts: Use specific CSS classes
4. Mobile Display: Check viewport settings
