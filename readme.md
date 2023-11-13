## Authentication with express, passport and JWT

The auth-jwt package - is a component of the @jla/node [packages set](https://github.com/JuliusAgency/node-packages-set) for Nodejs applications.  

<p>
  <a href="https://www.npmjs.com/package/@jla/auth-jwt" target="_blank">
    <img alt="Version" src="https://img.shields.io/npm/v/@jla/auth-jwt.svg">
  </a>
  <a href="https://github.com/JuliusAgency/auth-jwt#readme" target="_blank">
    <img alt="Documentation" src="https://img.shields.io/badge/documentation-yes-brightgreen.svg" />
  </a>
  <a href="https://github.com/JuliusAgency/auth-jwt/graphs/commit-activity" target="_blank">
    <img alt="Maintenance" src="https://img.shields.io/badge/Maintained%3F-yes-green.svg" />
  </a>
  <a href="https://github.com/JuliusAgency/auth-jwt/blob/master/LICENSE" target="_blank">
    <img alt="License: MIT" src="https://img.shields.io/badge/License-MIT-yellow.svg" />
  </a>
</p>

### Installation
```bash
  npm install --save @jla/auth-jwt
```

### Pre-conditions:
```
```

### Usage  
```
  import { AuthJwtOptions, setupAuthMiddleware } from '@jla/auth-jwt';  

  // Auth middleware setup
  const authJwtOptions: AuthJwtOptions = {
    secretKey: process.env.SECRET_JWT,
    lifeTime: 5, // minutes
  };
  const { authMiddleware, encodeToken } = setupAuthMiddleware(authJwtOptions);
  const protectedRoutes = ['/first', '/second'];
  app.use(protectedRoutes, authMiddleware);

  // Setup routers ...

```
