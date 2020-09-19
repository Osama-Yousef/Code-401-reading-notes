# Read:26 Summary 
## Intro to Django
* `django` : The web framework for perfectionists with deadlines.
* With Django, you can take Web applications from concept to launch in a matter of hours. Django takes care of much of the hassle of Web development, so you
can focus on writing your app without needing to reinvent the wheel. It’s free and open source.
* Django was designed to help developers take applications from concept to completion as quickly as possible.
* Deﬁne your data models entirely in Python. You get a rich, dynamic database-access API for free — but you can still write SQL if needed.
* A clean, elegant URL scheme is an important detail in a high-quality Web application. Django encourages beautiful URL design and doesn’t put any cruft 
in URLs, like .php or .asp.
* To design URLs for an application, you create a Python module called a URLconf. Like a table of contents for your app, it contains a simple mapping
between URL patterns and your views.
* Django’s template language is designed to strike a balance between power and ease. It’s designed to feel comfortable and easy-to-learn to those used
to working with HTML, like designers and front-end developers. But it is also flexible and highly extensible, allowing developers to augment the template 
language as needed.
* Django provides a powerful form library that handles rendering forms as HTML, validating user-submitted data, and converting that data to native
Python types. Django also provides a way to generate forms from your existing models and use those forms to create and update data.
* Django comes with a full-featured and secure authentication system. It handles user accounts, groups, permissions and cookie-based user sessions. This lets
you easily build sites that let users to create accounts and safely log in/out.
* One of the most powerful parts of Django is its automatic admin interface. It reads metadata in your models to provide a powerful and production-ready 
interface that content producers can immediately use to start managing content on your site. It’s easy to set up and provides many hooks for customization.
* Django offers full support for translating text into different languages, plus locale-specific formatting of dates, times, numbers and time zones. It lets 
developers and template authors specify which parts of their apps should be translated or formatted for local languages and cultures, and it uses these hooks
to localize Web applications for particular users according to their preferences.
* Django provides multiple protections against:

  * Clickjacking
  * Cross-site scripting
  * Cross Site Request Forgery (CSRF)
  * SQL injection
  * Remote code execution
--------------------------------------------------------------------------------------------------------------------------------------------------------------------
## How Django Works Behind the Scenes
* Django is a Python-based web framework used by millions of developers and billions of consumers through popular apps like Instagram. It is open 
source, meaning the code is available for free on Github and can be downloaded onto any developer’s computer and used alongside the official documentation.
* Django’s code is open source and available to all. Django’s organization is managed by a non-profit, the DSF, with a miniscule budget. And Django code 
is lead by a core team of volunteers, two paid Django Fellows, and a larger group of contributors.
* One of the best ways to become more involved in Django is to attend an annual conference and meet all the contributors in person. Currently there are 
DjangoCons in the US, Europe, Australia, and Africa in 2020 for the first time
------------------------------------------------------------------------------------------------------------------------------------------------------------------
## What is Django ??!!
* `Django` : is a high-level Python web framework that enables rapid development of secure and maintainable websites. Built by experienced developers, Django takes
care of much of the hassle of web development, so you can focus on writing your app without needing to reinvent the wheel. It is free and open
source, has a thriving and active community, great documentation, and many options for free and paid-for support. 


***Django helps you write software that is:***


  * Complete : provides almost everything developers might want to do "out of the box". Because everything you need is part of the one "product", it all works 
  seamlessly together, follows consistent design principles

  * Versatile : Django can be (and has been) used to build almost any type of website — from content management systems and wikis, through to social networks 
  and news sites. It can work with any client-side framework, and can deliver content in almost any format (including HTML, RSS feeds, JSON, XML, etc). 
  * Secure : Django helps developers avoid many common security mistakes by providing a framework that has been engineered to "do the right things" to 
  protect the website automatically. For example, Django provides a secure way to manage user accounts and passwords, avoiding common mistakes like
  putting session information in cookies where it is vulnerable (instead cookies just contain a key, and the actual data is stored in the database) or
  directly storing passwords rather than a password hash.Django enables protection against many vulnerabilities by default, including SQL injection,
  cross-site scripting, cross-site request forgery and clickjacking (see Website security for more details of such attacks).
  * Scalable : Django uses a component-based “shared-nothing” architecture (each part of the architecture is independent of the others, and can hence be
  replaced or changed if needed). Having a clear separation between the different parts means that it can scale for increased traffic by adding hardware at
  any level: caching servers, database servers,or application servers. Some of the busiest sites have successfully scaled Django to meet their
  demands (e.g. Instagram and Disqus, to name just two).
  * Maintainable : Django code is written using design principles and patterns that encourage the creation of maintainable and reusable code. In particular,
  it makes use of the Don't Repeat Yourself (DRY) principle so there is no unnecessary duplication, reducing the amount of code. Django also promotes the
  grouping of related functionality into reusable "applications" and, at a lower level, groups related code into modules (along the lines of the Model
  View Controller (MVC) pattern).
  * Portable : Django is written in Python, which runs on many platforms. That means that you are not tied to any particular server platform, and can run
  your applications on many flavours of Linux, Windows, and Mac OS X. Furthermore, Django is well-supported by many web hosting providers, who often
  provide specific infrastructure and documentation for hosting Django sites.
* Django is "somewhat opinionated", and hence delivers the "best of both worlds". It provides a set of components to handle most web development tasks
and one (or two) preferred ways to use them. However, Django's decoupled architecture means that you can usually pick and choose from a number of 
different options, or add support for completely new ones if desired.
----------------------------------------------------------------------------------------------------------------------------------------------------------------------

  
















