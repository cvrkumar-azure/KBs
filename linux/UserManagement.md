# User Management

All user manangment commands need to be executed with `sudo`, so the user who is creating/modifying users should be part of `sudoers` file.

## Adding users

`useradd` is the command that let's you add users. However, this is a very basic command with limited options.

`adduser` is an enhanced command and generally used.

```bash
sudo add user <user_name>
```
Example
```bash
sudo add user wjohnson
```
when you create a user in `Ubuntu` with `adduser` command it will prompt you to enter password for the user.
However in some distributinos like `Centos`, you may have to update password manually using the below commands

```bash
sudo passwd <user_name>
```
Example

```bash
sudo passwd wjohnson
```

Everytime a user account is created a group with the same name is also created by default.
For example, if a user called `testuser` is created and a group with the name `testuser` is also created.

To create a user in a different group other than the one with his user name, use `--ingroup` option.
```bash
sudo adduser <newusername> --ingroup <groupname>
```

For instance if you would like to create a user with the username `tester` but not create a group with the same name and want him to be part of the group `qa`
then use the below command:

```bash
sudo adduser tester --ingroup qa
```

To delete a user use the below commands

```bash
sudo userdel <user-name>
```

All the user details are stored in the file `/etc/passwd`. It is not recommended to edit these files, use usermod instead


## User Groups

Groups are a way to organize users. Everyuser is part of a default group.

To create a group use the below command

```bash
sudo groupadd <group_name>
```

Example:

```bash
sudo groupadd tesers
```

To delete a user, use the below command


```bash
sudo groupdel <group_name>
```

Example:

```bash
sudo groupdel tesers
```

To see the groups to which a user belongs to use the `groups` command

The below command gives the list of groups to which the current user is part of

```bash
groups
```

To see the list of groups for another user, use the below command

```bash
groups <username>
```

For example if you're logged in as `john` but would like to see the groups of `alice`, use the below command:

```bash
groups alice
```


Information about all the groups is stored in the file `/etc/group`

## Switching Users

su  -- Switch user ; to login as a different user
```bash
su - <username>
```
For example if you're logged in as `john` but would like to switch to tu user `alice`, use the below command:
[this assumes you know the password for the user `alice`]

```bash
su - alice
```

If you're a superuser, you need not know the password for the user you can `sudo su`

```bash
sudo su - alice
```

To logout from the session:

```bash
exit
```


# Modfiy user attributes:

The command `usermod` is used to change the attributes of a user

For instance, to add a user to an existing group we use usermod


```bash
sudo usermod -aG <groupname> <username>
```

Exmple: Lets add a user `tester4` to the group `qa`

```bash
sudo usermod -aG qa tester4
```
