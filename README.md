# TakeProfit API Testing Project

## Overview
This project contains API tests for the TakeProfit platform - a cryptocurrency trading bot creation and management system. The test suite is implemented using Postman and covers all major functionality of the platform.

## Project Structure

### Environment Configuration
- Base URL: `https://takeprofit.tech`
- Environment variables file: `TakeProfit.postman_environment.json`
- Collection file: `TakeProfitProject.postman_collection.json`

### Test Groups

1. **Authentication Module**
   - Registration (Positive/Negative scenarios)
   - Login functionality
   - Token management

2. **User Management**
   - User profile operations
   - Email updates
   - Password management
   - Account deletion

3. **Exchange Management**
   - Exchange listing
   - Exchange connections
   - Portfolio management
   - Exchange configuration

4. **Trading Operations**
   - Candle data retrieval
   - Symbol information
   - Interval management
   - Market data validation

5. **Bot Management**
   - Bot creation
   - Bot configuration
   - Bot status management
   - Bot deletion
   - Trading simulation

### Test Coverage

Total test cases: 419
- Positive scenarios: ~70%
- Negative scenarios: ~30%

Test types:
- Functional tests
- Authorization tests
- Data validation tests
- Error handling tests
- Performance tests (response time validation)

## Test Execution

### Prerequisites
- Postman version 11.21.0 or higher
- Valid API access
- Environment configuration set up

### Environment Variables
Key variables required:
- `baseUrl`
- `accessToken`
- `loginEmail`
- `password`
- Various API keys and tokens for different operations

### Running Tests
1. Import the collection and environment files
2. Set up the environment variables
3. Run the collection using Postman Collection Runner

## API Endpoints

### Authentication
- POST `/api/v1/register` - User registration
- POST `/api/v1/login` - User login

### User Management
- GET `/api/v1/users` - Get user information
- PATCH `/api/v1/users` - Update user data
- DELETE `/api/v1/users` - Delete account
- PATCH `/api/v1/users/password` - Update password

### Exchange Operations
- GET `/api/v1/exchanges` - List exchanges
- POST `/api/v1/exchanges` - Add new exchange
- GET `/api/v1/exchanges/{id}` - Get exchange details
- PATCH `/api/v1/exchanges/{id}` - Update exchange
- DELETE `/api/v1/exchanges/{id}` - Remove exchange

### Trading Operations
- GET `/api/v1/candles/{symbol}` - Get candle data
- GET `/api/v1/symbols` - Get trading symbols
- GET `/api/v1/intervals` - Get trading intervals

### Bot Management
- GET `/api/v1/bots` - List all bots
- POST `/api/v1/bots` - Create new bot
- GET `/api/v1/bots/{id}` - Get bot details
- PATCH `/api/v1/bots/{id}` - Update bot
- DELETE `/api/v1/bots/{id}` - Delete bot
- POST `/api/v1/bots/simulations` - Run bot simulation

## Test Validation

Each test validates:
- Response status codes
- Response body structure
- Data integrity
- Response time (threshold: 2000ms)
- Authorization requirements
- Error handling

## Known Limitations
- Some endpoints have higher response times under load
- Simulation endpoints may occasionally exceed timeout thresholds
- CSV handling requires additional error checking

## Reporting
Test execution generates detailed reports including:
- Test pass/fail statistics
- Response times
- Error details
- Coverage metrics

## Best Practices
- Token refresh handling
- Proper error validation
- Response schema validation
- Environment isolation
- Consistent data cleanup

## Support
For questions about the test suite, contact the QA team or project maintainers.
