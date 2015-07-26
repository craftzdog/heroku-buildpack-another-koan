# Heroku buildpack for Another koan

This is a Heroku buildpack for web applications of [Another Koan](/noradaiko/another-koan) stack.

## Usage

The `bin/compile` script run webpack with the default configuration file (`production.webpack.config.js` in your main directory). To use the buildpack:

1. Use the [multi buildpack](https://github.com/ddollar/heroku-buildpack-multi):

   ```bash
   $ heroku config:set BUILDPACK_URL=https://github.com/ddollar/heroku-buildpack-multi
   ```

2. Configure your `.buildpacks` file:

   ```
   https://github.com/heroku/heroku-buildpack-nodejs
   https://github.com/noradaiko/heroku-buildpack-another-koan
   ```

3. Deploy to Heroku.
