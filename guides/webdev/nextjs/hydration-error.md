# Hydration Error

[Documentation](https://nextjs.org/docs/messages/react-hydration-error)

Hydration Error can be a few things, but it typically means the virtual DOM that is rendered from the server **does not match** the DOM rendered to the client.

This generally happens when there are **interactive(client)** components that are not being **hydrated(updated)** by the server.

The simplest way to fix most hydration errors is to add **'use client'** to the top of the file on interactive components, 
but this doesnt always work when the component can be opened from multiple sources like modals or pop ups.

A fix that works is forcing the mounting/dismounting of the interactive component using useState and useEffect:
```typescript
const [isMounted,setIsMounted] = useState(false);

  useEffect(() => {
    setIsMounted(true);
  },[])

  if(!isMounted) {
    return null;
  }
```

