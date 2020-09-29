# Read:34 Summary
## Configuring Django Settings: Best Practices
### Managing Django Settings: Issues
* `Different environments`. Usually, you have several environments: local, dev, ci, qa, staging, production, etc. Each environment can have its own specific settings 
(for example: DEBUG = True, more verbose logging, additional apps, some mocked data, etc). You need an approach that allows you to keep all these Django 
setting configurations.

* `Sensitive data`. You have SECRET_KEY in each Django project. On top of this there can be DB passwords and tokens for third-party APIs like Amazon or Twitter. This 
data cannot be stored in VCS.

* `Sharing settings between team members`. You need a general approach to eliminate human error when working with the settings. For example, a developer may add a 
third-party app or some API integration and fail to add specific settings. On large (or even mid-size) projects, this can cause real issues.

* `Django settings are a Python code.` This is a curse and a blessing at the same time. It gives you a lot of flexibility, but can also be a problem – instead of 
key-value pairs, settings.py can have a very tricky logic.
### Setting Configuration: Different Approaches
* There is no built-in universal way to configure Django settings without hardcoding them. But books, open-source and work projects provide a lot of 
recommendations and approaches on how to do it best. Let’s take a brief look at the most popular ones to examine their weaknesses and strengths.

#### 12 Factors
* 12 Factors is a collection of recommendations on how to build distributed web-apps that will be easy to deploy and scale in the Cloud. It was created 
by Heroku, a well-known Cloud hosting provider.
* As the name suggests, the collection consists of twelve parts:

  * Codebase
  * Dependencies
  * Config
  * Backing services
  * Build, release, run
  * Processes
  * Port binding
  * Concurrency
  * Disposability
  * Dev/prod parity
  * Logs
  * Admin processes
* Each point describes a recommended way to implement a specific aspect of the project. Some of these points are covered by instruments like
Django, Python, pip. Some are covered by design patterns or the infrastructure setup.
#### django-environ
* Writing code using os.environ could be tricky sometimes and require additional effort to handle errors. It’s better to use django-environ instead.

* Technically it’s a merge of:

  * envparse
  * honcho
  * dj-database-url
  * dj-search-url
  * dj-config-url
  * django-cache-url
* This app gives a well-functioning API for reading values from environment variables or text files, handful type conversion, etc
#### Setting Structure
* Instead of splitting settings by environments, you can split them by the source: Django, third- party apps (Celery, DRF, etc.), and your custom settings.

#### Naming Conventions
* Naming of variables is one of the most complex parts of development. So is naming of settings. We can’t imply on Django or third-party
applications, but we can follow these simple rules for our custom (project) settings:
  * Give meaningful names to your settings.

  * Always use the prefix with the project name for your custom (project) settings.

  * Write descriptions for your settings in comments.

#### Django Settings: Best practices
  * Keep settings in environment variables.
  * Write default values for production configuration (excluding secret keys and tokens).

  * Don’t hardcode sensitive settings, and don’t put them in VCS.

  * Split settings into groups: Django, third-party, project.
  * Follow naming conventions for custom (project) settings.
#### Conclusion
* The Settings file is a small but very important part of any Django project. If you do it wrong, you’ll have a lot of issues during all phases of 
development. But if you do it right, it will be a good basis for your project that will allow it to grow and scale in the future.
* Using the environment variables approach, you can easily switch from a monolith to microservice architecture, wrap your project in Docker 
containers, and deploy it in any VPS or Cloud hosting platform such as: Amazon, Google Cloud, or your own Kubernetes cluster.

--------------------------------------------------------------------------------------------------------------------------------------------------
## SSH
* SSH, or Secure Shell, is a remote administration protocol that allows users to control and modify their remote servers over the Internet. The service was
created as a secure replacement for the unencrypted Telnet and uses cryptographic techniques to ensure that all communication to and from the remote
server happens in an encrypted manner. It provides a mechanism for authenticating a remote user, transferring inputs from the client to the host, and
relaying the output back to the client.
* The SSH key command instructs your system that you want to open an encrypted Secure Shell Connection. {user} represents the account you want to access.
For example, you may want to access the root user, which is basically synonymous for system administrator with complete rights to modify anything on the system.
{host} refers to the computer you want to access. This can be an IP Address (e.g. 244.235.23.19) or a domain name (e.g. www.xyzdomain.com).
* When you hit enter, you will be prompted to enter the password for the requested account. When you type it in, nothing will appear on the screen, but
your password is, in fact being transmitted. Once you’re done typing, hit enter once again. If your password is correct, you will be greeted with a 
remote terminal window.

* Gaining an in-depth understanding of the underlying how SSH works can help users understand the security aspects of this technology. Most people consider 
this process to be extremely complex and un-understandable, but it is much simpler than most people think. If you’re wondering how long it takes for
a computer to calculate a hash and authenticate a user, well, it happens in less than a second. In fact, the maximum amount of time is spent in 
transferring data across the Internet























































































