---
layout: post
title: css radio buttons and check boxes
---
Last 3 years almost every web or software design I've worked on required some kind of unique version of these.

Every time I forget how I did it and have to refer back to a previous project. Problem is over time they get more bloated as I build from one to the other.

Today when I yet again had to make a custom radio button design I decided to pair it down once and for all.

This is my starting point for truly CSS based radio and check box forms. Mainly just for my reference down the road. But if it helps anyone else, well that's good too.

The only thing that is different from just writing normal check box & radio form elements to make this work?

Add `<span class="checkmark-selection"></span>` right **after** the `<input>` types.  
That's it. The rest is done with CSS. No images. No JavaScript.

##Example
<style>
  .example .checkbox,
  .example .radio {
    position: relative;
    display: block;
    margin-top: 10px;
    margin-bottom: 10px;
  }
  .example .checkbox label,
  .example .radio label {
    min-height: 20px;
    padding-left: 20px;
    margin-bottom: 0;
    font-weight: 400;
    line-height: 25px;
    cursor: pointer;
  }
  .example label {
    display: inline-block;
    max-width: 100%;
    margin-bottom: 5px;
    font-weight: 700;
  }
  .example .radio input[type="radio"],
  .example .checkbox input[type="checkbox"] {
    position: absolute;
    display: block;
    float: left;
    margin: 0px;
    width: 25px;
    height: 25px;
    opacity: 0;
    cursor: pointer;
  }
  .example span.checkmark-selection {
    display: block;
    float: left;
    margin: 0px 20px 0px 0px;
    width: 20px;
    height: 20px;
    background: #fff;
    border: 3px solid #ccc;
    border-radius: 50%;
  }
  .example input:checked + .checkmark-selection {
    background: green;
    border: 3px solid green;
  }
  .example input:checked + .checkmark-selection:before {
    content: "";
    position: absolute;
    margin: 2px 1px;
    height: 0.2rem;
    width: .5rem;
    background: transparent;
    border: 3px solid #f2f2f2;
    border-top-style: none !important;
    border-right-style: none !important;
    border-radius: 0px;
    transform: rotate(-45deg);
  }
  .example input[type="checkbox"] + .checkmark-selection {
    border-radius: 0px;
  }
</style>
<div class="example">
  <form>
    <div class="radio">
      <label>
        <input type="radio" name="optionsRadios" id="optionsRadios1" value="option1" checked>
        <span class="checkmark-selection"></span>
        No
      </label>
    </div>
    <div class="radio">
      <label>
        <input type="radio" name="optionsRadios" id="optionsRadios2" value="option2">
        <span class="checkmark-selection"></span>
        Yes
      </label>
    </div>
    <hr>
    <div class="checkbox">
      <label>
        <input type="checkbox" value="">
        <span class="checkmark-selection"></span>
        Yes
      </label>
    </div>
    <div class="checkbox">
      <label>
        <input type="checkbox" value="">
        <span class="checkmark-selection"></span>
        No
      </label>
    </div>
  </form>
</div>

##CSS/HTML set up
{% gist b9c63fd6ca3413183966 %}

The html set is based on the form elements in the bootstrap documentation.

The `<span>` for each `input` has been added in these examples.

You can adjust the `margin:` and `height:` & `width:` in the `input:checked + .checkmark-selection:before` CSS if you want to change the way the check mark looks.
