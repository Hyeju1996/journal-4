# Jan 28,2022 Gallery Layout and User Input I

Today we learn about how to crete imeages with css grid and layouts. 
We focus on about form use **ID** and **label** code.

## code:

**HTML:**

```
<div class="grid-layout">
<header>
<h1>A form example</h1>
</header>
<main>
    <form action="" method="post">
      <!-- Input Group 1 -->
      <fieldset>
        <legend>Basic Info</legend>
        <!-- Text Input -->
        <label for="user">User Name</label>
        <input type="text" name="user" id="user" maxlength="20" placeholder="required" required>   
        <!-- Email Input -->
        <label for="email">Email</label>
        <input type="email" id="email" name="email" placeholder="required" required>
        <!-- Phone Input -->
        <label for="phone">Phone Number</label>
        <input type="tel" name="phone" id="phone" placeholder="optional"> 
        <!-- Date Picker --> 
        <label for="date">Date</label>
        <input type="date" placeholder="optional">       
      </fieldset>

      <!-- Second Data Group -->
      <fieldset>
        <legend>Extra Info</legend>

        <!-- Checkboxes -->
        <fieldset class="flex row wrap no-border">
          <legend>Favourite Deserts</legend>
          <div>
            <label for="pie">Pie</label>
            <input type="checkbox" value="pie" id="pie" name="deserts">         
          </div>
          <div>
            <label for="cake">Cake</label>
            <input type="checkbox" value="cake" id="pie" name="deserts">         
          </div>
          <div>
            <label for="brownies">Brownies</label>
            <input type="checkbox" value="brownies" id="brownies" name="deserts">         
          </div>

        </fieldset>

        <!-- Radio Buttons -->
        <fieldset class="flex row no-border">
          <legend>Class</legend>
          <div>
            <label for="mage">Mage</label>
            <input type="radio" value="mage" name="class" id="mage">         
          </div>
          <div>
            <label for="warrior">Warrior</label>
            <input type="radio" value="warrior" name="class" id="warrior">         
          </div>
          <div>
            <label for="bard">Bard</label>
            <input type="radio" value="bard" name="class" id="bard">         
          </div>
          <div>
            <label for="demagorgon">Demagorgon</label>
            <input type="radio" value="demagorgon" name="class" id="demagorgon">         
          </div>
        </fieldset>

        <!-- Dropdown Menu -->
        <label for="motorcycles">Favourite Motorcycles</label>
        <select name="motorcycles" id="motorcycles" class="no-border">
          <option selected="true" disabled="disabled">Select a Bike Manufacturer</option>
          <option value="ducati">Ducati</option> 
          <option value="yamaha">Yamaha</option>
          <option value="Honda">Honda</option>
          <option value="Harly Davidson">Harley Davidson</option>
        </select>

        <!-- Textarea -->
        <label for="feedback">Feedback</label>
        <textarea name="feedback" id="feedback" rows="5" cols="20" placeholder="optional"></textarea>
      </fieldset>
      <button type="submit" class="no-border">Submit</button>
    </form> 
  </main>
  <footer>
    <p>&copy; 2022 Ash</p>
  </footer>
</div>
```

**css:**
```
body {
  background-color: whitesmoke;
}
.grid-layout {
  display: grid;
  justify-items: center;
  gap: 1rem;
}
main {
  display: grid;
  justify-content: center;
  align-items: center;
}

footer, header {
  text-align: center;
  background-color: black;
  color: whitesmoke;
  width: 100%;
}

form {
  display: flex;
  flex-direction: column;
  gap: 10px;
  margin: 4rem;
}
fieldset {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  gap: 10px;
}

.flex {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  gap: 10px;
  
}

.no-border {
  border: none;
}
```
## What we working on:

Also, we working on form with partner and we made Hack MD for plane.
[HackMD](https://hackmd.io/ZGERBX_BTS63h_nG6K6fmQ?view)
This what we planning for it. I am the coder and Jibril is navigater. We compunication well but later that we are comfsed how we have code form and looking nice. We looked at the Ashlyn's code but we still trying to figure it out the from code looks really nice.

## prove of work: 

[codepen](https://codepen.io/hyeju1996/pen/XWzdaEg);

## proof out work

[codepen](https://codepen.io/hyeju1996/pen/XWzdaEg);


# Jan 31,2022 Galleries, Flex + Grid

Today we are working on Galleries, and Flex +Grid. Ashlyn showed us how she want to design of gallery and she want us to use design on Assighnment #3 on Due Feb 03 project. 

## How we did:

- Firstly, she set up some goals for working on and diffrent layout grid.
- Secondly, She show us design how she want to design layouts [Ashlyn's work](https://hyeju1996.github.io/gallery-example/) This is out Exmaple.
- Also she told us about when we want to desighn we need to make css file. 

## How she put design:
she put lay-out wireframe in design 
![](https://i.imgur.com/Zhxg9jC.png).This is  what she design it on the file.

## challange:

## More focus:

**main-css:**

```
/* Layout */
main {
  margin: 0 auto;
  min-width: 300px;
  max-width: 1400px;
}

.grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
  gap: 2rem;
}

/* ************* */
/* Gallery Items */
/* ************* */

/* gallery item container */
figure {
  display: grid;
  height: 100%;
}

/* 2 row spanning image */
.fig-portrait {
  grid-row: span 2;
  height: 100%;
}

/* full width image */
.fig-landscape {
  grid-column: 1 / -1;
}
/* gallery item image */
img {
  max-width: 100%;
  height: 100%;
  object-fit: cover;

  grid-row: 1;
  grid-column: 1;
}

/* gallery item text layout */
figcaption {
  grid-row: 1;
  grid-column: 1;

  justify-self: end;
  align-self: end;

  text-align: end;

  color: rgb(169, 219, 235);
  margin: 0 8px 4px 0;
}

/* *********************** */
/* Non Gallery UI Elements */
/* *********************** */
header {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  margin: 2rem 0 4rem 0;
  width: 100%;
  text-align: center;
}

footer {
  display: flex;
  text-align: center;
  justify-content: center;

  margin-top: 4rem;
  padding: 2rem;
  background-color: black;
  color: whitesmoke;
}

```

# Feb 1, 2022 Hero Sections

 Today we learn how to make Hero section, and Ashlyn use codepen to fix more css on hreo section. I didn't finished yet also I want a working on it so I didn't typed yet. Also, we also use **Hack MD** for the make goals.Also, we planning designs and how we are going to adding codes. This is the project of lollipop project.
 
 [HAck MD](https://hackmd.io/@QPSs5iv3R26SYaf5b8FxNg/rJ-_UgDCK/edit)
 
 Also, we putting together working what is problem and solving problem.
