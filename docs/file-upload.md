# Send files

You can send files, by modifying `body` argument of action call.

```jsx
import ReactResource from 'react-resource';

// User model
const User = new ReactResource('/api/users/{:id}', { id: ':id' });

// User instance
const user = new User({id: 10});

// Make FormData
const input = document.querySelector('input[type="file"]');
const bodyData = new FormData().append('file', input.files[0]);

// Send request
user.$update({}, bodyData);
```
See more https://github.com/github/fetch#file-upload
