# Blitz.js Application with Vercel Speed Insights

This Blitz.js application has been configured with Vercel Speed Insights to track real-world performance metrics.

## Features

- ✅ Blitz.js 2.0 with Next.js App Router
- ✅ TypeScript support
- ✅ Vercel Speed Insights integration
- ✅ ESLint configuration

## Speed Insights Implementation

Speed Insights has been integrated following Vercel's best practices for Next.js App Router applications:

### Implementation Details

The `SpeedInsights` component from `@vercel/speed-insights/next` has been added to the root layout (`app/layout.tsx`):

```tsx
import { SpeedInsights } from "@vercel/speed-insights/next";

export default function RootLayout({
  children,
}: {
  children: React.ReactNode;
}) {
  return (
    <html lang="en">
      <body>
        {children}
        <SpeedInsights />
      </body>
    </html>
  );
}
```

### What Speed Insights Tracks

Speed Insights automatically collects:
- Core Web Vitals (LCP, FID, CLS)
- First Contentful Paint (FCP)
- Time to First Byte (TTFB)
- Real user performance data

### Enabling Speed Insights on Vercel

1. Deploy this application to Vercel
2. Navigate to your project in the Vercel Dashboard
3. Go to the **Speed Insights** tab
4. Click **Enable**
5. After the next deployment, Speed Insights will be active

The tracking script will be automatically loaded at `/_vercel/speed-insights/script.js`.

### Viewing Your Data

Once enabled and deployed:
1. Visit your Vercel Dashboard
2. Select your project
3. Click the **Speed Insights** tab
4. View real-time performance metrics and trends

## Getting Started

### Development

```bash
npm install
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) to view the application.

### Build

```bash
npm run build
npm start
```

### Linting

```bash
npm run lint
```

## Deployment

Deploy to Vercel:

```bash
npm install -g vercel
vercel deploy
```

Or connect your Git repository to Vercel for automatic deployments.

## Learn More

- [Vercel Speed Insights Documentation](https://vercel.com/docs/speed-insights)
- [Blitz.js Documentation](https://blitzjs.com/docs)
- [Next.js Documentation](https://nextjs.org/docs)
