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
import React, { useState } from 'react';
import ItemList from '../ItemList/ItemList';
import Footer from '../Footer/Footer';
import InputItem from '../InputItem/InputItem';
import styles from './Todo.module.css';
import PropTypes from 'prop-types';

const Todo = () => {
  const initialState = {
    items: [
      {
        value: 'открыть холодильник',
        isDone: true,
        index: 0,
      }, 
      {
        value: 'вытащить слона',
        isDone: false,
        index: 1,
      }, 
      {
        value: 'положить оленя',
        isDone: false,
        index: 2,
      }, 
      {
        value: 'закрыть холодильник',
        isDone: false,
        index: 3,
      },
    ]
  };
  
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

    if (value.length > 30) {
      value = value.slice(0,30) + '...';
    }

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

  return (
    <div className={styles.wrap}>
      <h1 className={styles.title}>
        Список дел:
      </h1>
      <InputItem onClickAdd={onClickAdd} />
      <ItemList
        todoItem={items}
        onClickDone={onClickDone}
        onClickDelete={onClickDelete} 
      />
      <Footer
        onClickFilter={onClickFilter}
        selectedDelete={selectedDelete}
        count={items.filter(item => item.isDone === false).length} 
        countAll={items.length}
        /> 
    </div>
  );
};

export default Todo;

Todo.propTypes = {
  index: PropTypes.number,
  value: PropTypes.string,
  isDone: PropTypes.bool,
  items: PropTypes.arrayOf(PropTypes.object)
};
```
## Experience
-

## Education
-

## English

Pre-inte