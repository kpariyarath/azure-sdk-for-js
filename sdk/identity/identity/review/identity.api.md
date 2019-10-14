## API Report File for "@azure/identity"

> Do not edit this file. It is a report generated by [API Extractor](https://api-extractor.com/).

```ts

import { AccessToken } from '@azure/core-http';
import { GetTokenOptions } from '@azure/core-http';
import { ServiceClientOptions } from '@azure/core-http';
import { TokenCredential } from '@azure/core-http';

export { AccessToken }

// @public
export class AggregateAuthenticationError extends Error {
    constructor(errors: any[]);
    errors: any[];
}

// @public
export const AggregateAuthenticationErrorName = "AggregateAuthenticationError";

// @public
export class AuthenticationError extends Error {
    constructor(statusCode: number, errorBody: object | string | undefined | null);
    readonly errorResponse: ErrorResponse;
    readonly statusCode: number;
}

// @public
export const AuthenticationErrorName = "AuthenticationError";

// @public
export class AuthorizationCodeCredential implements TokenCredential {
    constructor(tenantId: string, clientId: string, clientSecret: string | undefined, authorizationCode: string, redirectUri: string, options?: IdentityClientOptions);
    getToken(scopes: string | string[], options?: GetTokenOptions): Promise<AccessToken | null>;
    }

// @public
export type BrowserLoginStyle = "redirect" | "popup";

// @public
export class ChainedTokenCredential implements TokenCredential {
    constructor(...sources: TokenCredential[]);
    getToken(scopes: string | string[], options?: GetTokenOptions): Promise<AccessToken | null>;
    }

// @public
export class ClientCertificateCredential implements TokenCredential {
    constructor(tenantId: string, clientId: string, certificatePath: string, options?: IdentityClientOptions);
    getToken(scopes: string | string[], options?: GetTokenOptions): Promise<AccessToken | null>;
    }

// @public
export class ClientSecretCredential implements TokenCredential {
    constructor(tenantId: string, clientId: string, clientSecret: string, options?: IdentityClientOptions);
    getToken(scopes: string | string[], options?: GetTokenOptions): Promise<AccessToken | null>;
    }

// @public
export class DefaultAzureCredential extends ChainedTokenCredential {
    constructor(identityClientOptions?: IdentityClientOptions);
}

// @public
export class DeviceCodeCredential implements TokenCredential {
    constructor(tenantId: string, clientId: string, userPromptCallback: DeviceCodePromptCallback, options?: IdentityClientOptions);
    getToken(scopes: string | string[], options?: GetTokenOptions): Promise<AccessToken | null>;
    }

// @public
export interface DeviceCodeDetails {
    message: string;
    userCode: string;
    verificationUri: string;
}

// @public
export type DeviceCodePromptCallback = (deviceCodeDetails: DeviceCodeDetails) => void;

// @public
export class EnvironmentCredential implements TokenCredential {
    constructor(options?: IdentityClientOptions);
    getToken(scopes: string | string[], options?: GetTokenOptions): Promise<AccessToken | null>;
}

// @public
export interface ErrorResponse {
    correlation_id?: string;
    error: string;
    error_codes?: number[];
    error_description: string;
    timestamp?: string;
    trace_id?: string;
}

// @public
export function getDefaultAzureCredential(): TokenCredential;

export { GetTokenOptions }

// @public
export interface IdentityClientOptions extends ServiceClientOptions {
    authorityHost?: string;
}

// @public
export class InteractiveBrowserCredential implements TokenCredential {
    constructor(tenantId: string, clientId: string, options?: InteractiveBrowserCredentialOptions);
    getToken(scopes: string | string[], options?: GetTokenOptions): Promise<AccessToken | null>;
}

// @public
export interface InteractiveBrowserCredentialOptions extends IdentityClientOptions {
    loginStyle?: BrowserLoginStyle;
    postLogoutRedirectUri?: string | (() => string);
    redirectUri?: string | (() => string);
}

// @public
export class ManagedIdentityCredential implements TokenCredential {
    constructor(clientId?: string, options?: IdentityClientOptions);
    getToken(scopes: string | string[], options?: GetTokenOptions): Promise<AccessToken | null>;
    }

export { TokenCredential }

// @public
export class UsernamePasswordCredential implements TokenCredential {
    constructor(tenantIdOrName: string, clientId: string, username: string, password: string, options?: IdentityClientOptions);
    getToken(scopes: string | string[], options?: GetTokenOptions): Promise<AccessToken | null>;
    }


// (No @packageDocumentation comment for this package)

```