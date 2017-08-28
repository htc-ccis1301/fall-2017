---
title: "DOM Relationships Puzzle"
summary: "Practice identifying relationships in the Document Object Model (DOM)."
---

# {{ page.title }}
{{page.summary}}


## Prerequisites
This practice exercise requires an understanding of the material from:
- [HTML Document Structure]({{ "/readings/intro-dom.html " | prepend: site.baseurl }})

## DOM Crossword Puzzle
Complete the crossword puzzle below using the following HTML.  Make a note of the answers to submit in the DOM Relationships Puzzle "quiz" on D2L.

A [PDF version]( {{ "/assets/files/intro-dom-puzzle/DOMRelationshipsPuzzle.pdf " | prepend: site.baseurl }} ) is available for those who would like to print the puzzle.

### Reference HTML
{% include alert.html type="info"
    content="Note that this HTML page uses tags that have not been introduced yet, but don't let that distract you!  You don't need to understand what an element does in order to determine its relationships to other elements in the DOM."
%}

{% gist mbMosman/5785c6e9534e956b79d7 domPuzzle.html %}

### Puzzle
{% include img-medium.html url="/assets/images/intro-dom-puzzle/domPuzzle.png"
      alt="DOM Crossword Puzzle - See hints below."
%}

<div style="padding:10px">
  <div class="row">
    <div class="col-xs-12 col-md-6">
        <h4>Across</h4>
        <p>
          2. child of p<br>
          4. relationship of li to ul<br>
          5. number of link's siblings<br>
          6. name of footer's child<br>
          9. first child of head<br>
          11. last child of body<br>
          12. first child of html
        </p>
    </div>
    <div class="col-xs-12 col-md-6">
        <h4>Down</h4>
        <p>
          1. parent of favs<br>
          2. relationship shared by title, meta, and link<br>
          3. relationship of charset to meta<br>
          7. child of header<br>
          8. Root element for every HTML page<br>
          9. number of body's children<br>
          10. sibling of head
        </p>
    </div>
  </div>
</div>

## Submit
Once you have finished the puzzle, make sure to enter your answers in the DOM Relationships Puzzle "quiz" on D2L to check your answers and get credit for the assignment.  
