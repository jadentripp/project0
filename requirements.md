**Website Specifications**

1. **Page requirements**
   - Minimum of three pages: Google Search (`index.html`), Google Image Search, and Google Advanced Search.
   - Navigation links should be present in the upper-right corner of each page.

2. **Google Search page**
   - Centralized search bar with rounded corners.
   - Centralized search button below the search bar.
   - A user should be able to enter a query and get Google search results.

3. **Google Image Search page**
   - A user should be able to enter a query and get Google Image search results.

4. **Google Advanced Search page**
   - Users should be able to input the following fields:
     - "all these words:"
     - "this exact word or phrase:"
     - "any of these words:"
     - "none of these words:"
   - Fields should be stacked vertically and left-aligned.
   - The "Advanced Search" button should be blue with white text.
   - Clicking the button should display search results for the query.

5. **Additional features**
   - An "I'm Feeling Lucky" button on the Google Search page.
     - Clicking this button should display the first Google search result for the query.

6. **CSS**
   - The design should resemble Google's aesthetics.

**Hints**
- Experiment with Google searches to find the correct parameter names.
- Use the "Network" inspector to view request details.
- <input> elements can have name and value attributes that become GET parameters when a form is submitted.
- Use a "hidden" input field to include an input field that users can't see or modify.

**URL Breakdown: Regular Search for "Harvard"**

