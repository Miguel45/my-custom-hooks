# Use example

```javascript
import React from 'react'
import { useCounter } from '...'

export const MyComponent = () => {
    
    const {counter, increment, decrement, reset} = useCounter(0)

    return (
        <>
            <h1>{counter}</h1>

            <hr/>

            <button onClick={increment(10)}>+1</button>

            <button onClick={decrement(10)}>-1</button>

            <button onClick={reset()}>RESET</button>
        </>
    )
}
```