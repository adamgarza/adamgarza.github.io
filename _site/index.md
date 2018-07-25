
![Google Summer of Code](https://developers.google.com/open-source/gsoc/resources/downloads/GSoC-logo-horizontal.svg)
&nbsp;&nbsp; ![OpenCensus](img/opencensus_logo.svg)

<br />

## Migrate OpenCensus.io into HUGO markdown theme + Develope OpenCensus Zpages UI

---
### What is OpenCensus
OpenCensus is single distribution of libraries that automatically collects traces and metrics from your app, displays them locally, and sends them to any analysis tool.

---
<br />
## Table of Content

### 1. [Migrate OpenCensus.io into a HUGO markdown theme](#migrate)
 * 1.1 [The Commits](#migrate-commits)

### 2. [Develope OpenCensus Zpages UI](#zpages)
 * 1.1 [The Commits](#zpages-commits)
 
### 3. [Overall Experience](#experience)

### 4. [Final Thoughts](#final)
<br />

---
 
<br />

<a id="migrate"></a>
### 1. Migrate OpenCensus.io into a HUGO markdown theme
The various OpenCensus development teams were in need of a fast and easy method to add and update their corresponding section of documenation on the OpenCensus.io website. The use of markdown allows them to do so with ease. Markdown would allow them to add new pages and/or edit existing page content in plain text using any text editor. This liberates the developers and the opensource contributing community from cumbersome HTML modifications, allowing them to focus on the quality and accuracy of content.

I proposed converting the existing HTML OpenCensus.io website into a HUGO markdown theme. Prior to GSoC2018, I have never worked in markdown, much less know anything about the satic site generator platform of HUGO. I accepted this as a programming challenge and had to quickly learn it on the fly.

#### Challenges in Migration
At Web Development I'm a wiz, so I thought "Hey, I can do this easily." In reallity, it took me close to 3 weeks just to capture a good understanding of the HUGO directory structure, and how to implement best practices. With the use of heavy JavaScript on the original site, I attempted to use a combination of markdown and shortcode to properly rendor the site.  

<a id="migrate-commits"></a>
#### Website Commits

Dates | Commit Description  |
----------------| --------------------|
May 9, 2018     | [LICENSE and AUTHORS added (#65)](https://github.com/census-instrumentation/opencensus-website/commit/fd1d0a62d653b2fece03190687c2b44487d19ae0) |
May 16, 2018    | [Updated blog posts (#66)](https://github.com/census-instrumentation/opencensus-website/commit/add8c9913cb0c45a7a095c75297543a3ae3b641a) |
May 26, 2018    | [Modified Docs, Overview, Roadmap and created GogRPC (#68)](https://github.com/census-instrumentation/opencensus-website/commit/c212cef05ddc9efadfa821c891dee048ae02241e)|
Jun 4, 2018     | [Initial PR for Hugo theme - markdown (#69)](https://github.com/census-instrumentation/opencensus-website/commit/fd4a91371cb221483db8c75964321f5876f17ed9) |
Jun 6, 2018     | [Updated README, modified docs.md for improved mobile rendering, cleaned shortcodes (#80)](https://github.com/census-instrumentation/opencensus-website/commit/cd66fcf0db2bce8815c873db6853030b967c07e6) |
Jun 8, 2018     | [Optimizing Docs, FAQ & Roadmap pages for mobile (#81)](https://github.com/census-instrumentation/opencensus-website/commit/d9fb4b09c32d844c8c0932edd35380a0c20fc396) |
Jun 11, 2018    | [Added partners/branding + github-corner disappears on mobile view (#84)](https://github.com/census-instrumentation/opencensus-website/commit/81248096613ed386d87349ae36fbdb20f01037b7) |
Jun 12, 2018    | [Landing navbar fix (#85)](https://github.com/census-instrumentation/opencensus-website/commit/4db4c343066ca6d51bbbeb801cf3e8a031da4629) |
Jun 13, 2018    | [Thinned out navbar & shrunk banner height on landing (#89)](https://github.com/census-instrumentation/opencensus-website/commit/6b2d0e69e5f54cda133d213c57db066826c23247) |
Jun 14, 2018    | [Updated README Hugo version and pointing tutorials link to spanner (#90)](https://github.com/census-instrumentation/opencensus-website/commit/da81c9e29fa79a31a99162231bb23d43a7aeb108) |
Jun 14, 2018    | [New Blog entry & some CSS to help (#91)](https://github.com/census-instrumentation/opencensus-website/commit/5380dbf0da4a3659014423cbd894499b2447adbc) |
Jun 16, 2018    | [added new blog entry, and link to the same blog on the overview page (#92)](https://github.com/census-instrumentation/opencensus-website/commit/aea30970c2390826049d62d7705b8588a635fc06) |
Jun 16, 2018    | [Shifted Nic Munroe blog link to top of Overview page (#93)](https://github.com/census-instrumentation/opencensus-website/commit/1b4ee3130c5454da7b01de19339551366dd7f31a) |
Jun 19, 2018    | [Added Ben Ripkens quote to top of Index and removed the last sentence in About - Who is behind OpenCensus (#97)](https://github.com/census-instrumentation/opencensus-website/commit/0ff791409eafa9abe9bf7b8f48e99a04653284a2) |
Jun 19, 2018    | [Dropped Ben Ripkens name down to new line (#98)](https://github.com/census-instrumentation/opencensus-website/commit/fad5343d1b49d66979c770c125d3d192f7231ed7) |
Jul 9, 2018     | [Fixed licensing on the footer to reflect Apache License 2.0 (#163)](https://github.com/census-instrumentation/opencensus-website/commit/06badd9f5d836904d1d7e2e214a5d50e2d32fb17) |
Jul 12, 2018    | [Added Datadog logo to partners & contributors section (#165)](https://github.com/census-instrumentation/opencensus-website/commit/8d807664cffd0dc7486c4aef2883eeded8a84872) |
Jul 13, 2018    | [Updated Who is Behind OC and added Microsoft+Solarwinds to partners section on index, added new blog entry (#168)](https://github.com/census-instrumentation/opencensus-website/commit/64e58db1cec24d6b0e088bdc9b59e39a88e090da) |
Jul 13, 2018    | [Replaced markup with markdown in blog.md (#170)](https://github.com/census-instrumentation/opencensus-website/commit/75a82b1c9590256dfb9bdc4413b8e5b6f19151ab) |
Jul 16, 2018    | [Updated node.js stats as supported on languages table (#177)](https://github.com/census-instrumentation/opencensus-website/commit/701f94daaa6358b9551ab2da40298e8e89bf5a24) |
Jul 19, 2018    | [Included svg images for Stackdriver, Zipkin, Jaeger and Prometheus logos (#181)](https://github.com/census-instrumentation/opencensus-website/commit/90feb88ad200230914748d78c2cea4375af3b31b) |
Jul 19, 2018    | [All partner logos have been replaced with high quality images (#183)](https://github.com/census-instrumentation/opencensus-website/commit/dfa74dcdf237d31f9a31ab3ee01e48601072e42c) |

[Commit list Authored by Adam Garza](https://github.com/census-instrumentation/opencensus-website/commits?author=adamgarza)
<br/>

<a id="zpages"></a>
### 2. Develope OpenCensus Zpages UI

#### What are Zpages?
In OpenCensus, zpages implements a collection of HTML pages that display RPC stats and trace data. My task was to standardize the look and feel of the multiple zpages.
1. Rpcz
2. Statsz
3. Tracez
4. Traceconfigz

To acheive the base UI, I began work on the most complete set of Zpages built in Java. But, since OpenCensus will support multiple languages, I had to also create an external CSS of commonalities among the variaous zpages to be used across all languages. Basically, we need the zpages for all the supported languages to look and feel the same. To save myself from having to style each of the four zpages for every language supported, a single external CSS can acheive this, as well as, making changes in a single location very accommodating.

#### Chalenges in Zpages
Some challenges I came across while working on the Zpages was the unique structure of the numerous tables used among the four Zpages. Just as everyone has a distinct writing style, so do programmers. I quickly learned that Open Source Development is a collaborative effort, and every contributor has a unique programming style.

Yet, another challenge I faced while styling the Zpages was how to properly implement an external resource such as a CSS, and use a Gradle build for resource availability. As you can see in the snippets of code below, I was able to build the resource with Gradle, and it is available to the rpcz handler (with help from a mentor). Although, I 

Gradle build lines added:
```
sourceSets.main.resources.srcDirs = [ "src/resources/" ]
sourceSets.main.resources.includes = [ "**/*.css" ]
```

Java rpcz handler lines added:
```java
private static final String CSS_PATH =
        "/Users/username/Desktop/opencensus-java" +
        "/contrib/zpages/src/resources/style.css";
```

Java method for reading in the CSS:
```java
private static final String STYLE;
  static {
    String style = "";
    try {
      Reader fileReader = Files.newBufferedReader(Paths.get(CSS_PATH), UTF_8);
      char[] chars = new char[100000000];
      fileReader.read(chars);
      style = String.valueOf(chars);
    } catch (Exception e) {
      e.getMessage();
    }
    STYLE = style;
  }
  ```
<br />

<a id="zpages-commits"></a>
#### Zpage Commits

Dates | Commit Description  |
----------------| --------------------|
Jun 10, 2018    | [Rpcz, Statsz, Tracez, and Traceconfigz page styling modifications (#1295)](https://github.com/census-instrumentation/opencensus-java/commit/2d1e5c8486bbb5f1101a057d7e044dc60f80a50d)

<br />

---
<br />
<a id="experience"></a>
## Overall Experiance 
Prior to my participation in Google Summer of Code 2018, I had no experience with and in some cases have never heard of the platforms, programs or concepts used in Open Source Development. Things like Markdown, HUGO platform, Git and Github, and colaborative development were all forgien to me. Knowing that I might struggle throughout much of this summer program, I chose to dive into it... as an effort to breakout of my comfort zone and force myself to quickly learn and adapt.

<br />

<a id="final"></a>
## Final Thoughts
I am not much of a write, but I will try to make this as elequent as possible. In full disclosure, knowing this program is such an enormouse opportunity for me as a new developers, I'm certain I placed an overwhelming pressure upon myself to acheive. I've always considered myself a below average programmer, as I often need to reference outside resources to complete certain tasks. Although, what I lack in know-how, I more make up for in determination.  It was stressful, chalLenging, and rewarding for sure.  We all have goals and dreams and my participation in Google Summer of Code 2018 gets me one step closer to realizing that dream.

>Many have made great sacrifices in order for me to have the oppotunities I have today. There is no better way to repay those sactifices, than to acheive when those opportunities are presented, making things better for those generations who follow behind me.

\- Adam Garza