The provided GET URL: [https://www.google.com/search?q=Harvard&newwindow=1&sxsrf=AB5stBhq3HDPfQVksBM9MvMc29BtgkUv8g:1691187789098&ei=TXrNZLjHBZXIkPIP6dCqqA0&ved=0ahUKEwj4oau7hcSAAxUVJEQIHWmoCtUQ4dUDCBE&uact=5&oq=Harvard&gs_lp=Egxnd3Mtd2l6LXNlcnAiB0hhcnZhcmQyBBAAGEcyBBAAGEcyBBAAGEcyBBAAGEcyBBAAGEcyBBAAGEcyBBAAGEcyBBAAGEdItgFQAFgAcAB4ApABAJgBAKABAKoBALgBA8gBAOIDBBgAIEGIBgGQBgg&sclient=gws-wiz-serp](https://www.google.com/search?q=Harvard&newwindow=1&sxsrf=AB5stBhq3HDPfQVksBM9MvMc29BtgkUv8g:1691187789098&ei=TXrNZLjHBZXIkPIP6dCqqA0&ved=0ahUKEwj4oau7hcSAAxUVJEQIHWmoCtUQ4dUDCBE&uact=5&oq=Harvard&gs_lp=Egxnd3Mtd2l6LXNlcnAiB0hhcnZhcmQyBBAAGEcyBBAAGEcyBBAAGEcyBBAAGEcyBBAAGEcyBBAAGEcyBBAAGEcyBBAAGEdItgFQAFgAcAB4ApABAJgBAKABAKoBALgBA8gBAOIDBBgAIEGIBgGQBgg&sclient=gws-wiz-serp) can be broken down into several components(important query params only):

- `https://www.google.com/search`: This is the base URL, which points to Google's search engine. (Needed for any search type)
- `q=Harvard`: A query parameter where `q` stands for 'query'. The value `Harvard` is what is being searched for. (Needed for any search type)
- `newwindow=1`: A query parameter that instructs the browser to open the search results in a new window. (This could be a toggle)

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <title>Search</title>
        <link rel="stylesheet" href="styles.css">
    </head>
    <body>
         <!-- The action attribute on the form told the browser that when the form is submitted, the data should be sent to https://www.google.com/search. -->
        <form action="https://www.google.com/search">
            <input type="text" name="q">
            <!-- And by adding an input field to the form whose name attribute was q, whatever the user types into that input field is included as a GET parameter in the URL. -->
            <input type="submit" value="Google Search">
        </form>
        <!-- This produced https://www.google.com/search?q=hello+world with the query 'hello world'-->
        <a href="indexImage.html" class="upper-right">Image Search</a>
    </body>
</html>
```

**URL Breakdown: Image Search for "Harvard"**

Given URL: [https://www.google.com/search?q=harvard&newwindow=1&hl=en&tbm=isch&sxsrf=AB5stBi-Mzmmj_qXyePskktkjscMfhMEfw%3A1691189863094&source=hp&biw=1510&bih=1030&ei=Z4LNZP2-A6XzkPIP5pKNuAg&iflsig=AD69kcEAAAAAZM2Qd5nUUS6wj3Tq_eRwBZJHVCp9t9rD&ved=0ahUKEwi9jqSYjcSAAxWlOUQIHWZJA4cQ4dUDCAc&uact=5&oq=harvard&gs_lp=EgNpbWciB2hhcnZhcmQyCBAAGIAEGLEDMggQABiABBixAzIIEAAYgAQYsQMyCBAAGIAEGLEDMggQABiABBixAzIIEAAYgAQYsQMyBRAAGIAEMggQABiABBixAzIIEAAYgAQYsQMyCBAAGIAEGLEDSPUNUABYzwlwAHgAkAEAmAFHoAGGA6oBATe4AQPIAQD4AQGKAgtnd3Mtd2l6LWltZ8ICBBAjGCfCAgsQABiABBixAxiDAcICCBAAGLEDGIMB&sclient=img](https://www.google.com/search?q=harvard&newwindow=1&hl=en&tbm=isch&sxsrf=AB5stBi-Mzmmj_qXyePskktkjscMfhMEfw%3A1691189863094&source=hp&biw=1510&bih=1030&ei=Z4LNZP2-A6XzkPIP5pKNuAg&iflsig=AD69kcEAAAAAZM2Qd5nUUS6wj3Tq_eRwBZJHVCp9t9rD&ved=0ahUKEwi9jqSYjcSAAxWlOUQIHWZJA4cQ4dUDCAc&uact=5&oq=harvard&gs_lp=EgNpbWciB2hhcnZhcmQyCBAAGIAEGLEDMggQABiABBixAzIIEAAYgAQYsQMyCBAAGIAEGLEDMggQABiABBixAzIIEAAYgAQYsQMyBRAAGIAEMggQABiABBixAzIIEAAYgAQYsQMyCBAAGIAEGLEDSPUNUABYzwlwAHgAkAEAmAFHoAGGA6oBATe4AQPIAQD4AQGKAgtnd3Mtd2l6LWltZ8ICBBAjGCfCAgsQABiABBixAxiDAcICCBAAGLEDGIMB&sclient=img)

- `https://www.google.com/search`: Base URL for Google's search engine. (Needed for any search type)
- `q=harvard`: Query parameter where `q` stands for 'query'. The value `harvard` is the search term. (Needed for any search type)
- `newwindow=1`: Query parameter that instructs the browser to open the search results in a new window. (This could be a toggle)
- `tbm=isch`: `tbm` stands for 'to be matched'. The `isch` value is short for 'image search'. (Needed for image search) (This could be a toggle)

## Shortened URL(Only what is needed):
`https://www.google.com/search?q=harvard&newwindow=1&tbm=isch`

### Possible HTML
```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <title>Search</title>
        <link rel="stylesheet" href="styles.css">
    </head>
    <body>
         <!-- The action attribute on the form told the browser that when the form is submitted, the data should be sent to https://www.google.com/search. -->
        <form action="https://www.google.com/search">
            <input type="text" name="q">
            <label><input type="checkbox" name="tbm" value="isch" /> Image</label>
            <!-- And by adding an input field to the form whose name attribute was q, whatever the user types into that input field is included as a GET parameter in the URL. -->
            <input type="submit" value="Google Search">
        </form>
        <a href="index.html" class="upper-right">Regular Search</a>
        <!-- This produced https://www.google.com/search?q=hello+world with the query 'hello world'-->
    </body>
</html>
```

**URL Breakdown**

Given URL: [https://www.google.com/search?q=harvard&newwindow=1&hl=en&biw=1510&bih=1030&sxsrf=AB5stBhvRfJe0rGLyxmwf6lp5TRGjoBNaw%3A1691190007821&source=lnt&tbs=cdr%3A1%2Ccd_min%3A8%2F4%2F2023%2Ccd_max%3A8%2F1%2F2023&tbm=](https://www.google.com/search?q=harvard&newwindow=1&hl=en&biw=1510&bih=1030&sxsrf=AB5stBhvRfJe0rGLyxmwf6lp5TRGjoBNaw%3A1691190007821&source=lnt&tbs=cdr%3A1%2Ccd_min%3A8%2F4%2F2023%2Ccd_max%3A8%2F1%2F2023&tbm=)

- `https://www.google.com/search`: Base URL for Google's search engine.
- `q=harvard`: Query parameter where `q` stands for 'query'. The value `harvard` is the search term.
- `newwindow=1`: Query parameter that instructs the browser to open the search results in a new window.
- `hl=en`: The `hl` parameter specifies the interface language. Here, `en` stands for English.
- `biw=1510` and `bih=1030`: These parameters indicate the browser's viewport size. `biw` stands for 'browser inner width' and `bih` for 'browser inner height'.
- `sxsrf=AB5stBhvRfJe0rGLyxmwf6lp5TRGjoBNaw%3A1691190007821`: A security-related parameter, likely a token to prevent cross-site request forgery.
- `source=lnt`: The `source` parameter refers to the origin of the search. Here, `lnt` likely stands for 'tools' as this search uses Google's search tools.
- `tbs=cdr%3A1%2Ccd_min%3A8%2F4%2F2023%2Ccd_max%3A8%2F1%2F2023`: `tbs` stands for 'to be specified'. This parameter is used to apply filters to the search. Here, it is specifying a custom date range (cdr). `cd_min` and `cd_max` are specifying the start and end of the date range.
- `tbm=`: `tbm` stands for 'to be matched'. Here, no value is given, indicating a standard web search is to be performed.

**Note**: Google uses many encoded or proprietary parameters for its own tracking and customization purposes, so exact definitions for some parameters may not be publicly documented.

- `tbs=cdr%3A1%2Ccd_min%3A8%2F4%2F2023%2Ccd_max%3A8%2F1%2F2023`

This parameter is defining a custom date range for the Google search. `tbs` stands for 'to be specified', and it indicates that additional parameters are being specified.

The `%3A` and `%2C` you see in the URL are URL encoded characters representing `:` and `,` respectively. URL encoding is used to replace unsafe ASCII characters with a "%" followed by two hexadecimal digits. 

The `cdr:1` value means that a custom date range is being used (with `cdr` standing for 'custom date range'). The `1` value is enabling this feature.

The `cd_min:8/4/2023` and `cd_max:8/1/2023` values are specifying the start and end of the date range. `cd_min` is the minimum (or start) date and `cd_max` is the maximum (or end) date. The dates are in the format month/day/year. 

Thus, the search is applying a filter to only return results from between August 1, 2023, and August 4, 2023. 

Note that the start date is later than the end date in this particular example, which seems unusual. The user might have intended to swap these dates.