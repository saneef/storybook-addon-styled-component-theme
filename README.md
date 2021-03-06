[![npm version](https://badge.fury.io/js/storybook-addon-styled-component-theme.svg)](https://badge.fury.io/js/storybook-addon-styled-component-theme)
[![build status](https://travis-ci.org/echoulen/storybook-addon-styled-component-theme.svg?branch=master)](https://travis-ci.org/echoulen/storybook-addon-styled-component-theme)


![](https://media.giphy.com/media/FfFvOA9C0h9bhfCuNX/giphy.gif)


#### Installation
```bash
yarn add storybook-addon-styled-component-theme --dev
```

#### Add to .storybook/addons.js 

```javascript
import 'storybook-addon-styled-component-theme/dist/register';
```

#### addDecorator to .storybook/config.js
```javascript
import {addDecorator} from '@storybook/react';
import {withThemesProvider} from 'storybook-addon-styled-component-theme';

const themes = [theme1, theme2];
addDecorator(withThemesProvider(themes));
```

> or

#### addDecorator to stories 

```javascript
import {withThemesProvider} from 'storybook-addon-styled-component-theme';

const themes = [theme1, theme2];

storiesOf("demo", module)
  .addDecorator(withThemesProvider(themes))
  .add("demo div", () => <div>DEMO</div>);
```

#### Remind
Make sure every theme with `name` property
