##FontLoader


An easy to use Roboto font loader for Android. Easily apply typefaces to TextView or its subclasses, or just easily load a typeface into memory.

There is also a ````Span```` for creating spannable strings with this typeface loader system called ````TypefaceSpan````

---
### Types

````Types```` are string constants used to identify which Roboto typeface you are trying to load and are formated to be as intuitive and easy as possible. Here are all the ````Types```` available to you in the ````Types.java```` class:

	public class Types {

	    /**
	     * Roboto Types
	     */
	
	    public static final String ROBOTO_BLACK = "roboto-black";
	    public static final String ROBOTO_BLACK_ITALIC = "roboto-black-italic";
	    public static final String ROBOTO_BOLD = "roboto-bold";
	    public static final String ROBOTO_BOLD_ITALIC = "roboto-bold-italic";
	    public static final String ROBOTO_ITALIC = "roboto-italic";
	    public static final String ROBOTO_LIGHT = "roboto-light";
	    public static final String ROBOTO_LIGHT_ITALIC = "roboto-light-italic";
	    public static final String ROBOTO_MEDIUM = "roboto-medium";
	    public static final String ROBOTO_MEDIUM_ITALIC = "roboto-medium-italic";
	    public static final String ROBOTO_REGULAR = "roboto-regular";
	    public static final String ROBOTO_THIN = "roboto-thin";
	    public static final String ROBOTO_THIN_ITALIC = "roboto-thin-italic";
	
	    /**
	     * Roboto Condensed Types
	     */
	
	    public static final String CONDENSED_BOLD = "condensed-bold";
	    public static final String CONDENSED_BOLD_ITALIC = "condensed-bold-italic";
	    public static final String CONDENSED_ITALIC = "condensed-italic";
	    public static final String CONDENSED_LIGHT = "condensed-light";
	    public static final String CONDENSED_LIGHT_ITALIC = "condensed-light-italic";
	    public static final String CONDENSED_REGULAR = "condensed-regular";
	
	}

---
### Usage

Here are some example usages of the library.

	TextView title = (TextView) findViewById(R.id.title);
	
	FontLoader.applyTypeface(title, "roboto-bold");
	
	// Or...
	
	FontLoader.applyTypeface(title, Types.ROBOTO_BOLD);
	

Or by applying to a view in layout without having to 'find' it

	View parent = LayoutInflater.from(this).inflate(R.layout.something);
	
	FontLoader.applyTypeface(parent, R.id.subtitle, "roboto-light");
	
	// Or
	
	FontLoader.applyTypeface(parent, R.id.subtitle, Types.ROBOTO_LIGHT);
	
	// Or
	
	FontLoader.applyTypeface(this, R.id.subtitle, Types.ROBOTO_LIGHT);
	
Or just get the Typeface directly

	Typeface robotoRegular = FontLoader.getTypeface(this, Types.ROBOTO_REGULAR);
	


---
### Author

* **Drew Heavner** (r0adkll) @ [52inc](http://www.52inc.co)



---
### License

	Copyright (c) 2014 52inc
  
    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at
  
       http://www.apache.org/licenses/LICENSE-2.0
  
	Unless required by applicable law or agreed to in writing, software
	distributed under the License is distributed on an "AS IS" BASIS,
	WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
	See the License for the specific language governing permissions and
	limitations under the License.
   