# NOTE this will be updated frequently! 

## Technologies learned🛠️ <br>
### HTML <br>
  `h1`-`h6`, `p`, `ul`, `ol`, `li`, `script`, `a`, `title`, `span`, `div`
  - void tags (they only have an opening tag): <br>
   `img`, `style`, `link`, `hr`, `meta`

### CSS
  `width`, `height`, `color`, `background-color`, `display`, `position`, `float`, `clear`, `@media`, `flex`, `inline-flex`, `justify-content`, `align-items`
  
#### Types of CSS: `internal`, `external`, `inline` 
  - internal: Write the CSS code in the **SAME** HTML file using the `<style></style>` tag. <br>
    Example: <br>
    <style> <br>
      p{ <br>
        color: red; <br>
      } <br>
    </style>
    
  - external: Write the CSS code in an external file for example `style.css` and we access it with the <link> tag. <br>
    Example: <br>
    `<link rel="stylesheet" href="./style.css"/>` <br>
    note: Inside the href attribute it might be different depending on your file location!
  
  - inline: Write the CSS code directly in the tag's attribute section using the `style` keyword. <br>
    Example: <br>
    `<p style="color: red;>`
#### CSS NOTES
  - **font-size**
    - 1pt (point) = 1/72nd inch
    - 1px = 1/96th inch
    - 1em = 100% of parent (meaning if the parent is 20px the element will be 20px too)
    - 2em = 200% (meaning if the parent is 20px the element will be 2 x 20px = 40px)
  
  - **display**
    - block (takes up the entire full width of the web page) <br><br>
      <img src="https://github.com/ZYMNZ/WebDev/assets/98342638/aff2b44c-df0d-44f3-9927-df4a181ecb26" width=500px>
      
    - inline (only takes up as much width as necessary. It does not start on a new line and allows other elements to appear beside it.) <br><br>
      <img src="https://github.com/ZYMNZ/WebDev/assets/98342638/1e86f080-e2f6-41e3-9eda-e2af672b6e3e" width=500px>
      
    - inline-block (make an element behave like an inline and a block-level element. It allows the element to flow inline with surrounding content while maintaining block-level properties, such as setting a specific width and height.) <br><br>
    
      <img src="https://github.com/ZYMNZ/WebDev/assets/98342638/0716a631-c872-45ba-bf46-7b59ef6e98ce" width=500px>
    - flex <br>
      - We wrap the elements(tags) with a div with the display=flex to apply the flex structure. We add "flex" in the **_container_** div. <br><br>
      <img src="https://github.com/ZYMNZ/WebDev/assets/98342638/dec7624e-e086-4d0b-b00d-812f82dd86de" width=500px>
      
      <img src="https://github.com/ZYMNZ/WebDev/assets/98342638/62ef91f7-8659-4133-92a8-2552f0de6b54" width=500px>
      
    - inline-flex <br>
      - Similar to the normal but flex, but the difference is that it doesn't take the full width, it allows other elements to occupy the same line. **_It will only occupy as much width as the content_** <br>
        <img src="https://github.com/ZYMNZ/WebDev/assets/98342638/b47aa49a-07f1-4a36-8803-2940de1f6396" width=450px>

    ### **_flex_**
    #### PARENT (CONTAINER)
    -  flex-direction: row (by default, APPLIED TO THE PARENT) <br><br>
        <img src="https://github.com/ZYMNZ/WebDev/assets/98342638/553b8a35-8a2c-4a2c-a48b-bb15f7961d39" width=500px>
    - flex-direction: column <br><br>
      <img src="https://github.com/ZYMNZ/WebDev/assets/98342638/effaf000-eea9-4cc1-8529-98ada6a3df6b" width= 500px> <br><br>
    - flex: nowrap <br>
      it's ***NOT*** **responsive**, used when we don't want the child flex-items to move to the next line! <br> 
      <img src="https://github.com/ZYMNZ/WebDev/assets/98342638/c79e498f-6786-42d6-b4e1-68c3cfa335b9" width=500px> <br>
    - flex: wrap <br>
      It's opposite to `nowrap`, where if the flex-items cant fit in one line because of the screen size, it'll wrap/move the items to the next line! (RESPONSIVE) <br>
      <img src="https://github.com/ZYMNZ/WebDev/assets/98342638/b8ea7522-0c79-4e17-9e47-74c367850f90" width=500px> <br><br>

      ### **justify-content** <br>
        - Sets the distribution of the items along the `**main-axis**` <br>
      > Note: to apply this type of CSS, there should be some space left! Meaning the items don't occupy the entire container. <br>
      
        - justify-content: flex-start
          This value will squish everything to the `left/start` side of the **container** <br>
        <img src="https://github.com/ZYMNZ/WebDev/assets/98342638/e6cbf8f3-2195-4097-ad37-349891be0e93" width=500px> <br>
        
        - justify-content: flex-end
          This value will squish everything to the `right/end` side of the **container** <br>
        <img src="https://github.com/ZYMNZ/WebDev/assets/98342638/8e7ccccb-7332-4f40-b4f0-5be629c81e32" width=500px> <br>
        
        - justify-content: center
          This value will squish everything to the `center` of the **container** <br>
        <img src="https://github.com/ZYMNZ/WebDev/assets/98342638/12013ae5-9a06-4a4c-ae45-caddc2e0812f" width=500px> <br>
        
        - justify-content: space-between <br>
          This value will input a space between every element and its adjacent item<br>
        <img src="https://github.com/ZYMNZ/WebDev/assets/98342638/9d273f5f-fb54-4090-9a54-c61c80ff8cda" width=500px> <br><br><br>

        <img src="https://github.com/ZYMNZ/WebDev/assets/98342638/739de739-de90-4ff2-b34f-43ed2c968ce2" width=550px> <br>

      ### **align-items**
        - Sets the distribution of the items along the `**cross-axis**` <br>
      > Note: That we need to set a **height** to the container, otherwise we won't see any changes! Another thing is, that flex-wrap has to be set to `nowrap` because it'll affect the behavior! <br>

         - align-items: flex-start; height: 70vh (viewport height)
           - `vh` (viewport height): it's the height of the window that you are viewing the page
         <img src="https://github.com/ZYMNZ/WebDev/assets/98342638/3a866206-cd71-4f5e-85c8-ccdb63d767db" width=500px> <br>
         
         - align-items: flex-end; height: 70vh <br>
           <img src="https://github.com/ZYMNZ/WebDev/assets/98342638/6d4545c9-3857-46eb-9209-29ac8fa3d88f" width=500px>
           



    #### CHILDREN (ELEMENTS INSIDE THE CONTAINER)
    - flex-basis: ###px (APPLIED TO THE CHILDREN) <br>
      This will extend along the main-axis, we add "flex-basis" in the **_child_** div  <br><br>
        - Column direction <br><br>
          <img src="https://github.com/ZYMNZ/WebDev/assets/98342638/535290c8-6652-498d-a443-e08fc6ebc987" width=500px> <br>
        - Row direction <br><br>
          <img src="https://github.com/ZYMNZ/WebDev/assets/98342638/4eb35126-7ca0-4040-b9da-1558dffccb5b" width=500px>
    - order <br><br>
        The `order` is used to change the order of the child flex item! <br><br>
        <img src="https://github.com/ZYMNZ/WebDev/assets/98342638/b1effae6-7df7-4084-bb4a-196b9b1b5471" width=500px> <br><br>
        If only one of the items has the order set to any number greater than 0 then it'll shift to the end. <br><br>
        <img src="https://github.com/ZYMNZ/WebDev/assets/98342638/9f24ed19-ed2d-4862-a965-143308e20179" width=500px> <br><br>
        But of course, if you have more than one child item with an order number > 0, then they will be ordered accordingly <br><br> 
        <img src="https://github.com/ZYMNZ/WebDev/assets/98342638/be562e5c-82e5-4f8f-9a53-e5db7c956c64" width=500px>

      
  <br><br>
  - **position**
    - static
    - relative
    - absolute
    - fixed
   
  - **float**  
    - left <br><p>
      BEFORE:<br>
      <img src="https://github.com/ZYMNZ/WebDev/assets/98342638/0663c868-da33-4a86-9213-78c4c9146627" width=200px> <br>
      AFTER: <br>
      <img src="https://github.com/ZYMNZ/WebDev/assets/98342638/f6dd7682-9bdd-41f2-b256-df32f8f6f648" width=500px>
     - right <br><p>
      BEFORE:<br>
      <img src="https://github.com/ZYMNZ/WebDev/assets/98342638/0663c868-da33-4a86-9213-78c4c9146627" width=200px> <br>
      AFTER: <br>
      <img src="https://github.com/ZYMNZ/WebDev/assets/98342638/5c6dd494-65c6-4776-b737-ac1bffef2fb2" width=500px> <br>
  - **clear**
    Used when we need to avoid the style effect "float: left" that the element before has. 
     - left <br><p>
      BEFORE:<br>
      <img src="https://github.com/ZYMNZ/WebDev/assets/98342638/476358c1-c3c8-47b6-9c2a-0bf948589ad5" width=500px> <br>
      AFTER: <br>
      <img src="https://github.com/ZYMNZ/WebDev/assets/98342638/9a15498c-6419-4d95-ae03-f7ae3b5d133b" width=500> <br>
    - both <br>
      <img src="https://github.com/ZYMNZ/WebDev/assets/98342638/99149cfd-62ff-4441-816f-0a948acc4147" width=500> <br>
      
  - **@media**
    - @media(max-width: ###px)
     BEFORE:<br>
     <img src="https://github.com/ZYMNZ/WebDev/assets/98342638/b11c648a-3b42-406d-a405-ce705593352a" width=500px> <br>
     AFTER: <br>
     <img src="https://github.com/ZYMNZ/WebDev/assets/98342638/24fd9dbd-e4d8-4eff-baf5-70865de0713c" width=500> <br>
     - @media(min-width: ###px)
     - @media(min-width: ###px) and (max-width: ###px) <br>
       <img src="https://github.com/ZYMNZ/WebDev/assets/98342638/c46c8d9d-c0d0-440e-9a92-080cc66238f5" width=500> <br>
     - @media(max-width: ###px) and (min-width: ###px) <br>
       <img src="https://github.com/ZYMNZ/WebDev/assets/98342638/2e4b9411-8307-4d7b-84d3-d48fb690193a" width=500> <br>
     - @media ~screen~ (orientation: landscape) <br>
       The screen keyword is _not_ necessary by default because it's going to apply to all screens. Where do we use the orientation? It's when we want to target the website whenever it's being ***printed***
