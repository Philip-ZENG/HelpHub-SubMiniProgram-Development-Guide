# 【学习笔记】JavaScript 特有函数语法 & React Hook 



## JavaScript语法

### 函数定义

> https://www.liaoxuefeng.com/wiki/1022910821149312/1023021087191360 

源码中大量使用了一种JavaScript特有的函数定义方式：匿名箭头函数。

- 普通的函数定义方式

  ```javascript
  function abs(x) {
      if (x >= 0) {
          return x;
      } else {
          return -x;
      }
  }
  ```

- 匿名函数定义方式 (Stateless Function)

  ```javascript
  var abs = function (x) {
      if (x >= 0) {
          return x;
      } else {
          return -x;
      }
  };
  ```

  - 在这种方式下，`function (x) { ... }`是一个匿名函数，它没有函数名。但是，这个匿名函数赋值给了变量`abs`，所以，通过变量`abs`就可以调用该函数。
  - 上述两种定义完全等价，注意第二种方式按照完整语法需要在函数体末尾加一个`;`，表示赋值语句结束。

- 箭头函数定义方式 (Arrow Function)

  - 箭头函数相当于匿名函数，并且简化了函数定义。箭头函数有两种格式，一种像上面的，只包含一个表达式，连`{ ... }`和`return`都省略掉了。

    ```javascript
    x => x * x
    ```

    - 相当于

      ```javascript
      function (x) {
          return x * x;
      }
      ```

  - 另一种可以包含多条语句，这时候就不能省略`{ ... }`和`return`：

    ```javascript
    x => {
        if (x > 0) {
            return x * x;
        }
        else {
            return - x * x;
        }
    }
    ```

  - 如果参数不是一个，就需要用括号`()`括起来

    ```javascript
    // 两个参数:
    (x, y) => x * x + y * y
    
    // 无参数:
    () => 3.14
    
    // 可变参数:
    (x, y, ...rest) => {
        var i, sum = x + y;
        for (i=0; i<rest.length; i++) {
            sum += rest[i];
        }
        return sum;
    }
    ```

  - 如果要返回一个对象，就要注意，如果是单表达式，这么写的话会报错：

    ```javascript
    // SyntaxError:
    x => { foo: x }
    ```

    因为和函数体的`{ ... }`有语法冲突，所以要改为：

    ```javascript
    // ok:
    x => ({ foo: x })
    ```



### Destructuring assignment

> https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Destructuring_assignment#array_destructuring





## React Hooks

> https://reactjs.org/docs/hooks-overview.html

- Motivation

  With Hooks, you can extract stateful logic from a component so it can be tested independently and reused. **Hooks allow you to reuse stateful logic without changing your component hierarchy.**

- Definition

  Hooks are functions that let you “hook into” React state and life-cycle features from function components. Hooks don’t work inside classes — they let you use React without classes. 

- Several Build-in Hooks will be introduced below



### `State Hook`

> https://reactjs.org/docs/hooks-state.html

- An example

  This example renders a counter. When you click the button, it increments the value:

  ```javascript
  import React, { useState } from 'react';
  
  function Example() {
    // Declare a new state variable, which we'll call "count"
    const [count, setCount] = useState(0);
  
    return (
      <div>
        <p>You clicked {count} times</p>
        <button onClick={() => setCount(count + 1)}>
          Click me
        </button>
      </div>
    );
  }
  ```

  - Remark

    - Here, `useState` is a *Hook*.
    - We call it inside a function component to add some local state to it. 
    - React will remember its current value between re-renders, and provide the most recent one to our function.
    - `useState` returns a pair: the *current* state value and a function that lets you update it.
    - The only argument to `useState` is the initial state. In the example above, it is `0` because our counter starts from zero.
    - We declare a state variable called `count`, and set it to `0`.  If we want to update the current `count`, we can call `setCount`.

  - Tips: What Do Square Brackets Mean?

    - You might have noticed the square brackets when we declare a state variable:

      ```javascript
      const [count, setCount] = useState(0);
      ```

    - The names on the left aren’t a part of the React API. You can name your own state variables:

      ```javascript
      const [fruit, setFruit] = useState('banana');
      ```

  - Tips: Using Multiple State Variables

    - Declaring state variables as a pair of `[something, setSomething]` is also handy because it lets us give *different* names to different state variables if we want to use more than one:

      ```javascript
      function ExampleWithManyStates() {
        // Declare multiple state variables!
        const [age, setAge] = useState(42);
        const [fruit, setFruit] = useState('banana');
        const [todos, setTodos] = useState([{ text: 'Learn Hooks' }]);
      ```

      In the above component, we have `age`, `fruit`, and `todos` as local variables, and we can update them individually:

      ```javascript
      function handleOrangeClick() {
          // Similar to this.setState({ fruit: 'orange' })
          setFruit('orange');
      }
      ```

    - You **don’t have to** use many state variables. State variables can **hold objects and arrays just fine**, so you can still group related data together.

- Syntax

  - Use Hooks in function components

    ```javascript
    const Example = (props) => {
      // You can use Hooks here!
      return <div />;
    }
    ```

  - Declare a Hook

    ```javascript
    import React, { useState } from 'react';
    
    function Example() {
      // Declare a new state variable, which we'll call "count"
      const [count, setCount] = useState(0);}
    ```

