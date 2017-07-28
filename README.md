# How to implement forms authentication?

## What is Authentication?
> Authentication is giving access to the user for a specific service by verifying his/her identity using his/her credentials like username and password or email and password.

## What is Authorization?
> Authorization is Verify the user logged-in and check he/she can able to access the page.

## What is forms authentication?
> In this type of authentication, the user will explicitly have to provide his credentials and these credentials, once verified by the server, will let the user to log in.

## How to enable forms authentication?
> Edit web.config file and add following lines inside tag.

```xml
<authentication mode="Forms">
   <forms loginUrl="~/Account/Login" timeout="2000"/>
</authentication>
```
> After successfully validate the user credentials use below line for enable forms authentication.
```c#
FormsAuthentication.SetAuthCookie("Name", false);
```
> Logout the loggedin user use below code.
```c#
FormsAuthentication.SignOut();
```
