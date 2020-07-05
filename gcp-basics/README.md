# GCP Basics

```
Organization
                                                                Company
                                                                  |
                                                                  |
                                       ___________________________|_________________________
                                       |                          |                         |
                                     Dept A                      Dept B                    Dept C
                                       |                            |                       |
                                       |                            |                       |
                                       Projects                     Projects                Projects
                                        |                            |                      |
                                        |                            |                      |
                                        |__________                  |_________             |__________
                                        |       Project-A            |      Project-A       |       Project-A
                                        |                            |                      |
                                        |__________                  |_________             |__________
                                                Project-B                   Project-B               Project-B


```

Each Project Have these Values:

```
Project ID         Unique          Immutable

Project Name       Not-Unique      Mutable

Project Number     Unique          Immutable

```

# IAM-ROLES

3 Kind of Roles:

```
Primitive Roles ------- These are Wide Open Roles 

Predefined Roles ------ These are Service Level Roles

Custom Roles     ------ These are Custom Policies Developed By Customer
```

# Preexisting Roles 

```
Owner                 ---- Owner of the Project
Editor                ---- Role with Permissions on Specific Service
Viewer                ---- Read Only Role
Billing Administartor ---- Billing Access
```