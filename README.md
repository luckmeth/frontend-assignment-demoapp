# Frontend Assignment Demo App

A comprehensive loan management dashboard built with modern web technologies, featuring borrower pipeline management, AI-powered risk assessment, and broker analytics.

## 🚀 Tech Stack

- **Framework**: Next.js 13 with TypeScript
- **Styling**: Tailwind CSS + ShadCN/UI
- **State Management**: Zustand
- **Forms & Validation**: React Hook Form + Zod
- **Icons**: Lucide React
- **Testing**: Cypress for E2E testing
- **Deployment**: Vercel (Static Export)

## ✨ Features

### Borrower Pipeline Management
- **Multi-status filtering**: Filter borrowers by status (New, In Review, Approved)
- **Interactive cards**: Click to select borrowers with visual feedback
- **Real-time updates**: State management ensures instant UI updates
- **Risk indicators**: Visual risk scores and warning flags

### AI-Powered Risk Assessment
- **Explainable AI**: Expandable accordion showing detailed AI decision factors
- **Risk scoring**: Color-coded risk scores from 0-100
- **Flag categorization**: Success, warning, and info flags with severity levels
- **Visual indicators**: Icons and badges for quick risk assessment

### Comprehensive Borrower Details
- **Contact information**: Email, phone with clickable links
- **Loan summary grid**: Property value, LTV ratio, interest rate, terms
- **Action buttons**: Request docs, send to valuer, approve, escalate
- **Status tracking**: Real-time status updates with color coding

### Broker Analytics & Management
- **Performance metrics**: Total deals, approval rates, processing times
- **Contact integration**: Call, email, and chat buttons
- **Workflow tracking**: Visual onboarding progress with status indicators
- **Settings toggle**: E-Assist feature toggle

### Enterprise-Grade UX
- **Responsive design**: Mobile-first approach with breakpoints
- **Loading states**: Skeleton loading and spinner indicators
- **Error handling**: Toast notifications for user feedback
- **Accessibility**: ARIA labels and keyboard navigation
- **Professional styling**: Consistent spacing, shadows, and animations

## 🛠 Installation & Setup

```bash
# Clone the repository
git clone https://github.com/yourusername/frontend-assignment-demoapp
cd frontend-assignment-demoapp

# Install dependencies
npm install

# Start development server
npm run dev

# Open http://localhost:3000
```

## 📱 Responsive Design

The application features a sophisticated responsive layout:

- **Desktop (>1024px)**: Three-column grid layout
- **Tablet (768-1024px)**: Stacked panels with maintained functionality
- **Mobile (<768px)**: Single-column vertical stack with touch-optimized interactions

## 🧪 Testing

### End-to-End Testing with Cypress

```bash
# Run Cypress tests
npm run cypress:open

# Or run headless
npm run cypress:run
```

Test coverage includes:
- Borrower selection and detail updates
- Filter functionality across different statuses  
- Accordion expand/collapse interactions
- Action button functionality with mock API responses

## 📊 State Management Architecture

The application uses Zustand for predictable state management:

```typescript
interface AppStore {
  // Borrower data
  activeBorrowerId: string | null;
  borrowers: Borrower[];
  activeBorrower: Borrower | null;
  
  // UI state
  filterStatus: 'all' | 'new' | 'in_review' | 'approved';
  isLoading: boolean;
  
  // Actions
  setActiveBorrowerId: (id: string | null) => void;
  // ... other actions
}
```

## 🔄 Mock API Integration

Simulated backend API calls with realistic delays:

- `getBorrowerPipeline()`: Fetches all borrowers
- `getBorrowerDetail(id)`: Gets specific borrower details
- `getBrokerInfo()`: Retrieves broker statistics
- `getOnboardingWorkflow()`: Loads workflow steps

## 🎨 Design System

### Color Palette
- **Primary**: Blue (#3B82F6) for main actions and highlights
- **Success**: Green (#10B981) for positive states and approvals
- **Warning**: Yellow (#F59E0B) for attention and caution
- **Error**: Red (#EF4444) for errors and high-risk items
- **Neutral**: Gray scale for backgrounds and secondary text

### Typography
- **Headings**: Inter font family with consistent line heights
- **Body**: 16px base with 1.5 line height for readability
- **Small text**: 14px for secondary information

### Spacing System
- **Base unit**: 8px spacing system for consistent layouts
- **Components**: 16px (p-4) standard padding
- **Sections**: 24px (gap-6) between major elements

## 🚀 Deployment

The application is configured for static export and can be deployed on any static hosting platform:

```bash
# Build for production
npm run build

# The 'out' directory contains the static files
```

### Vercel Deployment
1. Connect your GitHub repository to Vercel
2. Configure build settings (automatically detected)
3. Deploy with zero configuration

## 📈 Performance Optimizations

- **Static Generation**: Next.js static export for fast loading
- **Image Optimization**: Optimized images with proper sizing
- **Code Splitting**: Automatic code splitting by Next.js
- **Tree Shaking**: Unused code elimination
- **CSS Optimization**: Tailwind CSS purging for minimal bundle size

## 🔧 Development Scripts

```bash
npm run dev          # Start development server
npm run build        # Build for production  
npm run start        # Start production server
npm run lint         # Run ESLint
npm run test         # Run tests
npm run cypress:open # Open Cypress test runner
```

## 📝 Project Structure

```
src/
├── app/                    # Next.js 13 app directory
│   ├── dashboard/         # Dashboard page
│   ├── globals.css        # Global styles
│   ├── layout.tsx         # Root layout
│   └── page.tsx          # Landing page
├── components/            # React components
│   ├── ui/               # ShadCN UI components
│   ├── BorrowerPipeline.tsx
│   ├── BorrowerDetail.tsx
│   ├── BrokerOverview.tsx
│   └── Layout.tsx
├── lib/                  # Utility functions
│   ├── api.ts           # Mock API functions
│   ├── store.ts         # Zustand store
│   └── utils.ts         # Helper functions
└── tests/               # Test files
    └── e2e/            # Cypress E2E tests
```

## 🎯 Key Features Implemented

✅ **Three-panel responsive layout**
✅ **Borrower pipeline with filtering**  
✅ **Interactive borrower selection**
✅ **AI explainability accordion**
✅ **Loan summary dashboard**
✅ **Broker performance analytics**
✅ **Onboarding workflow tracker**
✅ **Mobile-responsive design**
✅ **Loading states and error handling**
✅ **E2E testing with Cypress**
✅ **TypeScript for type safety**
✅ **Professional UI/UX design**

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

**Live Demo**: [https://frontend-assignment-demoapp.vercel.app](https://frontend-assignment-demoapp.vercel.app)

**Repository**: [https://github.com/yourusername/frontend-assignment-demoapp](https://github.com/yourusername/frontend-assignment-demoapp)