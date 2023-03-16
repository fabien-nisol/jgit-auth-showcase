# jgit-auth-showcase
A showcase for cloning a git repository with jgit using either username/password, or username/private_access_token

## Building

> ./gradlew shadowJar

## Running

> java -jar ./app/build/libs/app-all.jar

### Public github access example

> java -jar app/build/libs/app-all.jar <gitlab|github project url> ./clone

### Private github/gitlab access example with username/password

❯ java -jar app/build/libs/app-all.jar <gitlab|github project url> ./clone -u <username> -p
Enter value for --password (Password): ***********

### Private github/gitlab access example with username/token

Create a personal access token from [github](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token) or [gitlab](https://docs.gitlab.com/ee/user/profile/personal_access_tokens.html) and then use it with this command:

❯ java -jar app/build/libs/app-all.jar <gitlab|github project url> ./clone -u <username> -t
Enter value for --personal-access-token (Personal access token): ***********
