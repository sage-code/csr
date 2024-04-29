+++
title = "Symbols"
description = "From pictograms to ASCII and Unicode"
collection = "basics"
date = 2023-12-22
weight = 4
chapter = false
disableToc = false
pre = "<b>📜</b>"
tags = ["symbols", "basics"]
+++

Pictograms, alphabets and numeric symbols are 3 important pillars of civilization.These three, have played a crucial role in the development and advancement of human civilization. Each pillar has had a profound impact on how we communicate, record information, and organize knowledge.

* **Pictograms:** The earliest form of written communication, pictograms served as a way to visually represent objects, ideas, and events. They laid the foundation for the development of writing systems by establishing the principle of using symbols to convey meaning.

* **Alphabets:** The shift from pictograms to alphabets marked a significant leap in the efficiency and complexity of written communication. Alphabets represent sounds instead of whole objects or ideas, allowing for the creation of words and the expression of a wider range of concepts. This paved the way for the development of literature, philosophy, and complex legal and social systems.

* **Numeric symbols:** The invention of numeric symbols revolutionized our ability to quantify, calculate, and track information. It enabled the development of mathematics, science, engineering, and trade, which in turn fueled innovation and progress in countless fields.

These three pillars have not only shaped the course of human history, but they continue to be essential to our lives today. We use pictograms in emojis and road signs, alphabets in every written language, and numeric symbols in everything from financial transactions to scientific research.

It's fascinating to learn about how these seemingly simple systems have had such a profound impact on our world. In this article I we will study how symbols are used in computer science, business and software industry.

---

## Encoding

Let's start with encoding. Many programmers have difficulties understanding the symbols and representations in computer science. We will crack these concepts with help from AI.

**What is Encoding?**

* In computer science, encoding is the process of converting information into a format that a computer can understand, store, and transmit. It's like a language that computers use to represent data.
* Different encoding schemes exist for different types of data, such as text, numbers, images, and sounds.

**Key Concepts:**

1. **Character Encoding:**
   - It focuses on representing text characters as unique numbers.
   - Popular encoding schemes include:
     - **ASCII (American Standard Code for Information Interchange):** Supports basic English characters and some symbols.
     - **Unicode:** A universal standard that supports characters from most languages around the world.
     - **UTF-8:** A widely used encoding format for Unicode, compatible with ASCII.

2. **Binary Number System:**
   - Computers use the binary system (base 2) to represent all data as combinations of 0s and 1s.
   - Each 0 or 1 is called a bit, and a group of 8 bits forms a byte.

3. **Data Types:**
   - Programming languages use different data types to represent different kinds of information:
     - Integers (whole numbers)
     - Floating-point numbers (decimals)
     - Characters
     - Strings (text)
     - Booleans (true/false values)

**How AI Can Help:**

- **Visualizations:** AI can create interactive demos and visualizations to illustrate encoding concepts.
- **Interactive Exercises:** AI can generate practice problems and adaptive feedback to reinforce understanding.
- **Code Conversion:** AI can assist with converting code between different encoding schemes.
- **Error Detection:** AI can help identify and correct encoding errors in code.
- **Language Translation:** AI can translate text and code between different languages, automatically handling encoding differences.

---

### ASCII

Let's study the first ASCII encoding. Let's start with a table that show ASCII symbols with hexadecimal, decimal and description. Let's mention the history of this encoding, advantages and issues.

 **Here's a table showing ASCII symbols with hexadecimal, decimal, and description, followed by its history, advantages, and issues:**

**ASCII Table:**

Here's the ASCII table with 8 column and decimal code. First characters before 32 are special characters that do not have a visual representation. Sending these characters to console have different effects.

