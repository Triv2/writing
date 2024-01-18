 # Debugging Clerk for Next.js 14 App Router

[Documentation](https://clerk.com/docs/quickstarts/nextjs)

*Upgrade node version to 18.16 LTS or more recent, prior node versions have reported clerk components not rendering correctly.*

Reset your system time to sync it with clerk by turning off automatic updates and turning it back on.

##Setup

1. Clerk NPM package has been installed using:
```coffeescript 
npm install @clerk/nextjs
```
2. Environment keys are set in the .env file:
```prolog
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=your_publishable_key
CLERK_SECRET_KEY=your_secret_key
```
3. ClerkProvider is imported and mounted in /app/layout.tsx file:
```typescript
import { ClerkProvider } from '@clerk/nextjs'
 
export const metadata = {
  title: 'Next.js 13 with Clerk',
}
 
export default function RootLayout({
  children,
}: {
  children: React.ReactNode
}) {
  return (
    <ClerkProvider>
      <html lang="en">
        <body>{children}</body>
      </html>
    </ClerkProvider>
  )
}
```
4. Middleware.ts file is setup:
```typescript
import { authMiddleware } from "@clerk/nextjs";

export default authMiddleware({});
 
export const config = {
      matcher: ['/((?!.+\\.[\\w]+$|_next).*)', '/', '/(api|trpc)(.*)'],
};
 ```
5. Sign-in and sign-up pages are setup correct with correct routes:
```typescript
    /app/sign-up/[[…sign-up]]/page.tsx

import { SignUp } from "@clerk/nextjs";
 
export default function Page() {
  return <SignUp />;
}
```
```typescript
    /app/sign-in/[[…sign-in]]/page.tsx

import { SignIn } from "@clerk/nextjs";
 
export default function Page() {
  return <SignIn />;
}
```
6. Paths for your environment variables in your .env file:
```prolog
NEXT_PUBLIC_CLERK_SIGN_IN_URL=/sign-in
NEXT_PUBLIC_CLERK_SIGN_UP_URL=/sign-up
NEXT_PUBLIC_CLERK_AFTER_SIGN_IN_URL=/
NEXT_PUBLIC_CLERK_AFTER_SIGN_UP_URL=/
```
If all that fails, contact Clerk support here:
https://discord.com/invite/b5rXHjAg7A

## Additional Notes
<p>Sometimes browser extensions can cause issues with Clerk as well, turn them off temporarily until you get Clerk running, then turn them back on one by one to see if any of them are causing errors.</p>

<p>Had an error with clerk components not rendering. Saw my date/time hadn't be resynced in a week. Even though clerk was not giving that error, re-syncing the date/time in windows fixed the error.
To fix this go into your windows date/time settings and hit "Sync now".</p>

