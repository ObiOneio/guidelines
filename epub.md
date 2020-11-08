##
# Guidelines for Creating Accessible EPUB 3 Files for the GDL platform

### 1. All text must be available in a logical reading order

Text must not be presented as images, be reordered by CSS, or require scripting to be accessed. Use structural markup to define the natural reading order of the primary narrative and to distinguish secondary material such as footnotes, references, figures, and other auxiliary content.

### 2. Separate presentation and content

Visual reading is only one way of accessing content. Do not use visual-only cues such as colored text, font size or positioning as the only clue to the meaning or importance of a word or section. Do not use tables or pictures of text to control the appearance of the content. The meaning of the content should be the same both with and without any styles or formatting applied.

### 3. Provide complete navigation

Include a complete table of contents in the front matter and consider smaller tables of contents at the start of each section. Use \&lt;section\&gt; and \&lt;aside\&gt; tags in the content and the \&lt;itemref linear=&quot;no&quot;\&gt; tag in the manifest file to define a logical reading order. This is particularly important for academic, educational, and other complex texts.

### 4. Create meaningful structure wherever possible

Create a structure by using numbered headings in a logical structure. For other tagged structures, specify their content with the epub:type attribute. For example, the tag that contains the preface of a book might look like \&lt;section epub:type=&quot;preface&quot;\&gt;. Specific tags are for specific content only (i.e., the \&lt;cite\&gt; tag is only for citations) and should be used according to the standard. Use the most specific tag available and do not automatically wrap \&lt;div\&gt; or \&lt;span\&gt; tags around everything.

### 5. Define the content of each tag

Include semantic information to describe the content of a tag. A section tag for the table of contents would look like \&lt;section epub:type=&quot;toc&quot;\&gt; or a list of definitions in a glossary would be tagged with \&lt;dl epub:type=&quot;glossary&quot;\&gt;. Use the EPUB 3 Structural Semantics Vocabulary as defined at (http://idpf.org/epub/vocab/structure/) to identify content.

### 6. Use images only for pictures, not for tables or text

Any content embedded in an image is not available to visually impaired readers. If the textual contents of a table or image are required for comprehension of the document, use proper and complete markup for text and tabular data, including headers and scope attributes for tables. If images of text are unavoidable, provide a description and transcription of the text and use [accessible SVG](http://www.w3.org/2000/10/wcag2-svg-techs-020318). Accessible SVG graphics allow text in images to be rendered in an accessible way. They can also make it possible to deliver tactile images electronically to blind users with appropriate devices or to help automate the creation of tactile images that can be mailed to the reader with minimum human intervention.

### 7. Use image descriptions and alt text

Every image should have a description, caption or alt text unless it is solely decorative. See the [DIAGRAM Center Image Guidelines for EPUB 3](http://diagramcenter.org/standards-and-practices/59-image-guidelines-for-epub-3.html)for mark up best practices.

### 8. Include page numbers

Page numbers are the way many people navigate within a book. For any book with a print equivalent, use the epub:type=&quot;pagebreak&quot; attribute to designate page numbers. Include the ISBN of the source of the page numbers in the package metadata for the book. A tag for a page number might look like \&lt;span xml:id=&quot;page361″ epub:type=&quot;pagebreak&quot;\&gt;361\&lt;/span\&gt;.

### 9. Define the language(s)

To make sure each word will be rendered correctly, specify the default language of the content in the root html tag. Indicate any words, phrases or passages in a different language by using the xml:lang attribute: \&lt;span xml:lang=&quot;fr&quot; lang=&quot;fr&quot;\&gt;rue Saint-Andre-des-Arts\&lt;/span\&gt;.

### _10. Use MathML_

MathML makes mathematical equations accessible to everyone by eliminating the ambiguity of a verbal description of a picture. There are many tools available to support MathML creation.

### _11. Provide alternative access to media content_

Make sure the native controls for video and audio content are enabled by default. Provide fallback options such as captions or descriptions for [video](http://www.idpf.org/accessibility/guidelines/content/xhtml/video.php) and transcripts for [audio](http://www.idpf.org/accessibility/guidelines/content/xhtml/audio.php).

### 12. [Make interactive content accessible](http://www.idpf.org/accessibility/guidelines/)

Interactive content using JavaScript or SVG should be accessible. All custom controls should fully implement ARIA roles, states, and properties, as appropriate.

### 13. [Use accessibility metadata](http://www.a11ymetadata.org/)

As part of a general good practice of documenting the accessibility of your content, provide accessibility metadata in your files so end users know what features are there and search engines can discover your accessible materials.

The GDL standard metadata includes 4 separate properties for Accessibility.

### 14. Make sure your processes support the above best practices

- Initiate a sustained project-wide effort to make accessibility a core value in the production and dissemination of content, including development of a company policy statement to express the accessibility commitment.
- Develop and implement accessibility guidelines and training for authors.
- Develop and implement accessibility guidelines and training for editorial and production staff.
- Discuss accessibility requirements and standards with vendors.
- Include an accessibility review in the quality-assurance process.
- Include accessibility information on your website and appropriate marketing materials.
- Add accessibility awareness training for customer service staff.

This work is a derivative of &quot;Top Tips for Creating Accessible EPUB 3 Files&quot; by DIAGRAM Center and Benetech, used under [CC BY-NC 2.5](https://creativecommons.org/licenses/by-nc/2.5/) . This work is licensed under [CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/) by The Global Digital Library.
