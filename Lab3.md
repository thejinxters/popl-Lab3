# Answers to Questions for Labe 3

#### 1. JavaScripty Interpreter: Tag Testing, Recursive Functions, and Dynamic Scoping.

  <em> Give one test case that behaves differently under dynamic scoping versus static scoping (and does not crash). Explain the test case and how they behave differently in your write-up. </em>

  Answer to question 1 goes here
  ```javascript
  function container(){

    function f1(){
      var x = 2;
      f2();
    }

    function f2(){
      console.log(x);
    }

    x = 3;
    f1();

  }
  ```

#### 2. JavaScripty Interpreter: Substitution and Evaluation Order.

  <em> Explain whether the evaluation order is deterministic as specified by the
judgment form <code>e &#8594; e'</code>. </em>

    Answer to question 2 goes here

#### 3. Evaluation Order.

  <em> Consider the small-step operational semantics for JAVASCRIPTY shown in Figures 7, 8, and 9. What is the evaluation order for e<sub>1</sub> + e<sub>2</sub>? Explain. How do we change the rules obtain the opposite evaluation order?</em>

    Answer to question 3 goes here

#### 4. Short-Circuit Evaluation.

  a) <em>Give an example that illustrates the usefulness of short-circuit evaluation. Explain your example.</em>

    Answer to question 4a goes here

  b) <em>Consider the small-step operational semantics for JAVASCRIPTY shown in Figures 7, 8, and 9. Does e<sub>1</sub> && e<sub>2</sub> short circuit? Explain.</em>

    Answer to question 4b goes here



# Symbol shortcuts:

right arrow, line left side: &#8614;

thin arrow pointing right: &rarr;

not equal to: &ne;

eval to: &dArr;

epsilon : &epsilon;

element of: &isin;

right tack: &#8866;

not sign: &not;

subscript: e<sub>1</sub>
