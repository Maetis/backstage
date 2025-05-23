## API Report File for "@backstage/backend-defaults"

> Do not edit this file. It is a report generated by [API Extractor](https://api-extractor.com/).

```ts
import { AuthService } from '@backstage/backend-plugin-api';
import express from 'express';
import { HttpAuthService } from '@backstage/backend-plugin-api';
import { HttpRouterService } from '@backstage/backend-plugin-api';
import { HttpRouterServiceAuthPolicy } from '@backstage/backend-plugin-api';
import { LifecycleService } from '@backstage/backend-plugin-api';
import { RequestHandler } from 'express';
import { RootConfigService } from '@backstage/backend-plugin-api';
import { Router } from 'express';
import { ServiceFactory } from '@backstage/backend-plugin-api';

// @public (undocumented)
export function createAuthIntegrationRouter(options: {
  auth: AuthService;
}): express.Router;

// @public
export function createCookieAuthRefreshMiddleware(options: {
  auth: AuthService;
  httpAuth: HttpAuthService;
}): Router;

// @public (undocumented)
export function createCredentialsBarrier(options: {
  httpAuth: HttpAuthService;
  config: RootConfigService;
}): {
  middleware: RequestHandler;
  addAuthPolicy: (policy: HttpRouterServiceAuthPolicy) => void;
};

// @public
export function createLifecycleMiddleware(
  options: LifecycleMiddlewareOptions,
): RequestHandler;

// @public
export const httpRouterServiceFactory: ServiceFactory<
  HttpRouterService,
  'plugin',
  'singleton'
>;

// @public
export interface LifecycleMiddlewareOptions {
  // (undocumented)
  config: RootConfigService;
  // (undocumented)
  lifecycle: LifecycleService;
}

// (No @packageDocumentation comment for this package)
```
