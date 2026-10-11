# Multi-Tier Architecture Overview

## The Web/Application Tier
The Web/Application Tier serves as the user-facing layer of the stack. Its primary roles include:
* Handling incoming HTTP/HTTPS user requests.
* Rendering user interfaces and views.
* Executing core application logic and passing database inquiries down to the data tier.

## The Database Tier
The Database Tier functions as the persistence layer. Its primary roles include:
* Storing persistent enterprise data, user credentials, system settings, and metadata securely.
* Executing database queries reliably and ensuring data consistency across operations.

## Why Separate Them?
Separating the web server and database into distinct containers isolates security vulnerabilities, ensuring an exploit in the frontend doesn't immediately compromise backend data. It also enables independent scaling and maintenance—you can easily update or scale the web application without tearing down or risking corrupting the persistent database environment.
