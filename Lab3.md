# Answers to Questions for Lab 3

#### 1. JavaScripty Interpreter: Tag Testing, Recursive Functions, and Dynamic Scoping.

  <em> Give one test case that behaves differently under dynamic scoping versus static scoping (and does not crash). Explain the test case and how they behave differently in your write-up. </em>

  ```javascript
  function container(){

    function f1(){
      var x = 2;
      f2();
    }

    function f2(){
      console.log(x);
    }

    var x = 3;
    f1();

  }
  container();
  ```
  In the example above, we can see that var x is defined in both function 1 and container.
  - In dynamic scoping, the function container() would print out '2' because f2() would get its scope from the calling function, in this case f1() where x is defined as 2.
  - In static scoping, the function container() would print out '3' because f2() would get its scop from the parent function, in this case container() where x is defined as 3.

#### 2. JavaScripty Interpreter: Substitution and Evaluation Order.

  <em> Explain whether the evaluation order is deterministic as specified by the
judgment form <code>e &#8594; e'</code>. </em>

Yes, the evaulation order is determined by the judgement form <code>e &#8594; e'</code>. THis is evident in a simple step such as SearchBinary<sub>1</sub>, where <code>e<sub>1</sub> &rarr; e<sub>1</sub>'</code> fr a binary operation between e<sub>1</sub> and e<sub>2</sub>. In this case, the evaluation order is left associative.

#### 3. Evaluation Order.

  <em> Consider the small-step operational semantics for JAVASCRIPTY shown in Figures 7, 8, and 9. What is the evaluation order for e<sub>1</sub> + e<sub>2</sub>? Explain. How do we change the rules obtain the opposite evaluation order?</em>

The evaluation order for figures 7, 8, and 9 is left associative, meaning the left hand side of the most inner expression is evaluated first. This can be changed by changing the search rules to step e<sub>2</sub> first instead of e<sub>1</sub> and also the Do rules to check for values in the right side of the expression.

#### 4. Short-Circuit Evaluation.

  a) <em>Give an example that illustrates the usefulness of short-circuit evaluation. Explain your example.</em>

Short circuit evaluation is exemplified through the AND and OR rule. For example, with AND we see if (A) then B else false. The usefulness of this type of evaluation is that when A is evaluated first. If A is false, we do not need to evaluate B, saving steps in runtime.

  b) <em>Consider the small-step operational semantics for JAVASCRIPTY shown in Figures 7, 8, and 9. Does e<sub>1</sub> && e<sub>2</sub> short circuit? Explain.</em>

Yes, in our small step semantics AND does short circuit. This is due to the evaluation order, evaluating the left side of the equation first. We step through e1 until there is a value(v1) for e1. Once there, we call if v1 then e2 else false. This will stop evaluating e2 if v1 is false, thus short circuiting.



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
