# How to Bring Room Kits Back

When you're ready to feature Room Kits on the live site again, do these steps:

## 1. Remove the noindex meta from `room-kits.html`
At the top of `room-kits.html`, find this line and delete it:
```html
<meta name="robots" content="noindex,nofollow">
```

## 2. Add Room Kits back to the nav menu on all 7 pages
In each of `index.html`, `virtual.html`, `inperson.html`, `gallery.html`, `about.html`, `contact.html`, `reviews.html`:

Find the `<ul class="nav-menu">` block. Add this `<li>` between Home and the next item:
```html
<li><a href="room-kits.html">Room Kits</a></li>
```

## 3. Add Room Kits back to the footer Services list on the same 7 pages
In each page's footer find `<div class="footer-col"><h4>Services</h4><ul>` and add as the FIRST `<li>`:
```html
<li><a href="room-kits.html">Designer Room Kits</a></li>
```

## 4. Restore the homepage (index.html) features
Restore these elements to the homepage:

**Hero — primary CTA back to "$49 Designer Room":**
Find `Book a $297 Design Session →` in the hero and decide whether to swap back. (Recommend: keep $297 as primary, demote kits to a tertiary mention.)

**Stats bar — change $297 back to $49 if desired:**
```html
<div class="proof-stat text-center"><span class="num">$49</span><span class="lbl">Starting Investment</span></div>
```

**Three Paths section — restore the Room Kits card as Path 01:**
The current Path 01 is "Design Direction Session ($297)". To restore, replace it with:
```html
<div class="path-card">
  <div class="path-num">01</div>
  <div class="path-name">Designer Room Kits</div>
  <div class="path-price">From $49 · Instant Download</div>
  <p class="path-desc"><strong style="color:var(--accent);font-size:10px;letter-spacing:.14em;text-transform:uppercase">DIY — You execute it yourself</strong><br><br>Get a complete designer room — built from my real client projects — for 0.3% of what my full-service clients paid. Every product sourced. Every decision made. Implement it on your own timeline.</p>
  <a href="room-kits.html" class="btn btn-sm">Shop Kits →</a>
</div>
```
Then move the Direction Session into a 4-tier offering, or make it a sub-option of Virtual Design.

**Section 9 — Restore the lead magnet section:**
Currently removed. Insert as section 9 (between Why Me and Limited Availability):
```html
<!-- ═══ 9. LEAD MAGNET — $49 ENTRY POINT ═══ -->
<section style="background:var(--ink);padding:var(--sp) var(--px)">
  <div style="max-width:1000px;margin:0 auto;text-align:center">
    <span class="eyebrow" style="color:var(--alt)">Not ready for a full service?</span>
    <h2 class="serif" style="color:var(--white);margin-top:14px;margin-bottom:20px">Start with a <em>$49 designer room.</em></h2>
    <p class="body-lg" style="color:rgba(255,255,255,.7);max-width:680px;margin:0 auto 32px">Real rooms from my real client projects — packaged so you can own every design decision for what most people spend on takeout in a week. Instant download. Your room, professionally designed, in your hands in 10 minutes.</p>
    <div style="display:flex;flex-direction:column;align-items:center;gap:12px;background:rgba(255,255,255,.04);padding:32px 40px;border:1px solid rgba(255,255,255,.08);margin:0 auto 28px;max-width:520px">
      <span style="font-size:10px;letter-spacing:.18em;text-transform:uppercase;color:var(--alt)">What you get for $49</span>
      <div style="font-family:var(--serif);font-size:clamp(32px,5vw,56px);font-weight:400;color:var(--white);line-height:1;text-align:center">A $15,000 room</div>
      <span style="font-size:13px;color:rgba(255,255,255,.5);text-align:center">Paint · 3D rendering · Floor plan · Shopping list · Styling · Implementation guide</span>
    </div>
    <div>
      <a href="room-kits.html" class="btn btn-lg" style="background:var(--accent);color:var(--white);border-color:var(--accent);font-weight:500">Browse Designer Room Kits →</a>
    </div>
  </div>
</section>
```

**Reviews page — Restore the Room Kits service card:**
Find the Designer Room Kits / Direction Session card on `reviews.html` and swap back to:
```html
<div style="background:var(--off);padding:28px 24px;text-align:center">
  <div style="font-size:10px;font-weight:500;letter-spacing:.18em;text-transform:uppercase;color:var(--accent);margin-bottom:10px">DIY</div>
  <div style="font-family:var(--serif);font-size:20px;font-weight:500;color:var(--ink);margin-bottom:8px">Designer Room Kits</div>
  <div style="font-family:var(--serif);font-size:26px;font-weight:400;color:var(--mid);margin-bottom:16px">$49</div>
  <a href="room-kits.html" class="btn btn-sm" style="display:inline-block">Shop Kits →</a>
</div>
```

## 5. Update the credit reassurance bar copy
Currently reads:
> Start with a $297 Design Direction Session. Decide to go bigger? The full $297 comes off a Virtual Room Design...

Restore to:
> Start with a $49 Room Kit. Like what you see? The full $49 comes off your $297 Direction Session. Love that? Your $297 comes off the Virtual Room Design...

## Current state summary

| Element | Status |
|---|---|
| `room-kits.html` page | EXISTS, has noindex meta |
| Homepage hero | $297 Design Session as primary CTA |
| Homepage Three Paths | Direction Session, Virtual Room Design, In-Person |
| Homepage Section 9 lead magnet | REMOVED entirely |
| Nav menu | 7 items (Home / Virtual / In-Person / Gallery / Reviews / About / Work With Me) |
| Footer Services lists | No Room Kits link |
| Reviews page service cards | Direction Session in DIY slot |

When you reinstate, you'll be reverting these.
