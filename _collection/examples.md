---
layout: page
title: "E-Cart Prototype"
summary: "Stand-alone shop page for albums"
img: "/public/images/e-store-prototype.jpg"
tag: [prototype, wireframe]
---

_The following is a collection of notes and sketches for a micro-site store prototype._
-----------------------------------------------------------------------------------

---

I am currently working with a performer/musician/public speaker, that would like to extend the “paypal buy” button option he has on his site into a custom store.

Client wants this store to have a preview player for songs and the option to sell digital downloads.

Summary
-------

**Physical and digital sales**

Currently he sells physical items and wants a digital download option.

Must be:

* Full album downloads
* Value bundle package options
* Promotional sale codes

Current site has:

* Paypal button

New Site Possibilities
----------------------

**Cart**

The option for the cart will be cashmusic.js. I have worked with the developer of [cashmusic.org](https://cashmusic.org) on his project. Using this as the cart will give us access to support if needed and has no additional fees. It also includes all of the options requested.

**Cashmusic.js**

* Paypal integration
* Download code capabilities
* Physical/digital options
* Connects to **amazon storage** or **Google drive** for digital items
* Hosted library management back end
* Embedded, custom design

**Site**

The site will be a static **liquid template** using a **jekyll** based design hosted on our Amazon server.
The site will be designed to look like the main site with navigation that will like back to all of section on that main site. We will host it on a subdomain like store.example.com

---

Wireframes
==========

_Working out the structure - How the pages will be put together_
--------------------------------------------------------------


Store Landing page
------------------

![store home wireframe example](/public/images/wireframe-store-landing-page.jpg)

**Components for Store Home Page**

1. Header
  * Match current site
2. Navigation
  * Similar links as website
3. Feature component
  * Product image - left
  * Description - right
  * Showcases current release
  * Component links to release album page
4. Card components
  * Product image - top
  * Title and short description
  * Cards will display two per row
  * Card rows will repeat as many times as needed
  * Clicking cards will open release album page
5. Parallax window
  * Faded background image
  * Text - information and more about the project
6. Second feature component
  * This is the same as the top component featuring bundle package
7. Footer
  * Information and design of footer will match the main site


Album Page
----------

![store album page wireframe example](/public/images/wireframe-album-page.jpg)

**Components for album pages**

1. Navigation
  * Same as store landing page
2. Feature component
  * On album pages the feature component will be used to display the album connected to that page
  * Cashmusic.js cart buttons are below the album description
3. Album player
  * Start/stop button
  * Playlist
  * Clicking a song title will also play song
  * Album description displayed to right of player
  * Cashmusic.js buttons will also display below player
4. Card components
  * Same as store landing page
  * Will display the other available albums
5. Footer
  * Information and design of footer will match the main site

---

Prototypes
==========

_Working example based on approved wireframes_
----------------------------------------------

![prototype screenshot](/public/images/e-store-prototype-large.png)

Prototype example
-----------------

To start the discussion a prototype was made to confirm everything discussed from the wireframe session worked on the page and create a dialog with the client.

This is to check that the components meet the expectations before implementing any design.

**Examples created**

* Store home page - [https://goo.gl/pEXq9p](https://goo.gl/pEXq9p)
* Album preview/buy page - [https://goo.gl/XKj0I8](https://goo.gl/XKj0I8)

---

Next steps
----------
Color branding and image sources artwork for approval



Github code repository for project - https://goo.gl/sDzbCG
