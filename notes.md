# Frontend Masters - Full Stack - Scott Moss

## Info

- Netflix most recently, now is a full-time investor!
- Hands-on project: build a Spotify clone

## Dependencies

- Low barrier to entry for this course - all you need is Node on your machine!
- React, Postgres, Prisma, Next.js, React, Vercel, Heroku, etc...
- Notes: <https://tinted-gym-f99.notion.site/Fullstack-course-notes-Students-3202660c315b438aba6c1ae051963572>
- We are going to build from scratch - will reference other repo

## Build

- Use npx
- Have gone back to having backend and frontend in same app, but deployed differently
- Renamed eslint to js
- Added Babel file
- Copy/pasted dependencies and dev dependencies
- Renamed app and index with tsx
- Overwrote tsconfig with provided sample after changing items above
- Adding underscore on app blocks it from creating a route, everything else will be a route
- May need to substitue `bcryptjs` for Mac

## Design

- Break down of layout - ALWAYS START HERE
  - Left nav and play bar at bottom - sit on top of page and don't change!
  - Main area is where things change
  - Note what things are reusable and how those modules change
  - This is often an interview question
- Install UI library - chakra (part of dependencies) <https://chakra-ui.com/> => more open source!!; also recommends Evergreen UI <https://evergreen.segment.com/>; Tailwind makes you pay and you still need to write your own components
- Prefers to live close to JS for CSS styling
- His linter asked him to do ES6, I'm leaving as 5 for now, ended up copying because something I typed was wrong
- Prefers navigation to be positioned and sized in px
- em for layout, rem for components
- He does like building out the visible stuff and mock in until data is truly needed
- Will add his own TSLint rule to keep components under 50 lines

## Data

- Using Prisma <https://www.prisma.io/>
- Find Prisma extension for VS Code
- Run `npx prisma init`
- Go to Heroku and add a new app, add 2 postgress (Heroku) dbs; use URIs in `.env` file
- Need to capture `.env` file settings
- Postgres needs a "shadow" db - make sure your user has permission to create dbs or do this Heroku version
- Check lines 10-13 on settings.json to put on Mac (how to get to JSON file)
- push vs migration for Prisma => check into this
- Commands

```javascript
npx prisma db push
npx prisma migrate dev // actual application of changes, will walk you through the changes
npx prisma migrate reset // truncates data
npx prisma db seed
npx prisma studio
npx prisma generate // (new client)
```

## API

- Files in pages/api are routes

## Day 2

- Review Typescript checking of components from Scott's code
- Recommends keeping up Inspect to do hard reloads
- Used kkinnea@gmail.com/abc123 and bob@dobbs.com/xyz987
- Study validateRoute for structure in me.ts
- Study service vs edge functions; service spins up when needed, edge sits on edge of CDN and is middleware between API service functions and client; review Nextjs site for examples
- Review NextAuth for using OAuth; overkill for simple email/pass
- `_middleware` file will execute ahead of other pages in dir; 1 level only; can put one in API as well

## Day 3

- Look inito Snowpack and Pika instead of webpack?
- Always use CanIUse!!
- Testing: use Jest for unit, Cypress for end-to-end, Supertest or Superagent for API; see Next website
- CI: Use GitHub Actions for build testing; can also use Travis CI, Circle CI, Jenkins for non-personal work
- Next will build static pages for any pages that don't have `getServerSideProps` by default; opted in by default
