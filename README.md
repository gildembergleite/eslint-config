## Package @gildembergleite/eslint-config

This package contains ESLint configurations for JavaScript and TypeScript projects with React.js and Next.js. It defines linting rules to help maintain clean and consistent code. Here are the configurations and plugins included in this package:

### ESLint Configurations

The package includes the following configurations:

- Environment:
  - browser: true
  - es2021: true
  - jest: true

- Extended from:
  - 'standard'
  - 'plugin:react/recommended'
  - 'plugin:react-hooks/recommended'
  - 'plugin:prettier/recommended'

- Plugins:
  - 'react'
  - 'jsx-a11y'
  - '@typescript-eslint'
  - '@next/eslint-plugin-next' (for Next.js projects)

### Additional Configurations

The `@gildembergleite/eslint-config` package also includes the following configurations:

- settings.react: { version: 'detect' }
- 'import/parsers':
  - '@typescript-eslint/parser': ['.ts', '.tsx', '.d.ts'],

### Installation and Configuration

To use the `@gildembergleite/eslint-config` package in your project, follow the steps below:

1. Install the package as a dev dependency:
   ```
   npm install --save-dev @gildembergleite/eslint-config
   ```

2. Make sure you have ESLint installed in your project:
   ```
   npm install --save-dev eslint
   ```

3. Create an `.eslintrc.json` file in the root of your project (or update the existing one) and add the following content:

   For Next.js projects:
   ```javascript
   {
     "extends": [
       "@gildembergleite/eslint-config/next",
       "next/core-web-vitals"
     ]
   }
   ```

   For React.js projects:
   ```javascript
   {
     "extends": [
       "@gildembergleite/eslint-config/react"
     ]
   }
   ```

4. You also need to have Prettier installed to leverage the configurations provided by the package. If you don't have Prettier installed yet, run the following command:
   ```
   npm install --save-dev prettier
   ```

5. Great! Now you can run ESLint on your code using the following command:
   ```
   npx eslint .
   ```

   This will run linting on all files in the current directory.

Remember that you can further customize the ESLint configurations as needed to meet the specific requirements of your project.