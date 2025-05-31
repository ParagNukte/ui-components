
```markdown
# My UI Library

My UI Library is a React-based component library built using Tailwind CSS and TypeScript. The project is organized as a monorepo with two main packages:
- **ui-components:** The core library containing reusable React components, utilities, and tests.
- **docs:** A Next.js documentation and demo site that showcases the components in action.

## Repository Structure

```plaintext
my-ui-library/
├── package.json           // Root workspace configuration
├── tsconfig.json          // Global TypeScript config (optional)
├── README.md              // Project overview and workflow
└── packages/
    ├── ui-components/     // Core component library
    │   ├── package.json
    │   ├── tsconfig.json
    │   ├── tailwind.config.js
    │   ├── postcss.config.js
    │   ├── src/
    │   │   ├── components/  // React components (e.g., Button.tsx, Modal.tsx)
    │   │   ├── utils/       // Utility functions (e.g., cn.ts for class merging)
    │   │   └── styles/      // Global Tailwind CSS styles (optional)
    │   └── tests/           // Tests using Jest & React Testing Library
    └── docs/               // Next.js based demo & documentation site
        ├── package.json
        ├── tsconfig.json
        ├── next.config.js
        ├── tailwind.config.js
        ├── postcss.config.js
        ├── public/          // Static assets (images, fonts, etc.)
        ├── pages/           // Documentation pages (_app.tsx, index.tsx, etc.)
        └── components/      // Demo site specific components (e.g., Layout.tsx)
```
## Workflow

1. **Setup & Installation:**
   - Clone the repository.
   - In the root directory, run `npm install` (or your favorite package manager) to install all dependencies for both packages.

2. **Development:**
   - **UI Components:**  
     Develop your reusable components in `packages/ui-components/src/components`. Use the utility functions in `packages/ui-components/src/utils` (e.g., the `cn` function for merging Tailwind classes) to ensure clean and conflict-free styling.
   - **Styles & Configuration:**  
     Update Tailwind CSS settings in the provided configuration files (`tailwind.config.js` and `postcss.config.js`).
   - **Documentation:**  
     Use the Next.js demo in `packages/docs` to document and showcase your components in real-time. Run the development server from within the docs folder via `npm run dev`.

3. **Testing:**
   - Write unit and integration tests with Jest and React Testing Library in the `__tests__` folder of the `ui-components` package.
   - Run tests using `npm test` to ensure that all components behave as expected.

4. **Building & Bundling:**
   - Build your component library using Vite (or Tsup) from within `packages/ui-components` by running `npm run build`.
   - This step bundles your code, generates type declarations, and prepares the package for publishing.

5. **Publishing:**
   - Once the library is built and validated locally (using `npm pack` in a separate test project), update the relevant package fields (`main`, `module`, `types`, `peerDependencies`) in `packages/ui-components/package.json`.
   - Log in to npm and publish the package using `npm publish`.
   - The docs site can be deployed separately for online documentation.

## Contributing

- Please adhere to the code style and commit guidelines.
- Add tests alongside new components or features.
- Update the documentation in the docs site accordingly.

## License

This project is licensed under the MIT License.
```
