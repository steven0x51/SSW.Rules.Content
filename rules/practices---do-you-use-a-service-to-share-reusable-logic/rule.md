---
type: rule
archivedreason: 
title: Practices - Do you use a Service to share reusable logic?
guid: f9f41249-c8c4-4d11-a75a-79d397810ff1
uri: practices---do-you-use-a-service-to-share-reusable-logic
created: 2018-11-01T21:11:35.0000000Z
authors:
- id: 82
  title: Barry Sanders
- id: 34
  title: Brendan Richards
related: []

---

A Service is a singleton object with a lifetime scope of the application.  It is instantiated only once during the lifetime of an application.  When combined with Angular’s Dependency Injection, a service can be injected into any component in an application via Constructor Injection. This makes a Service perfect for sharing reusable functionality throughout an application.

<!--endintro-->

A common example of when you’d use a Service is when you want to retrieve data from a WebApi using the HttpClient. There may be several places in your application where you need to retrieve the same list of data. By placing this functionality in a Service it gets rid of the duplicated code in the components that make the WebApi call.
<dl class="badImage">&lt;dt&gt;<img src="reusable-service-bad.jpg" alt="reusable-service-bad.jpg">&lt;/dt&gt;<dd>Figure: Bad Example - Code that is reusable should be placed in a Service</dd></dl><dl class="goodImage">&lt;dt&gt;<img src="reusable-service-good.jpg" alt="reusable-service-good.jpg">&lt;/dt&gt;<dd>Figure: Good Example -  Reusable code is placed in a Service and the component calls the Service</dd></dl>