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
- Install UI library - chakra (part of dependencies) <https://chakra-ui.com/>
- Prefers to live close to JS for CSS styling
- His linter asked him to do ES6, I'm leaving as 5 for now, ended up copying because something I typed was wrong
- Prefers navigation to be positioned and sized in px
- em for layout, rem for components
