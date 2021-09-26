# typescript-for-nodejs

## tsconfig.json
```
{
  "compilerOptions": {
    "target": "es6",
    "module": "commonjs",
    "outDir": "./dist",
    "rootDir": "./src",
    "strict": true,
    "moduleResolution": "node",
    "esModuleInterop": true
  },
  "exclude": [
    "./node_modules"
  ]
}
```

## server.ts
```
import * as dotenv from 'dotenv'
import express, { Request, Response, Application } from 'express'

dotenv.config()

// if (!process.env.PORT) process.exit(1)

const PORT: number = Number(process.env.PORT)

const app: Application = express()

app.use(express.json())

app.get('/', (req: Request, res: Response): void => {
  res.send('Hello Typescript with Node.js!')
})

app.listen(PORT, () => console.log(`Server running here 👉 http://localhost:${PORT}`)
)

```

## dependencies
```
"devDependencies": {
    "@types/cors": "^2.8.12",
    "@types/dotenv": "^8.2.0",
    "@types/express": "^4.17.13",
    "@types/helmet": "^4.0.0",
    "@types/node": "^16.10.1",
    "ts-node": "^10.2.1",
    "ts-node-dev": "^1.1.8",
    "ts-standard": "^10.0.0",
    "typescript": "^4.4.3"
  },
  "dependencies": {
    "cors": "^2.8.5",
    "dotenv": "^10.0.0",
    "express": "^4.17.1",
    "helmet": "^4.6.0"
  }
```
