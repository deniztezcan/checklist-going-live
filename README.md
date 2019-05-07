# A checklist for all projects that are going live

This checklist is used whenever a project is going live at https://deniztezcan.me

## 1. Browserstack tests
- [ ] Desktop: test on latest versions of Chrome, IE/Edge, Firefox, Safari
- [ ] Mobile: test on latest versions of Mobile Safari, Android

## 2. Front end checklist

### Assets
- [ ] Search sources for `http://`. Replace by `https://`
- [ ] Lint (s)css sources

### Scripts
- [ ] Check JS lint errors. Remove all `console.log` lines in scripts
- [ ] Check for console errors

### Page weight
- [ ] Evaluate total weight of at least homepage
- [ ] Open Inspector network/timeline tab to identify heavy assets 
- [ ] Check if heavy assets are cached 

### Audits
- [ ] Use the Chrome DevTools (in incognito mode) and perform a mobile audit (with throttling) to fix common problems.
- [ ] Repeat with a desktop audit.

## 3. Check content (with an open console)
- [ ] Are all strings / images present (and translated)?
- [ ] Does menu/submenu have a correct active state on every page?
- [ ] Are 404, 500 and 503 pages provided? Do they provide useful content like 'back to home', search or a navigation tree?
- [ ] Check all pages for n+1 problems

### Meta
- [ ] Check page titles / descriptions
- [ ] Test Facebook sharing. Provide og-tags if needed
- [ ] Does Favicon load? Pin the tab in Safari to check pinned icon

_Repeat this section for all languages_

### Components
- [ ] Google Maps
    - [ ] API key needed/configured?
    - [ ] Prevent zoom out beyond 1x world
    - [ ] Try clicking on markers
- [ ] Forms: fill out with wrong/right values
- [ ] Video: check with sound on
- [ ] Try subscribing to a newsletter with incorrect & correct email (use correct mail twice to get 'already subscribed' message)
- [ ] Check layout of emails

## 4. Back end checklist
- [ ] Open up `/varenyky`
- [ ] Remove unused modules from main menu 
- [ ] Configure Analytics dashboard
- [ ] Create a new admin and try to log in
- [ ] Try saving article / page / product / etc...
- [ ] Scan database for urls to development domain
- [ ] Check client's logo in header

## 5. Server, DNS & Services
- [ ] Add redirects from old to new pages if necessary.
- [ ] Check SSL certificate health https://www.ssllabs.com/ssltest/ (optional)
- [ ] Check your hostfile to make sure you're looking at the live site
- [ ] Try out visiting `http`, should redirect to `https`
- [ ] Check dns propagation with https://www.whatsmydns.net/
- [ ] Verify Tag Manager / Analytics have been correctly set up

### Google Search Console
- [ ] Submit all www/non-www http/https variations
- [ ] Set up non-www https as the preferred domain 
- [ ] Crawl > Fetch as Google > Submit to index to kickstart index

### Server
- [ ] Are backups enabled?
- [ ] Is the url being monitored?
- [ ] Is the server being monitored by our server-monitor?
