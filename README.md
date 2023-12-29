# CrossOrigin, CORS, Preflight Request, Options Method

Welcome to the repository for my blog post on Cross-Origin Resource Sharing (CORS). In this article, we explore the ins and outs of CORS, offering insights into its importance, preflight request, options method. Whether you're a developer, system administrator, or just curious about CORS, this blog post is designed to provide valuable information on managing cross-origin requests.

## Table of Contents

1. [Introduction to CORS](#introduction-to-cors)
2. [Why CORS Matters](#why-cors-matters)
3. [CORS as a Security](#cors-as-a-security)
4. [Preflight Mechanism](#preflight-mechanism)
5. [Option Method](#option-method)
6. [Conclusion](#conclusion)
7. [Resources](#resources-to-deep-down-into-cors)
8. [Connect for more](#connect-with-me-for-more)

## Introduction to CORS

CORS stands for Cross Origin Resource Sharing. It is an HTTP Header based mechanism. CORS is a critical security feature implemented by web browsers to control how web pages in one domain can request and interact with resources hosted on another domain. It is a mechanism which uses additional HTTP headers to tell the browser whether the specific web app can share resource with another web app.

It should be noted that both the web app should have different origin. Origin simply means some website link or domain or sub-domains.

## Why CORS Matters

Imagine you live in a city where each building represents a different website, and you, as a resident, are logged into these buildings with your personal information. Now, let's consider CORS as the security measures in place to prevent unauthorized access between these buildings. 

In a city without CORS-like security measures, any person from any building can freely enter other buildings. This poses a significant risk because a malicious person from one building could easily access and manipulate your personal belongings in other buildings where you are logged in. This lack of control allows for potential theft, unauthorized access, and compromise of your privacy across different buildings.

CORS ensures that only trusted websites (approved origins) can make requests to access your sensitive information.

## CORS as a Security

CORS as the security measures implemented between these buildings. With CORS, each building establishes rules and restrictions on who can enter. These rules ensure that only authorized individuals (requests from specific origins) are allowed access.

In this scenario:

1) Each building has a list of approved visitors (allowed origins).
2) If someone from a malicious building tries to enter another building, the security system (CORS) blocks their entry unless they are on the approved list.
3) This way, your personal belongings (data) are more secure because unauthorized access is restricted.

## Preflight Mechanism

Preflight Call or Request is made before the actual API call is made. Suppose website A wants resource from website B then firstly preflight request is made. After this browser allows CORS which uses additional headers to verify preflight request first then after verification it sends headers HTTP back to the website A or sender then the actual call is made (Post/Get/Put).

![CORS Image](https://miro.medium.com/v2/resize:fit:1400/1*zCXcC1VkBB16BDXUxkWoew.png)

## Option Method

The HTTP OPTIONS method plays a crucial role in the Cross-Origin Resource Sharing (CORS) preflight mechanism. The preflight mechanism is used by web browsers to check whether a cross-origin request is safe to send by first making an HTTP OPTIONS request to the server. Let's break down the role of the OPTIONS method in CORS preflight:

### Preflight Request: 
(i) Triggered by Complex Requests: When a web application makes a cross-origin request that is considered "complex" (e.g., includes headers such as Authorization or uses methods other than simple methods like GET or POST), browsers send an initial OPTIONS request to the target server before the actual request.

(ii) Additional Headers: The OPTIONS request includes headers like Access-Control-Request-Method and Access-Control-Request-Headers, indicating the intended method and additional headers that will be used in the actual request.

### Server Handling:
(i) Server Response: The server needs to handle the preflight request. It should respond with appropriate headers indicating which methods, headers, and origins are allowed.

(ii) CORS Headers: Common headers in the preflight response include Access-Control-Allow-Origin, Access-Control-Allow-Methods, and Access-Control-Allow-Headers. These headers specify the allowed origins, methods, and headers for the actual request.

## Conclusion

Summarize key takeaways from the blog post and emphasize the importance of CORS in building secure and robust web applications. Browsers use CORS in API such as Fetch or XMLHTTP Request to mitigate the risks of Cross origin HTTP Requests.

## Resources to deep down into CORS
- [CORS](https://developer.mozilla.org/en-US/docs/Glossary/CORS)
- [Ways to Reduce CORS Preflight Time](https://blog.bitsrc.io/4-ways-to-reduce-cors-preflight-time-in-web-apps-1f47fe7558)
- [Option Method Detail](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods/OPTIONS)

## Connect with me for more
-[LinkedIn](https://www.linkedin.com/in/vishakha-singhal-18983b1bb/)
-[Github](https://github.com/vishakha-singhal01)

Feel free to explore the resources in this repository to complement your understanding of CORS. Follow my Github Account for more such detailed and easy understanding of complex topics. 

