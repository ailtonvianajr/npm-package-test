# npm-package-test

## Steps
1. Start npm:
   ```
   npm init
   ```
   or, start npm for a organization
   ```
   npm init --scope=@org-name
   ```
2. Install typescript:
   ```
   npm i typescript -D
   ```
3. Run typescript with npx:
   ```
   npx tsc --init
   ```
4. Modify "tsconfig.json" file to:
   ```
   {
     "compilerOptions": {
       "module": "commonjs",                     /* Specify module code generation: 'none', 'commonjs', 'amd', 'system', 'umd', 'es2015', 'es2020', or 'ESNext'. */
       "declaration": true,                      /* Generates corresponding '.d.ts' file. */
       "outDir": "dist",                         /* Redirect output structure to the directory. */
       "strict": true,                           /* Enable all strict type-checking options. */
       "esModuleInterop": true,                  /* Enables emit interoperability between CommonJS and ES Modules via creation of namespace objects for all imports. Implies 'allowSyntheticDefaultImports'. */
       "forceConsistentCasingInFileNames": true  /* Disallow inconsistently-cased references to the same file. */
     },
     "include": [
       "src"
     ]
   }
   ```
5. Create 3 folders at the root of project: dist, example and src
6. Install ts-node:
   ```
   npm i ts-node -D
   ```
7. Create build and dev scripts at "package.json" and set types and main to dist folder:
   ```
   "main": "dist/index.js",
   "types": "dist",
   "scripts": {
     "build": "tsc -p .",
     "dev": "ts-node example/example.ts"
   },
   ```
