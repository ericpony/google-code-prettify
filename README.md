# Javascript code prettifier

Imported from http://code.google.com/p/google-code-prettify 
## Setup

1. [Download](http://code.google.com/p/google-code-prettify/downloads/list) a distribution
2. Include the script tag below in your document
        
<pre class="prettyprint">&lt;script src="https://google-code-prettify.googlecode.com/svn/loader/run_prettify.js"&gt;&lt;/script&gt;</pre>

3. See [Getting Started](http://code.google.com/p/google-code-prettify/wiki/GettingStarted) to configure that URL with options you need.</a>
4. Look at the [skin gallery](http://google-code-prettify.googlecode.com/svn/trunk/styles/index.html) and pick styles that suit you.

## Usage

Put code snippets in <tt>&lt;pre class="prettyprint"&gt;...&lt;/pre&gt;</tt> or <tt>&lt;code class="prettyprint"&gt;...&lt;/code&gt;</tt> and it will automatically be pretty printed.

## FAQ

### For which languages does it work?

The comments in <tt>prettify.js</tt> are authoritative but the lexer
    should work on a number of languages including C and friends,
    Java, Python, Bash, SQL, HTML, XML, CSS, Javascript, Makefiles,
    and Rust. It works passably on Ruby, PHP, VB, and Awk and a decent subset of Perl
    and Ruby. It doesn't work on Smalltalk because of commenting conventions.

Other languages are supported via extensions:
      [Apollo](http://code.google.com/p/google-code-prettify/source/browse/trunk/src/lang-apollo.js)
      [Basic](http://code.google.com/p/google-code-prettify/source/browse/trunk/src/lang-basic.js)
      [Clojure](http://code.google.com/p/google-code-prettify/source/browse/trunk/src/lang-clj.js)
      [CSS](http://code.google.com/p/google-code-prettify/source/browse/trunk/src/lang-css.js)
      [Dart](http://code.google.com/p/google-code-prettify/source/browse/trunk/src/lang-dart.js)
      [Erlang](http://code.google.com/p/google-code-prettify/source/browse/trunk/src/lang-erlang.js)
      [Go](http://code.google.com/p/google-code-prettify/source/browse/trunk/src/lang-go.js)
      [Haskell](http://code.google.com/p/google-code-prettify/source/browse/trunk/src/lang-hs.js)
      [Lisp, Scheme](http://code.google.com/p/google-code-prettify/source/browse/trunk/src/lang-lisp.js)
      [Llvm](http://code.google.com/p/google-code-prettify/source/browse/trunk/src/lang-llvm.js)
      [Lua](http://code.google.com/p/google-code-prettify/source/browse/trunk/src/lang-lua.js)
      [Matlab](http://code.google.com/p/google-code-prettify/source/browse/trunk/src/lang-matlab.js)
      [MLs:F#, Ocaml,SML](http://code.google.com/p/google-code-prettify/source/browse/trunk/src/lang-ml.js)
      [Mumps](http://code.google.com/p/google-code-prettify/source/browse/trunk/src/lang-mumps.js)
      [Nemerle](http://code.google.com/p/google-code-prettify/source/browse/trunk/src/lang-n.js)
      [Pascal](http://code.google.com/p/google-code-prettify/source/browse/trunk/src/lang-pascal.js)
      [Protocol buffers](http://code.google.com/p/google-code-prettify/source/browse/trunk/src/lang-proto.js)
      [R, S](http://code.google.com/p/google-code-prettify/source/browse/trunk/src/lang-r.js)
      [RD](http://code.google.com/p/google-code-prettify/source/browse/trunk/src/lang-rd.js)
      [Scala](http://code.google.com/p/google-code-prettify/source/browse/trunk/src/lang-scala.js)
      [SQL](http://code.google.com/p/google-code-prettify/source/browse/trunk/src/lang-sql.js)
      [TCL](http://code.google.com/p/google-code-prettify/source/browse/trunk/src/lang-tcl.js)
      [Latek](http://code.google.com/p/google-code-prettify/source/browse/trunk/src/lang-tex.js)
      [Visual Basic](http://code.google.com/p/google-code-prettify/source/browse/trunk/src/lang-vb.js)
      [CHDL](http://code.google.com/p/google-code-prettify/source/browse/trunk/src/lang-vhdl.js)
      [Wiki](http://code.google.com/p/google-code-prettify/source/browse/trunk/src/lang-wiki.js)
      [XQ](http://code.google.com/p/google-code-prettify/source/browse/trunk/src/lang-xq.js)
      [YAML](http://code.google.com/p/google-code-prettify/source/browse/trunk/src/lang-yaml.js).

If you'd like to add an extension for your favorite language, please look at <tt>src/lang-lisp.js</tt> and file an [issue](http://code.google.com/p/google-code-prettify/issues/list) including your language extension, and a testcase.

### How do I specify the language of my code?

You don't need to specify the language since `prettyprint()`
    will guess.  You can specify a language by specifying the language extension
    along with the `prettyprint` class like so:

    <pre class="prettyprint lang-html*">

  The **lang-*** class specifies the language file extensions.
  File extensions supported by default include
    "bsh", "c", "cc", "cpp", "cs", "csh", "cyc", "cv", "htm", "html",
    "java", "js", "m", "mxml", "perl", "pl", "pm", "py", "rb", "sh",
    "xhtml", "xml", "xsl".

You may also use the [HTML 5](http://dev.w3.org/html5/spec-author-view/the-code-element.html#the-code-element) convention of embedding a <tt>code</tt> element inside the `PRE` and using `language-java` style classes. E.g.
     
    <pre class="prettyprint"><code class="language-java">...</code></pre>
	 
### It doesn't work on obfuscated code sample?

Yes.  Prettifying obfuscated code is like putting lipstick on a pig&mdash;i.e. outside the scope of this tool.

### Which browsers does it work with?

It's been tested with IE 6, Firefox 1.5 &amp; 2, and Safari 2.0.4.
    Look at [the test page](tests/prettify_test.html) to see if it
    works in your browser.

### What's changed?

See the [ChangeLog](CHANGES.html).

### Why doesn't Prettyprinting of strings work on WordPress?

Apparently wordpress does "smart quoting" which changes close quotes. This causes end quotes to not match up with open quotes. This breaks prettifying as well as copying and pasting of code samples. See [WordPress's help center](http://wordpress.org/support/topic/125038) for info on how to stop smart quoting of code snippets.

### How do I put line numbers in my code?

You can use the `linenums` class to turn on line numbering.  If your code doesn't start at line number 1, you can add a colon and a line number to the end of that class. For example,

	<pre class="prettyprint linenums:4">

### How do I prevent a portion of markup from being marked as code?

You can use the `nocode` class to identify a span of markup that is not code.

    <pre class=prettyprint>
    int x = foo();  
    /* This is a comment  
    <span class="nocode">This is not code</span>
    Continuation of comment 
    */
    int y = bar();
    </pre>

For a more complete example see the issue22 [testcase](tests/prettify_test.html#issue22).

### I get an error message "a is not a function" or "opt_whenDone is not a function"

If you are calling `prettyPrint` via an event handler, wrap it in a function.
Instead of doing

    addEventListener('load', prettyPrint, false);

wrap it in a closure like

    addEventListener('load', function (event) { prettyPrint() }, false);

so that the browser does not pass an event object to `prettyPrint` which will confuse it.

### How can I customize the colors and styles of my code?

Prettify adds `<span>` with `class`es describing the kind of code. You can create CSS styles to matches these
classes. See the [theme gallery](http://google-code-prettify.googlecode.com/svn/trunk/styles/index.html) for examples.

### I can't add classes to my code (because it comes from Markdown, etc.)

Instead of `<pre class="prettyprint ...">` you can use a comment or processing instructions that survives processing instructions :
    
    <?prettify ...?>

works as explained in [Getting Started](http://code.google.com/p/google-code-prettify/wiki/GettingStarted)

### How can I put line numbers on every line instead of just every fifth line?

Prettify puts lines into an HTML list element so that line numbers aren't caught by copy/paste. The line numbering is controlled by CSS in the default stylesheet, "prettify.css".
