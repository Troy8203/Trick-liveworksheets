# Trick-liveworksheets
This is a repo to get answers of Liveworksheets

Open your console in your terminal and run this code

```javascript
function getAnwers() {
    const scriptTag = document.querySelector('script[data-drupal-selector="drupal-settings-json"]');
    const jsonContent = scriptTag.textContent.trim();
    const data = JSON.parse(jsonContent);
    const result = JSON.parse(data.worksheet.json);
  
  return result
}

function showAnwers(response){
  for (let i = 0; i < response.length; i++) {
    const element = response[i][0];
    console.log(`${i+1}-${element}`)
  }
}

//Execute
const resultOfAllAnswers = showAnwers(getAnwers())
```

To show the answers, write this

```javascript
console.log(resultOfAllAnswers)
```

> Warning: It just works with test about words
