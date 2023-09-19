# REST Star Wars User Security Endpoints


### Features
- Signup
  - Endpoint de registro de usuario, con comprobacion en caso de que el usuario o correo ya exista en la base de datos. El registro de contraseña se hará encriptad mediante JWT
- Login
  - Checking both by email or username that they exist, and checking that the password matches the one registered. A JWT function will be used to do this so as not to decrypt it and thus not to compromise the security of the user. Additionally, a token will be created and stored in the user's LocalStorage to verify that the user is logged in.
- Private
  - By using a JWT decorator, the user's profile entry is protected. You will only be able to log in if you have saved your token (i.e. if you are logged in).

>[!IMPORTANT]
> In all cases, checks will be made of the data submitted, as well as the type of data, in order to record all possible **types of errors**
