# Full Nav Menu

###### This is the basic <a href="https://www.npmjs.com/package/full-menu">"full-menu"</a> version and does not contain additional modules and settings. If you want to get the full version with settings and modules, then use the npm i -D full-menu package. Here is a link to npm => <a href="https://www.npmjs.com/package/full-menu">"full-menu"</a> and to the GitHub repository <a href="https://github.com/wikiour/full-menu">"full-menu"</a>.

If you are looking for a library to create a complete menu for your site, then "menu-full" might be a great choice for you. This library provides an easy and convenient way to create beautiful and functional menus on your web pages.

One of the features of "menu-full" is its ease of use. No special programming knowledge is required to create a menu, as the library provides a simple and intuitive interface. All you need to do is just install the npm package and add it to your project. In your navigation menu, add the nav-menu class and then our script will do the rest. You can create menus with unlimited nested items, dropdowns, animations and more.

If you want to add a navigation menu to your site, you can do so with our "menu-full" library, which can be installed into your project via npm or downloaded from our GitHub repository.

This menu works on any device and works both on hover and on click, so you can be sure that the user will open this menu on any site. It also thought out all the user actions that help to work with this menu.

##### Here is an example of what your html code might look like:
```
      <nav class="nav-menu">
        <ul>
          <li>Home</li>
          <li>Catalog
            <ul>
              <li>Category
                <ul>
                  <li>Products</li>
                </ul>
              </li>
            </ul>
          </li>
        </ul>
      </nav>
```

Our JavaScript will add all the necessary classes to your menu so that you can do CSS-only styling of your menu however you want. It adds extra classes as soon as the submenu appears in your html so you don't have to worry about automating the process. It will automatically assign an extra class to the nav (nav-sub-menu) which will mean the menu contains a submenu, it will also assign the li which contains the submenu the class nav-menu-li and wrap your li content in a span with the class nav-menu-span , will additionally assign the class nav-menu-ul to the nested ul element. On click or hover, the active class will be added and removed for the nav-menu-li, av-menu-span, nav-menu-ul elements, allowing you to customize any behavior of the menu.

##### Here is how the same code will look like after being processed by our script:
```
     <nav class="nav-menu nav-sub-menu">
        <ul>
          <li>Home</li>
          <li class="nav-menu-li">
           <span class="nav-menu-span">Catalog</span>
            <ul class="nav-menu-ul">
              <li class="nav-menu-li">
              <span class="nav-menu-span">Category</span>
                <ul class="nav-menu-ul">
                  <li>Products</li>
                </ul>
              </li>
            </ul>
          </li>
        </ul>
      </nav>

```

Our "menu-full" library has a fast and optimized code that guarantees fast loading of your website. This makes our JavaScript a great choice for sites of any size and scale. Install right now and see the simplicity and quality of our code.

##### Connecting via npm
```
npm i -D menu-full
```

##### Connecting to the project
```
import navMenu from 'menu-full';
navMenu();
```

The "menu-full" library is a great choice for those who are looking for an easy, fast and flexible way to create a complete menu on their website. With it, you can quickly create a beautiful and functional menu that will work on all devices and match your design.

##### Here is an example of basic SASS for your menu
```
nav.nav-menu.nav-sub-menu ul > li > ul.active {
	opacity: 1;
	visibility: visible;
	@media (max-width: 768px) {
		display: block;
	}
}
nav.nav-menu.nav-sub-menu ul > li > ul > li > ul.active {
	display: block;
}

nav.nav-menu.nav-sub-menu {
	font-family: Georgia, "Times New Roman", Times, serif;
	font-weight: 16px;
	font-style: normal;
	line-height: normal;
	letter-spacing: rem(1);
	color:#232b32;
	a {
		color: #232b32;
		&:hover {
			color: #a41111;
		}
		&:active {
			color: #a41111;
		}
	}

	& > ul {
		display: flex;
		flex-wrap: wrap;
		flex-direction: row;
		justify-content: flex-start;
		align-content: flex-start;
		align-items: left;
		gap: 5px 10px;
		text-align: left;
		@media (max-width: 768px) {
			flex-direction: column;
			width: 100%;
		}
	}

	& > ul > li > ul {
		opacity: 0;
		visibility: hidden;
		position: absolute;
		top: 95%;
		left: 0;
		width: 300px;
		padding: 10px 0 0 0;
		@media (max-width: 768px) {
			display: none;
			position: relative;
			top: 0;
			padding: 5px 0 5px;
			width: 100%;
		}
	}

	& ul > li > ul > li > ul {
		display: none;
	}

	li {
		position: relative;
		cursor: pointer;
		@media (max-width: 768px) {
			width: 100%;
		}
	}

	ul > li > ul > li {
		background-color: #d1effc;
		padding: 0 10px 5px 10px;
		&:first-child {
			padding: 5px 10px 5px 10px;
		}
		&:last-child {
			padding: 0 10px 5px 10px;
		}
		&:only-child {
			padding: 10px 10px 10px 10px;
		}
	}

	ul > li > ul > li > ul > li {
		padding: 0 0 5px 5px;
		&:first-child {
			padding: 5px 0 5px 5px;
		}
		&:last-child {
			padding: 0 0 0 5px;
		}
		&:only-child {
			padding: 5px 0 0 5px;
		}
	}

	ul > li > ul > li > ul > li > ul > li {
		padding: 0 0 5px 0;
		&:first-child {
			padding: 5px 0 5px 0;
		}
		&:last-child {
			padding: 0 0 0 0;
		}
		&:only-child {
			padding: 5px 0 0 0;
		}
	}

	span.nav-menu-span {
		display: block;
		position: relative;
		padding: 0 25px 0 0;
		&::after {
			content: "⬇️";
			position: absolute;
			top: -2px;
			right: 0;
			width: auto;
			height: auto;
		}
		&.active {
			&::after {
				content: "⬆️";
			}
		}
	}
	
	& > ul > li > span.nav-menu-span {
		@media (max-width: 768px) {
			margin: 0 10px 0 0;
		}
	}

}
```

You can modify this SASS to suit your needs as you wish.

__________________________________________________________
* Author: WikiOur
* Author website: https://wikiour.com
* GitHub: https://github.com/wikiour
* Patreon: https://patreon.com/wikiour
* YouTube: https://youtube.com/@wikiour
* Facebook: https://facebook.com/wikiour
* Instagram: https://instagram.com/wikiour


