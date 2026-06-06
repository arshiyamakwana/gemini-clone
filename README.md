# Gemini Clone

A modern AI chatbot interface built with React and powered by Google's Gemini API. This project replicates the functionality of Google Gemini with a clean, responsive UI.

## Features

- 💬 **AI Chat Interface** - Chat with Google's Gemini 2.0 Flash model
- 📱 **Responsive Design** - Works seamlessly on desktop and mobile devices
- 🎯 **Sidebar Navigation** - View chat history and start new conversations
- ⚡ **Real-time Responses** - Animated text streaming for responses
- 🎨 **Modern UI** - Clean and intuitive user interface
- 🔒 **Safety Features** - Content filtering with harm prevention settings

## Tech Stack

- **Frontend Framework**: React 19.1.0
- **Build Tool**: Vite 6.3.5
- **API Integration**: Google Generative AI (@google/generative-ai)
- **Styling**: CSS3

## Prerequisites

Before you begin, ensure you have the following installed:

- Node.js (v16 or higher)
- npm or yarn package manager
- A Google API key for Gemini (get it from [Google AI Studio](https://aistudio.google.com/apikey))

## Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/yourusername/gemini-clone.git
   cd gemini-clone
   ```

2. **Install dependencies**

   ```bash
   npm install
   ```

3. **Configure your API Key**
   - Open `src/config/gemini.js`
   - Replace `"Paste Your API KEY Here"` with your actual Google API key
   ```javascript
   const API_KEY = "your-api-key-here";
   ```

## Running the Project

### Development Mode

Start the development server:

```bash
npm run dev
```

The application will be available at `http://localhost:5173` (or the port shown in your terminal).

### Build for Production

Build the project for production:

```bash
npm run build
```

### Preview Production Build

Preview your production build locally:

```bash
npm run preview
```

## Project Structure

```
gemini-clone/
├── src/
│   ├── components/
│   │   ├── Main/           # Main chat interface
│   │   │   ├── Main.jsx
│   │   │   └── Main.css
│   │   └── Sidebar/        # Chat history sidebar
│   │       ├── Sidebar.jsx
│   │       └── Sidebar.css
│   ├── config/
│   │   └── gemini.js       # Gemini API configuration
│   ├── context/
│   │   └── Context.jsx     # React Context for state management
│   ├── assets/
│   │   └── assets.js       # Asset imports
│   ├── App.jsx             # Main app component
│   ├── main.jsx            # Entry point
│   └── index.css           # Global styles
├── public/                 # Static files
├── index.html              # HTML template
├── package.json            # Project dependencies
└── vite.config.js          # Vite configuration
```

## Configuration

### Gemini Model Settings

The following configuration is set in `src/config/gemini.js`:

- **Model**: `gemini-2.0-flash`
- **Temperature**: 0.75 (controls randomness)
- **Max Output Tokens**: 2048
- **Safety Level**: Blocks medium and above harmful content

You can modify these settings as needed for your use case.

## Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run lint` - Run ESLint to check code quality
- `npm run preview` - Preview production build

## Usage

1. Start the application using `npm run dev`
2. Enter your message in the input field
3. Click send or press Enter
4. View the AI response with animated text streaming
5. Access previous conversations from the sidebar

## Safety Features

The application includes content filtering:

- Harassment protection
- Hate speech filtering
- These can be adjusted in `src/config/gemini.js`

## Troubleshooting

### API Key Not Working

- Verify your API key is valid from [Google AI Studio](https://aistudio.google.com/apikey)
- Ensure it has proper access permissions for Gemini API
- Check for any whitespace in the API key

### Build Errors

- Clear `node_modules` and reinstall: `rm -rf node_modules && npm install`
- Make sure you're using Node.js v16 or higher

### Port Already in Use

- Change the port in `vite.config.js` or use: `npm run dev -- --port 5174`

## Environment Variables

For security, consider using environment variables instead of hardcoding your API key:

```javascript
// In src/config/gemini.js
const API_KEY = import.meta.env.VITE_GEMINI_API_KEY;
```

Create a `.env` file in the root:

```
VITE_GEMINI_API_KEY=your-api-key-here
```

**Note**: Add `.env` to `.gitignore` to prevent exposing your API key.

## Contributing

Contributions are welcome! Feel free to submit a Pull Request.

## License

This project is open source and available under the MIT License.

## Acknowledgments

- Built with [Vite](https://vitejs.dev/)
- Powered by [Google Generative AI](https://ai.google.dev/)
- React Community

## Support

For issues and questions, please open an issue on the repository.

---

**Happy Coding!** 🚀
