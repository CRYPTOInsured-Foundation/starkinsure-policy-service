# StarkInsure Policy Service

The **StarkInsure Policy Service** is a Laravel microservice that manages insurance policy underwriting, claims processing, and public policy listings for the StarkInsure DeFi platform. Running on port `5002`, it bridges on-chain smart contracts with traditional insurance workflows.

---

## 🔗 API Documentation  
[View API Docs](http://localhost:5002/doc) | [Postman Collection](docs/StarkInsure-Policy-API.postman_collection.json)

---

## ✨ Policy Management Features  
- **Smart Policy Underwriting**:  
  - 🧮 Risk-adjusted premium calculation  
  - 📝 Policy template engine (ERC-721 compatible)  
  - ⚡ Instant policy issuance via StarkNet  
- **Claims Processing**:  
  - 🕵️‍ Automated claim validation  
  - 💸 Payout scheduling (fiat/crypto)  
  - 🛡️ Dispute resolution framework  
- **Public Marketplace**:  
  - 🔍 Policy search with risk filters  
  - 📊 Coverage comparison tools  
  - 🤝 Peer-to-pool underwriting  

---

## 🛠️ Tech Stack  
| Component           | Technology                                                                 |
|---------------------|---------------------------------------------------------------------------|
| Framework           | [Laravel 10](https://laravel.com/docs/10.x)                              |
| Blockchain          | [starknet-php](https://github.com/starknet-php/starknet-php)             |
| Database           | PostgreSQL 15 + [TimescaleDB](https://www.timescale.com/)                |
| Search             | [Meilisearch](https://www.meilisearch.com/) (for policy discovery)       |
| Events             | [Laravel Horizon](https://laravel.com/docs/10.x/horizon) + Webhooks      |

---

## 🚀 Quick Start  

### Prerequisites  
- PHP 8.2+  
- PostgreSQL 15+ with TimescaleDB  
- StarkNet full node access  
- Composer 2.5+  

### Installation  
1. **Clone the repo**:  
   ```bash
   git clone https://github.com/CRYPTOInsured-Foundation/starkinsure-policy-service.git
   cd starkinsure-policy-service
   ```
2. Install dependencies:
   ```bash
   composer install
   ```
3. Configure environment:
   ```bash
   cp .env.example .env
   ```
4. Generate keys:
   ```bash
   php artisan key:generate
   php artisan jwt:secret
   ```
5. Run migrations:
   ```bash
   php artisan migrate --seed
   ```
6. Start the service:
   ```bash
   php artisan serve --port=5002
   ```
## 🤝 Contributing

1. Fork the repository
2. Create your feature branch:
```bash
git checkout -b feat/your-feature
```
3. Commit changes following Conventional Commits
4. Push to the branch
5. Open a Pull Request
