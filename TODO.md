#html
✔ titles
✔- Fix word break
- texts
✔- Different aligns
✔ Specific texts
✔- strong + b
✔- em + i
✔- a href
✔- div
✔- p
✔- span

- semantic / good practices
-- articles https://developer.mozilla.org/fr/docs/Web/HTML/Element/article
-- https://www.alsacreations.com/article/lire/1376-html5-section-article-nav-header-footer-aside.html

- quotes > blockquote or q ?

# css fixs
✔ HX one words
- images mw 100% h auto
- minor transitions (ex: a hover)

# good practices
- w3c / https://www.w3.org/standards/webdesign/

- yay
-- http://wiki.accede-web.com/notices/html-css?DokuWiki=odg500eeh06othkknn70cj7s43
-- http://wiki.accede-web.com/notices/html-css/recommandations-additionnelles
-- http://www.accede-web.com/notices/ // recent

#verifications
- all html tags / https://developer.mozilla.org/en-US/docs/Web/HTML/Element
- w3c
- pagespeed

#html recommandations
- seo
-- strong / em use
--- b i fallbacks

-- head
--- title
--- meta
--- favicon
--- social medias

-- graphics
--- img
---- title / alt
---- text "habillage"
--- svg & ?

-- lang
--- i18n
--- nomenclature / price, adresse, zipcode, tel number, state/country (api normalisation)

-- a
--- states hover etc.
--- title
--- target
--- spams

-- robots nav skip
-- seo black list prevention
--- not enough contrast between color & bgc
--- overlapping

- acessibility
-- contrast
-- aria
--- /!\ semantics
-- outline (/!\ 0 / none)

- linters
- validators

- text
-- word break
-- aligns
-- ² et v

- Math symbols

- lists
-- nesting
-- directions
-- style none /!\ ol

- flex

- vertical aligns

- states / pseudo behaviors

- focus & outline (/!\ 0 / none)

- html5 semantics tags

- forms
-- select & multiple selects
-- custom radio / checkbox
--- groups
-- labels
-- fieldset & legends
-- resets > confirm
-- captchas

#css recommandations
- smacss
- don't overcharge if not needed (ex: parent border 1px solid #fff, child border-COLOR: #123123)

#folder & file recommandations
- images names
--  "-" separated words
-- SEO / proper names


#misc
✔ favicon
✔ basic GWFonts
✔ Mock images
✔- 4/3
✔-- 1280 x 960
✔-- 800 x 600
✔-- 400 x 300
✔- 16/9
✔-- 1280 x 720
✔-- 800 x 450
✔-- 400 x 225
✔ basic container
✔ info colors

- helpers
-- 2 pages > full html clean, html + helpers
-- Fixed menu for navigation ?


##reusability / optimisation
- gulp & custom functions
- pugjs
- sass
-- display grid half third forth

#More evolved
- Custom usual components
-- Responsive form (tab + inline block)
-- Containers
--- Full w
--- 1400mx

- Icôns
-- FAwesome / <https://www.npmjs.com/package/font-awesome>