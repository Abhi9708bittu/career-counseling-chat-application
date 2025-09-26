# Career Counseling Chat Application

A modern, AI-powered career counseling platform built with Next.js, TypeScript, tRPC, and OpenAI. This application provides personalized career guidance through an intuitive chat interface.

## Features

- 🤖 **AI Career Counselor**: Powered by OpenAI GPT-3.5-turbo for intelligent career guidance
- 💬 **Real-time Chat Interface**: Modern, responsive chat UI with message history
- 📚 **Chat Session Management**: Create, manage, and continue multiple chat sessions
- 🔐 **User Authentication**: Secure user registration and login system
- 💾 **Persistent Storage**: All conversations are saved to PostgreSQL database
- 📱 **Responsive Design**: Works seamlessly on desktop and mobile devices
- ⚡ **Type-Safe API**: Built with tRPC for end-to-end type safety

## Tech Stack

- **Frontend**: Next.js 14, TypeScript, Tailwind CSS
- **Backend**: tRPC, Next.js API Routes
- **Database**: PostgreSQL with Prisma ORM
- **Authentication**: NextAuth.js
- **AI Integration**: OpenAI API
- **State Management**: TanStack Query (React Query)

## Prerequisites

Before running this application, make sure you have:

- Node.js 18+ installed
- PostgreSQL database running
- OpenAI API key

## Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/Abhi9708bittu/career-counseling-chat-application.git
   cd career-counseling-chat-application
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up environment variables**
   ```bash
   cp env.example .env.local
   ```
   
   Update the following variables in `.env.local`:
   ```env
   DATABASE_URL="postgresql://username:password@localhost:5432/career_counseling_chat?schema=public"
   NEXTAUTH_URL="http://localhost:3000"
   NEXTAUTH_SECRET="your-secret-key-here"
   OPENAI_API_KEY="your-openai-api-key-here"
   ```

4. **Set up the database**
   ```bash
   npx prisma generate
   npx prisma db push
   ```

5. **Run the development server**
   ```bash
   npm run dev
   ```

6. **Open your browser**
   Navigate to [http://localhost:3000](http://localhost:3000)

## Usage

1. **Sign Up**: Create a new account or sign in with existing credentials
2. **Start a Chat**: Click "New Chat" to begin a new career counseling session
3. **Ask Questions**: Ask about career goals, skills, job searching, interviews, etc.
4. **Manage Sessions**: View all your previous conversations and continue where you left off
5. **Get Guidance**: Receive personalized, AI-powered career advice and recommendations

## API Endpoints

The application uses tRPC for type-safe API communication:

- `chat.getChatSessions` - Get all chat sessions for the current user
- `chat.getChatSession` - Get a specific chat session with messages
- `chat.createChatSession` - Create a new chat session
- `chat.sendMessage` - Send a message and get AI response
- `chat.deleteChatSession` - Delete a chat session

## Database Schema

- **Users**: User accounts with authentication
- **ChatSessions**: Individual chat conversations
- **Messages**: Individual messages within chat sessions
- **Accounts/Sessions**: NextAuth.js authentication tables

## Deployment

1. **Deploy to Vercel** (recommended):
   - Connect your GitHub repository to Vercel
   - Set environment variables in Vercel dashboard
   - Deploy automatically on push to main branch

2. **Deploy to other platforms**:
   - Build the application: `npm run build`
   - Start the production server: `npm start`
   - Ensure PostgreSQL database is accessible

## Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feature-name`
3. Commit changes: `git commit -m 'Add feature'`
4. Push to branch: `git push origin feature-name`
5. Submit a pull request

## License

This project is licensed under the MIT License.

## Support

For support or questions, please open an issue on GitHub or contact the development team.

---



