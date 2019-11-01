# Sports HTML Template
This is an exercise in the Seven Academy HTML5 fundermentals course. It demonstrates basic principles of layouts and use of CSS.

*Students are encouraged to check out this repository only after doing thier own work!*

## Work Break Down

### What are we trying to achieve?

*Add picture mockup here, Mr.!*

### 1. My path!

*So for the entire homepage, I explain my line of thought which would justify why the HTML page is structured as seen*

* First off, I started by writing the simplest w3 compliant HTML page, which includes `<!DOCTYPE html>` meaning I am using HTML5, the opening and closing tags for `<html></html>` with a `<body></body>` and the `<head>` which holds the page title in `<title></title>` which constitutes the bare minimum of compliant HTML5 code.

* Next I use the non-sematic element `div` to create a container for my page! I use a non-semantic tag because, the container has no meaning I don't care for anyone (like search engines to know). It's purely for styling.

* Within the container I add a `header` for my page which contains the `nav` and a list of links or `a` tags which constitutes the site menu.

 **NB: Since the design of our page keeps the navigation/menu on the side, students may be tempted to use the `aside` element for that!!! You can do that but it's not semantically as correct as using a the `header` + `nav` and putting with CSS as you would have done even with the aside**

* I also add another `div` to contain all the main components of the page, which includes a `topbar` showing contact infomation. A `sidbar` showing trending matches and the last section holding an article that links to full details for some match. For all the parts contained within the main-section, I use the `section` element because the are parts of our page which have meaning, for example contact, trendy matches and photo latest current match are all things we might want to be "semantically aware" of.

```
<!DOCTYPE html>
<html>
<head>
	<title></title>
</head>
<body>
	<div class="container">
		<header>
			<nav>
				<ul>
					<li><a href="#">Home</a></li>
					<li><a href="#">Sports</a></li>
					<li><a href="#">Events</a></li>
					<li><a href="#">Football</a></li>
					<li><a href="#">Basketball</a></li>
					<li><a href="#">Handball</a></li>
				</ul>
			</nav>
		</header>
		<div class="main-section">
			<section id="contact-topbar"></section>
			<section id="trending-sidebar"></section>
			<section id="article"></section>
		</div>
	</div>
</body>
</html>
```

### 2. Let's add some content and the internal sections

So in the main section I decide to divide it as show in the mockup into 3 main sections. 
* The first section, I give it a class `.contact-section` and add two spans in it for phone number and email in spans.
* Next I add a section which I indentify with the id `#sidebar` containing two sub-sections `.page-titile` and `.trending`
* Finally I add an `img` element, a `div` to help me hold article title and preview text and a read more link in the `#article` section!

Finally Time to write some CSS! But before that you should have thought about;

- HTML tags and Attributes
- Semantic and Non-Semantic Elements
- Divs versus Sections "controversy"
- HTML5 compliance (e.g "doctype" and not closing the tags like self-closing `img`)
- Basically! Recalling the fundermentals of writing good HTML! Now CSS!

```
<div class="main-section">
			<section id="contact-topbar">
				<span>Phone: +1 (345) 234-343-231</span>
				<span>Email: support@sportswebsite.com</span>
			</section>
			<section id="sidebar">
				<section class="page-title">

				</section>
				<section class="trending">
					<h1>Trending Sports Events</h1>
					<p>
						Lorem ipsum dolor sit, amet consectetur adipisicing elit.
						Modi commodi itaque atque ipsa repudiandae at nihil eos,
						earum pariatur mollitia nostrum, corporis dolorum voluptas
						deleniti qui nulla veniam, sint ipsum!
					</p>
					<ol>
						<li>Team A Vs Team B</li>
						<li>Team C Vs Team B</li>
						<li>Team B Vs Team D</li>
						<li>Team C Vs Team D</li>
					</ol>
				</section>
			</section>
			<section id="article">
				<img src="assets/images/fc-barcelona.png" alt="Merci in Barcelona Jersey">
				<div>
					<span>Talent in Action! FC Barcelona</span>
					<p>Lorem ipsum dolor sit amet consectetur adipisicing elit...</p>
				</div>
				<a href="">Read More</a>
			</section>
		</div>
```

### 3. Let's position and style our elements with CSS