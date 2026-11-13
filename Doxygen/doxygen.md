# Doxygen

## 1. Introduction

Doxygen is an open-source documentation generation tool used to create documentation directly from source code.

It supports programming languages such as C, C++, Python, and Java. It extracts specially formatted comments from source code and generates documentation in formats such as HTML and LaTeX/PDF.

Doxygen is mainly used to create API documentation and reference manuals for software projects.

## 2. Why Do We Need Documentation?

Technical documentation is important because it:

- Clarifies software requirements and specifications.
- Makes software maintenance easier.
- Helps new developers understand a project.
- Supports compliance, auditing, and quality assurance.
- Encourages knowledge sharing and collaboration.

## 3. Features of Doxygen

- **Automatic documentation generation:** Extracts information from specially formatted source-code comments.
- **Code documentation:** Documents functions, classes, modules, and variables.
- **Cross-referencing:** Creates links between related code elements.
- **Diagrams:** Supports call graphs, inheritance diagrams, and include diagrams.
- **Multiple formats:** Generates HTML, LaTeX/PDF, RTF, XML, DocBook, and man pages.
- **Markdown support:** Allows Markdown formatting, tables, and code examples.
- **CI/CD integration:** Documentation generation can be included in automated development workflows.

## 4. Installation of Doxygen

Doxygen can be installed on different operating systems.

### Windows

Download Doxygen from:

https://www.doxygen.nl/download.html

### macOS

```bash
brew install doxygen
```

### Linux

```bash
sudo apt-get install doxygen
```

### Verify Installation

After installation, check the installed version:

```bash
doxygen --version
```

## 5. Working with Doxygen

The basic Doxygen workflow consists of three steps:

### Step 1: Write Special Comments

Write specially formatted comments in your source-code files to describe functions, classes, and other code elements.

### Step 2: Generate a Configuration File

Run:

```bash
doxygen -g Doxyfile
```

This creates a configuration file named `Doxyfile`.

### Step 3: Generate Documentation

Run:

```bash
doxygen Doxyfile
```

Doxygen generates the documentation according to the configuration.

The generated HTML documentation can be opened using:

```text
html/index.html
```

## 6. Doxygen Comment Syntax

Doxygen uses special comment formats to identify documentation.

### C/C++ Example

```cpp
/**
 * \brief Brief description of the function.
 *
 * Longer detailed explanation.
 * \param x A parameter description.
 * \return Description of the return value.
 */
int myFunction(int x);
```

Explanation:

- `\brief`: Provides a short description.
- `\param`: Describes a function parameter.
- `\return`: Describes the return value.

### Python Example

```python
def foo(bar):
    """
    Brief description.
    More details here.

    :param bar: Bar parameter
    :type bar: int
    :return: Computed value
    :rtype: int
    """
    return bar + 1
```

## 7. Common Doxygen Commands and Tags

| Tag | Purpose |
|---|---|
| `\brief` | Provides a short description |
| `\param` | Describes a parameter |
| `\return` | Describes the return value |
| `\author` | Specifies the author |
| `\version` | Specifies the version |
| `\see` | Refers to related information |
| `\note` | Adds an important note |

## 8. Documenting Classes

Doxygen can also generate documentation for classes and their member functions.

Example:

```cpp
/**
 * \class Car
 * \brief Represents a car object.
 */
class Car {
public:

    /**
     * \brief Starts the car engine.
     * \return Status of the engine.
     */
    bool startEngine();
};
```

Here:

- `\class` identifies the class.
- `\brief` gives a short description.
- The member function is documented separately.

## 9. Advanced Documentation Features

### Grouping

Doxygen supports logical grouping of related documentation elements. The lecture slides mention using `|/|` for logical grouping.

### Diagrams

Doxygen can generate:

- Call graphs
- Include diagrams
- Inheritance diagrams

To enable Graphviz-based diagrams, set the following option in the Doxyfile:

```text
HAVE_DOT = YES
```

Doxygen also supports `@dot` and PlantUML directives for diagrams.

### Tables, Images, and Markdown

Doxygen supports Markdown and HTML features, including tables and images, to make documentation easier to understand.

## 10. Output Formats

Doxygen can generate documentation in multiple formats.

| Format | Description |
|---|---|
| HTML | Web-based documentation |
| LaTeX/PDF | Printable documentation |
| RTF | Rich Text Format |
| XML | Structured documentation data |
| DocBook | Documentation format |
| Man pages | Unix manual pages |

### Configuration Example

The output formats can be controlled through the Doxyfile.

```text
GENERATE_HTML = YES
GENERATE_LATEX = YES
GENERATE_RTF = NO
GENERATE_XML = NO
```

## 11. Best Practices

- Explain the purpose and behavior of functions, not just their parameters.
- Keep brief and detailed descriptions separate.
- Document public APIs and modules.
- Use consistent tags and formatting.
- Generate documentation regularly.
- Integrate documentation generation into CI/CD workflows.

## 12. Doxygen and Version Control

Doxygen can be used together with Git and GitHub.

- Store the `Doxyfile` in the source-code repository.
- Update documentation whenever code changes.
- Review documentation changes through code reviews.
- Publish generated documentation using GitHub Pages or an internal wiki.

## 13. Practical Exercise

A basic Doxygen exercise involves:

1. Installing Doxygen.
2. Creating a small C++ or Python codebase.
3. Adding Doxygen-style comments.
4. Generating a configuration file using `doxygen -g Doxyfile`.
5. Generating documentation using `doxygen Doxyfile`.
6. Opening `html/index.html` in a browser.
7. Exploring diagrams and cross-references.

## 14. Advantages of Doxygen

- Automatically generates documentation from source code.
- Supports multiple programming languages.
- Reduces manual documentation work.
- Provides cross-references and diagrams.
- Supports multiple output formats.
- Helps developers maintain API documentation.

## 15. Useful Resources

- Official Doxygen Website: https://www.doxygen.nl/
- Doxygen Manual: https://www.doxygen.nl/manual/
- Sphinx: https://www.sphinx-doc.org/
- MkDocs: https://www.mkdocs.org/
- Read the Docs: https://readthedocs.org/

## 16. Conclusion

Doxygen is a useful documentation tool for software developers. It generates structured documentation from source-code comments and helps make software projects easier to understand, maintain, and collaborate on.