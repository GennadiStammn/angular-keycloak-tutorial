# angular-keycloak-tutorial
Angular + Keycloak example projekt

## start keycloak

`docker-compose up`

## initialize keycloak and demo user

* log into administration console with admin user `http://localhost:8080/auth`
* create a new realm e.g. `my-demo-realm` 
* using the created realm create an new user
	* users -> add user
	* set username
	* set Email Verified to ON
	* in Credentials set a temporary password
* login with the new user / temporary password into the demo realm
	* `http://localhost:8080/auth/realms/my-demo-realm/account/`
	* insert a new password when asked
	* complete required fields such as email, firstname, lastname
* your are ready to use the user

## creating an angular project

Angular project with routing.

`ng new demo-frontend --routing`

Generate two components.

`ng generate component public-space`
`ng generate component restricted-space`

Add routing to the AppRoutingModule to redirect to the two components.

Create router links.

## install keylocak-angular and keycloak-js library

`npm install keycloak-angular keycloak-js`