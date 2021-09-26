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
import express, { Request, Response, Application} from 'express'

const app:Application = express()

const PORT = process.env.PORT || 8000

app.get('/', (req:Request, res:Response): void => {
  res.send("Hello Typescript with Node.js!")
})

app.listen(PORT, () => console.log(`⚡️[server]: Server running here 👉 http://localhost:${PORT}`)
)
```

## dependencies
```
"devDependencies": {
    "@types/express": "^4.17.13",
    "@types/node": "^16.10.1",
    "ts-node": "^10.2.1",
    "ts-node-dev": "^1.1.8",
    "ts-standard": "^10.0.0",
    "typescript": "^4.4.3"
  },
  "dependencies": {
    "express": "^4.17.1"
  }
```
