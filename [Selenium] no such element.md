## Error Message
NoSuchElementException: Message: no such element: Unable to locate element

## Reason 
내가 지정한 element를 발견하지 못할 시 발생한다. 

## Solution 
### class_name으로 접근시 
class_name에 공백이 있을 경우 공백을 마침표(.)로 대체해줘야 한다. 
```python
# Example
releaseDate = games[i].find_element(By.CLASS_NAME, 'col.search_released responsive_secondrow').text # X
releaseDate = games[i].find_element(By.CLASS_NAME, 'col.search_released.responsive_secondrow').text # O
```

## Source 
https://zeuskwon-ds.tistory.com/67
