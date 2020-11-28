# letsTalk_reactnative


![Let's Talk](assets/lets_talk_logo.png)

___

## Description: 
![afya](assets/afya_logo.png)

*A reproductive health app will allow users to:*
1. READ information on SRH 
2. FIND links to service providers
3. ASK questions to counsellors on platform
4. SHARE experiences with each other.

## STEPS

### Ideation stage:
* Source an idea and refine it. DONE
* Market research SKIPPED
* Define functionality DONE

### Design stage:
* Sketch the web app DONE
* Plan the workflow DONE
* Wireframe the UI DONE
* Seek early validation SKIPPED

### Development stage: 
* Architect the database - an ERM (Entity-Relationship Model) 
diagram to map out the data relationship. WORK IN PROGRESS 
* Develop the frontend - WORK IN PROGRESS 
* Build the backend

### Launch stage:
* Host the web app
* Deploy the web app

## App UI Sketches
![App UI Overview](assets/lets_talk_ui.png)

### App UI Pages
![Homepage](assets/home_page.jpg)
![Find page](assets/find_page.jpg)
![Login/SignUp page ](assets/login_page.jpg)
![Ask me page](assets/ask_me.jpg)
![User profile page](assets/user_profile.jpg)

## Color Palettes 
#### *[Tool used - Color Space](https://mycolor.space/)*
![App Colors - Lets Talk](assets/lt_colors_scheme2.png)


## App UI Figma Designs 
![Final UI](assets/letstalk_final_UI.png)

## Technologies Used
1. React Native 
2. Mongo DB
3. React-UI
4. Expo CLI

[Project Link on Github](https://github.com/users/nashthecoder/projects/2)

#### Navigation

At the default, you can see 3 types of navigation; stack, tab, and drawer. Here in the [code](https://github.com/WataruMaeda/react-native-boilerplate/tree/master/src/routes/navigation), files are separated by the navigation types. If you don't need drawer navigation for example, you can the remove drawer file and replace the import status [here](https://github.com/WataruMaeda/react-native-boilerplate/blob/master/src/routes/navigation/Navigation.js#L2) to tab or stack navigator.

#### Authentication

If your app requires authorization, you need to implement login, signup function. After the user login or logout, the navigation flow should be different. In this case, the route should be switched by the login status. In the [route](https://github.com/WataruMaeda/react-native-boilerplate/blob/master/src/routes/Routes.js#L14-L19), you can set the different navigation changed by login status.

#### Redux

Redux can contain global state of the app. This is very useful but on the other hand, it takes time to setup if you are not familiar with it. In the boilerplate, you see [module file](https://github.com/WataruMaeda/react-native-boilerplate/blob/master/src/modules/app.module.js) which contains actions, reducer and store in a file. To connect with actions and state from component, you need to call [connector](https://github.com/WataruMaeda/react-native-boilerplate/blob/master/src/utils/connector.js). You can use actions and state from props. Here is an [example](https://github.com/WataruMaeda/react-native-boilerplate/blob/master/src/routes/Routes.js#L10-L15). To combine reducer, first you can add another module file then import in connector like this [code](https://github.com/WataruMaeda/react-native-boilerplate/blob/master/src/utils/connector.js#L41-L42). Lastly import module in [store](https://github.com/WataruMaeda/react-native-boilerplate/blob/master/src/utils/store.js#L21) as well.

#### Assets

Images, icons and fonts are controlled under [theme](https://github.com/WataruMaeda/react-native-boilerplate/tree/master/src/theme). If you add new assets, you need to import the new assets in each files to access the assets from theme. Also, assets preloading is implemented as well. You can also use svg file in the boilerplate. All the assets are ready to use by importing theme.

#### Absolute path

If your project structure become complicated and has a lot of nested folders, you will have problem with relative paths. In the boilerplate, you can use absolute paths. You can write simple import statement i.e 'components/Button'. No more ../../../components/Button. The configuration is written in `babel.config.js`.

#### Code formatting, fixing and testing on pre commit

It's very important to keep code clean to maintain readability and productivity. In the boilerplate, Eslint, Prettier and Jest configuration are done. It's continuously checking and format your code while you coding (Please enable "Format on Save" option if you prefer to format code after save change). After you submit changes, pre commit script will run to handle checking and formatting your code, run test. If the 3 steps are passed, you will be able to push the change.

## Libraries

- [expo](https://github.com/expo/expo)
- [react-navigation 4.x](https://github.com/react-navigation/react-navigation)
- [redux](https://github.com/reduxjs/redux)
- [redux-logger](https://github.com/LogRocket/redux-logger)
- [redux-thunk](https://github.com/reduxjs/redux-thunk)
- [moment](https://github.com/moment/moment)
- [axios](https://github.com/axios/axios)
- [react-native-vector-icons](https://github.com/oblador/react-native-vector-icons)
- [react-native-svg](https://github.com/react-native-community/react-native-svg)

## Libraries for development

- [eslint](https://github.com/eslint/eslint)
- [prettier](https://github.com/prettier/prettier)
- [jest](https://jestjs.io/)
- [pre commit](https://github.com/observing/pre-commit)

*Developer: NashTheCoder*