|dec|32 | 33| 34| 35| 36| 37| 38| 39|
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
| 32|   | ! | " | # | $ | % | & | ' |
| 40| ( | ) | * | + | , | - | . | / |
| 48| 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 |
| 56| 8 | 9 | : | ; | < | = | > | ? |
| 64| @ | A | B | C | D | E | F | G |
| 72| H | I | J | K | L | M | N | O |
| 80| P | Q | R | S | T | U | V | W |
| 88| X | Y | Z | [ | \ | ] | ^ | _ |
| 96| ` | a | b | c | d | e | f | g |
|104| h | i | j | k | l | m | n | o |
|112| p | q | r | s | t | u | v | w |
|120| x | y | z | { | | | } | ~ |   |
|128|DEL|   |   |   |   |   |   |   |

**Special characters.**

 Here's a table of special characters from 0 to 31 in ASCII, with their codes, descriptions, and console effects. These characters also use to control the older character matrix printers.

| Code| Dec| Hex | Description | Console Effect |
|-----|----|:---:|-------------|----------------|
| NUL | 0  | 00  | Null character (no character) | Often used to terminate strings |
| SOH | 1  | 01  | Start of Heading | Transmission control character |
| STX | 2  | 02  | Start of Text | Transmission control character |
| ETX | 3  | 03  | End of Text | Transmission control character |
| EOT | 4  | 04  | End of Transmission | Transmission control character |
| ENQ | 5  | 05  | Enquiry | Transmission control character |
| ACK | 6  | 06  | Acknowledge | Transmission control character |
| BEL | 7  | 07  | Bell (beep) | Produces an audible or visible alert |
| BS  | 8  | 08  | Backspace | Moves the cursor one position backward |
| HT  | 9  | 09  | Horizontal Tab | Moves the cursor to the next tab stop |
| LF  | 10 | 0A  | Line Feed (new line) | Moves the cursor to the next line |
| VT  | 11 | 0B  | Vertical Tab | Moves the cursor to the next vertical tab stop |
| FF  | 12 | 0C  | Form Feed (new page) | Advances the printer to a new page |
| CR  | 13 | 0D  | Carriage Return | Moves the cursor to the beginning of the current line |
| SO  | 14 | 0E  | Shift Out | Switches to an alternate character set |
| SI  | 15 | 0F  | Shift In | Switches back to the standard character set |
| DLE | 16 | 10  | Data Link Escape | Used for data communication purposes |
| DC1 | 17 | 11  | Device Control 1 |  Device control character |
| DC2 | 18 | 12  | Device Control 2 | Device control character |
| DC3 | 19 | 13  | Device Control 3 | Device control character |
| DC4 | 20 | 14  | Device Control 4 | Device control character |
| NAK | 21 | 15  | Negative Acknowledge | Transmission control character |
| SYN | 22 | 16  | Synchronous Idle | Used for synchronization in data communication |
| ETB | 23 | 17  | End of Transmission Block | Transmission control character |
| CAN | 24 | 18  | Cancel | Cancels the current operation |
| EM  | 25 | 19  | End of Medium | Indicates the end of a physical medium |
| SUB | 26 | 1A  | Substitute | Substitutes one character for another |
| ESC | 27 | 1B  | Escape | Control characters or escape sequences |
| FS  | 28 | 1C  | File Separator | Used to separate files or records |
| GS  | 29 | 1D  | Group Separator | Used to separate groups of data |
| RS  | 30 | 1E  | Record Separator | Used to separate records within a file |
| US  | 31 | 1F  | Unit Separator | Used to separate units of data within a record |
| EL  | 127| 7F  | Delete | Deletes the character at the cursor position |
 

**History of ASCII:**

- Developed in the 1960s by the American Standards Association (ASA).
- Aimed to standardize data communication among different devices.
- Originally used 7 bits to represent 128 characters.
- Later extended to 8 bits for compatibility with extended character sets.

**Advantages of ASCII:**

- **Simplicity:** Straightforward encoding with a limited set of characters.
- **Wide Compatibility:** Supported by most computers and devices.
- **Foundation for Text-Based Communication:** Essential for email, text files, programming, and the internet.

**Issues with ASCII:**

- **Limited Character Set:** Doesn't support characters from many languages, symbols, or emojis.
- **Potential for Misinterpretation:** Different systems might interpret non-ASCII characters differently, leading to text corruption.

**Beyond ASCII:**

- For broader language support, Unicode and its encodings like UTF-8 have become the global standard.
- However, ASCII remains important for understanding fundamental encoding principles and compatibility with legacy systems.

---

### UNICODE

Unicode is a universal character encoding standard that aims to represent all the writing systems of the world in a computer-friendly way. It does this by assigning a unique code point to each character, regardless of the language or platform it's used on. This allows different computers and software to process and display text consistently.

 **Unicode encodings:**

| Encoding | Description | 
|---|---| 
| **UTF-8** |  - Variable-width encoding using 1-4 bytes per character.   - Efficient for ASCII text (1 byte per character).   - Widely used on the web and in most operating systems. | 
| **UTF-16** |  - Variable-width encoding using 2 or 4 bytes per character.   - Often used internally in Windows and Java systems.   - Less efficient for ASCII text (2 bytes per character). | 
| **UTF-32** |  - Fixed-width encoding using 4 bytes per character.   - Simple to process but less space-efficient.   - Not as commonly used as UTF-8 or UTF-16. | 

**Other encodings:**

- **UCS-2:** An older fixed-width 2-byte encoding, now mostly replaced by UTF-16.
- **GB18030:** A Chinese encoding that can represent all Unicode characters.
- **UTF-7:** An encoding for use in email headers, but not recommended for general use.

**Key considerations for choosing an encoding:**

- **Compatibility:** UTF-8 is the most widely supported encoding, ensuring compatibility across different systems and software.
- **Space efficiency:** UTF-8 is generally more space-efficient than UTF-16 or UTF-32, especially for text that contains primarily ASCII characters.
- **Processing efficiency:** UTF-32 can be simpler to process in certain cases due to its fixed-width nature, but its larger size can impact performance.
- **Specific requirements:** Certain systems or applications may have specific requirements for encoding, such as UTF-16 in Windows environments.

**Examples of Unicode**

 Here's a table of the top 30 most useful Unicode symbols used in mathematics or computer science, along with their visual glyphs, Unicode codes, and descriptions:

| Glyph | Unicode Code | Description |
|---|---|---|
| ± | U+00B1 | Plus-minus sign (approximately, plus or minus) |
| ¬ | U+00AC | Not sign (negation) |
| √ | U+221A | Square root |
| ∛ | U+221B | Cube root |
| ∞ | U+221E | Infinity |
| ∠ | U+2220 | Angle |
| ∡ | U+2221 | Measured angle |
| ∢ | U+2222 | Spherical angle |
| ≈ | U+2248 | Approximately equal to |
| ≠ | U+2260 | Not equal to |
| ≤ | U+2264 | Less than or equal to |
| ≥ | U+2265 | Greater than or equal to |
| ∝ | U+221D | Proportional to |
| ∫ | U+222B | Integral |
| ∬ | U+222C | Double integral |
| ∭ | U+222D | Triple integral |
| ∇ | U+2207 | Nabla (vector differential operator) |
| ∂ | U+2202 | Partial differential |
| ∑ | U+2211 | Summation |
| ∏ | U+220F | Product |
| ∐ | U+2210 | Coproduct |
| ∅ | U+2205 | Empty set |
| ∈ | U+2208 | Element of |
| ∉ | U+2209 | Not an element of |
| ⊂ | U+2282 | Subset of |
| ⊃ | U+2283 | Superset of |
| ∪ | U+222A | Union |
| ∩ | U+2229 | Intersection |
| ∀ | U+2200 | For all |
| ∃ | U+2203 | There exists |
| ⇒ | U+21D2 | Implies |
| → | U+2192 | Right arrow (often used for function mapping) |


**Categories of Unicode**

Sure! Unicode is a universal character encoding standard that aims to represent all the writing systems of the world in a computer-friendly way. It does this by assigning a unique code point to each character, regardless of the language or platform it's used on. This allows different computers and software to process and display text consistently.

Here's a table of some of the main Unicode types and their descriptions:

| Type | Description |
|---|---|
| Cc | Control characters: These characters don't have a visible representation but are used to control formatting, such as tabs, newlines, and carriage returns. |
| Cf | Formatting characters: These characters have a visible representation but are used to modify the appearance of other characters, such as bold, italic, and underline. |
| Cn | Unassigned characters: These characters are currently not assigned to any specific character and may be used in the future for new characters or symbols. |
| Co | Private Use characters: These characters are reserved for private use by organizations or individuals and may not be interpreted consistently across different systems. |
| Cs | Surrogate characters: These characters are used in pairs to represent characters that require more than one code point, such as some emoji or complex CJK characters. |
| Ll | Lowercase letters: These are the standard lowercase letters of the alphabet, such as a, b, c, etc. |
| Lm | Modifier letters: These letters are used to modify the appearance of other letters, such as accents or diacritics. |
| Lo | Other letters: These are letters that don't fit into the other categories, such as Greek or Cyrillic letters. |
| Lt | Titlecase letters: These are letters that are capitalized in the middle of a word, such as Proper nouns. |
| Lu | Uppercase letters: These are the standard uppercase letters of the alphabet, such as A, B, C, etc. |
| Mn | Marks: These are non-spacing characters that are placed above or below other characters to modify their appearance, such as accents, diacritics, and combining vowel signs. |
| Mc | Spacing Combining Marks: These are combining marks that occupy their own space in the text, such as superscripts and subscripts. |
| Nd | Decimal Digit Numbers: These are the standard decimal digits 0 through 9. |
| Nl | Letter Number: These are characters that are used as both letters and numbers, such as Roman numerals. |
| No | Other Number: These are numbers that don't fit into the other categories, such as fractions or percentage signs. |
| Pc | Connector Punctuation: These are punctuation marks that are used to connect words or phrases, such as hyphens and commas. |
| Pd | Dash Punctuation: These are punctuation marks that are used to represent dashes, such as en dashes and em dashes. |
| Pe | Close Punctuation: These are punctuation marks that are used to mark the end of a phrase or sentence, such as parentheses, brackets, and braces. |
| Pf | Final Punctuation: These are punctuation marks that are used at the end of a sentence, such as periods, question marks, and exclamation points. |
| Pi | Initial Punctuation: These are punctuation marks that are used at the beginning of a phrase or sentence, such as quotes and colons. |
| Ps | Modifier Symbol: These are symbols that are used to modify the meaning of other characters, such as currency symbols and mathematical operators. |
| Sc | Currency Symbol: These are symbols that are used to represent currencies, such as the dollar sign (€) and the yen sign (¥). |
| Sk | Symbol: These are symbols that don't fit into the other categories, such as musical symbols and punctuation marks. |
| Sm | Math Symbol: These are symbols that are used in mathematics, such as plus (+), minus (-), and equal (=). |
| So | Other Symbol: These are symbols that don't fit into the other categories, such as emoji and pictographs. |
| Zl | Line Separator: These are characters that are used to separate lines of text, such as the newline character. |
| Zp | Paragraph Separator: These are characters that are used to separate paragraphs of text. |

---

## From Carving to Code

**The Ancient Inkwell: The Prehistory of Fonts (Before 15th Century)**

* **From Hieroglyphics to Handwriting:** Our journey begins with early writing systems like Egyptian hieroglyphics and Chinese calligraphy, where each character held individual meaning and artistic expression.
* **Scribe's Tools and Artistic Flourishes:** With the development of tools like quill pens and parchment, medieval scribes meticulously copied manuscripts, often embellishing them with decorative fonts and illuminations.

**Gutenberg's Spark: The Birth of Modern Typography (15th-19th Century)**

* **Movable Type Revolution:** Johannes Gutenberg's invention of the printing press in 1440 marked a turning point. Metal typefaces allowed for mass production of printed materials, standardizing and propagating specific font styles.
* **From Blackletter to Italic:** Early movable type fonts like Blackletter and Roman type dominated, later joined by humanist styles like Italic, emphasizing legibility and elegance.
* **Evolution of Design:** Over centuries, type design flourished, giving birth to iconic styles like Garamond, Baskerville, and Bodoni, each reflecting the artistic trends of their eras.

**Technological Transformations: The Digital Age of Fonts (20th-21st Century)**

* **The Digital Revolution:** The advent of computers in the 20th century ushered in a new era for fonts. Vector fonts, defined by mathematical curves, replaced bitmap fonts, enabling scalability and smoother rendering.
* **Software and Open Source:** Font creation tools like Adobe Illustrator and FontLab Studio empowered designers to develop even more diverse and specialized fonts. The open-source movement led to projects like Google Fonts, offering free and readily available fonts for non-commercial use.
* **Unicode and Global Communication:** The emergence of Unicode, a universal character encoding standard, allows fonts to encompass characters from various languages and scripts, paving the way for truly global communication through text.

**Google Fonts: Selecting Your Digital Palette**

* **A Vast Library:** Google Fonts is a treasure trove of over 1,400 open-source font families, catering to a wide range of styles and Unicode support.
* **Customization at Your Fingertips:** The easy-to-use interface allows you to choose fonts based on various parameters like size, weight, language, and theme, empowering you to tailor the typeface to your website's aesthetic and functionality.
* **Accessibility and Performance:** Google Fonts seamlessly integrates with your website, optimizing website loading speeds and ensuring accessibility for users with visual impairments.

**The Future of Fonts: A Canvas of Endless Possibilities**

* **AI-Powered Design:** Artificial intelligence is making inroads into font design, generating unique variations and adaptations based on existing styles.
* **Interactive and Contextual Fonts:** Dynamic fonts that change based on user interaction or context are emerging, potentially shaping the future of digital storytelling and communication.
* **A Universe of Characters:** As Unicode continues to expand, fonts will play a critical role in bridging language barriers and representing the diverse tapestry of human expression.

The history of fonts is a fascinating journey of human ingenuity and artistic expression, intertwined with technological advancements. Google Fonts stands as a testament to the democratization of design, providing an accessible platform for individuals and organizations to personalize their digital spaces with the richness of diverse typeface expressions.

---

## Non-Printable Fonts:

**Why not all Unicode characters are printable in all fonts?**

Unicode is a vast character encoding standard encompassing virtually all languages and symbols you can imagine. However, displaying such a diverse spectrum requires fonts to actually include the glyphs (visual representations) for these characters. Not all fonts are created equal:

* **Limited Character Sets:** Many common fonts, especially older ones, only support a subset of Unicode. They might miss less common languages, specialized symbols, or newer additions.
* **Incomplete Glyphs:** Even within their supported range, some fonts might lack individual glyphs. For example, a font may depict basic Cyrillic letters but miss rare punctuation marks.
* **Font Rendering Issues:** Rendering engines and operating systems can also play a role. Improper font rendering can lead to missing characters or garbled displays.

**Dejavu Sans Mono and Developer Fonts:**

* **Dejavu Sans Mono:** This open-source font family specifically targets developers. It boasts wide Unicode coverage, including private use areas used for custom symbols and compatibility with programming languages. It's well-regarded for its clean monospaced design and extensive glyph repertoire.
* **Other Notable Developer Fonts:**
    * **Fira Code:** Another popular option, known for its ligatures and programming language support.
    * **Source Code Pro:** A widely used font with excellent legibility and a clean aesthetic.
    * **Consolas:** A popular default font in many development environments, offering good Unicode coverage and readability.
    * **Iosevka:** A customizable font family with several variants, allowing users to tailor the typeface to their preferences.

**Benefits of Dev-Friendly Fonts:**

* **Improved Accuracy:** Developers can be confident that their code and documentation will display correctly across different platforms and tools.
* **Enhanced Communication:** Sharing code and symbols becomes easier without worrying about character compatibility issues.
* **Greater Efficiency:** Less time spent troubleshooting display issues and ensuring consistent visual representation.

Choosing the right font for developers depends on individual needs and preferences. Dejavu Sans Mono stands out for its comprehensive Unicode coverage and monospaced design, but other options cater to specific aesthetic or functional requirements. Ultimately, the ideal font should contribute to a productive and efficient development workflow.

---

## Open Source Fonts 

**Unleashing Creativity Without Copyright Constraints**

Open source fonts are those where the underlying design data is freely available for anyone to use, modify, and redistribute. This contrasts with traditional fonts, which are often restricted by commercial licenses. Here are some key benefits of open source fonts:

* **Free to Use:** No licensing fees or restrictions, making them ideal for personal and commercial projects alike.
* **Greater Customization:** Developers and designers can modify the fonts to suit their needs, creating unique variations or even entirely new fonts.
* **Collaboration and Innovation:** The open-source spirit fosters collaboration among designers, leading to a wider range of creative and diverse fonts.
* **Accessibility and Sustainability:** Open fonts ensure widespread availability and contribution to a thriving digital ecosystem.

**Top Open Source Fonts for Websites:**

1. **Roboto:** A versatile sans-serif family with multiple weights and styles, perfect for a clean and modern website aesthetic.
2. **Noto Sans:** Specifically designed for global legibility, supporting over 100 languages, ideal for multilingual websites.
3. **Fira Sans/Code:** A popular choice for developers and programming interfaces, offering excellent spacing and clarity for code blocks.
4. **Source Sans Pro:** A well-balanced sans-serif font with a friendly personality, suitable for various content types and contexts.
5. **Libre Baskerville:** A modern interpretation of the classic Baskerville typeface, adding elegance and sophistication to content-heavy websites.
6. **Inter:** A geometric sans-serif with clean lines and open counters, great for both body text and headlines.
7. **Merriweather:** A serif font with a warm and approachable feel, ideal for blog posts, articles, and long-form content.
8. **Open Sans:** A widely used neutral sans-serif, offering good legibility and a familiar feel for general website use.
9. **Montserrat:** A bold and dynamic sans-serif with playful geometric shapes, ideal for adding personality and emphasis.
10. **Raleway:** A versatile slab-serif font with a modern twist, offering a unique and impactful presence for headings and logos.

**Bonus Tip:** Check out Google Fonts, an extensive directory of open-source fonts with convenient sorting and filtering options to find the perfect match for your website!

Remember, the "best" fonts are subjective and depend on your website's specific needs and style. Explore these open-source options and let your creativity shine!

***

> "In the digital age, where pixels reign supreme, fonts are the brushstrokes that paint meaning onto the empty canvas of the screen." - _Ellen Lupton_, American graphic designer

