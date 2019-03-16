# TiL
Today I learned

1. What was changed in PHP from v.5.4 to 7.4?

2. What is a difference between composer install and composer update?

3. what is composer.lock?

4. What is pattern design?

5. What is antipattern?

6. What is interface and abstract class?

7. What is PSR and describe shortly 0-4.

Ad. 2.
Composer install at start checks is composer.lock file exist and: 
- if it does composer install starts to install all packages based on composer.lock file. 
- if it does not exist it applies composer update path: based on composer.json file checks are all packages from this 
file installed and:
    - if it is -> composer will check is new version of current package is available and if it is - it will be installed
    - if it is not - composer will get newest version of this package and install it
    - at the end, after installing all actual version of packages new composer.lock file will be created and saved in project