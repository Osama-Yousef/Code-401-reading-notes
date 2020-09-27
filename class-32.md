# Read:32 Summary 
## DRF Permissions
### Permissions
* `permissions` : determine whether a request should be granted or denied access
* `Permission` : checks are always run at the very start of the view, before any other code is allowed to proceed. Permission checks will typically use the
authentication information in the request.user and request.auth properties to determine if the incoming request should be permitted.
* `Permissions` : are used to grant or deny access for different classes of users to different parts of the API.
* The simplest style of permission would be to allow access to any authenticated user, and deny access to any unauthenticated user. This corresponds to 
the IsAuthenticated class in REST framework.
* A slightly less strict style of permission would be to allow full access to authenticated users, but allow read-only access to unauthenticated users. This 
corresponds to the IsAuthenticatedOrReadOnly class in REST framework.
### How permissions are determined
* Permissions in REST framework are always defined as a list of permission classes.

* Before running the main body of the view each permission in the list is checked. If any permission check fails an exceptions.PermissionDenied or
exceptions.NotAuthenticated exception will be raised, and the main body of the view will not run.

* When the permissions checks fail either a "403 Forbidden" or a "401 Unauthorized" response will be returned, according to the following rules:

  * The request was successfully authenticated, but permission was denied. — An HTTP 403 Forbidden response will be returned.
  * The request was not successfully authenticated, and the highest priority authentication class does not use WWW-Authenticate headers. — An HTTP 403 Forbidden response will be returned.
  * The request was not successfully authenticated, and the highest priority authentication class does use WWW-Authenticate headers. — An HTTP 401 Unauthorized response, with an appropriate WWW-Authenticate header will be returned.

### Object level permissions
* REST framework permissions also support object-level permissioning. Object level permissions are used to determine if a user should be allowed to 
act on a particular object, which will typically be a model instance.

* Object level permissions are run by REST framework's generic views when .get_object() is called. As with view level permissions, an exceptions.PermissionDenied 
exception will be raised if the user is not allowed to act on the given object.

* If you're writing your own views and want to enforce object level permissions, or if you override the get_object method on a generic view, then you'll need to 
explicitly call the .check_object_permissions(request, obj) method on the view at the point at which you've retrieved the object.

* This will either raise a PermissionDenied or NotAuthenticated exception, or simply return if the view has the appropriate permissions.

### Limitations of object level permissions
* For performance reasons the generic views will not automatically apply object level permissions to each instance in a queryset when returning a list of objects.

* Often when you're using object level permissions you'll also want to filter the queryset appropriately, to ensure that users only have visibility onto instances
that they are permitted to view.

-------------------------------------------------------------------------------------------------------------------------------------------------------
## API Reference
### AllowAny
* The AllowAny permission class will allow unrestricted access, regardless of if the request was authenticated or unauthenticated.

* This permission is not strictly required, since you can achieve the same result by using an empty list or tuple for the permissions setting, but you may find it
useful to specify this class because it makes the intention explicit.
### IsAuthenticated
* The IsAuthenticated permission class will deny permission to any unauthenticated user, and allow permission otherwise.

* This permission is suitable if you want your API to only be accessible to registered users.
### IsAdminUser
* The IsAdminUser permission class will deny permission to any user, unless user.is_staff is True in which case permission will be allowed.

* This permission is suitable if you want your API to only be accessible to a subset of trusted administrators.
### IsAuthenticatedOrReadOnly
* The IsAuthenticatedOrReadOnly will allow authenticated users to perform any request. Requests for unauthorised users will only be permitted if the request 
method is one of the "safe" methods; GET, HEAD or OPTIONS.

* This permission is suitable if you want to your API to allow read permissions to anonymous users, and only allow write permissions to authenticated users.

### DjangoModelPermissions
* This permission class ties into Django's standard django.contrib.auth model permissions. This permission must only be applied to views that have 
a .queryset property set. Authorization will only be granted if the user is authenticated and has the relevant model permissions assigned.

  * POST requests require the user to have the add permission on the model.
  * PUT and PATCH requests require the user to have the change permission on the model.
  * DELETE requests require the user to have the delete permission on the model.
* The default behaviour can also be overridden to support custom model permissions. For example, you might want to include a view model permission for GET requests.

* To use custom model permissions, override DjangoModelPermissions and set the .perms_map property. Refer to the source code for details.


***Using with views that do not include a queryset attribute.***

* If you're using this permission with a view that uses an overridden get_queryset() method there may not be a queryset attribute on the view. In this 
case we suggest also marking the view with a sentinel queryset, so that this class can determine the required permissions. For example:
```queryset = User.objects.none()  # Required for DjangoModelPermissions```

## Generic views
* `Django’s generic views`... were developed as a shortcut for common usage patterns... They take certain common idioms and patterns found in view development 
and abstract them so that you can quickly write common views of data without having to repeat yourself.
* One of the key benefits of class-based views is the way they allow you to compose bits of reusable behavior. REST framework takes advantage of this by
providing a number of pre-built views that provide for commonly used patterns.
* The generic views provided by REST framework allow you to quickly build API views that map closely to your database models.

* If the generic views don't suit the needs of your API, you can drop down to using the regular APIView class, or reuse the mixins and base classes used by
the generic views to compose your own set of reusable generic views.

-------------------------------------------------------------------------------------------------------------------------------------------------------------



























































