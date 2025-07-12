# Simple Book API - Automated Testing Project

## 🚀 Project Overview

This is an API automation testing project developed in collaboration with **Nest Academy** team members. The project focuses on testing a Simple Book API service using modern JavaScript testing frameworks and tools.

### 🎯 Purpose
- Automated testing of Simple Book API endpoints
- Comprehensive API validation using schema validation
- Test reporting and documentation
- Learning API automation best practices

## 👥 Team Collaboration

This project was developed as a collaborative effort with the **Nest Academy** team:

- **Yahyalt** (Yahya) - Contributor
- **marthawege** - Contributor 
- **rifqi23ahmad** (Ah Rifqi Ubaidilah) - Contributor

## 🏗️ Project Structure

```
Nest2project-simplebook/
├── tests/
│ ├── data/ # Test data files
│ │ └── user.data.js
│ ├── helper/ # Helper functions
│ │ └── lib-api.js
│ ├── pages/ # API endpoint definitions
│ │ ├── base.api.js # Base API configuration
│ │ └── simplebook.api.js # Simple Book API methods
│ ├── scenarios/ # Test scenarios
│ │ ├── getAllOrder.test.js
│ │ ├── getBookbyLimit.test.js
│ │ ├── getBookbyType.test.js
│ │ ├── getListofBooks.test.js
│ │ ├── getSingleBook.test.js
│ │ ├── getStatus.test.js
│ │ └── orderBook.test.js
│ └── schema/ # JSON Schema validation
│ ├── getAllOrder.schema.js
│ └── getListofBooks.schema.js
├── reports/ # Test reports (auto-generated)
└── readme.md
```

## 🛠️ Tech Stack

- **Testing Framework**: Mocha & Chai
- **HTTP Client**: Axios
- **Schema Validation**: Chai-JSON-Schema
- **Test Reporting**: Mochawesome
- **Environment Management**: Dotenv
- **Language**: JavaScript (ES6+ Modules)

## 📋 Prerequisites

Before running this project, ensure you have:

- **Node.js** (v14 or higher)
- **npm** or **yarn** package manager
- Access to the Simple Book API endpoint

## 🚀 Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/Yahyalt/Nest2project-simplebook.git
   cd Nest2project-simplebook
   ```

2. **Install dependencies**
   ```bash
   npm install
   # or
   yarn install
   ```

3. **Set up environment variables**
   Create a `.env` file in the root directory:
   ```env
   BASE_URL=https://simple-books-api.glitch.me
   ```

## 🧪 Running Tests

### Run All Tests
```bash
npm run mocha:test
# or
yarn mocha:test
```

### Run Specific Test File
```bash
npx mocha tests/scenarios/getListofBooks.test.js
```

### Generate Test Reports
The test runner automatically generates HTML reports in the `reports/` directory using Mochawesome.

## 📊 Test Scenarios

### 1. **API Status Check** (`getStatus.test.js`)
- Verifies API health and status
- Validates response structure

### 2. **Book Listing** (`getListofBooks.test.js`)
- Tests getting all available books
- Validates book list schema
- Supports filtering by type and limit

### 3. **Single Book Details** (`getSingleBook.test.js`)
- Retrieves specific book information
- Validates individual book data structure

### 4. **Book Filtering** 
- **By Type** (`getBookbyType.test.js`): Filter books by fiction/non-fiction
- **By Limit** (`getBookbyLimit.test.js`): Limit number of returned books

### 5. **Order Management**
- **Create Order** (`orderBook.test.js`): Submit book orders
- **Get All Orders** (`getAllOrder.test.js`): Retrieve order history

## 🔧 Configuration

### Environment Variables
- `BASE_URL`: The base URL of the Simple Book API

### Test Data
Test data is managed in `tests/data/user.data.js`:
```javascript
export const ORDER_BOOK = {
    "bookId": 97,
    "customerName": "YahyaH"
}
```

## 📖 API Endpoints Tested

| Endpoint | Method | Description |
|----------|--------|-------------|
| `/status` | GET | API health check |
| `/books` | GET | Get all books |
| `/books/{id}` | GET | Get single book |
| `/books?type=fiction` | GET | Filter books by type |
| `/books?limit=2` | GET | Limit book results |
| `/orders` | POST | Create new order |
| `/orders` | GET | Get all orders |

## 🎯 Key Features

- **Schema Validation**: Comprehensive JSON schema validation for API responses
- **Modular Design**: Organized code structure with separate concerns
- **Environment Configuration**: Easy configuration management
- **Detailed Reporting**: Rich HTML test reports with Mochawesome
- **Error Handling**: Robust error handling and validation
- **Reusable Components**: Modular API methods and helpers

## 🤝 Contributing

This project was developed as part of a collaborative learning experience with Nest Academy. When contributing:

1. Follow the existing code structure
2. Add appropriate test coverage
3. Update documentation as needed
4. Ensure all tests pass before submitting

## 📝 Learning Outcomes

Through this collaboration, the team gained experience in:
- API automation testing
- JavaScript testing frameworks (Mocha/Chai)
- Schema validation techniques
- Test reporting and documentation
- Git collaboration workflows
- Modern JavaScript (ES6+ modules)

## 🐛 Troubleshooting

### Common Issues:
1. **Package.json syntax error**: Ensure proper JSON formatting
2. **Environment variables**: Verify `.env` file exists and is properly configured
3. **API connectivity**: Check BASE_URL and network connectivity

### Running Tests:
```bash
# Debug mode
npx mocha tests/scenarios --reporter spec

# Verbose output
npx mocha tests/scenarios --reporter json
```

## 📄 License

MIT License - feel free to use this project for educational purposes.

## 🙏 Acknowledgments

Special thanks to **Nest Academy** for providing the collaborative learning environment and guidance throughout this project development.

---

*This project demonstrates practical API testing skills and collaborative development practices learned through the Nest Academy program.*

