# React TypeScript Chatbot UI

A modern chatbot interface built with React and TypeScript. This project provides a clean, responsive UI for chatbot interactions with support for Dialogflow integration.

## Features

- 🎨 Modern and clean UI design
- 💬 Real-time message display
- 🤖 Bot and user message components
- 📱 Responsive design
- 🔌 Ready for Dialogflow API integration
- ⚡ Built with React and TypeScript

## Project Structure

```
├── public/
│   └── index.html          # HTML template
├── src/
│   ├── components/         # React components
│   │   ├── BotMessage.tsx  # Bot message component
│   │   ├── UserMessage.tsx # User message component
│   │   ├── Messages.tsx    # Messages container
│   │   ├── Input.tsx       # Input component
│   │   └── Header.tsx      # Header component
│   ├── Api.ts              # API integration (Dialogflow ready)
│   ├── Chatbot.tsx         # Main chatbot component
│   ├── index.tsx           # Application entry point
│   └── styles.css          # Application styles
├── package.json
├── tsconfig.json
└── README.md
```

## Prerequisites

- Node.js (v12 or higher)
- npm or yarn

## Installation

1. Clone the repository:
```bash
git clone https://github.com/miguelmontanez/react-chatbot.git
cd react-chatbot
```

2. Install dependencies:
```bash
npm install
```

## Usage

### Development

Start the development server:
```bash
npm start
```

The application will open at `http://localhost:3000`

### Build

Create a production build:
```bash
npm run build
```

### Test

Run tests:
```bash
npm test
```

## Configuration

### Dialogflow Integration

The project is set up to work with Dialogflow. To enable it:

1. Get your Dialogflow access token
2. Update the `accessToken` in `src/Api.ts`
3. Uncomment the Dialogflow API calls in `src/Api.ts`:

```typescript
const API = {
  GetBotResponse: async (message: string): Promise<string> => {
    let response = await client.textRequest(message);
    return response.result.fulfillment.speech;
  }
};
```

Currently, the API uses a mock implementation that echoes messages for testing purposes.

## Technologies Used

- **React** (v16.12.0) - UI library
- **TypeScript** (v3.7.5) - Type safety
- **api-ai-javascript** (v2.0.0-beta.21) - Dialogflow client
- **react-scripts** (v3.3.0) - Build tooling

## Browser Support

- Modern browsers (Chrome, Firefox, Safari, Edge)
- Not supported: IE 11 and below

## License

This project is open source and available for use.

## Author

miguelmontanez
