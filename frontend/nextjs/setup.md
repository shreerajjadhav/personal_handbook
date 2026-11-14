## **New project setup**

1. **Create project**
   ```
   npx create-next-app@latest frontend --typescript --tailwind --eslint --app --src-dir --use-npm --import-alias "@/*"
   ```
2. **Enter frontend directory**
   ```
   cd frontend
   ```
3. **Install animation library**
   ```
   npm install motion
   ```
4. **Start development server**
   ```
   npm run dev
   ```
5. **Start developing**

   Edit files, save, and see changes in the browser.

## **Existing project workflow**
```
cd frontend
npm run dev
```
add in google localhost:3000
and the official link will be http://localhost:3000/
That's all you need for everyday development.

## **5. One more thing: production verification**

When you want to verify that your project can build for production:
```
npm run build
```

To run that production build:
```
npm run start
```

Remember, `npm run start` requires a successful production build first. this thing we will add inside the next js setup now give the good version of it to add it inside the setup file
