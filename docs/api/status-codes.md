# Status Codes

In general we show meaningful error messages when something goes wrong in the iPad or Web app. However, there may be cases when you're working directly with the API (i.e. in [webhooks](./concepts/webhooks.md) where you receive a status code that you need clarity on.

> Use of the word "client" in this topic is a reference to the requesting user/application, not a client in the customer sense.

## 200 OK
- **Description**: The request has succeeded.

## 201 Created
- **Description**: The request has been fulfilled, and a new resource has been created.

## 400 Bad Request
- **Description**: The server could not process the request due to invalid syntax, malformed data, or because the request violates business rules, even if it is properly formed.

## 401 Unauthorized
- **Description**: The client must authenticate itself to get the requested response. Typically used when authentication credentials are missing or incorrect.

## 402 Payment Required
- **Description**: The subscription payment is either past-due or is a trial and has expired.

## 403 Forbidden
- **Description**: The client does not have permission to access the requested resource. Unlike 401, authenticating will not make a difference.

## 404 Not Found
- **Description**: The server could not find the requested resource. This status code is commonly used for non-existent endpoints or resources.

## 409 Conflict
- **Description**: Indicates that the request could not be completed due to a conflict with the current state of the target resource. Used for operations that would result in a conflict such as duplicate entries.

## 451 Unavailable For Legal Reasons
- **Description**: The tenant subscription has been suspended. This will occur if we suspect your tenant of violating terms of service and is being suspended.

## 500 Internal Server Error
- **Description**: A generic error message indicating that the server encountered an unexpected condition that prevented it from fulfilling the request.

## 503 Service Unavailable
- **Description**: The server is currently unable to handle the request due to temporary overloading or maintenance of the server. Typically, this is a temporary state.

