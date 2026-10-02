# Welcome to My Levenshtein Web
***

## Task
The goal of this project is to build a web page that computes the Levenshtein distance between two strings.
The Levenshtein distance is the minimum number of single-character edits (insertions, deletions or substitutions) needed to turn one string into the other.
The challenge lies in implementing the algorithm correctly in JavaScript and presenting the result clearly in the browser, including the edge cases (empty strings, identical strings, strings of very different lengths).

## Description
I solved this problem by separating the algorithm from the interface:
- **Algorithm** : a JavaScript function builds a matrix of size `(len(a) + 1) x (len(b) + 1)` using dynamic programming. Each cell holds the minimum of an insertion, a deletion or a substitution, and the bottom-right cell is the distance.
- **Edge Cases** : if one string is empty, the distance is the length of the other. If both strings are equal, the distance is `0`.
- **User Interface** : an HTML form with two text fields and a button lets the user enter the strings and run the computation.
- **Result Display** : the distance is shown on the page as soon as the user submits the strings, without reloading.
- **Styling** : the layout is written in plain CSS and adapts to different screen sizes.
- **Input Handling** : the page reads the fields, handles empty inputs, and updates the result when the values change.

## Installation
The project runs entirely in the browser, so no compilation is needed.
1. Get the project :
```bash
git clone [REPOSITORY_URL]
cd my_levenshtein_web
```

2. Open the page directly in a browser :
```bash
open index.html
```

3. Or serve it locally (optional) :
```bash
python3 -m http.server 8000
```
Then visit `http://localhost:8000` in your browser.

## Usage
Enter two strings in the fields and click the button. The page displays the Levenshtein distance between them.

**Examples :**

| String 1 | String 2 | Distance |
|----------|----------|----------|
| `kitten` | `sitting` | 3 |
| `flaw` | `lawn` | 2 |
| `abc` | `abc` | 0 |
| `` (empty) | `abc` | 3 |
| `abc` | `` (empty) | 3 |

**Explanation of `kitten` → `sitting` (3 edits) :**
1. `kitten` → `sitten` (substitute `k` with `s`)
2. `sitten` → `sittin` (substitute `e` with `i`)
3. `sittin` → `sitting` (insert `g`)

### The Core Team


<span><i>Made at <a href='https://qwasar.io'>Qwasar SV -- Software Engineering School</a></i></span>
<span><img alt='Qwasar SV -- Software Engineering School's Logo' src='https://storage.googleapis.com/qwasar-public/qwasar-logo_50x50.png' width='20px' /></span>
