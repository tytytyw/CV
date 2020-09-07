# Kolesnikov Dmitriy

## Contacts
- [Telegram](https://t.me/tytytyw "write to telegram")
- [VK](https://vk.com/tytytyw "vk profile")
- [Linkedin](https://www.linkedin.com/in/tytytyw "linkedin profile")

## About

## Skills
- Git
- HTML
- CSS
- JavaScript
- React

-
## Code example
```
  const [items, setItems] = useState(initialState.items);
  const onClickDone = index => {
    const newItemList = items.map(item => {
      const newItem = {...item};
      if (item.index === index) {
        newItem.isDone = !item.isDone;
      }
      return newItem;
    });
    setItems(newItemList);
  };
  const onClickDelete = index => {
    setItems(item => (items.filter(item => item.index !== index)));
    items.forEach(item => {
      if (item.index > index) {
        item.index--;
      }
    });
  };
  const onClickAdd = value => {
    setItems(items => ([
        ...items,
        {
          value,
          isDone: false,
          index: items.length,
        }
      ]
    ));
  };
  const selectedDelete = () => {
    let count = 0;
    items.forEach(item => {
      if (item.isDone === true) {
        count = count + 1;
      }
      item.index = item.index - count ;
    });
    setItems(items => (items.filter(item => item.isDone !== true)));
  };
  const onClickFilter = () => {
  };
 ```
## Experience
- 

## Education
- Git/HTLM/CSS/JS/React courses in Web Hero School
- JS/React course in Udemy

## English

Pre-intermediate