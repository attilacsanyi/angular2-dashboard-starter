# angular2-dashboard-starter
Ready to use dashboard starter/seed project based on Angular 2

##Features

- Angular version 2.0.0-beta.6 using Typescript
- Live reload & compile
- Login module with input validations (Utilizes src/login.json)
- Signup module with input validations
- Auth module to protect dashboard pages
- Dashboard Layout as a separate directive
- Best open source admin dashboard & control panel theme ['AdminLTE 2'](https://almsaeedstudio.com/) by Abdullah Almsaeed.

## Installation

1. Checkout this repo in a folder make sure to give root permissions.
2. Run `npm install` once to install app dependencies.
3. Run `npm start` in a separate terminal window to start the server and launch the app.

## Protect Routes

```TypeScript
import { ComponentInstruction, CanActivate } from 'angular2/router';
import { checkAuth } from '../auth/check_auth';

// just include this code above your component class
@CanActivate((next: ComponentInstruction, previous: ComponentInstruction) => {
  return checkAuth(next, previous);
})
```

## Easy to use Dashboard Layout in your templates

Use DashboardLayout directive in your component's template to use dashboard layout. This makes easy for views in our app which do not utilize dashboard layout.

```HTML
<dashboard-layout pageTitle="Home" pageSubtitle="Your personalized dashboard and control panel">
    <div class="home">
      <!--- Your template code -->
    </div>
</dashboard-layout>
```




Help me make it better by [contributing](./CONTRIBUTING.md)

@author Hasan Hameed <hasan.hameed07@gmail.com>
