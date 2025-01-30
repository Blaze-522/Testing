# Tech Quiz Application

## Description
A full-stack tech quiz application that tests developers' knowledge through interactive questions. The application includes comprehensive testing using Cypress for both component and end-to-end testing.

[Link to Walkthrough Video]

## Table of Contents
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Installation](#installation)
- [Testing](#testing)
- [Usage](#usage)
- [Screenshots](#screenshots)
- [Contributing](#contributing)

## Features
- Interactive tech quiz interface
- Random question selection
- Score tracking
- Immediate feedback on answers
- Multiple quiz attempts
- Comprehensive test coverage

## Technologies Used
### Frontend
- React
- TypeScript
- CSS/SCSS
- Vite

### Backend
- Node.js
- Express
- MongoDB

### Testing
- Cypress
- Component Testing
- End-to-End Testing

## Installation

1. Clone the repository:
```bash
git clone [your-repo-link]
```

2. Install dependencies:
```bash
npm install
```

3. Set up environment variables:
```bash
# Rename .env.example to .env
mv .env.example .env
```

4. Start the application:
```bash
npm run dev
```

## Testing

### Running Tests
Execute all tests with:
```bash
npm run test
```

### Component Tests
Located in `cypress/component/Quiz.cy.jsx`:
```typescript
describe('Quiz Component', () => {
  beforeEach(() => {
    cy.mount(<Quiz />)
  })

  it('renders quiz start button', () => {
    cy.get('[data-testid="start-button"]').should('exist')
  })

  it('displays first question after starting', () => {
    cy.get('[data-testid="start-button"]').click()
    cy.get('[data-testid="question"]').should('be.visible')
  })

  it('tracks score correctly', () => {
    // Test implementation
  })
})
```

### End-to-End Tests
Located in `cypress/e2e/quiz.cy.js`:
```typescript
describe('Tech Quiz E2E', () => {
  beforeEach(() => {
    cy.visit('/')
  })

  it('completes full quiz flow', () => {
    cy.get('[data-testid="start-button"]').click()
    // Complete quiz flow test
  })

  it('displays final score', () => {
    // Score display test
  })

  it('allows starting new quiz', () => {
    // New quiz test
  })
})
```

### Test Structure
```
cypress/
├── component/
│   └── Quiz.cy.jsx
├── e2e/
│   └── quiz.cy.js
├── fixtures/
│   └── questions.json
└── tsconfig.json
```

## Project Structure
```
tech-quiz/
├── client/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   └── App.tsx
├── server/
├── cypress/
├── cypress.config.ts
└── package.json
```

## Usage

1. Start the development server:
```bash
npm run dev
```

2. Access the application at `http://localhost:3000`

3. Run tests:
```bash
# Run all tests
npm run test

# Run component tests only
npm run test:component

# Run e2e tests only
npm run test:e2e
```

## Test Coverage
The application includes tests for:
- Quiz component rendering
- Question progression
- Score calculation
- Quiz completion
- New quiz initialization
- Error handling

## Screenshots
[Add screenshots/GIFs of your application and tests running]
- Quiz interface
- Test execution
- Test results

## Deployment
This application can be deployed using your preferred hosting service. Ensure environment variables are properly configured in your deployment environment.

## Contributing
1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Open a Pull Request

## License
[Choose and include an appropriate license]

## Contact
- Developer: [Your Name]
- GitHub: [Your GitHub Profile]
- Email: [Your Email]
