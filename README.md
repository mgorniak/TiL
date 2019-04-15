# TiL
Today I learned

1. What was changed in PHP from v.5.6 to 7.3 (at least 3 main differences)?

2. Wha is a difference between composer install and composer update?

3. what is composer.lock?

4. What is pattern design?

5. What is antipattern?

6. What is interface and abstract class?

7. What is PSR and describe shortly 0-4.

Ad. 1.
- speed/performance - php 7 is minimum 2 times faster than php 5 - depends on kind of test/benchmark (including operations 
on databases), and using less amount of memory
- enable accurate type declarations (for arguments and returns) - in php 7 we can describe what kind of argument will be 
passed to function and we can describe what kind of data will be returned from function (integer, array, object, etc.)
- spaceship operator ('<=>'') - if left side is greater than right one it returns 1, if right side is greater than 
returns -1 and when both side are equal it returns 0
- null coalesce operator - it returns left side if it is different than null, if left side is null than returns right 
side (i.e. $userSecondName = $user->getSecondName() ?? 'no_second_name' it is equal to 
$userSecondName = ($user->getSecondName() === null) ? 'no_second_name' : $user->getSecondName() ). 
Additionally, if we use on the left side non-existing variable 
we won't get an error message (like it happens with '?:' operator) 
- group use declarations - when some use declarations have a common path part, we don't need to repeat it anymore. 
Instead, we can use it once and different end of the path we can put inside curly braces divided by comma and space 
(i.e. 'Doctrine\Common\Collections\{ArrayCollection, Collection}' )
- 64-bit - in php 7 we can use 64bit integers with no doubt (in php 5 we had 32bit integers as biggest)