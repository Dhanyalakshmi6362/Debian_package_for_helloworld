classDiagram
class UserController {
-CreateUserService _createUserService
+UserController(CreateUserService createUserService)
+Create(string email, string username) User
}
class CreateUserService {
-UserModel _userModel
-SendWelcomeEmailService _sendWelcomeEmailService
-Kafka _kafka
+CreateUserService(UserModel um, SendWelcomeEmailService es, Kafka k)
+Call(string email, string username) User
-CheckActiveUsers(List~User~ users) bool
}# Debian_package_for_helloworld
