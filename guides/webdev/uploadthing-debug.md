# Uploadthing - Debug Guide

Documentation: https://docs.uploadthing.com/nextjs/appdir

*First update your node version to 18.16 or higher. Users with older versions of node have reported issues with newer versions of uploadthing.*

## Uploadthing File Requirements

1. `/app/api/uploadthing/core.ts`
>Establishes a FileRouter, similar to an endpoint.

![image](https://github.com/Triv2/writing/assets/126743500/8ca3720c-a251-4584-821f-ec3bf908a3ae)



2. `/app/api/uploadthing/route.ts` 
>Creates an API route for the FileRouter to use.*

![image](https://github.com/Triv2/writing/assets/126743500/3a7844a9-b1b6-467f-9513-df38de01741d)


3. `/lib/uploadthing.ts`
>Imports the pre-made components from uploadthing.

![image](https://github.com/Triv2/writing/assets/126743500/fb105c26-b5cc-41e0-913d-20020f37ef84)


4. `/components/file-upload.tsx`
>Custom component used for file uploads.

![image](https://github.com/Triv2/writing/assets/126743500/f6ee0542-99a0-4789-af2b-94f0327dc0cb)


5. `middleware.ts`
>Gives uploadthing access through authentication.

![image](https://github.com/Triv2/writing/assets/126743500/69e5cc20-ef68-4ab2-a80e-8408625c16b1)

```typescript

export default authMiddleware({
  publicRoutes: ["/api/uploadthing"]
});
```

6. `next.config.js`
> Setups up the project configuration to interact with uploadthing servers.

![image](https://github.com/Triv2/writing/assets/126743500/7c09ab58-6681-42df-a979-4f71f32db6f4)

```typescript
images: {
    domains: [
      "uploadthing.com",
      "utfs.io"
    ]
  }
```

7. `.env`
>This connects your project to your uploadthing server.

```prolog
UPLOADTHING_SECRET= your_uploadthing_secret
UPLOADTHING_APP_ID= your_uploadthing_app_id
```

8. `/app/globals.css`
>Adds uploadthing component CSS styles to the project.


```css
@import "~@uploadthing/react/styles.css";
```


**Component Implementation**
>This is a basic component for implementation. Endpoint must match the file-upload.tsx endpoint.

```typescript
<FileUpload 
  endpoint='imageUploader' 
  value={field.value} 
  onChange={field.onChange}
/>
```



