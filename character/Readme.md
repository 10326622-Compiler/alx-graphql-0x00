# alx-graphql-0x00

Rick and Morty Next.js Application
A Next.js application built with TypeScript, Apollo Client, and Tailwind CSS to explore the Rick and Morty universe using the Rick and Morty GraphQL API.
🚀 Getting Started
Prerequisites

Node.js (v16 or higher)
npm or yarn

Installation

Create the Next.js project with TypeScript, ESLint, and Tailwind CSS

bashnpx create-next-app@latest alx-rick-and-morty-app --typescript --eslint --tailwind
When prompted, select the following options:

✅ Would you like to use TypeScript? Yes
✅ Would you like to use ESLint? Yes
✅ Would you like to use Tailwind CSS? Yes
✅ Would you like to use src/ directory? No
✅ Would you like to use App Router? No (we're using Pages Router)
❌ Would you like to customize the default import alias? No

Navigate to the project directory

bashcd alx-rick-and-morty-app

Install Apollo Client and GraphQL dependencies

bashnpm install @apollo/client graphql
npm install @types/graphql
📁 Project Structure
alx-rick-and-morty-app/
├── graphql/
│   ├── apolloClient.ts
│   └── queries.ts
├── pages/
│   ├── _app.tsx
│   └── index.tsx
├── styles/
│   └── globals.css
├── public/
├── package.json
├── tsconfig.json
├── tailwind.config.ts
└── README.md
🔧 Configuration Files
Apollo Client Setup (graphql/apolloClient.ts)
Configures the Apollo Client to connect to the Rick and Morty GraphQL API with in-memory caching.
GraphQL Queries (graphql/queries.ts)
Contains reusable GraphQL query definitions. Currently includes:

GET_EPISODES - Fetches paginated episodes with filtering capabilities

App Component (pages/_app.tsx)
Wraps the entire application with the Apollo Provider to enable GraphQL queries throughout the app.
🎯 Features

TypeScript - Type-safe development
Apollo Client - Efficient GraphQL data management
Tailwind CSS - Utility-first styling
ESLint - Code quality and consistency
Next.js - Server-side rendering and optimization

🏃 Running the Application
Start the development server:
bashnpm run dev
Open your browser and navigate to:
http://localhost:3000
📚 API Reference
This application uses the Rick and Morty GraphQL API:

Endpoint: https://rickandmortyapi.com/graphql
Documentation: https://rickandmortyapi.com/documentation

🛠️ Available Scripts

npm run dev - Start development server
npm run build - Build for production
npm start - Start production server
npm run lint - Run ESLint

📦 Dependencies
Core Dependencies

next - React framework
react - UI library
react-dom - React DOM rendering
@apollo/client - GraphQL client
graphql - GraphQL implementation

Dev Dependencies

typescript - TypeScript compiler
@types/react - React type definitions
@types/node - Node.js type definitions
@types/graphql - GraphQL type definitions
eslint - Code linting
tailwindcss - CSS framework

🎨 Styling
This project uses Tailwind CSS for styling. The configuration is in tailwind.config.ts and global styles are in styles/globals.css.
📝 Next Steps

Create components for displaying episodes
Add character listing and details pages
Implement location exploration
Add search and filter functionality
Implement pagination controls

🤝 Contributing
This is a learning project for ALX GraphQL curriculum.
📄 License
This project is part of the ALX Software Engineering program.