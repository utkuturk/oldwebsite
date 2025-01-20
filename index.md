---
layout: page
title:
permalink: /
---
<!-- change font color -->

<link rel="stylesheet" href="/css/fontawesome/css/all.css" >
<link rel="stylesheet" href="css/academicons/css/academicons.min.css"/>


{%
  include image.html
  url="images/utkuturkumd.jpeg"
  caption="<font size = 2px>e-mail: firstnamelastname@umd.edu <br><a href='/files/cv.pdf'> <i>Full CV as PDF</i> </a><br><a href='https://twitter.com/UtkuTurkLing'>[twitter]</a> | <a href='https://bsky.app/profile/utkuturk.com'>[bsky]</a> | <a href='https://scholar.google.com/citations?hl=tr&user=wa7LG9gAAAAJ'>[scholar]</a> | <a href='https://github.com/utkuturk'>[github]</a></font>"
  href="/files/cv.pdf"
  href="https://twitter.com/UtkuTurkLing"
  href="https://bsky.app/profile/utkuturk.com"
  href="https://scholar.google.com/citations?hl=tr&user=wa7LG9gAAAAJ"
  href="https://github.com/utkuturk"
  width="330px"
  align="right"
%}

<br>

I am a third year Ph.D. student in <a href='https://linguistics.umd.edu/'>linguistics</a> at <a href='https://umd.edu/'>University of Maryland</a>, working  with <a href='https://www.colinphillips.net/'>Colin Phillips</a> and <a href='https://ellenlau.net/'>Ellen Lau</a>. My main <a href='https://www.utkuturk.com/research/'>research interests</a> are in morphology and psycholinguistics, both comprehension and production.

Before UMD, I completed my masters at <a href='https://linguistics.boun.edu.tr'>Bogazici University Linguistics</a>, where I worked with <a href='https://scholar.google.com/citations?user=fhbdTJIAAAAJ&hl=en'>Pavel Logačev</a> and write my thesis titled <a href='https://www.utkuturk.com/ma/'>Agreement Attraction in Turkish</a>.

I also visited <a href = 'https://www.muni.cz/en'>Masaryk University</a> where I worked with <a href = 'https://scholar.google.cz/citations?user=-T030GMAAAAJ&hl=no'>Pavel Caha</a> on Turkish case morphology and adjectival decomposition.


<br><br>

<h2 class="news-header">News</h2>

<div class="news-container">
  <ul>
    {% for item in site.data.cv.news %}
      <li>
        <span class="date"><strong>{{ item.date }}:</strong></span>
          {{ item.description }}
          {% if item.hlink %} <a href="{{ item.hlink }}"> [handout] </a> {% endif %}
          {% if item.slink %} <a href="{{ item.slink }}"> [slides] </a> {% endif %}
          {% if item.pdf %} <a href="{{ item.pdf }}"> [pdf] </a> {% endif %}
          {% if item.extra %} {{ item.extra }} {% endif %}
      </li>
    {% endfor %}
  </ul>
</div>

<style>
  .news-container {
    width: 90%;
    height: 300px;
    overflow-y: auto;
    border: 1px solid #ccc;
    margin: 20px auto;
    padding: 20px;
    box-shadow: 5px 5px 10px rgba(0, 0, 0, 0.2);
  }

  .news-header {
    text-align: center;
    margin-bottom: 15px;
  }

  .news-container ul {
    list-style-type: square;
    padding-left: 20px;
  }

  .news-container li {
    margin-bottom: 10px;
    display: flex; /* Use flexbox for layout */
  }

  .date {
    flex: 0 0 120px; /* Set a fixed width for the date */
  }

  /* Custom scrollbar styles */
  .news-container::-webkit-scrollbar {
    width: 4px;
  }

  .news-container::-webkit-scrollbar-track {
    background: #f1f1f1;
  }

  .news-container::-webkit-scrollbar-thumb {
    background: #888888;
    border-radius: 4px;
  }
</style>

{% include image.html url="images/bosphorous.jpg" caption="view of bosphrous and kennedy lodge, photo by me, aug 18" width="800px" align="middle" %}

<!--
In my freetime, I usually play games on [Steam][steam] or take amateur [photographs][flickr]. My favorite food is [gata][gata] with koritz and my favorite icecream flavor is [saffron and rose][rose]. -->



  [cal]:   resources/calligraphy/
  [thesis]: ma/
  [glide]:  2022/130/glide.html
  [sa]:     research/sa/
  [case]:   research/case/
  [aug]:    research/aug/
  [hc]:     2022/130/as-if.html
  [trlazud]: research/trlazud/
  [grtr]:   research/grtr/
  [deepl]:  research/deepl/
  [taship]: teaching.md
  [dept]:   https://linguistics.boun.edu.tr
  [umdling]: https://linguistics.umd.edu/
  [langsci]: http://languagescience.umd.edu
  [ellen]: https://ellenlau.net/
  [uni]:    http://www.boun.edu.tr
  [pavel]:  https://scholar.google.com/citations?user=fhbdTJIAAAAJ&hl=en
  [colin]:  https://www.colinphillips.net/
  [gata]:   https://en.wikipedia.org/wiki/Gata_(food)
  [rose]:   https://explorepartsunknown.com/koreatown-la/koreatown-perfect-day/
  [steam]:  https://steamcommunity.com/id/lecagot
  [flickr]: https://flickr.com/photos/97029582@N03/albums
  [caha]:   https://www.muni.cz/en/people/53172-pavel-caha/cv
  [mas]:    https://www.muni.cz/en
  [ud]:     https://www.universaldependencies.org
  [cv]:     files/cv.pdf
  [manu]:   https://github.com/utkuturk/tr_bias/blob/master/paper/draft/manuscript.pdf
  [o]:      https://en.wikipedia.org/wiki/Gender_neutrality_in_genderless_languages#Turkish
  [twitter]:https://www.twitter.com/utkuturkling
  [tfj]:    https://translateforjustice.wordpress.com/
  [gezi]:   https://en.wikipedia.org/wiki/Gezi_Park_protests


<!--

- 🌱 <span style="text-decoration: underline">learning</span>
  - *stan & multinomial processing trees*
  - *horseshoe priors and sparsity*<br><br>


**utkuturk/utkuturk** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
