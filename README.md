<p align="center">
  <h2 align="center">Serverless form-based Angular6+ starter</h2>
  <p align="center">
    <a href="https://travis-ci.org/me-io/angular-2-starter">
      <img src="https://img.shields.io/travis/me-io/angular-2-starter/master.svg?style=flat-square" alt="Travis Status">
    </a>
    <a href="LICENSE.md">
      <img src="https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square" alt="Software License">
    </a>
    <a href="https://david-dm.org/me-io/angular-2-starter">
      <img src="https://img.shields.io/david/me-io/angular-2-starter.svg?style=flat-square" alt="Dependencies">
    </a> 
    <a href="https://david-dm.org/me-io/angular-2-starter?type=dev">
      <img src="https://img.shields.io/david/dev/me-io/angular-2-starter.svg?style=flat-square" alt="devDependencies">
    </a> 
    <a href="https://www.paypal.me/meabed">
      <img src="https://img.shields.io/badge/paypal-donate-179BD7.svg?style=flat-squares" alt="Donate">
    </a>
  </p>
</p>



Changelog
---------
Changes and version updates will be posted here





Using Form.io
---------
You can also use this application with your own Form.io project. This will use the API's provided by your project to host all of
the data for this application. 

1. First login or create an account @ [Form.io](https://portal.form.io)
2. Create a new project called "Event Manager"
3. Under Advanced Options, click on **Upload A Project Template**, then select the **```/src/project.json```** file from this repository.
  
    ![](https://monosnap.com/file/yITvSniWzfdYJPLdfhC4bWHZEd9LBq.png)
  
4. Click on **Create Project** button.
5. After the project is created, copy the API path of your project. It should look like https://yourproject.form.io
6. Make the following change to the **```src/config.ts```** file, and replace ```[PROJECT_API]``` with the api of your project.

    ```ts
    import { FormioAppConfig } from 'angular-formio';
    import { FormioAuthConfig } from 'angular-formio/auth';

    export const AppConfig: FormioAppConfig = {
      appUrl: '[PROJECT_API]',
      apiUrl: 'https://api.form.io',
      icons: 'fontawesome'
    };

    export const AuthConfig: FormioAuthConfig = {
      login: {
        form: 'user/login'
      },
      register: {
        form: 'user/register'
      }
    };
    ```

7. Launch the application

    ```
    ng serve
    ```


