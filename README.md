<a id="readme-top"></a>

<!-- PROJECT LOGO -->
<br />
<div align="center">
  <p>Company or propject logo here</p>
  <a href="https://github.com/Tjwever/readme-template">
    <img src="images/logo.png" alt="Logo" width="80" height="80">
  </a>

  <h3 align="center">Project Name</h3>

  <p align="center">
    <a href="https://github.com/Tjwever/readme-template">View Demo</a>
  </p>
</div>



<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>



### Built With

This section should list any major frameworks/libraries used to bootstrap your project. Leave any add-ons/plugins for the acknowledgements section. Here are a few examples.

* [![Nest][Nest.js]][Nest-url]
* [![Next][Next.js]][Next-url]
* [![React][React.js]][React-url]
* [![ReactQuery][ReactQuery.js]][ReactQuery-url]
* [![MySql][MySql.js]][MySql-url]
* [![Postgres][Postgres.js]][Postgres-url]

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- GETTING STARTED -->
## Getting Started

This is an example of how you may give instructions on setting up your project locally.
To get a local copy up and running follow these simple example steps.

### Prerequisites

This is an example of how to list things you need to use the software and how to install them.
* npm
  ```sh
  npm install npm@latest -g
  ```

### Installation

_Below is an example of how you can instruct your audience on installing and setting up your app. This template doesn't rely on any external dependencies or services._

