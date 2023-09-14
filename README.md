# Genify

Genify is a Python script that allows you to render HTML templates using Jinja2. You can specify an input HTML file and a list of template files to include in the rendering process. The resulting HTML file will be saved in a "dist" directory.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Examples](#examples)
- [Contributing](#contributing)
- [License](#license)

## Installation

1. Clone the Genify repository to your local machine:

```bash
git clone https://github.com/your-username/genify.git
```

2. Navigate to the Genify project directory:

```bash
cd genify
```

3. Create and activate a virtual environment (recommended):

```bash
python -m venv venv
source venv/bin/activate # On Windows, use `venv\Scripts\activate`
```

4. Install the required dependencies using `pip`:

```bash
pip install -r requirements.txt
```

## Usage

You can use Genify to render HTML templates by providing an input HTML file and one or more template files. Follow these steps to use Genify:

1. Ensure you have Python 3.x installed on your system.
2. Run Genify using the following command:

```bash
python genify.py -i input.html -t navbar.html -t footer.html ...
```

Replace `input.html` with the path to your input HTML file and `navbar.html`, `footer.html`, etc., with the paths to your template files.

3. The rendered HTML file will be saved in a "dist" directory within the Genify project folder.

## Examples

Here's an example of how to use Genify with a base HTML file and separate templates for a navbar and a footer:

**base.html**
```html
<!DOCTYPE html>
<html>
	<head>
		<title>Genify Example</title>
	</head>

	<body>
		<!-- Include the navbar template -->
		{% include 'navbar.html' %}
		<main>
			<h1>Hello, Genify!</h1>
			<p>This is the main content of your page.</p>
		</main>
		<!-- Include the footer template -->
		{% include 'footer.html' %}
	</body>
</html>
```

navbar.html
```html
<nav>
	<ul>
		<li><a href="#">Home</a></li>
		<li><a href="#">About</a></li>
		<li><a href="#">Services</a></li>
		<li><a href="#">Contact</a></li>
	</ul>
</nav>
```

footer.html
```html
<footer>
	<p>&copy; 2023 Genify. All rights reserved.</p>
</footer>
```

Run Genify to render `base.html` using `navbar.html` and `footer.html`:

```bash
python genify.py -i base.html -t navbar.html -t footer.html
```

This command will render `base.html` with the provided navbar and footer templates and save the result in the "dist" directory.

## Contributing

Contributions to Genify are welcome! If you find any issues or have suggestions for improvements, please open an issue or create a pull request on the Genify GitHub repository.

## License

Genify is open-source software licensed under the MIT License. See the LICENSE file for details.
