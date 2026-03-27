WEEK 1 – Start the app + UI foundations (required for next meeting)
1) Confirm local setup works
•	Pull/clone the repo and run:
o	cd web
o	npm install
o	npm run dev
2) Start the landing page (simple version)
Based on the project description, create a basic landing page with these sections:
•	Hero section: short headline + short description + a button (example: “Browse Products”)
•	How it works: 3 short steps (Browse → Choose → Review)
•	Featured categories (just cards or buttons for now)
•	Call to action for sellers (example: “Become a Seller”)
Keep it simple (text + basic layout). No final design needed yet.
3) Create page shells (routes) so navigation works
Create basic pages (even placeholders are fine):
•	Home / Landing
•	Catalog (product list)
•	Product detail
•	Seller profile (public)
•	Login
•	Register
•	Seller dashboard shell (seller-only later)
4) Basic accessibility from day one
•	Every input has a label
•	Focus outline visible for keyboard users
•	Images have alt text (even placeholder)
•	Headings use correct order (H1, H2, H3)
Week 1 “Done” checklist (frontend)
•	Landing page started and visible on Vercel preview
•	All main pages exist and you can click through them
•	Uses mock data where needed (no API required yet)

WEEK 2 – Catalog + Product pages + Seller UI (connect when possible)
Week 2 is about building the main shopping experience.
1) Catalog page (product list)
Build a clean product list view:
•	Product cards should show:
o	image
o	title
o	price
o	category
o	rating (optional for now)
•	Add “No products found” empty state
•	Add loading state (simple text like “Loading…” is fine)
2) Filters UI (category + price range)
Add filter controls:
•	Category dropdown/select
•	Min price / Max price inputs
•	“Clear filters” button
For now it can filter mock data locally. Later it will call the API.
3) Product detail page
Show:
•	product image
•	title
•	price
•	category
•	description
•	seller link (go to seller profile page)
•	section for reviews (can be placeholder until Week 3)
4) Seller dashboard UI (product management)
Create seller pages for managing products:
•	“My Products” list
•	Add product form
•	Edit product form
Start with mock actions first (UI only). When backend is ready, connect to API.
Week 2 “Done” checklist (frontend)
•	Catalog page looks good and works on mobile/desktop
•	Filters exist and work (mock/local)
•	Product detail page shows all main info
•	Seller product forms exist (UI ready)

WEEK 3 – Reviews + Seller profiles + Real API wiring
Week 3 is about finishing required features and connecting to real backend endpoints.
Part A: Seller profile page
Seller profile should show:
•	seller name
•	seller bio/story
•	list of seller’s products (same product cards)
Also add a simple “Seller info” area.
Part B: Reviews & ratings UI
On the product detail page:
•	Show average rating (if available)
•	List reviews (rating + text)
•	Add review form:
o	star rating input (1–5)
o	comment textarea
o	submit button
Part C: Connect UI to backend (when endpoints are ready)
Connect these parts to the API (using docs/api.md):
•	Catalog: fetch products from GET /products
•	Product detail: fetch from GET /products/:id
•	Seller profile: fetch from GET /sellers/:id
•	Seller product management: create/update/delete
•	Reviews: create and list reviews
Important: Keep error messages simple and helpful (example: “Please log in to continue.”)
Week 3 “Done” checklist (frontend)
•	Seller profile works and shows seller products
•	Reviews section works (list + create review)
•	Filters work with the real API (or ready to connect)
•	Main pages are connected to backend

WEEK 4 – Accessibility, SEO, responsiveness, final polish
Week 4 is about quality and making the app “submission-ready”.
1) Accessibility pass (WCAG basics)
Check these on all pages:
•	keyboard navigation works
•	focus outline visible
•	form labels exist and make sense
•	alt text for images
•	good color contrast
•	error messages are readable and clear
2) Responsive polish
Test mobile + tablet + desktop:
•	navigation usable on mobile
•	filters usable on mobile (collapsible if needed)
•	product cards look clean
•	no horizontal scrolling
3) SEO basics + usability
•	Add clear page titles (example: “Catalog – Handcrafted Haven”)
•	Use proper headings (one H1 per page)
•	Add friendly empty states and loading states
Week 4 “Done” checklist (frontend)
•	UI works well on all screen sizes
•	Accessibility basics completed
•	SEO basics added
•	Pages feel consistent and clean

What you should always communicate to the team
When you finish a page or component, share:
•	which route/page is done
•	what data it expects (fields)
•	any missing backend endpoint needed
•	any bugs found during integration
This helps Steven merge cleanly and helps Daniel know what the UI needs.

