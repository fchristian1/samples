npm init
tsc --init

npm install -D @types/node node tsx typescript

package.json:
...
  "scripts": {
    "test": "node --import tsx --test **/*.test.ts",
    "start": "node --import tsx src/index.ts",
    "dev": "node --import tsx --watch src/index.ts",
    "tdd": "node --import tsx --test --watch src/index.ts",
    "build": "tsc"
  },
...

tsconfig.json:
{
  "compilerOptions": {
    "target": "es2016",
    "module": "commonjs",
    "rootDir": "./src",
    "outDir": "./dist",
    "esModuleInterop": true,
    "forceConsistentCasingInFileNames": true,
    "strict": true,
    "skipLibCheck": true
  }
}
