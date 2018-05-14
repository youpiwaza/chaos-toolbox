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







////// Forms Brainstorm

//// form tag
	https://developer.mozilla.org/en-US/docs/Web/HTML/Element/form

	// spécifier method get/post
	// specifier attribut action

//// form elements

// all
<div class="info">
	All fields are displayed with their own label.<br />
	Fill the <em>name</em> attributes with usual names, to help browser auto-fill.
	// autocomplete
</div>


// name, (autofill) & autocomplete off
	// add name attribute & precise autocomplete attributes // has all
	https://cloudfour.com/thinks/autofill-what-web-devs-should-know-but-dont/

		// Codepen all fields w. autocomplete
		https://codepen.io/grigs/pen/NNVZPZ

		// autocomplete terms list
		https://html.spec.whatwg.org/multipage/form-control-infrastructure.html#inappropriate-for-the-control

		// Safari recommanded names for auto complete (billing mostly)
		https://stackoverflow.com/questions/25163891/when-is-the-scan-credit-card-option-available-on-ios8-safari/36151606#36151606

	// auto complete off
	https://www.w3schools.com/tags/att_input_autocomplete.asp

	MDN List
		Possible values are:
		off: The user must explicitly enter a value into this field for every use, or the document provides its own auto-completion method. The browser does not automatically complete the entry.
		on: The browser is allowed to automatically complete the value based on values that the user has entered during previous uses, however on does not provide any further information about what kind of data the user might be expected to enter.
		name: Full name.
		honorific-prefix: Prefix or title (e.g. "Mr.", "Ms.", "Dr.", "Mlle").
		given-name: First name.
		additional-name: Middle name.
		family-name: Last name.
		honorific-suffix: Suffix (e.g. "Jr.", "B.Sc.", "MBASW", "II").
		nickname
		email
		username
		new-password: A new password (e.g. when creating an account or changing a password).
		current-password
		organization-title: Job title (e.g. "Software Engineer", "Senior Vice President", "Deputy Managing Director").
		organization
		street-address
		address-line1, address-line2, address-line3, address-level4, address-level3, address-level2, address-level1
		country
		country-name
		postal-code
		cc-name: Full name as given on the payment instrument.
		cc-given-name
		cc-additional-name
		cc-family-name
		cc-number: Code identifying the payment instrument (e.g. the credit card number).
		cc-exp: Expiration date of the payment instrument.
		cc-exp-month
		cc-exp-year
		cc-csc: Security code for the payment instrument.
		cc-type: Type of payment instrument (e.g. Visa).
		transaction-currency
		transaction-amount
		language: Preferred language; a valid BCP 47 language tag.
		bday: birthday
		bday-day
		bday-month
		bday-year
		sex: Gender identity (e.g. Female, Fa'afafine), free-form text, no newlines.
		tel: full telephone number, including country code
		additional tel variants: tel-country-code, tel-national, tel-area-code, tel-local, tel-local-prefix, tel-local-suffix, tel-extension
		url: Home page or other Web page corresponding to the company, person, address, or contact information in the other fields associated with this field.
		photo: Photograph, icon, or other image corresponding to the company, person, address, or contact information in the other fields associated with this field.


// required
	<!--
	required field * > use < abbr >  <abbr title="required">*</abbr>
	-->
	ex : 
	<!-- 
	<p>
		<label for="name">
			<span>Nom : </span>
			<strong><abbr title="required">*</abbr></strong>
		</label>
		<input type="text" id="name" name="username">
	</p>
	-->
	https://developer.mozilla.org/fr/docs/Web/HTML/Element/abbr










//// Layout
	https://developer.mozilla.org/en-US/docs/Learn/HTML/Forms/How_to_structure_an_HTML_form

	// regroup thematic fields
	Regrouper les champs similaires dans des tag < section >

	Fieldset & legend
		contour & title

	autofocus attribute
		HTML5
		This Boolean attribute lets you specify that a form control should have input focus when the page loads, unless the user overrides it (e.g. by typing in a different control). Only one form element in a document can have the autofocus attribute, which is a Boolean. It cannot be applied if the type attribute is set to hidden (that is, you cannot automatically set focus to a hidden control). Note that the focusing of the control may occur before the firing of the DOMContentLoaded event.

////Elements
	// list of all form elements at the bottom
	https://developer.mozilla.org/fr/docs/Web/HTML/Element/Form

	// Implémentation basique
	https://developer.mozilla.org/en-US/docs/Learn/HTML/Forms/The_native_form_widgets

	// Compatibilité
	https://www.wufoo.com/html5/
	https://quirksmode.org/html5/inputs/mobile.html

	// Attributs
	https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input#attr-list

	// Compatibilité des attributs !
	https://developer.mozilla.org/en-US/docs/Web/API/HTMLInputElement
	
	// button
		https://developer.mozilla.org/en-US/docs/Web/HTML/Element/button
		autofocus
		disabled
		type
			submit
				accessibility
					Permitted ARIA roles	
					None

			reset
			button // prevent submit, à préférer pour comportement JS
				value // envoie de la donnée, ptet utile pour savoir quel bouton à été cliqué ?

		contenu > html (em strong img i)
		
		Firefox styles
			bg gradient by default, to disable > bgi: none
			dotted border on focus, to disable > button::-moz-focus-inner { }
				Attention accessibilité

		icon button & accessibility : add text & hide it
		https://gomakethings.com/hidden-content-for-better-a11y/#hiding-the-link

		Let space between buttons

		/!\ CSS /!\ Peut être invoqué via input
			type=submit
			type=reset
			type=button

		Avec button, possibilité de passer une value != (quel interêt x'))

		accessibility
			Permitted ARIA roles	
			type=button: link, menuitem, menuitemcheckbox, menuitemradio, radio, switch, tab

	
	// checkbox / radio
		https://developer.mozilla.org/en-US/docs/Learn/HTML/Forms/The_native_form_widgets > Ctrl F > "Checkable items"

		Recommandé fieldset / legend / label
		Recommandé : chaque input + label dans son conteneur (liste, div, etc.)
		Obligatoie : value
		
		// checkbox
			checked // attribut sans valeur, préchocher par défaut
			Valeurs multiples, name="hey[]"
		// radio
			Possibilité de regrouper des radios, attribut name similaire
			/!\ Possibilité aucune valeur sélectionnée

			accessibility
				Permitted ARIA roles	
				type=radio: menuitemradio

	
	// color

		! Ko safari IE

		accessibility
			Permitted ARIA roles	
			None


	// datalist // ~select, but better
		Select from a list, ability to type text & auto completion
		https://developer.mozilla.org/en-US/docs/Web/HTML/Element/datalist
		
		/!\ Must have an <input list="datalist-id" /> tag attached
		/!\ Needs polyfill for safari
		https://github.com/mfranzke/datalist-polyfill

		fallback compatibilité :
		https://developer.mozilla.org/en-US/docs/Learn/HTML/Forms/The_native_form_widgets > Ctrl F > "Datalist support and fallbacks"

		Peut être utilisé avec tout, mais n'est pas recommandé pour des dates/couleurs (comportement erratiques en fonctions des navigateurs, cf. mdn)


	// Date and time picker
		
		/!\ peut de compatibilité
		FF & Safari ~, IE ko

		// date
			accessibility
				Permitted ARIA roles	
				None
		
		// datetime
			! OBSOLETE
			accessibility
				Permitted ARIA roles	
				None

		// datetime-local
			This creates a widget to display and pick a date with time, but without any specific time zone information.

			accessibility
				Permitted ARIA roles	
				None

		// month
			accessibility
				Permitted ARIA roles	
				None

		// time
			accessibility
				Permitted ARIA roles	
				None

		// week
			accessibility
				Permitted ARIA roles	
				None

	

	// fieldset & legend
		// fieldset
		https://developer.mozilla.org/en-US/docs/Web/HTML/Element/fieldset
		
		can be disabled > disable all children
		form
		name

		// legend
		https://developer.mozilla.org/en-US/docs/Web/HTML/Element/legend
		used as fieldset child. nothing much to say
	

	// file

		accept 
			Possibilité de spécifier le type de fichier envoyé via attribute accept
			
			A file extension starting with the STOP character (U+002E). (e.g. .jpg, .png, .doc).
			A valid MIME type with no extensions.
			audio/* representing sound files. HTML5
			video/* representing video files. HTML5
			image/* representing image files. HTML5
		
		capture
			When the value of the type attribute is file, the presence of this Boolean attribute indicates that capture of media directly from the device's environment using a media capture mechanism is preferred.

		multiple

		accessibility
			Permitted ARIA roles	
			None


	// hidden
		required > name & value

		accessibility
			Permitted ARIA roles	
			None

	
	// image !
		
		Image button. Behave like a submit button
		Data send : position on clicked image (from top left)

		accessibility
			Permitted ARIA roles	
			type=image: link, menuitem, menuitemcheckbox, menuitemradio, radio, switch


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


// Design / ergo
	https://www.slideshare.net/jwegesin/forms-suck/27-First_Name_right_Last_Name
	Label en haut des champs
	Une seule colonne
	Boutons
		Ajouter des couleurs (vert validation, rouge nope)
		Utiliser des liens à la place si comportement peu utilisé
		Ordonner (gauche vers droite)
		Btn validation, inline avec le formulaire
	Ne pas utiliser d'acronymes/prog oriented > labels, exemples

	Seulement les champs indispensables
	Flexibilité sur les champs alakon // tel
		exemples de format avec vraies données

	Validation à la volée, pas en fin de formulaire
	Auto complétion (cf. autocomplétion avec suggestion persos, cf. autocomplétion sugg. navigateur)

	Gestion des erreurs par champs + récapitulatif a la validation





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


 ! Lint all this sh*t x)
 ! Auto prefix
