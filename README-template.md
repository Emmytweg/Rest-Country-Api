# Frontend Mentor - REST Countries API with color theme switcher solution

This is a solution to the [REST Countries API with color theme switcher challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/rest-countries-api-with-color-theme-switcher-5cacc469fec04111f7b848ca). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)
- [Acknowledgments](#acknowledgments)

**Note: Delete this note and update the table of contents based on what sections you keep.**

## Overview

### The challenge

Users should be able to:

- See all countries from the API on the homepage
- Search for a country using an `input` field
- Filter countries by region
- Click on a country to see more detailed information on a separate page
- Click through to the border countries on the detail page
- Toggle the color scheme between light and dark mode *(optional)*

### Screenshot

C:\Users\TWEG\Desktop\REST API\Screenshot 2024-12-17 211444.png

Add a screenshot of your solution. The easiest way to do this is to use Firefox to view your project, right-click the page and select "Take a Screenshot". You can choose either a full-height screenshot or a cropped one based on how long the page is. If it's very long, it might be best to crop it.

Alternatively, you can use a tool like [FireShot](https://getfireshot.com/) to take the screenshot. FireShot has a free option, so you don't need to purchase it. 

Then crop/optimize/edit your image however you like, add it to your project, and update the file path in the image above.

**Note: Delete this note and the paragraphs above when you add your screenshot. If you prefer not to add a screenshot, feel free to remove this entire section.**

### Links

- Solution URL: http://127.0.0.1:5500/rest.html
- Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow


**Note: These are just examples. Delete this note and replace the list above with your own choices**

### What I learned

Use this section to recap over some of your major learnings while working through this project. Writing these out and providing code samples of areas you want to highlight is a great way to reinforce your own knowledge.

To see how you can add code snippets, see below:

```html
<h1>Some HTML code I'm proud of</h1>
```

```
```js
fetch('data.json').then(response => response.json()).then(data => {
            const dataArray = Object.values(data)
            dataArray.forEach(item => {


                        const countryCon = document.createElement('div');
                        countryCon.addEventListener('click', (e) => {
                            console.log('works')
                            mainCon.style.display = 'none'
                            const showCountryDetails = document.createElement('div');
                            
                           
                            showCountryDetails.innerHTML = `
            <div class='flagDetailContainer'>
            <div class='backBtn'>
            <button id='directBtn' onclick="location.reload();">
            <svg  xmlns="http://www.w3.org/2000/svg"  width="24"  height="24"  viewBox="0 0 24 24"  fill="none"  stroke="currentColor"  stroke-width="2"  stroke-linecap="round"  stroke-linejoin="round"  class="icon icon-tabler icons-tabler-outline icon-tabler-arrow-left"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M5 12l14 0" /><path d="M5 12l6 6" /><path d="M5 12l6 -6" /></svg>
            Back</button>
            </div>
            <div class='countryFlag-name'> 

            <div class='countryFlag'>
            <img src=${item.flag} alt=${item.name}>
            </div>
            <div class='countryName'> 
            <h1>${item.name} </h1>
            <div class='countryItemsCon'> 
            <div>
            <p> Native Name: ${item.nativeName} </p>
             <p> Population: ${item.population} </p>
              <p> Region: ${item.region} </p>
               <p> Sub Region:  ${item.subregion} </p>
                <p> Capital: ${item.capital} </p>
                </div>
                <div>
 <p> Top Level Domain: ${item.nativeName} </p>
  <p> Currencies: ${item.nativeName} </p>
   <p> Language: ${item.languages.map(lang =>  lang.name).join(' ')} </p>
                </div>
            </div>
            <div class='countryBorder'>
         ${item.borders.map(border =>`<button>${border}</button>`).join('')}



                    </div> 
                    </div>

                    </div>
                     </div>

                    `
            showCountry.appendChild(showCountryDetails)
            console.log(item.borders)
        })
        countryCon.innerHTML = ` 
        <div class = 'flagComponent' id = 'flagComponents' >
                    <img src = '${item.flag}'
                    alt = '${item.name}' >
                    <div class = 'population' >
                    <p> <b> ${ item.name } </b> </p>
                    <div class = 'population-region' >
                    <span> <b> Population </b>: ${item.population}</span >
                    <span> <b> Region </b>: ${item.region}</span>
                    <span> <b> Capital </b>: ${item.capital}</span >
                    </div> 
                    </div>
</div>

                    `
        countryDetails.appendChild(countryCon)
    });
})

```

If you want more help with writing markdown, we'd recommend checking out [The Markdown Guide](https://www.markdownguide.org/) to learn more.

**Note: Delete this note and the content within this section and replace with your own learnings.**

### Continued development

Use this section to outline areas that you want to continue focusing on in future projects. These could be concepts you're still not completely comfortable with or techniques you found useful that you want to refine and perfect.

**Note: Delete this note and the content within this section and replace with your own plans for continued development.**

### Useful resources

- [Example resource 1](https://www.example.com) - This helped me for XYZ reason. I really liked this pattern and will use it going forward.
- [Example resource 2](https://www.example.com) - This is an amazing article which helped me finally understand XYZ. I'd recommend it to anyone still learning this concept.

**Note: Delete this note and replace the list above with resources that helped you during the challenge. These could come in handy for anyone viewing your solution or for yourself when you look back on this project in the future.**

## Author

- Website - [Add your name here](https://www.your-site.com)
- Frontend Mentor - [@yourusername](https://www.frontendmentor.io/profile/yourusername)
- Twitter - [@yourusername](https://www.twitter.com/yourusername)

**Note: Delete this note and add/remove/edit lines above based on what links you'd like to share.**

## Acknowledgments

This is where you can give a hat tip to anyone who helped you out on this project. Perhaps you worked in a team or got some inspiration from someone else's solution. This is the perfect place to give them some credit.

**Note: Delete this note and edit this section's content as necessary. If you completed this challenge by yourself, feel free to delete this section entirely.**
