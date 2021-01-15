# Use example

```javascript
import React from 'react'
import { useFetch } from '...'

export const MyComponent = ({url}) => {
    
    const {data, loading, error} = useFetch(url)

    return (
        <>
            {data &&
                <pre>
                    {JSON.stringify(data, null, 3)}
                </pre>
            }

            {loading && <h3>Loading...</h3>}

            {error && <h2>Error!: {error}</h2>}
        </>
    )
}
```