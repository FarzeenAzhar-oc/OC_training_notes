2#authFrzn
Check out link [Browser Stack](https://www.browserstack.com/guide/xpath-in-selenium)
Basic idea is Xpath helps to navigate html like an xml tree

# Absolute Xpath
- The complete path to the element starting from `html`
e.g. `/html/body/div/div/div/div/main/div[2]/div/div[1]/div[2]/div/div/span`
`div[2]` means the second div


# Relative xpath
1. Using attribute
	`//el[@atr='val']/el[num]`
	e.g: `//div[@id='dashboard']`

2.  Logical operator in attribute sel
	or , and  can be used

3. Using text
	`//el[text() = "txt"]`
	e.g. `//span[text() = 'Dashboard']`
use `*[text()='txt']/` for any with txt