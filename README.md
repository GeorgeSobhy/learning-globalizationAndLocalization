# learning-globalizationAndLocalization
Learn how to best approach globalization and localization in .NET.

### Resources that I studied:<br>
- [Globalization and Internationalization in .NET - Pluralsight](https://app.pluralsight.com/library/courses/dot-net-6-globalization-internationalization/table-of-contents)
- [Globalization and Internationalization in ASP.NET Core - Pluralsight](https://app.pluralsight.com/library/courses/asp-dot-net-core-6-globalization-internationalization/table-of-contents)


  
# Globalization and Internationalization in .NET:
## Module 1:
*Globalization*: Make it possible to your application to support multiple languages and cultures. (application configuration) <br>
*Localization* : Customize and translate your files and text for specific Culture. (resx files and content)
Culture = Language + region?  and any other properties that rely on it like *Number Format*<br>


Library: `System.Globalization`

##### Notes:
- .NET core support Cultural configuration per thread.
- Use CultureInfo.InVariantCulture to parse or serilize data.

## Module 2:
![image](https://github.com/user-attachments/assets/376eb9ee-e037-4b38-99ea-8cc6b312db37)

##### Notes:
- You can use *Numberstyles* for parsing numbers (ex numbers with currency [$100 || 100 kr])
- You can use *RegionInfo* to get data like distance or units
  
## Module 3:


