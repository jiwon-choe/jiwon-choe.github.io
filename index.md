---
layout: default
---

Hi! I am a 4th year PhD student in the Computer Science department at Brown University, 
co-advised by professors [Iris Bahar](https://vivo.brown.edu/display/rbahar) and [Maurice Herlihy](http://cs.brown.edu/~mph/).

My research interests are at the intersection of computer architecture and concurrent computing. 
I am particularly interested in the **hardware-software co-design** of **concurrent data structures and algorithms** with emerging memory technologies, such as **compute-capable memory** or **non-volatile memory**. 

[My CV can be found here](jiwonchoe-cv.pdf).


* * *

# research & publications

## Concurrent Data Structures with Near-Data-Processing

* Jiwon Choe, Amy Huang, Tali Moreshet, Maurice Herlihy, R. Iris Bahar. **Concurrent Data Structures with Near-Data-Processing: an Architecture-Aware Implementation**. In _31st ACM Symposium on Parallelism in Algorithms and Architectures (SPAA 2019)_. [[pdf](spaa19-choe.pdf)][[practice talk](https://youtu.be/trjnYpnq8t4)]
* Jiwon Choe, Tali Moreshet, Maurice Herlihy, R. Iris Bahar. **Hybrid Skiplists: Combining the Best of Near-Data-Processing and Lock-Free Algorithms**. _MICRO-52 Student Research Competition_. [[poster](micro19-poster-final.pdf)]

I am interested in improving the performance and energy efficiency of general-purpose concurrent data structures with _Near-Data-Processing (NDP)_. 

In the _SPAA '19_ paper, NDP-based concurrent data structures that leverage the flat-combining synchronization scheme were implemented and evaluated on [Brown-SMCSim](https://github.com/jiwon-choe/Brown-SMCSim), a cycle-accurate, full-system NDP architecture simulator. 
This yielded a more realistic and detailed performance, energy, and power analysis, compared to prior theoretical analysis. We showed that lightweight hardware modifications can significantly improve the performance and energy consumption of NDP-based concurrent data structures, even without any algorithmic changes. In many cases, the resulting data structures outperform state-of-the-art concurrent data structures.

More recently, I have been looking into how _"large yet cache-friendly"_ concurrent data structures can be integrated with NDP, in order to take advantage of concurrency, host processor cache locality, and computation near memory. The poster on **Hybrid Skiplists** summarizes the preliminary work in this direction. 


## Impact of Compute-Capable Memory on Memory-Hard Cryptographic Functions

* Jiwon Choe, Tali Moreshet, R. Iris Bahar, Maurice Herlihy. **Attacking Memory-Hard Scrypt with Near-Data-Processing** (extended abstract). In _The International Symposium on Memory Systems (MEMSYS 2019)_. [[pdf](memsys19-choe.pdf)][[practice talk](https://youtu.be/94dx7xmZBAM)]

The fact that memory access operations require much more time and energy than simple logic operations in a traditional DRAM-based main memory architecture is exploited to build time-consuming and power-hungry _memory-hard_ cryptographic functions, which serve the purpose of hindering brute-force security attacks. 

The security of these memory-hard functions depend entirely on the non-trivial costs of memory access. However, various compute-capable memory technologies have recently emerged as promising ways around the memory wall. As a preliminary investigation into how compute-capable memory can impact the security of memory-hard functions, we looked into _scrypt_, a widely-used memory-hard PBKDF, and how it can be accelerated with near-data-processing. 

* * *

# more about me

I received my Bachelor's degree in Electrical Engineering from Rice University (along with a dual degree in Computer Science). After Rice, I was at Oracle as a Software Engineer for 2.5 years, where I developed server hardware management tools. 

I am a recipient the [Cadence Women in Technology Scholarship](https://community.cadence.com/cadence_blogs_8/b/insights-culture/posts/the-cadence-women-in-technology-scholarship-winners). As part of the application, I wrote an essay about the challenges that I have faced as a female in STEM, and I recently found out that [the essay had been shared on the Cadence blog](https://community.cadence.com/cadence_blogs_8/b/on-the-beat/posts/insights-from-the-cadence-women-in-technology-scholarship-winners)! 
My story is not all that dramatic, but it is an honest reflection of how the discrimination towards women in STEM had misguided me in the past and how my own misperceptions may have harmed the community, even as a fellow woman. 

Other random fun facts about me:

I love writing -- yes, no joke! Not that it's not painful, but I love the feeling when my ideas and thoughts get written down and become a coherent story. 

I am also an avid coffee drinker. Some of my favorite coffee places are Bolt Coffee (Providence, RI), Borealis Coffee Company (Riverside, RI), Ritual Coffee Roasters (San Francisco, CA), Four Barrel Coffee (San Francisco, CA), and Devout Coffee (Fremont, CA).

<!---I received my Bachelor's degree from [Rice University](http://www.rice.edu/), where I studied Electrical Engineering and Computer Science. 
Before coming to Brown, I was at Oracle for 2.5 years, where I worked as a Software Engineer developing server hardware management tools. 

Text can be **bold**, _italic_, or ~~strikethrough~~.

[Link to another page](./another-page.html).

There should be whitespace between paragraphs.

There should be whitespace between paragraphs. We recommend including a README, or a file with information about your project.

# Header 1

This is a normal paragraph following a header. GitHub is a code hosting platform for version control and collaboration. It lets you and others work together on projects from anywhere.

## Header 2

> This is a blockquote following a header.
>
> When something is important enough, you do it even if the odds are not in your favor.

### Header 3

```js
// Javascript code with syntax highlighting.
var fun = function lang(l) {
  dateformat.i18n = require('./lang/' + l)
  return true;
}
```

```ruby
# Ruby code with syntax highlighting
GitHubPages::Dependencies.gems.each do |gem, version|
  s.add_dependency(gem, "= #{version}")
end
```

#### Header 4

*   This is an unordered list following a header.
*   This is an unordered list following a header.
*   This is an unordered list following a header.

##### Header 5

1.  This is an ordered list following a header.
2.  This is an ordered list following a header.
3.  This is an ordered list following a header.

###### Header 6

| head1        | head two          | three |
|:-------------|:------------------|:------|
| ok           | good swedish fish | nice  |
| out of stock | good and plenty   | nice  |
| ok           | good `oreos`      | hmm   |
| ok           | good `zoute` drop | yumm  |

### There's a horizontal rule below this.

* * *

### Here is an unordered list:

*   Item foo
*   Item bar
*   Item baz
*   Item zip

### And an ordered list:

1.  Item one
1.  Item two
1.  Item three
1.  Item four

### And a nested list:

- level 1 item
  - level 2 item
  - level 2 item
    - level 3 item
    - level 3 item
- level 1 item
  - level 2 item
  - level 2 item
  - level 2 item
- level 1 item
  - level 2 item
  - level 2 item
- level 1 item

### Small image

![Octocat](https://assets-cdn.github.com/images/icons/emoji/octocat.png)

### Large image

![Branching](https://guides.github.com/activities/hello-world/branching.png)


### Definition lists can be used with HTML syntax.

<dl>
<dt>Name</dt>
<dd>Godzilla</dd>
<dt>Born</dt>
<dd>1952</dd>
<dt>Birthplace</dt>
<dd>Japan</dd>
<dt>Color</dt>
<dd>Green</dd>
</dl>

```
Long, single-line code blocks should not wrap. They should horizontally scroll if they are too long. This line should be long enough to demonstrate this.
```

```
The final element.
```
--->
