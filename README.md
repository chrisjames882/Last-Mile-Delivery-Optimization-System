# Last-Mile Delivery Optimization System

A comprehensive blockchain-based solution for coordinating delivery routes, tracking packages, and optimizing logistics operations across multiple carriers using Clarity smart contracts.

## 🚀 Overview

This system provides a decentralized platform for last-mile delivery optimization that coordinates multiple carriers, tracks packages in real-time, calculates transparent pricing, and promotes sustainable delivery practices.

### Key Features

- **Multi-Carrier Coordination**: Seamlessly manage deliveries across different carrier networks
- **Real-Time Package Tracking**: Complete visibility from pickup to delivery with handoff management
- **Dynamic Pricing Engine**: Transparent, fair pricing based on distance, weight, urgency, and sustainability factors
- **Sustainable Operations**: Carbon footprint tracking and eco-friendly delivery incentives
- **Vehicle Management**: Optimize fleet utilization and route planning across carriers

## 🏗️ System Architecture

The system consists of five interconnected Clarity smart contracts:

### 1. Delivery Core Contract (`delivery-core.clar`)
Central coordination hub for all delivery operations.

**Key Functions:**
- `register-carrier`: Register new delivery carriers
- `create-delivery-request`: Create new delivery requests
- `assign-delivery-to-carrier`: Assign deliveries to specific carriers
- `update-delivery-status`: Track delivery progress
- `complete-delivery`: Mark deliveries as completed

### 2. Vehicle Management Contract (`vehicle-management.clar`)
Manages vehicle fleets and route optimization.

**Key Functions:**
- `register-vehicle`: Add vehicles to carrier fleets
- `allocate-vehicle-for-deliveries`: Optimize vehicle assignments
- `create-optimized-route`: Generate efficient delivery routes
- `update-vehicle-status`: Track vehicle availability
- `schedule-vehicle-maintenance`: Manage maintenance schedules

### 3. Package Tracking Contract (`package-tracking.clar`)
Provides comprehensive package tracking and handoff management.

**Key Functions:**
- `create-package-tracking`: Initialize package tracking
- `update-package-status`: Real-time status updates
- `initiate-package-handoff`: Secure carrier-to-carrier transfers
- `confirm-delivery`: Digital proof of delivery
- `notify-customer`: Automated customer notifications

### 4. Pricing Engine Contract (`pricing-engine.clar`)
Calculates transparent, dynamic pricing for deliveries.

**Key Functions:**
- `calculate-delivery-price`: Dynamic pricing based on multiple factors
- `apply-eco-pricing`: Sustainable delivery discounts
- `set-carrier-pricing`: Carrier-specific pricing models
- `get-price-breakdown`: Transparent cost itemization

### 5. Sustainability Tracker Contract (`sustainability-tracker.clar`)
Monitors environmental impact and promotes eco-friendly practices.

**Key Functions:**
- `track-environmental-impact`: Calculate carbon footprint
- `create-sustainability-goal`: Set environmental targets
- `purchase-carbon-offset`: Offset carbon emissions
- `get-sustainability-stats`: Environmental reporting

## 🛠️ Installation & Setup

### Prerequisites
- Node.js (v16 or higher)
- Clarinet CLI
- Git

### Installation Steps

1. **Clone the repository**
   \`\`\`bash
   git clone <repository-url>
   cd delivery-optimization
   \`\`\`

2. **Install dependencies**
   \`\`\`bash
   npm install
   \`\`\`

3. **Initialize Clarinet project**
   \`\`\`bash
   clarinet integrate
   \`\`\`

4. **Run tests**
   \`\`\`bash
   npm test
   \`\`\`

5. **Deploy contracts**
   \`\`\`bash
   clarinet deploy --testnet
   \`\`\`

## 📋 Usage Examples

### Register a New Carrier
```clarity
(register-carrier "FastDelivery Inc" (list "downtown" "suburbs") u1000)
