# Permissions In Django Rest Framework

- Permissions in Django Rest Framework are used to grant or deny access for different types of users to different parts of the API. Permissions are very useful when serving API resources/end-points with certain restrictions. 
-  For example, let's consider you are writing an api endpoint to create an answer to a question just like stackoverflow. It only allows an authenticated user to create the answers. In this case we restrict the user by checking user is authenticated or not. If user user is authenticated then we allow user to access the API resource otherwise we deny the user. It's a simple example to use django rest permission

# Permissions Flow in DRF
- Whenever any request comes to DRF then it enters the "dispatch" method. "dispatch" method should route the request to appropriate request method like "get", "post", "put", "delete", etc. But, before routing the request to the one of these methods it will checks the authentication, "permissions" and then it checks throttles(i.e used to limit the number of requests per user or per IP). In Django REST framework we always define permissions as a list. In DRF we can setup global permission classes or we can specify the permission classes in Views and Viewsets. If all permission checks are valid then request will be passed to appropriate method (i.e "get", "post", "put", "delete", etc. ) based on the request type otherwise an exception will be raised.

# Default Permissions Classes provided by DRF¶
- AllowAny : This permission class do not restrict the user to access the API resource.
- IsAuthenticated : This permission class only permits authenticated or logged in users to access the API resource.
- IsAdminUser : This permission class only allows Django Admin Users(i.e user.is_staff = True) to access the api resource and all other users will not be able access the API resource.
- IsAuthenticatedOrReadOnly
    - This permission class allows authenticated users to perform read and write operations on the API resource.
    - All users which are not authenticated will have read access only. If they try to update the API resource then it will raise permission denied error.
- DjangoModelPermissions
    - It is based on model permissions provided by django.contrib.auth.
    - It only be applied to views that have a queryset property.
    - It only applied on authenticated users who has the relevant model permissions assigned.
    - POST requests require the user to have the add permission on the model.
    - PUT and PATCH requests require the user to have the change permission on the model.
    - DELETE requests require the user to have the delete permission on the model.
- DjangoModelPermissionsOrAnonReadOnly : Same as DjangoModelPermissions, but it also allows unauthenticated users to have read-only access to the API resource.
