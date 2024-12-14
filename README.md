# learning-globalizationAndLocalization
Learn how to best approach globalization and localization in .NET.

### Resources that I studied:<br>
- [Globalization and Internationalization in .NET - Pluralsight](https://app.pluralsight.com/library/courses/dot-net-6-globalization-internationalization/table-of-contents)
- [Globalization and Internationalization in ASP.NET Core - Pluralsight](https://app.pluralsight.com/library/courses/asp-dot-net-core-6-globalization-internationalization/table-of-contents)
- [Globalization and Localization (Multi-Language) In .Net 5 (Core) -Youtube](https://www.youtube.com/watch?v=PyCGEO4b6F0&list=PL62tSREI9C-cJtB90kxb76SDCpXKuOfUH)

  
# Globalization and Internationalization in .NET:
## Module 1 - Introducing Globalization and Internationalization:
*Globalization*: Make it possible to your application to support multiple languages and cultures. (application configuration) <br>
*Localization* : Customize and translate your files and text for specific Culture. (resx files and content)<br>
Culture = Language + region?  and any other properties that rely on it like *Number Format*<br>


Library: `System.Globalization`

##### Notes:
- .NET core support Cultural configuration per thread.
- Use CultureInfo.InVariantCulture to parse or serilize data.

## Module 2 - Working with Numbers:
![image](https://github.com/user-attachments/assets/376eb9ee-e037-4b38-99ea-8cc6b312db37)

##### Notes:
- You can use *Numberstyles* for parsing numbers (ex numbers with currency [$100 || 100 kr])
- You can use *RegionInfo* to get data like distance or units
  
## Module 3 - Working with Dates:
When to use Datetime ONLY without time zone info(DateTimeOffset):
![image](https://github.com/user-attachments/assets/8d7e7406-a4b2-448a-8547-3086aebffa88)

![image](https://github.com/user-attachments/assets/03de1456-87ba-48ab-afee-c4035ddf0340)
![image](https://github.com/user-attachments/assets/54211364-c0ce-4c03-8b34-2c96d6965a25)

For custom format use `DateTimeOffset.Parse` and `DateTimeOffset.TryParse`.
Unix `Timestamp` : Number of seconds that have been since 1970-01-01-00-00-00.

##### Notes:
- It is better to store data on UTC time zone at the system and customize it for your system.
- You could use IFormatProvidor at `DateTimeOffset.Parse(dateText,"MMMM",*IFormatProvidoer*)` to print the month based on a specific culture.

## Module 3 - Working with Strings
`String.Equal()` depends on binaries of the words.
`String.Compare()` depends on system *culture*.
`Array.Sort()` uses compare method, So culture matters.

![image](https://github.com/user-attachments/assets/e95dc93e-d36f-4d56-a65f-a3a9b9a637a9)

##### Notes:
- Don't use `InvariantCulture` when you compare two strings.
- You could use *Ordinal* comparing or *InvariantCulture* to satisfy security considerations.

## Module 4 - Globalization and Internationalization in ASP.NET Core
 ![image](https://github.com/user-attachments/assets/0d00875d-7a57-4f45-a4b9-1e1cf2b26aa6)
watch the module videos :)


# Globalization and Internationalization in ASP.NET Core:
## Module 2 - Working with Cultures:
The order that application uses to get culture:
![image](https://github.com/user-attachments/assets/b79d5fe1-2458-4a93-be63-3556edbc8d44)

How to create custom Culture provider:
![image](https://github.com/user-attachments/assets/afb687d7-9f21-4a28-905d-d563248be7df)
check [Microsoft Documentation](https://learn.microsoft.com/en-us/aspnet/core/fundamentals/localization/select-language-culture?view=aspnetcore-9.0)

## Module 3 - Using Resource Files:
![image](https://github.com/user-attachments/assets/34740cc2-4b9c-4196-8ea2-9f7a6a8ee328)

## Module 4 - Working with String Localizers:
![image](https://github.com/user-attachments/assets/2764c5e5-4d61-4c39-904f-11c2ab6ba68e)

using *Localizer* with parameters
![image](https://github.com/user-attachments/assets/6e5be575-7a7b-4678-a935-b0643ec0b649)

Implementing custom Localizer:
![image](https://github.com/user-attachments/assets/f0f1e51c-e208-4a17-b724-105e40966ed6)
Example:
![image](https://github.com/user-attachments/assets/2be30faf-5416-4b3a-b69b-ba127677c532)

To localize data annotation attributes which has error message 
![image](https://github.com/user-attachments/assets/92514e1c-a52e-4cb1-af53-179279bd2167)
![image](https://github.com/user-attachments/assets/5d24b916-3b95-43e8-9358-971ec0123f58)

To localize data annotation attributes with built in error messages
![image](https://github.com/user-attachments/assets/ac713418-3eef-47bf-ab11-8a6e27b1b2de)

To localize user defined data annotation attributes
watch 37th video ;)

Extra points:
- Use `IStringLocalizer` for general localization needs throughout your application.
- Use `IViewLocalizer` for localizing Razor views.
- Use `IHtmlLocalizer` when you need to include HTML content in localized strings.

Extra resources:
[ASP.NET 8 - Multilingual Application with Single Resx File](https://www.c-sharpcorner.com/article/asp-net-8-multilingual-application-with-single-resx-file/)
