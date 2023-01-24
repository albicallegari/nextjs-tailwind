# Next.js - Tailwind
Build a Single page application using Next.js and Tailwind, deploying it on Vercel

# Next.js App
This project was bootstrapped with [Create next App](https://nextjs.org/learn/basics/create-nextjs-app/setup).
### `npx create-next-app nextjs-blog`

## SWR
The team behind Next.js has created a React hook for data fetching called [SWR](https://swr.vercel.app/). We highly recommend it if you’re fetching data on the client side. It handles caching, revalidation, focus tracking, refetching on interval, and more. We won’t cover the details here, but here’s an example usage:
```
import useSWR from 'swr';
function Profile() {
  const { data, error } = useSWR('/api/user', fetch);

  if (error) return <div>failed to load</div>;
  if (!data) return <div>loading...</div>;
  return <div>hello {data.name}!</div>;
}
```