1. Get a free API Key at [https://example.com](https://example.com)
2. Clone the repo
   ```sh
   git clone https://github.com/github_username/repo_name.git
   ```
3. Install NPM packages
   ```sh
   npm install
   ```
4. Enter your API in `config.js`
   ```js
   const API_KEY = 'ENTER YOUR API';
   ```
5. Change git remote url to avoid accidental pushes to base project
   ```sh
   git remote set-url origin github_username/repo_name
   git remote -v # confirm the changes
   ```

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- Database -->
## Database useage

Section about what database technologies that are being used for this project, such as MySql or Postgres.
Also good for knowledge on how to setup locally if need be

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- Migrations -->
## Seeding and Migrations

A section on how Seeding and migrations are handled if they apply to the application.  How to handle new migrations, on each environment.

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- Repo Management -->
## Repository Management

How the CI / CD is handled, which branches are important for deploying and how developers should be handling pushing/pulling/forking of them.

### Pulling Pushing Forking Methods

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Naming Conventions for branches

Naming conventions dictated by your tech lead

Common naming conventions my be:
<ul>
  <li>feature/us-story-number/description</li>
  <li>bug/us-story-number/description</li>
  <li>feature/developer-name/description</li>
</ul>

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- Structure / Architecture -->
## Project Structure and Architecture

```sh
src/
├── main.ts             // Entry point of the application (bootstrapping Nest)
├── app.module.ts       // Root module, imports all feature modules
├── common/             // Shared, reusable components across modules
│   ├── filters/        // Exception filters (e.g., Global exceptions)
│   │   └── http-exception.filter.ts
│   ├── guards/         // Authentication/Authorization guards
│   │   └── auth.guard.ts
│   ├── interceptors/   // Interceptors (e.g., logging, transformation)
│   │   └── transform.interceptor.ts
│   ├── pipes/          // Validation pipes (e.g., DTO validation)
│   │   └── validation.pipe.ts
│   └── constants/      // Global constants or enums
│       └── roles.enum.ts
├── config/             // Configuration files (e.g., database, environment)
│   ├── configuration.ts
│   └── validation-schema.ts // Joi schema for environment variables
├── database/           // Database-related files (if not using ORM with entities in modules)
│   ├── migrations/
│   │   └── 20230101000000-initial-schema.ts
│   └── seeds/
│       └── initial-data.ts
├── modules/            // Feature modules (the core of your application)
│   ├── auth/
│   │   ├── auth.module.ts
│   │   ├── auth.controller.ts
│   │   ├── auth.service.ts
│   │   ├── strategies/ // Passport strategies (JWT, Local, etc.)
│   │   │   ├── jwt.strategy.ts
│   │   │   └── local.strategy.ts
│   │   └── dto/        // Data Transfer Objects (for request/response bodies)
│   │       ├── login.dto.ts
│   │       └── register.dto.ts
│   ├── users/
│   │   ├── users.module.ts
│   │   ├── users.controller.ts
│   │   ├── users.service.ts
│   │   ├── users.repository.ts // If using custom repositories
│   │   ├── entities/   // Database entities (TypeORM, Mongoose schemas)
│   │   │   └── user.entity.ts
│   │   └── dto/
│   │       ├── create-user.dto.ts
│   │       └── update-user.dto.ts
│   └── ... (other feature modules)
├── shared/             // Less common shared components, perhaps utilities
│   └── utils/
│       └── date.utils.ts
└── tests/              // End-to-end and unit tests
    ├── unit/
    │   ├── users/
    │   │   └── users.service.spec.ts
    │   └── ...
    └── e2e/
        ├── app.e2e-spec.ts
        └── users.e2e-spec.ts
```

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- ABOUT THE PROJECT -->
## About The Project

Brief description of your project.

<p align="right">(<a href="#readme-top">back to top</a>)</p>


<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/othneildrew/Best-README-Template.svg?style=for-the-badge
[contributors-url]: https://github.com/othneildrew/Best-README-Template/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/othneildrew/Best-README-Template.svg?style=for-the-badge
[forks-url]: https://github.com/othneildrew/Best-README-Template/network/members
[stars-shield]: https://img.shields.io/github/stars/othneildrew/Best-README-Template.svg?style=for-the-badge
[stars-url]: https://github.com/othneildrew/Best-README-Template/stargazers
[issues-shield]: https://img.shields.io/github/issues/othneildrew/Best-README-Template.svg?style=for-the-badge
[issues-url]: https://github.com/othneildrew/Best-README-Template/issues
[license-shield]: https://img.shields.io/github/license/othneildrew/Best-README-Template.svg?style=for-the-badge
[license-url]: https://github.com/othneildrew/Best-README-Template/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/othneildrew
[product-screenshot]: images/screenshot.png
[Next.js]: https://img.shields.io/badge/next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white
[Next-url]: https://nextjs.org/
[Nest.js]: https://img.shields.io/badge/nestjs-E0234E?style=for-the-badge&logo=nestjs&logoColor=white
[Nest-url]: https://nestjs.org/
[React.js]: https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB
[React-url]: https://reactjs.org/
[Vue.js]: https://img.shields.io/badge/Vue.js-35495E?style=for-the-badge&logo=vuedotjs&logoColor=4FC08D
[Vue-url]: https://vuejs.org/
[Angular.io]: https://img.shields.io/badge/Angular-DD0031?style=for-the-badge&logo=angular&logoColor=white
[Angular-url]: https://angular.io/
[Svelte.dev]: https://img.shields.io/badge/Svelte-4A4A55?style=for-the-badge&logo=svelte&logoColor=FF3E00
[Svelte-url]: https://svelte.dev/
[Laravel.com]: https://img.shields.io/badge/Laravel-FF2D20?style=for-the-badge&logo=laravel&logoColor=white
[Laravel-url]: https://laravel.com
[Bootstrap.com]: https://img.shields.io/badge/Bootstrap-563D7C?style=for-the-badge&logo=bootstrap&logoColor=white
[Bootstrap-url]: https://getbootstrap.com
[JQuery.com]: https://img.shields.io/badge/jQuery-0769AD?style=for-the-badge&logo=jquery&logoColor=white
[JQuery-url]: https://jquery.com
[ReactQuery.js]: https://img.shields.io/badge/React_Query-FF4154?style=for-the-badge&logo=react-query&logoColor=white
[ReactQuery-url]: https://tanstack.com/query/latest/docs/framework/react/overview
[MySql.js]: https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white
[MySql-url]: [https://img.shields.io/badge/React_Query-FF4154?style=for-the-badge&logo=react-query&logoColor=white](https://www.mysql.com/)
[Postgres.js]: https://img.shields.io/badge/postgresql-4169e1?style=for-the-badge&logo=postgresql&logoColor=white
[Postgres-url]: https://www.postgresql.org/
