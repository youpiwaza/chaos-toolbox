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

- details ? > https://developer.mozilla.org/en-US/docs/Web/HTML/Element/details

# css fixs
✔ HX one words
✔ images mw 100% h auto
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
- all links in english

#html recommandations
- seo
✔- strong / em use
✔-- b i fallbacks

-- head
--- title
--- meta
--- favicon
--- social medias

-- graphics
✔-- img
✔--- title / alt
---- text "habillage"
✔-- svg & ?

-- lang
✔-- i18n
--- nomenclature / price, adresse, zipcode, tel number, state/country (api normalisation)

-- a
✔-- states hover etc.
✔-- title
✔-- target
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
✔- word break
✔- aligns
-- ² et v pow power puissance
-- https://developer.mozilla.org/fr/docs/Web/HTML/Element/sup
-- https://developer.mozilla.org/fr/docs/Web/HTML/Element/sub

- Math symbols

- lists
✔- nesting
-- directions
-- style none /!\ ol

- flex

- vertical aligns

- states / pseudo behaviors

- focus & outline (/!\ 0 / none)

- html5 semantics tags


#css recommandations
- smacss
- itcss ? https://www.xfive.co/blog/itcss-scalable-maintainable-css-architecture/
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







////// Forms Brainstorm


////Elements


	// input

		Gestion des erreurs
		// Vérifier si le mauvais remplissage de champs typés empêche l'envoi du formulaire (au moins url & mail ?)
		https://developer.mozilla.org/en-US/docs/Learn/HTML/Forms/Form_validation

		// email
			attribute multiple ?

			accessibility
				Permitted ARIA roles	
				None
		
		// number !
			https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/number
			<input type="number" name="age" id="age" min="1" max="10" step="2">
			! Compatibilité IE10+

			placeholder != valeur finale, ex: "Multiples of 10"
			possibilité de suggestions datalist

			accessibility
				Permitted ARIA roles	
				None

		// password
			accessibility
				Permitted ARIA roles	
				None

		// search !
			Remove Webkit Search Input Styles
				Webkit browsers add extra styling to the search input field. To remove them, add the following CSS code:

				input[type=search] {	-webkit-appearance: none;}

				input[type="search"]::-webkit-search-decoration, 
				input[type="search"]::-webkit-search-cancel-button {
					display: none;
				}

			accessibility
				Permitted ARIA roles	
				None


		// tel // telephone
			accessibility
				Permitted ARIA roles	
				None

		// text
			// Peut avoir une liste de suggestions pré enregistrées !!!!!!!
			https://developer.mozilla.org/en-US/docs/Learn/HTML/Forms/The_native_form_widgets > ctrl F "Autocomplete box"

			accessibility
				Permitted ARIA roles	
				None

		// url !
			/!\ check pas les 404
			/!\ Empêche envoi du formulaire si syntaxe ko ?

			accessibility
				Permitted ARIA roles	
				None


	// meter
		https://developer.mozilla.org/fr/docs/Web/HTML/Element/meter
		~ barre de progression chelou, fixe

		/!\ non compatible IE, & safari mobile
	

	// optgroup
		https://developer.mozilla.org/en-US/docs/Web/HTML/Element/optgroup

		/!\ label, en tant qu'attribut, est obligatoire
		Possibilité d'ajouter plusieurs optgroup, mais d'en disabled que certains


	// option
		https://developer.mozilla.org/en-US/docs/Web/HTML/Element/option
		// enfant de select, optgroup ou datalist

		/!\ Si value attribute vide, le contenu des deux tags est envoyé
	

	// output
		https://developer.mozilla.org/en-US/docs/Web/HTML/Element/output

		Utilisé pour afficher le résultat d'un calcul
		for > list d'id de champs a additionner
		Pas dispo sur IE
		
		// http://html5doctor.com/the-output-element/
		Par défaut addition, mais possibilité de l'utiliser pour des opérations plus complexes via le formulaire (attributs onsubmit=false & oninput=output-id.value = champA-id.valueAsNumber * champB-id.valueAsNumber)
		
			// FF ne supporte pas valueAsNumber ?

		Possibilité de coupler anvec <range>


	// progress
		https://developer.mozilla.org/en-US/docs/Web/HTML/Element/progress
		barre de progression
		
		max // default 1
		value // si absent, etat indéterminé

		/!\ plein de config styles par navigateur (prefixes)

		utilisé pour : Nombre de questions remplies dans un form, % de fichier envoyé

	
	// radio
		cf. checkboxes


	// range
		https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/range
		
		IE ko

		/!\ compatibilité min max step optimum
		/!\ accessibilité : valeur imprécise ? coupler ek output & event change ? span + js ?
		! accéssibilité : La valeur contenue entre les tags est ce qui sera affiché en fallback

		3 couleurs possibles : rouge, jaune, vert (en fonction de la valeur, min max optimum)

		Recommandé pour volume, couleurs, contrôles de jeu (difficulté), nb de caractères pour générateur de mots de passe, etc.

		Possibilité de spécifier des valeurs pour chaque pas (tickmarks) avec le tag datalist, + labels pour certains
			// ~0 compatibilité pour le moment
			// > mdn recommande d'ajouter un span et de le maj avec JS (pour le moment)

		accessibility
			Permitted ARIA roles	
			None


	// select
		https://developer.mozilla.org/en-US/docs/Web/HTML/Element/select

		peut avoir pour enfant des option ou optgroup
		autofocus
		disabled

		multiple ; default nope // compatibilité ok

		size ; can specify number of displayed items
			// doesn't look like a select anymore, more like a list, with a scroll

		event fired : change, input


	// textarea
		https://developer.mozilla.org/en-US/docs/Web/HTML/Element/textarea

		cols / rows
		minlength / maxlength
		readonly
		spellcheck // nice
		wrap > soft / hard // Indicates how the control wraps text.
		/!\ pas d'attribut value, valeur par défaut entre les deux tags
		/!\ ne prend pas en compte le html

		css > possibilité de forcer l'abscence de resize
			textarea {
				resize: none;
			}
		
	// Voir pour éditeur de texte complexe

	// Voir pour éditeur markdown
		

