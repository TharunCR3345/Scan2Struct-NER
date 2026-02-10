# Scan2Struct-NER

A modern web application for automated invoice scanning and structured data extraction using Named Entity Recognition (NER). Built with React and TypeScript, this tool processes invoice images and PDFs to extract key information such as vendor details, amounts, dates, and line items.

## Features

- **Invoice Upload**: Support for multiple file formats including images (JPG, PNG) and PDFs
- **OCR Processing**: Advanced optical character recognition for text extraction
- **Named Entity Recognition**: Intelligent extraction of structured data from invoices
- **Real-time Processing**: Live processing status with progress indicators
- **Data Visualization**: Interactive charts and analytics for processed invoices
- **User Authentication**: Secure user management with Supabase
- **Export Capabilities**: Export extracted data in JSON and CSV formats
- **History Tracking**: Maintain processing history and results
- **Responsive Design**: Mobile-friendly interface built with Tailwind CSS

## Tech Stack

- **Frontend**: React 18, TypeScript, Vite
- **UI Components**: shadcn/ui, Radix UI, Tailwind CSS
- **Backend**: Supabase (Database, Auth, Edge Functions)
- **State Management**: TanStack Query (React Query)
- **Charts**: Recharts
- **PDF Processing**: PDF.js
- **Testing**: Vitest, Testing Library
- **Build Tools**: Vite, ESLint, TypeScript

## Prerequisites

- Node.js (version 18 or higher)
- npm or yarn package manager

## Installation

1. **Clone the repository**
   ```bash
   git clone <YOUR_GIT_URL>
   cd Scan2Struct-NER
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Environment Setup**
   - Copy `.env.example` to `.env.local` and configure your Supabase credentials
   - Set up your Supabase project and database schema

4. **Start the development server**
   ```bash
   npm run dev
   ```

   The application will be available at `http://localhost:5173`

## Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run build:dev` - Build for development
- `npm run preview` - Preview production build
- `npm run lint` - Run ESLint
- `npm run test` - Run tests once
- `npm run test:watch` - Run tests in watch mode

## Project Structure

```
Scan2Struct-NER/
├── src/
│   ├── components/          # Reusable UI components
│   │   ├── ui/             # shadcn/ui components
│   │   └── ...             # Feature-specific components
│   ├── pages/              # Page components
│   ├── hooks/              # Custom React hooks
│   ├── lib/                # Utility functions
│   ├── integrations/       # External service integrations
│   └── test/               # Test files
├── supabase/
│   ├── functions/          # Edge functions
│   └── migrations/         # Database migrations
├── docs/                   # Documentation
└── public/                 # Static assets
```

## Usage

1. **Authentication**: Sign up or log in to access the application
2. **Upload Invoices**: Drag and drop or select invoice files to upload
3. **Process Documents**: The system will automatically extract text and structure data
4. **Review Results**: View extracted entities in the results panel
5. **Export Data**: Download processed data in your preferred format
6. **Analytics**: Monitor processing statistics and performance metrics

## API Integration

The application integrates with Supabase Edge Functions for server-side processing:

- `extract-invoice`: Handles OCR and NER processing of uploaded invoices
- Real-time updates via Supabase subscriptions
- Secure file storage and processing

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## Testing

Run the test suite with:
```bash
npm run test
```

For watch mode:
```bash
npm run test:watch
```

## Deployment

Build the application for production:
```bash
npm run build
```

The built files will be in the `dist/` directory, ready for deployment to your preferred hosting platform.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Support

For support and questions, please open an issue in the GitHub repository.
