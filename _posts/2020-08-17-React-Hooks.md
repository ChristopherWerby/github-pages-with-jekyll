---
title: React Hooks
date: 2020-08-17
---

I've been exploring React's new hooks used with functional components, previously stateless components, although the name is obsolete now that these components can have state.

Here's a simple example taken from the React docs.

```javascript
import React, { useState, useEffect } from 'react';

export default function App() {
	//useState hook returns an array containing the value for the state (counter) and a setter method (setCounter)
	//Pass the initial value of counter into the useState hook.
	const [counter, setCounter] = useState(0);

	// Similar to componentDidMount and componentDidUpdate:
	useEffect(() => {
		// Update the document title using the browser API
		document.title = `You clicked ${counter} times`;
	});

	return (
		<div>
			<p>You clicked {counter} times.</p>
			<button onClick={() => setCounter(counter + 1)}>Click</button>
		</div>
	);
}
```
