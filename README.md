# CSRF-Quick

### Quick and dirty checklist for CSRF 


1. Does the application rely soley on session based cookies for identication, nothing else?
AND
2. Does the application NOT include any kind of CSRF token as a part of the request outside of the cookies OR is the token itself predictable in nature (easy to guess, non-unique, not tied to a user's session, global etc) OR is the token tied to something under your control IE the token is not validated if the request method GET/POST is changed?
AND
3. If CORS is configured does it allow cross origin resource sharing?

Signs you might not have CSRF 
1. CORS is enabled and strictly configured
2. CSRF tokens are sent with the body of a POST request