---
layout: page
title: Session
permalink: /docs/session/
---

The instance is stored in the global "Session" class.

## CSRF token

```
Session::getCsrfInput()
```

Between the "<form method="post">" and the "</form>" tag in the view one should add "<&#63;php Session::getCsrfInput();&#63;>".
This call will echo a hidden input field to the form that will prevent Cross-Site-Request-Forgery (CSRF) attacks.

Note: this is required when sending a form with the "post" method.