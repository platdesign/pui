#PUI#

Platdesign UI - A scss-library for your daily needs.


##Install
- Bower: `bower install pui --save-dev`
- Git: `git clone https://github.com/platdesign/pui.git`
- Zip: [Download](https://github.com/platdesign/pui/archive/v0.1.0.zip)



## Usage
Example for a scss file with pui components:

	@import './path/to/pui/pui.scss';
	
	@include pui-reset;
	@include pui-flex;
	@include pui-angular;
	@include pui-form;
	...

##Mixins
- **pui-reset**

	Not a whole reset like normalize, but some opinionated defaults.

- **pui-flex**

	Adds some classes to your css for working with flexible layouts.
	
	- `flex-horizontal` (wrapper for flex-items)
	- `flex-vertical` (wrapper for flex-items)
	- `flex-item` (column or row depending on wrapper)
	- `flex-item-stretch` (column or row which fills whole free space)

- **pui-angular**
	
	Some handy defaults for working with [angular.js](https://angularjs.org/).

	- `cursor: pointer` for ng-click and ui-sref directives

- **pui-form**

	Resets form elements on all devices to the same appearance.


- **pui-helper**
	
	Adds some helper-classes:

	- `.tl`, `.tc`, `.tr` for text-alignment (left, center, right).
	- `.fl`, `.fr` for `float:left` and `float:right`
	- `.antialised` sets font-smoothing for text on dark backgrounds.





- **grid**

	Adds classes `.row` and `.col`. (Uses floats and clearfix.)

- **grid-flex**
	
	Same classes `.row` and `.col` like with `@include grid` but uses new flexbox technology. Also adds `.col-stretch`-class for columns with undefined but fulfilling width.

- **page**
	
	Adds `.page`-class. It's a centered container which changes it's width responivley.

- **btn(** *string $name:false* **)**

	Creates a `.btn`-class or with given `$name` a `.btn-{$name}`-class. The content of the mixin will be the content of the class.

		@include btn {
			color:#444;
		}
		@include btn(submit) {
			color:green;
		}
	
	This little example will create classes `.btn` and `.btn-submit`.

- **w(** *int $colums* **)**

	Adds classes with a structure like `.w-1-3`, `.w-2-3`, etc. `$columns` defines the maximum divider of 100%.


-------

##Functions
- **first(** *list $list* **)**
	
	Returns the first item of `$list`.

- **last(** *list $list* **)**

	Returns the last item of `$list`.


- **prepend(** *list $list, int | float | string | list $item* **)**

	Prepends `$list` with `$item`.



-------



##Variables
###$breakpoints: (400px, 600px, 800px, 1000px, 1200px);
A list of breakpoints in `px` from narrow to wide.

###clrs.cc
PUI includes all color-variables of [clrs.cc](http://clrs.cc).





##License
This project is under the MIT license. Let me know if you'll use it. =)


##Contributors
This is a project by [Christian Blaschke](http://platdesign.de).	 
Get in touch: [mail@platdesign.de](mailto:mail@platdesign.de) or [@platdesign](https://twitter.com/platdesign)

