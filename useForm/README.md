# Use example

```javascript
import React from 'react'
import { useForm } from '...'

export const MyComponent = ({handle}) => {
    
    const [ values, handleInputChange, reset ] = useForm({
        name: '',
        email: '',
        password: '',
    })

    const { name, email, password } = values;

    const handleSubmit = (e) => {
        e.preventDefault();
        handle(values);
        reset();
    }

    return (
        <form onSubmit={handleSubmit}>
            <input type='text' name='name' value={name} onChange={handleInputChange}/>
            <input type='email' name='email' value={email} onChange={handleInputChange}/>
            <input type='password' name='password' value={password} onChange={handleInputChange}/>
            <button onClick={reset}>Reset</button>
        </form>
    )
}
```