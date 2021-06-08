# Survey Filters & Triggers

## **Survey Triggers**

What is a Survey Trigger?

**Trigger**: Triggers are also known as events, and are required to launch an **in product** microsurvey. Simply put, a trigger is an action that takes place that causes your microsurvey to appear

* Advanced: In the "Advanced" dropdown for triggers you can set a time delay \(web only\). This time delay is the number of seconds to wait after the trigger to display a microsurvey

![](../.gitbook/assets/image%20%2852%29.png)

### **Multiple Triggers**

UserLeap supports up to 5 **unique triggers** per **in product** microsurvey. To add additional triggers, click "Add Another Trigger"

![](../.gitbook/assets/image%20%2815%29.png)

## **Survey Filters**

What is a Survey Filter?

**Filter**: Filters are useful when you want to segment the audience that should qualify for a survey. We’ll sometimes reference these as “survey filters.” 

* Advanced: in the “Advanced” dropdown for filters, you have the option to add minimum page views & session parameters. 
* Sessions in UserLeap are measured as 12-hour windows in which has 1+ event tracked in UserLeap
* Page views are only applicable to web surveys \(will not be displayed for email, mobile, link-based surveys\)

![](https://p35.tr2.n0.cdn.getcloudapp.com/items/E0uYKBKq/dfd76105-9058-49f1-8263-e56da8c4cd62.png?v=32ea0bdd14a12c27003e1524c51f6547)

_Survey filters can be either events and/or attributes_

### **Events as Filters** 

Events are defined as the actions or behaviors users take on a given page or application. UserLeap relies on events to deliver highly customizable microsurveys that are targeted on an event or multiple groups of events. 

#### Included Event Filters

![](https://p35.tr2.n0.cdn.getcloudapp.com/items/p9ub5O4Z/241670d7-af4d-441b-965c-e4890c440010.jpg?v=feeb2abd9ad56beae48762afcd91f031)

**Filter**: Is Set

**Value**: `Yes` or `No` 

**Use**: The `Is Set` operator checks whether or not there is a value stored for the intended event



**Filter**: Occurrences

**Value**: `Is greater than`, `Is less than` , `is greater than or equal to` , `is less than or equal to` , `is equal to` 

**Use**: The `Occurrences` operator compares the total number of times an event is triggered to the specified value provided by the user



**Filter**: First Occurred

**Value**: `Is greater than`, `Is less than` , `is greater than or equal to` , `is less than or equal to` , `is equal to` 

**Use**: The `First Occurred` operator compares the first recorded event trigger and compares to the value specified by the user



**Filter**: Last Occurred

**Value**: `Is greater than`, `Is less than` , `is greater than or equal to` , `is less than or equal to` , `is equal to` 

**Use**: The `Last Occurred` operator compares the last recorded event trigger and compares to the value specified by the user

### **Attributes as Filters** 

Like events, attributes are just another way to enhance your microsurvey targeting functionality. While events are triggered behaviors that occur on the client-side, attributes can be thought of as groups or segmentations that are assigned based on that behavior.

#### Included Attribute Filters

![](https://p35.tr2.n0.cdn.getcloudapp.com/items/RBuYXkPn/8aaf3ac3-ff8e-4061-a78c-db04ceea2532.jpg?v=63a79aa614b5838c90fffdf453c937ec)

**Filters**: `is equal to`, `is not equal to` , `is set` , `is greater than` , `is greater than or equal to` , `is less than` ,  `is less than or equal to`

_Note: Attribute values are set on the client side, for more information on setting attributes please read through_ [_**UserLeap Installation & Setup**_](../installation/)_\*\*\*\*_

_Note: When adding attributes to use as filters, we limit the total number of **distinct key value pairs to be &lt;= to 100**. So for example, if you are trying to send an attribute that aims to compare `orderCartValue` it is best to convert and send as quantifiable buckets/ranges_

### AND/ORs

AND/ORs allow for increased functionality when targeting user cohorts, conditions with AND must satisfy all criteria, whereas conditions with OR only need to satisfy **one**   

![](https://p35.tr2.n0.cdn.getcloudapp.com/items/yAuDbrOv/934e8ef4-eb7b-4ab7-b03e-10ce219093ad.gif?v=ec370f8dceedd1072f67dcfc33bfd1c2)

### Logic Groups

Logic groups allow you to create more complex groupings of ANDs/ORs. For a survey to be delivered it must pass at least **one** of the logic groups

![](https://p35.tr2.n0.cdn.getcloudapp.com/items/eDujBym9/afaafec7-7795-4557-ac04-bcca1046c206.gif?v=346e72b0d2b48846869ff56bc5310cbc)

#### **Deleting Logic Groups/Filters**

To remove a logic group or a filter, click into the ellipsis dropdown and select **remove**

![](https://p35.tr2.n0.cdn.getcloudapp.com/items/yAuDbrpN/84ccb785-1e09-48e9-a802-2c22b1dfd8e9.gif?v=843f167eec5f22f139678bd01b775b84)

#### Insert New Below

Using **insert new below** will add another survey filter, if you do so in a logic grouping it will add an additional condition within the same logic group

![](https://p35.tr2.n0.cdn.getcloudapp.com/items/kpuKbn95/df780bcd-37de-410c-b7cd-db392bd863c8.gif?v=e6a2e60c6b338ac5ac42e51c6e1f6059)



