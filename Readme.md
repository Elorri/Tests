# Tests

This repository is design to shows examples of the different type of tests existing.

	Unit test
	Integrated test
	UI Integrated test
	Instrumented unit test/Connected unit test
	Instrumented integrated test/Connected integrated test
	UI Instrumented integrated test/UI Connected integrated test
	UI Automator Instrumented test/UI Automator Connected test
	
Most of the tests here are copy/paste from the googleSample repo.

	https://github.com/googlesamples/android-testing


## Unit test
	C:\AndroidStudioProjects\Examples\Tests\tests10\src\test\java\com\elorri\android\tests\EmailValidatorTest -> test email validity	
## Integrated test
	C:\AndroidStudioProjects\Examples\Tests\tests10\src\test\java\com\elorri\android\tests\SharedPreferencesHelperTest -> test a SharedPreferences
## UI Integrated test
Seems that testing a fragment will look something like this

	public class MyFragmentTest extends
		ActivityInstrumentationTestCase2<MyActivity>{

		MyFragment myFragment;

		public MyFragmentTest () {
			super(MyActivity.class);
		}

	   @Override
		public void setUp() throws Exception {
			super.setUp();

			// This have to be done because of some issues with dexmaker
			System.setProperty("dexmaker.dexcache", "/sdcard");
			// This have to be done because of the sharedUserId problem
			Thread.currentThread().setContextClassLoader(
				getClass().getClassLoader());

			myFragment = new MyFragment() {
				 //I can override methods here
			};

		}

		public void testMyMethod() throws Exception {
			myFragment.methodThatIWantToTest();
		}

	}


	 /************  CLASS THAT I WANT TO TEST *********/
	public class MyFragment extends Fragment{

		 public void methodThatIWantToTest(){
			/*..... more lines */
			final PackageManager packageManager = getActivity().getPackageManager();
			/*..... more lines ...*/
		 }
		 
	}
	
## Instrumented unit test/Connected unit test
	C:\AndroidStudioProjects\Examples\Tests\tests2\src\androidTest\java\com\elorri\android\tests\CalculatorTest -> test a Pojo object
## Instrumented integrated test/Connected integrated test
	C:\AndroidStudioProjects\Examples\Tests\tests1\src\androidTest\java\com\elorri\android\tests\LocalServiceTest -> test a Service
	C:\AndroidStudioProjects\Examples\Tests\tests11\src\androidTest\java\com\elorri\android\tests\LogHistoryAndroidUnitTest -> test parcelable write		
## UI Instrumented integrated test/UI Connected integrated test
	C:\AndroidStudioProjects\Examples\Tests\tests2\src\androidTest\java\com\elorri\android\tests\CalculatorActivityTest -> test an Activity
	C:\AndroidStudioProjects\Examples\Tests\tests2\src\androidTest\java\com\elorri\android\tests\HintMatcher -> test an EditText hint
	C:\AndroidStudioProjects\Examples\Tests\tests3\src\androidTest\java\com\elorri\android\tests\ChangeTextBehaviorTest -> test an Activity EditText
	C:\AndroidStudioProjects\Examples\Tests\tests4\src\androidTest\java\com\elorri\android\tests\HintMatchers -> test an EditText hint
	C:\AndroidStudioProjects\Examples\Tests\tests4\src\androidTest\java\com\elorri\android\tests\HintMatchersTest -> test an Activity EditText hint
	C:\AndroidStudioProjects\Examples\Tests\tests5\src\androidTest\java\com\elorri\android\tests\LongListActivityTest -> test an ListView
	C:\AndroidStudioProjects\Examples\Tests\tests6\src\androidTest\java\com\elorri\android\tests\LongListActivityTest -> test an implicit Espresso Intent (Camera take a picture)		
	C:\AndroidStudioProjects\Examples\Tests\tests6\src\androidTest\java\com\elorri\android\tests\ImageViewHasDrawableMatcher -> test an ImageView (if it has a drawable applied to it).	
	C:\AndroidStudioProjects\Examples\Tests\tests7\src\androidTest\java\com\elorri\android\tests\DialerActivityTest -> test an implicit Intent using Espresso Intent(Dialer)		
	C:\AndroidStudioProjects\Examples\Tests\tests8\src\androidTest\java\com\elorri\android\tests\MultiWindowTest -> test an AutocompleteTextView	
## UI Automator Instrumented test/UI Automator Connected test
	C:\AndroidStudioProjects\Examples\Tests\tests8\src\androidTest\java\com\elorri\android\tests\ChangeTextBehaviorTest -> test launching an app, press home, change edittext string
	

### Detail screen

