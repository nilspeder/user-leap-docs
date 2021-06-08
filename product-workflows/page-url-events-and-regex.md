# No Code - Page URL Events

## **UserLeap Events**

Events are defined as the actions or behaviors users take on a given page or application. UserLeap relies on events to deliver highly customizable microsurveys that are targeted on an event or multiple groups of events. 

There are two main types of events that you can add to UserLeap: 

1. No Code
2. Code

## **No Code - Page URL Events**

Like all events, you can find/add Page URL Events from the [**Events Page**](../product-navigation/the-events-page.md) in UserLeap. Once there, click on the "Add" in the top right and then select "Page URL Event" \(see below\)  


![](https://p35.tr2.n0.cdn.getcloudapp.com/items/Jru4zOkz/fba5191a-d419-494d-af4d-df03eb362011.jpg?v=816758657ac6def5440135a7a6f45d03)

### Creating a Page URL Event

In order to save a Page URL Event to UserLeap you'll need the following:

* Event URL Pattern: The URL of the page that you would like to add 
* Event Name: The name given to this event \(_note: names MUST be unique\)_ 
* Event Description \(_Optional_ \): A quick summary

{% embed url="https://www.loom.com/share/ec40234f0c8d4774a5054bc0a7eca9a8" %}

### \*\*\*\*

### **Pattern Matching & Regex**

Beyond simple matching, UserLeap ALSO supports **regex** \(also known as Regular Expression\). In short, regex allows for matching or partial matching on more complex patterns. 

It is important to note that by default UserLeap relies on `partial match` as opposed to a `full match`.

**Example**_**:**_ 

Let's say I add a regex pattern like this: `app.userleap.com`

I run the risk of allowing any **partial matches.** The above pattern will evaluate to `true` for `app.userleap.com/overview` AND `app.userleap.com/events`. **Partial Matches** can lead to either of the following:

* Surveys appearing on pages they are not supposed to
* Other regex patterns not firing due to overlap of events 

{% hint style="danger" %}
All URL patterns must be **&lt;= 250 characters** 
{% endhint %}

How do we avoid this? We use Tokens that allow us to get more granular when defining regex patterns. 

## **Popular Tokens**

While we will be unable to cover all tokens \(you can find them via Google\), this article will make sure to cover some of the most important ones you will find yourself needing in UserLeap. 

### \*

**Definition:** The `*` operator will match ANY all following characters

**Pattern**: `app.userleap.com/*`

| Example | Match |
| :--- | :--- |
| **`app.userleap.com/events`** | **True** |
| **`app.userleap.com/`** | **True** |
| `app.userleap.com/login` | True |

### $

**Definition**: The `$` operator signifies the end of the string. 

**Pattern**: `app.userleap.com/events$`

| Example | Match |
| :--- | :--- |
| **`app.userleap.com/events`** | **True** |
| `app.userleap.com/` | False |

### \| 

**Definition**: The `|` operator lets you and "OR" objection handling 

**Pattern**: `app.userleap.com/(events|overview)` 

| Example | Match |
| :--- | :--- |
| **`app.userleap.com/events`** | **True** |
| **`app.userleap.com/overview`** | **True** |
| `app.userleap.com/collections` | False |

### **?!**

**Definition**: The `?!` operator allows for a negative look-ahead 

**Pattern:** `app.userleap.com/(?!login|signup)`

_i.e. if the pattern matches the characters following `?!` then evaluate to False_

| **Example** | Match |
| :--- | :--- |
| **`app.userleap.com/login`** | **False** |
| **`app.userleap.com/signup`** | **False** |
| `app.userleap.com/overview` | True |

### **A-Z AND a-z**

**Definition:** The `a-z` operator matches any character a-z, the `A-Z` operator matches any character from A-Z \(capitalized\)

**Pattern**: `app.userleap.com/[a-z]`

| Example | Match |
| :--- | :--- |
| **`app.userleap.com/overiview`** | **True** |
| **`app.userleap.com/events`** | **True** |
| `app.userleap.com/Events` | False |

## How to Test Your Regex

You can test whether or not your regex function works as intended by copy and pasting the snippet below into your web developer console:

The snippet below will either evaluate to **True** or **False**

```text
new RegExp("sample.com").test(window.location.href)
```

{% hint style="info" %}
Replace **sample.com** with your own regex pattern
{% endhint %}

{% embed url="https://www.loom.com/share/5d579c2236d849d9bdf21003274d5ab8" %}



