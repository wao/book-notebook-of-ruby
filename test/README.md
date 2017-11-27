# Test

## Tip 1: Write UnitTest when you start to debug your code

Ruby is very handy to write tools. So people general ignore unittest for this purpose. However, small code snippets can grow to a huge project. When you keep running same command from console to debug your tools, it is time to refactory your code and write unit tests.

By writing unit test, you will get following benefit:
  * It can make your debug process more smoothly. With the help of existing tools such as fixtures, factory_girl, mock and stub, there is no need to keep typing same command again. No need to input same text in cosole repeatable.
  * To support unit test, you will be force to stop add adhoc code and rethink your archecture of code, split code into modules, classes, interfaces.
  * After that, you can rerun unit test routinely to assure yourself that the same bug desn't come back again.

Writing test cases is painful. But you have some method to relieve it.

  1. Using tools to generate skeleton code for unit test.
  2. Using increment method to add unit test. It means you can write unit test for any code you modified and new added.


## Tip 2: Using generator to generate support code for unit test

## Tip 3: Select your toolkit for unit test

Here are my choices.

#### Minitest

It's ruby stdlib test tools. Simple, Easy. However, it lacks class level setup() function due to the fact that for each case, it'll launch a new ruby process to run it.

#### Shoulda-Context

For a ruby class, at most time, you have several different setup/teardown to run. In traditional minitest, you must write several TestCase for these setups. Using Shoulda-Context, you can define as many setup() as you like.

#### Mocha

Although minitest has own mock support, I still recommdent to use 'mocha' since minitest-mock lack some important feature. Using mocha you can get all you want to write test.

#### FactoryGirl
