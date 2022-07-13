---
layout: default
---

Hello! I am a recent PhD grad from the Computer Science department at Brown University.
During my PhD, I was co-advised by professors [Iris Bahar](https://people.mines.edu/ribahar/) and [Maurice Herlihy](http://cs.brown.edu/~mph/).

My doctoral research was focused on the **hardware-software co-design** of **concurrent data structures** with **near-memory processing (NMP)** architectures.
This was a challenging problem, for the **NMP-aware data structures** had be carefully designed to preserve the high concurrency, correctness guarantees, and at times high on-chip cache locality provided by existing data structures which are highly optimized for conventional architectures. At the same time, they must take full advantage of the features and work around the challenges introduced by the new architecture. 

I am now a software engineer at Apple. I am part of a team that builds SoC simulations for Apple hardware-- if you are interested in joining our team, please send me an email with your resume.


* * *

# publications

#### Concurrent Data Structures with Near-Memory Processing
* Jiwon Choe, Andrew Crotty, Tali Moreshet, Maurice Herlihy, R. Iris Bahar. **HybriDS: Cache-Conscious Concurrent Data Structures for Near-Memory Processing Architectures**. In _34th ACM Symposium on Parallelism in Algorithms and Architectures (SPAA 2022)_. [[pdf](spaa2022-choe.pdf)]
* Jiwon Choe, Amy Huang, Tali Moreshet, Maurice Herlihy, R. Iris Bahar. **Concurrent Data Structures with Near-Data-Processing: an Architecture-Aware Implementation**. In _31st ACM Symposium on Parallelism in Algorithms and Architectures (SPAA 2019)_. [[pdf](spaa19-choe.pdf)][[practice talk](https://youtu.be/trjnYpnq8t4)]

In the SPAA '19 paper, NMP-based concurrent data structures that leverage the flat-combining synchronization scheme were implemented and evaluated on [Brown-SMCSim](https://github.com/jiwon-choe/Brown-SMCSim), a cycle-accurate, full-system NMP architecture simulator. 
This yielded a more realistic and detailed performance, energy, and power analysis, compared to prior theoretical analysis. We showed that lightweight hardware modifications can significantly improve the performance and energy consumption of NMP-based concurrent data structures, even without any algorithmic changes. In many cases, the resulting data structures outperform state-of-the-art concurrent data structures.

The SPAA '22 paper addresses the limitation of NMP-based data structures found in the SPAA '19 paper. Hierarchical data structures that benefit from on-chip cache locality could result in reduced performance when all pointer-chasing activity is offloaded to near-memory compute units of the NMP architecture. In the SPAA '22 work, we present **NMP-hybrid** algorithms of such hierarchical data structures, which take advantage of both the on-chip cache locality of hierarchical data structures and the benefits of NMP architecture.


#### Impact of Compute-Capable Memory on Memory-Hard Cryptographic Functions

* Jiwon Choe, Tali Moreshet, R. Iris Bahar, Maurice Herlihy. **Attacking Memory-Hard Scrypt with Near-Data-Processing** (extended abstract). In _The International Symposium on Memory Systems (MEMSYS 2019)_. [[pdf](memsys19-choe.pdf)][[practice talk](https://youtu.be/94dx7xmZBAM)]

The fact that memory access operations require much more time and energy than simple logic operations in a traditional DRAM-based main memory architecture is exploited to build time-consuming and power-hungry _memory-hard_ cryptographic functions, which serve the purpose of hindering brute-force security attacks. 

The security of these memory-hard functions depend entirely on the non-trivial costs of memory access. However, various compute-capable memory technologies have recently emerged as promising ways around the memory wall. As a preliminary investigation into how compute-capable memory can impact the security of memory-hard functions, we looked into _scrypt_, a widely-used memory-hard PBKDF, and how it can be accelerated with near-memory processing. 

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
