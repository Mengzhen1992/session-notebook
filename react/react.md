## 2022.09.19

1. React import fontawesome

```js
1. in Terminal
npm i --save @fortawesome/fontawesome-svg-core
npm install --save @fortawesome/free-solid-svg-icons
npm install --save @fortawesome/free-regular-svg-icons
npm install --save @fortawesome/react-fontawesome
2. in app.js
import { library } from '@fortawesome/fontawesome-svg-core'
import { fab } from '@fortawesome/free-brands-svg-icons' --> can cancel
import { faCheckSquare, faCoffee } from '@fortawesome/free-solid-svg-icons'
import { faCoffee as farCoffee } from '@fortawesome/free-regular-svg-icons'

library.add(fab, faCheckSquare, faCoffee, farCoffee)
3. in component.js
import { FontAwesomeIcon } from '@fortawesome/react-fontawesome'

  export const Beverage = () => (
    <div>
      <FontAwesomeIcon icon="check-square" />
      <FontAwesomeIcon icon={'far', 'coffee'} /> when regular icon has the same name with solid
      Your <FontAwesomeIcon icon="coffee" /> is hot and ready!
    </div>
```

2. in Terminal a project start

```js
npx create-react-app react-demo
git log --oneline
```