![screen](../master/screenshot/Screenshot_contact_detail_screen.png "Watch contact details")
* [Glide] (https://github.com/bumptech/glide) 
	Licensed mostly under the Apache License, Version 2.0 

## License
	
		The MIT License (MIT)

	Copyright (c) 2016 ETCHEMENDY ELORRI

	Permission is hereby granted, free of charge, to any person obtaining a copy
	of this software and associated documentation files (the "Software"), to deal
	in the Software without restriction, including without limitation the rights
	to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
	copies of the Software, and to permit persons to whom the Software is
	furnished to do so, subject to the following conditions:

	The above copyright notice and this permission notice shall be included in all
	copies or substantial portions of the Software.

	THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
	IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
	FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
	AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
	LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
	OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
	SOFTWARE.





C:\AndroidStudioProjects\Examples\Tests\tests1\		-> https://github.com/googlesamples/android-testing/tree/master/integration/ServiceTestRuleSample/app
	
	C:\AndroidStudioProjects\Examples\Tests\tests1\src\androidTest\java\com\elorri\android\tests\LocalServiceTest -> test a Service	

C:\AndroidStudioProjects\Examples\Tests\tests2\		-> https://github.com/googlesamples/android-testing/tree/master/runner/AndroidJunitRunnerSample/app

	C:\AndroidStudioProjects\Examples\Tests\tests2\src\androidTest\java\com\elorri\android\tests\CalculatorActivityTest -> test an Activity
	C:\AndroidStudioProjects\Examples\Tests\tests2\src\androidTest\java\com\elorri\android\tests\CalculatorTest -> test a Pojo object
	C:\AndroidStudioProjects\Examples\Tests\tests2\src\androidTest\java\com\elorri\android\tests\HintMatcher -> test an EditText hint
	
C:\AndroidStudioProjects\Examples\Tests\tests3\		-> https://github.com/googlesamples/android-testing/tree/master/ui/espresso/BasicSample
	
	C:\AndroidStudioProjects\Examples\Tests\tests3\src\androidTest\java\com\elorri\android\tests\ChangeTextBehaviorTest -> test an Activity EditText
	
	
C:\AndroidStudioProjects\Examples\Tests\tests4\		-> https://github.com/googlesamples/android-testing/tree/master/ui/espresso/CustomMatcherSample
	
	C:\AndroidStudioProjects\Examples\Tests\tests4\src\androidTest\java\com\elorri\android\tests\HintMatchers -> test an EditText hint
	C:\AndroidStudioProjects\Examples\Tests\tests4\src\androidTest\java\com\elorri\android\tests\HintMatchersTest -> test an Activity EditText hint
	
C:\AndroidStudioProjects\Examples\Tests\tests5\		-> https://github.com/googlesamples/android-testing/blob/master/ui/espresso/DataAdapterSample
	
	C:\AndroidStudioProjects\Examples\Tests\tests5\src\androidTest\java\com\elorri\android\tests\LongListActivityTest -> test an ListView
	
C:\AndroidStudioProjects\Examples\Tests\tests6\		-> https://github.com/googlesamples/android-testing/blob/master/ui/espresso/IntentsAdvancedSample/
	
	C:\AndroidStudioProjects\Examples\Tests\tests6\src\androidTest\java\com\elorri\android\tests\ImageViewerActivityTest -> test an implicit Intent using Espresso Intent(Camera take a picture)	
	C:\AndroidStudioProjects\Examples\Tests\tests6\src\androidTest\java\com\elorri\android\tests\ImageViewHasDrawableMatcher -> test an ImageView (if it has a drawable applied to it).

C:\AndroidStudioProjects\Examples\Tests\tests7\		-> https://github.com/googlesamples/android-testing/blob/master/ui/espresso/IntentsBasicSample
	
	C:\AndroidStudioProjects\Examples\Tests\tests7\src\androidTest\java\com\elorri\android\tests\DialerActivityTest -> test an implicit Intent using Espresso Intent(Dialer)	

C:\AndroidStudioProjects\Examples\Tests\tests8\		-> https://github.com/googlesamples/android-testing/blob/master/ui/espresso/MultiWindowSample
	
	C:\AndroidStudioProjects\Examples\Tests\tests8\src\androidTest\java\com\elorri\android\tests\MultiWindowTest -> test an AutocompleteTextView

C:\AndroidStudioProjects\Examples\Tests\tests9\		-> https://github.com/googlesamples/android-testing/blob/master/ui/uiautomator/BasicSample/app
	
	C:\AndroidStudioProjects\Examples\Tests\tests9\src\androidTest\java\com\elorri\android\tests\ChangeTextBehaviorTest -> test launching an app, press home, change edittext string

C:\AndroidStudioProjects\Examples\Tests\tests10\		-> https://github.com/googlesamples/android-testing/blob/master/unit/BasicSample/app
	
	C:\AndroidStudioProjects\Examples\Tests\tests10\src\androidTest\java\com\elorri\android\tests\EmailValidatorTest -> test email validity
	C:\AndroidStudioProjects\Examples\Tests\tests10\src\androidTest\java\com\elorri\android\tests\SharedPreferencesHelperTest -> test a SharedPreferences	

C:\AndroidStudioProjects\Examples\Tests\tests11\		-> https://github.com/googlesamples/android-testing/tree/master/unit/BasicUnitAndroidTest
	
	C:\AndroidStudioProjects\Examples\Tests\tests11\src\androidTest\java\com\elorri\android\tests\LogHistoryAndroidUnitTest -> test parcelable write
	



Things you usually need to mock

	Fragment
	FragmentManager
	Intent
	Context
	View
	Button
	Resources
	Bundle
	ViewPropertyAnimator
	Application
	Activity
	https://github.com/dpreussler/mockitoid/blob/master/lib/src/main/java/de/jodamob/mockitoid/AndroidMocks.java
	
https://github.com/dpreussler/mockitoid
difference between mock and any









