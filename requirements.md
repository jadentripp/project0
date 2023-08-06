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

Given URL: [https://www.google.com/search?as_q=harvard&as_epq=html&as_oq=html%2C+css%2C+javascript&as_eq=bears&as_nlo=&as_nhi=&lr=&cr=&as_qdr=all&as_sitesearch=&as_occt=any&as_filetype=&tbs=](https://www.google.com/search?as_q=harvard&as_epq=html&as_oq=html%2C+css%2C+javascript&as_eq=bears&as_nlo=&as_nhi=&lr=&cr=&as_qdr=all&as_sitesearch=&as_occt=any&as_filetype=&tbs=)

### URL Components:

#### 1. **Protocol**:
- `https://` 
  - Denotes the protocol used, which is HTTPS (Hypertext Transfer Protocol Secure).

#### 2. **Domain**:
- `www.google.com`
  - The domain name of the website, in this case, Google's domain.

#### 3. **Path**:
- `/search`
  - Represents the path on the website being accessed. Here, it indicates you're using Google's search feature.

#### 4. **Query Parameters**:
These are the key-value pairs after the `?` and are separated by `&`.

---

### Emphasized Query Parameters:

1. **Find pages with… “all these words:”**
    - Parameter: `as_q`
    - Value: `harvard`
    - In the URL: `as_q=harvard`
    - This means you're searching for pages containing the word "harvard".

2. **Find pages with… “this exact word or phrase:”**
    - Parameter: `as_epq`
    - Value: `html`
    - In the URL: `as_epq=html`
    - This means you're searching for pages with the exact phrase "html".

3. **Find pages with… “any of these words:”**
    - Parameter: `as_oq`
    - Value: `html, css, javascript`
    - In the URL: `as_oq=html%2C+css%2C+javascript` (Note: `%2C` is a URL-encoded comma `,` and `+` represents a space.)
    - This means you're searching for pages with any of the words "html", "css", or "javascript".

4. **Find pages with… “none of these words:”**
    - Parameter: `as_eq`
    - Value: `bears`
    - In the URL: `as_eq=bears`
    - This means you're excluding pages containing the word "bears".

---

### Conclusion:

The provided URL is a Google search URL. It's configured to find pages with the word "harvard", the exact phrase "html", any of the words "html", "css", or "javascript", but none of the word "bears".