//// Events
	// change
		Unlike the input event, the change event is not necessarily fired for each change to an element's value.
		// validation, loss of focus
		https://developer.mozilla.org/en-US/docs/Web/Events/change

	// input
		// every change (each letter in a text input)
		https://developer.mozilla.org/en-US/docs/Web/Events/input

	// keydown, keyup, keypress





//// Specific stuff
	
	// Captcha
		https://developers.google.com/recaptcha/intro

		google invisible captcha maintenant ?

	// payment

	// adress

	// tel


//// Submission

	security > CARE FOR HTML EDITS / BAD REQUESTS

	<ul>
	<li>JS / If form is handled by javascript, use the <em>submit</em> event on the form instead of a <em>click</em> event on the button. This way you'll proc even if the user submitted another way (any field > enter ; tabulation to navigate to the button > space) </li>
	</ul>
	
	// Form validation
	https://developer.mozilla.org/en-US/docs/Learn/HTML/Forms/Form_validation
	! Prévoir validation en back, en cas d'édition de HTML
		Faire concorder les tests
	
	min max // number
	minlength maxlength // text
	regexp si données ~

	// Ctrl F "Customized error messages"
	! Messages d'erreurs built navigateur, pas possible de changer le style
		Possibilité de changer le contenu

		// Propriétés js // Ctrl F > "Constraint validation API properties"
		Sinon utiliser du JS
		! polyfill > https://hyperform.js.org/

		! accéssibilité > attribut aria-live="polite"
			// Lib de validation
			Standalone library
			Validate.js // http://rickharrison.github.com/validate.js/

			jQuery plug-in:
			Validation // http://bassistance.de/jquery-plugins/jquery-plugin-validation/







//// Accessibility
	arias & roles
		https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input#attr-list



//// favorites
	Add an id to every title, to allow fav/ref links to index.html#daTitle



// CSS form related
	// Nouveau pseudo-attributes, selectors + BROWSER SPECIFIC STYLING !!!!!
	https://www.wufoo.com/html5/
	
	// custom elements
		// Pas lire le comportement Js, c'est ridicule, garder le comportement natif
	https://developer.mozilla.org/en-US/docs/Learn/HTML/Forms/How_to_build_custom_form_widgets
	
	// Validation
	css > :valid, :invalid
		// Est-ce que ça marche avec les :before / :after ?

	// Styling
	https://developer.mozilla.org/en-US/docs/Learn/HTML/Forms/Styling_HTML_forms
	https://developer.mozilla.org/en-US/docs/Learn/HTML/Forms/Advanced_styling_for_HTML_forms

	// Possibility to style the curson !
	https://developer.mozilla.org/en-US/docs/Web/CSS/caret-color
	caret-color: red;
	
	// Sticky css
	Déjà mentionné dans layout


https://developer.mozilla.org/fr/docs/Accessibilit%C3%A9/ARIA/Techniques_ARIA

 ! Lint all this sh*t x)
 ! Auto prefix

Accessibility > check design for colorblindness suffisant contrast
https://css-tricks.com/accessibility-basics-testing-your-page-for-color-blindness/
https://www.toptal.com/designers/colorfilter


Add emmet suggested tags generation
- Review doc to pass an array of data for generation, for complex stuff / ids list

clean .big classes / uniformiser

chaos repos
> Sass Mixins
> Page bloc templates
> Sublim text plugins auto install