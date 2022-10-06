```js
import react from '@vitejs/plugin-react'; // eslint-disable-line import/no-extraneous-dependencies
import { defineConfig, splitVendorChunkPlugin } from 'vite'; // eslint-disable-line import/no-extraneous-dependencies

require('dotenv').config();

// https://vitejs.dev/config/
export default defineConfig({
    base: `${process.env.PUBLIC_URL || '/rmn-portal'}/`,
    test: {
        globals: true,
        environment: 'jsdom',
        coverage: {
            all: true,
            src: 'src',
            extension: ['.js', '.jsx'],
            include: ['**/*.{js,jsx}'],
            exclude: ['**/*.{spec,stories}.*'],
        },
    },
    server: {
        port: process.env.PORT || 3000,
    },
    build: {
        sourcemap: true, // enabling to auto-upload to rollbar
    },
    plugins: [react(), splitVendorChunkPlugin()],
});
```
