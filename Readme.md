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
	
### Unit test
[test email validity] (https://github.com/Elorri/Tests/tree/master/tests10/src/androidTest/java/com/elorri/android/tests/EmailValidatorTest)
	taken from [GoogleSamples] (https://github.com/googlesamples/android-testing/blob/master/unit/BasicSample/app)	
### Integrated test
[test a SharedPreferences] (https://github.com/Elorri/Tests/tree/master/tests10/src/androidTest/java/com/elorri/android/tests/SharedPreferencesHelperTest)
	taken from [GoogleSamples] (https://github.com/googlesamples/android-testing/blob/master/unit/BasicSample/app)	
### UI Integrated test
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
	
### Instrumented unit test/Connected unit test
[test a Pojo object] (https://github.com/Elorri/Tests/tree/master/tests2/src/androidTest/java/com/elorri/android/tests/CalculatorTest)
	taken from [GoogleSamples] (https://github.com/googlesamples/android-testing/tree/master/runner/AndroidJunitRunnerSample/app)
### Instrumented integrated test/Connected integrated test
[Test a Service] (https://github.com/Elorri/Tests/tree/master/tests1/src/androidTest/java/com/elorri/android/tests/LocalServiceTest)
	taken from [GoogleSamples] (https://github.com/googlesamples/android-testing/tree/master/integration/ServiceTestRuleSample/app)
[test parcelable write] (https://github.com/Elorri/Tests/tree/master/tests11/src/androidTest/java/com/elorri/android/tests/LogHistoryAndroidUnitTest)
	taken from [GoogleSamples] (https://github.com/googlesamples/android-testing/tree/master/unit/BasicUnitAndroidTest)				
### UI Instrumented integrated test/UI Connected integrated test
[test an Activity] (https://github.com/Elorri/Tests/tree/master/tests2/src/androidTest/java/com/elorri/android/tests/CalculatorActivityTest)
	taken from [GoogleSamples] (https://github.com/googlesamples/android-testing/tree/master/runner/AndroidJunitRunnerSample/app)
[test an EditText hint] (https://github.com/Elorri/Tests/tree/master/tests2/src/androidTest/java/com/elorri/android/tests/HintMatcher)
	taken from [GoogleSamples] (https://github.com/googlesamples/android-testing/tree/master/runner/AndroidJunitRunnerSample/app)
[test an Activity EditText] (https://github.com/Elorri/Tests/tree/master/tests3/src/androidTest/java/com/elorri/android/tests/ChangeTextBehaviorTest)
	taken from [GoogleSamples] (https://github.com/googlesamples/android-testing/tree/master/ui/espresso/BasicSample)		
[test an EditText hint] (https://github.com/Elorri/Tests/tree/master/tests4/src/androidTest/java/com/elorri/android/tests/HintMatchers)
	taken from [GoogleSamples] (https://github.com/googlesamples/android-testing/tree/master/ui/espresso/CustomMatcherSample)	
[test an Activity EditText hint] (https://github.com/Elorri/Tests/tree/master/tests4/src/androidTest/java/com/elorri/android/tests/HintMatchersTest)
	taken from [GoogleSamples] (https://github.com/googlesamples/android-testing/tree/master/ui/espresso/CustomMatcherSample)
[test an ListView] (https://github.com/Elorri/Tests/tree/master/tests5/src/androidTest/java/com/elorri/android/tests/LongListActivityTest)
	taken from [GoogleSamples] (https://github.com/googlesamples/android-testing/blob/master/ui/espresso/DataAdapterSample)	
[test an implicit Intent using Espresso Intent(Camera take a picture)] (https://github.com/Elorri/Tests/tree/master/tests6/src/androidTest/java/com/elorri/android/tests/ImageViewerActivityTest)
	taken from [GoogleSamples] (https://github.com/googlesamples/android-testing/blob/master/ui/espresso/IntentsAdvancedSample)	
[test an ImageView (if it has a drawable applied to it)] (https://github.com/Elorri/Tests/tree/master/tests6/src/androidTest/java/com/elorri/android/tests/ImageViewHasDrawableMatcher)
	taken from [GoogleSamples] (https://github.com/googlesamples/android-testing/blob/master/ui/espresso/IntentsAdvancedSample)	
[test an implicit Intent using Espresso Intent(Dialer)] (https://github.com/Elorri/Tests/tree/master/tests7/src/androidTest/java/com/elorri/android/tests/DialerActivityTest)
	taken from [GoogleSamples] (https://github.com/googlesamples/android-testing/blob/master/ui/espresso/IntentsBasicSample)	
[test an AutocompleteTextView] (https://github.com/Elorri/Tests/tree/master/tests8/src/androidTest/java/com/elorri/android/tests/MultiWindowTest)
	taken from [GoogleSamples] (https://github.com/googlesamples/android-testing/blob/master/ui/espresso/MultiWindowSample)	
### UI Automator Instrumented test/UI Automator Connected test
[test launching an app, press home, change edittext string] (https://github.com/Elorri/Tests/tree/master/tests9/src/androidTest/java/com/elorri/android/tests/ChangeTextBehaviorTest)
	taken from [GoogleSamples] (https://github.com/googlesamples/android-testing/blob/master/ui/uiautomator/BasicSample/app)
	



### License
	
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