- Explanations

  - **What does calling `useState` do?** 

    It declares a “state variable”.

  - **What do we pass to `useState` as an argument?** 

    The only argument to the `useState()` Hook is the initial state

  - **What does `useState` return?** 

    It returns a pair of values: the current state and a function that updates it. This is why we write `const [count, setCount] = useState()`. 

    

### `Effect Hook`

> https://reactjs.org/docs/hooks-effect.html

- An Example

  The *Effect Hook* lets you perform side effects in function components: Data fetching, setting up a subscription, and manually changing the DOM (**Document Object Model**) in React components are all examples of side effects.

  ```javascript
  import React, { useState, useEffect } from 'react';
  
  function Example() {
    const [count, setCount] = useState(0);
  
    // Similar to componentDidMount and componentDidUpdate:
    useEffect(() => {
      // Update the document title using the browser API
      document.title = `You clicked ${count} times`;
    });
  
    return (
      <div>
        <p>You clicked {count} times</p>
        <button onClick={() => setCount(count + 1)}>
          Click me
        </button>
      </div>
    );
  }
  ```

  - Remark
    - We added a new feature to the example in state hook: we set the document title to a custom message including the number of clicks. 
    - The Effect Hook, `useEffect`, adds the ability to perform side effects from a function component.
    - When you call `useEffect`, you’re telling React to run your “effect” function after flushing changes to the DOM.
    - Effects are declared inside the component so they have access to its props and state.

- Another Example

  Effects may also optionally specify how to “clean up” after them by returning a function. For example, this component uses an effect to subscribe to a friend’s online status, and cleans up by unsubscribing from it:

  ```javascript
  import React, { useState, useEffect } from 'react';
  
  function FriendStatus(props) {
    const [isOnline, setIsOnline] = useState(null); // a state hook to record friend's status
  
    function handleStatusChange(status) {
      setIsOnline(status.isOnline);
    }
  
    useEffect(() => {
      ChatAPI.subscribeToFriendStatus(props.friend.id, handleStatusChange);
      return () => {
        // unsubscribe before leaving
        ChatAPI.unsubscribeFromFriendStatus(props.friend.id, handleStatusChange); 
      };
    });
  
    if (isOnline === null) {
      return 'Loading...';
    }
    return isOnline ? 'Online' : 'Offline';
  }
  ```

  - Remark

    - In this example, React would unsubscribe from our `ChatAPI` when the component unmounts, as well as before re-running the effect due to a subsequent render. 
    - Hooks let you organize side effects in a component by what pieces are related (such as adding and removing a subscription), rather than forcing a split based on lifecycle methods.

  - Use multiple Effect Hook in one component

    ```javascript
    function FriendStatusWithCounter(props) {
      const [count, setCount] = useState(0);
      useEffect(() => {
        document.title = `You clicked ${count} times`;
      });
    
      const [isOnline, setIsOnline] = useState(null);
      useEffect(() => {
        ChatAPI.subscribeToFriendStatus(props.friend.id, handleStatusChange);
        return () => {
          ChatAPI.unsubscribeFromFriendStatus(props.friend.id, handleStatusChange);
        };
      });
    
      function handleStatusChange(status) {
        setIsOnline(status.isOnline);
      }
      // ...
    ```




### Rules of Hooks

Hooks are JavaScript functions, but they impose two additional rules:

- Only call Hooks **at the top level**. Don’t call Hooks inside loops, conditions, or nested functions.
- Only call Hooks **from React function components**. Don’t call Hooks from regular JavaScript functions. (There is just one other valid place to call Hooks — your own custom Hooks. We’ll learn about them in a moment.)



### Building Hooks

- We’ll extract logics from the previous `FriendStatus`  function into a custom Hook called `useFriendStatus`

  ```javascript
  import React, { useState, useEffect } from 'react';
  
  function useFriendStatus(friendID) {
    
    const [isOnline, setIsOnline] = useState(null);
  
    function handleStatusChange(status) {
      setIsOnline(status.isOnline);
    }
  
    useEffect(() => {
      ChatAPI.subscribeToFriendStatus(friendID, handleStatusChange);
      return () => {
        ChatAPI.unsubscribeFromFriendStatus(friendID, handleStatusChange);
      };
    });
  
    return isOnline;
  }
  ```

  It takes `friendID` as an argument, and returns whether our friend is online.

  Now we can use it from both components:

  ```javascript
  function FriendStatus(props) {
    const isOnline = useFriendStatus(props.friend.id);
  
    if (isOnline === null) {
      return 'Loading...';
    }
    return isOnline ? 'Online' : 'Offline';
  }
  ```

  ```javascript
  function FriendListItem(props) {
    const isOnline = useFriendStatus(props.friend.id);
  
    return (
      <li style={{ color: isOnline ? 'green' : 'black' }}>
        {props.friend.name}
      </li>
    );
  }
  ```

- Explanation

  - The state of each component is completely independent. Hooks are a way to reuse *stateful logic*, not state itself. In fact, each *call* to a Hook has a completely isolated state — so you can even use the same custom Hook twice in one component.
  - Custom Hooks are more of a convention than a feature. If a function’s name starts with ”`use`” and it calls other Hooks, we say it is a custom Hook. The `useSomething` naming convention is how our linter plugin is able to find bugs in the code using Hooks.

