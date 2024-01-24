# Rails-SPA-Template
- Template for developing SPA front end with Rails
- `vite`, `React`, `React Router`, `tailwind CSS`, `Jest` are configured
- Backend and frontend are configured on the same server (backend integration)
- HMR compatible

## introduction
1. Create and move working directory  
`mkdir rails-spa`  
`cd rails-spa`

1. Obtain template resources and delete unnecessary files  
*Delete the `.git` linked to the template repository as it is unnecessary.  
`git clone --depth 1 https://github.com/nkwtnb/Rails-SPA-Template . && rm -rf .git`

1. Repository initialization  
`git init`

1. Container creation  
`docker-compose build`

1. Start the container and start working👍  
`docker-compose up [-d]`
- On the backend (Rails) side, if you update the file, it will be applied as is.
- HMR by vite is also enabled on the front end (React) side, so updates are applied as is.

## Production build
1. Compile TypeScript and build vite  
`npm run build`
   1. Execute the build using vite
      - Vite build results are output to `/app/assets/frontend/` and are subject to precompilation.

1. Rails asset precompilation  
`bundle exec rails assets:precompile RAILS_ENV=production`
   1. Execute asset precompilation using Rails
      - Asset precompilation results are output to `public/assets/frontend`