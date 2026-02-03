# Social Autonomies

Downlaod Here -> https://github.com/Too-Many-Ideas/socialautonomies

AI-driven X automation platform for creating intelligent agents that can post, engage, and analyze performance automatically. The idea is to allow users to organically grow their X accounts. 


## Features

- AI-powered tweet generation
- Analytics and performance tracking  
- Automated engagement and replies
- Tweet scheduling
- Subscription management

## 📱 Platform Overview

### Core Features
![Platform Features](/public/feature.png)
*Organic growth, intelligent scheduling, and smart content generation*

### Analytics Dashboard
![Analytics Dashboard](/public/analytics.png)
*Real-time monitoring of your agent's tweeting performance and engagement metrics*

![Tweet Analytics](/public/tweets.png)
*Detailed tweet analytics with success rates and activity tracking*

### Pricing Plans
![Pricing Structure](/public/oricing.png)
*Flexible pricing tiers for different account sizes and needs*

### User Profile & Usage
![User Profile](/public/profile.png)
*Track your subscription plan and usage limits in real-time*


This project is open source under the MIT license - you're free to use, modify, and distribute it however you like. No limits imposed. 

## Quick Start

1. **Clone and install**
   ```bash
   git clone https://github.com/Too-Many-Ideas/socialautonomies
   cd socialautonomies
   npm install
   ```

2. **Environment setup**
   ```bash
   cp env.example .env
   # Fill in your API keys (Openrouter, Twitter, Supabase, Stripe)
   ```

3. **Database setup**
   ```bash
   npx prisma generate
   npx prisma migrate deploy
   npx prisma db seed
   ```

4. **Run**
   ```bash
   npm run dev
   ```

## Configuration

Configure your own subscription plans by editing `prisma/seed.ts`:

### 1. Create Stripe Products
1. Go to your [Stripe Dashboard](https://dashboard.stripe.com/products)
2. Create products for each plan (Basic, Standard, Expert)
3. Copy the price IDs

### 2. Update Seed File
```typescript
{
  planName: 'Basic',
  price: 9.99, // Your pricing
  stripePriceId: 'price_your_stripe_id', // Your Stripe price ID
  maxTweetsPerAgent: 15, // Your limits
  maxRepliesPerAgent: 50,
  // ... other limits
}
```

### 3. Run Database Seed
```bash
npx prisma db seed
```


## Tech Stack

- **Frontend**: Next.js 14, TypeScript, Tailwind CSS
- **Auth**: Supabase
- **Payments**: Stripe

## Environment Variables

See `env.example` for all required configuration.

### Integration Opportunities
These libraries can be easily integrated into Social Autonomies to extend functionality:
- Enhanced scraping capabilities
- Alternative authentication methods  



## License

MIT - see [LICENSE](LICENSE) for details.

## Contributing

Fork the repository and submit pull requests for any improvements! 