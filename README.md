# Next.js 15 App Router Dynamic Route Trailing Slash Error

This repository demonstrates a bug in Next.js 15's App Router where using dynamic routes with a trailing slash results in an error.  The issue arises when navigating to a route with an unnecessary trailing slash, causing a 404 error or unexpected behavior.

## Steps to Reproduce

1. Clone this repository.
2. Install dependencies using `npm install`.
3. Run the development server using `npm run dev`.
4. Navigate to `/product/1/` (note the trailing slash).  This will likely result in an error.
5. Navigate to `/product/1` (without trailing slash). This should work correctly.

## Solution

The solution involves using the `trailingSlash: false` option in the `app` directory's `next.config.js`.  This ensures that trailing slashes are automatically removed and the application functions correctly.  Refer to `bugSolution.js` for the code changes.