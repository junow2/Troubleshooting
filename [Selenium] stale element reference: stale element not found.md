## Error Message
stale element reference: stale element not found 

## Reason 
It Occurs because of dynamic DOM. It means that after the initial appearance the web elements continue re-build, so even after Selenium caught some specific element to be clickable or visible this element may instantly continue changing so that the initial element reference becomes stale

## Solution 
Set first wait condition, after that set a delay and after that another wait condition
```python
# Example
from selenium.webdriver.support import expected_conditions as EC
wait = WebDriverWait(driver,60)
wait.until(EC.element_to_be_clickable((By.XPATH,"//input[@id='ContentPlaceHolder1_rcmbCapacityTranch_Input']")))
time.sleep(2)
wait.until(EC.element_to_be_clickable((By.XPATH,"//input[@id='ContentPlaceHolder1_rcmbCapacityTranch_Input']"))).click()
```

## Source 
https://stackoverflow.com/q/70405300/9819140
