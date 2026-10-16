## Category 10/11 relevance: TREK-specific live code-change asks (most likely for you)

These are gold because they're literally about apps like yours — pull these out and rehearse the actual code:This confirms it — plenty of proctors have actually examined **Trekking Management apps** exactly like yours. This is your single best prep resource. Let me organize it by rubric category.

## Category 6-7: Backend theory (highest frequency across all proctors)
From the 954-response frequency count, these dominate:
- **ORM** — "what is ORM" (32×) — explain it via your `Trek.query.filter_by(...)` pattern
- **MVC** — "what is MVC" (19×) — map it to your models.py / templates / app.py split, and be ready to literally point at "show MVC in code"
- **GET vs POST** (13-19×)
- **Template inheritance** (14-19×) — you'll need to explain *why you didn't use it* (your documented deviation)
- **backref vs backpopulates** (8×) — you use `backref='user'`, `backref='trek'` on Booking
- **PUT vs PATCH** (8×), **primary key vs foreign key** (7×), **cascade** (7×), **lazy loading** (5×)

## Category 8-9: Frontend theory
- **Bootstrap** (6×) — directly hits your deviation; rehearse the justification cold
- **CSS priority/specificity** ("order of importance in css", 3×)
- **DOM** (3×)

## Category 10/11: Live code-change — TREK-SPECIFIC asks (use these to drill yourself)

| Ask | Maps to your code |
|---|---|
| "Add a phone number field to trekker registration" | `User` model + `register.html` + register route |
| "Make trek name clickable but not redirect anywhere" | CSS/HTML only — `<a>` with `href="javascript:void(0)"` or no href |
| "Jinja: show treks with price > 3000, highlight them" | `{% if trek.price > 3000 %}` in `trekker/treks.html` |
| "Write SQLAlchemy query: treks with price < 3000" | `Trek.query.filter(Trek.price < 3000).all()` |
| "Show route where admin does CRUD on trek" | Your `admin_create_trek`/`admin_edit_trek`/`admin_delete_trek` |
| "Add validation: admin can't create new trek if already 5 open treks" | `Trek.query.filter_by(status='open').count() >= 5` check before insert |
| "Add height/discount/description field to trek" | Model column + `trek_form.html` + create/edit routes (classic "add a field end-to-end" pattern) |
| "Write route: treks that are 'hard' difficulty and capacity 20" | `Trek.query.filter_by(difficulty_level='Hard', total_seats=20)` |
| "Show overbooking prevention" | Your `if seats < 1 or seats > trek.available_seats` check |
| "Query: users who booked trek in location X" | Join via `Booking.query.join(Trek).filter(Trek.location=='Himalaya')` |
| "Add gender dropdown to trekker registration" | Model column + `<select>` in register.html |
| "Show route for user booking/cancelling trek" | `trekker_book_trek` / `staff_cancel_booking` |
| "Delete button on trek page" | POST form + `admin_delete_trek` (you already have this) |
| "Check starting date not after end date" | You already added this validation — know exactly where |

**Notably repeated pattern across ALL projects (not just trek)**: "add a field end-to-end" (model → form → route → template → show in DB) is by far the single most common live-code-change ask. Practice this exact motion on your own schema — e.g. add `emergency_contact` to `User`.

