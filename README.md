<div dir="rtl">

![data-structures.png](https://miro.medium.com/v2/resize:fit:1200/1*KpDOKMFAgDWaGTQHL0r70g.png)

<h3>ساختمان داده (Data Structure) چیست؟</h3>

تا الان هممون حداقل یک مفهوم سطحی از data structure رو یاد گرفتیم.
توی ویکی پدیا و اکثر وب سایت ها همون توضیح کوتاه رو میده.

اما بیاید یکم عمیق تر شیم

دیتا (Data) چیه؟ 
خب Structure که مشخصه یک آرایش، ساختار، سازمان دهی کردن هستش.

برای درک دیتا بهتره کمی درباره ساز و کار کامپیوتر بدونیم:
قلب تپنده کامپیوتر CPU هستش
سی پی یو یک چیزی داره به اسم ALU کار اصلی ایشون در واقع انجام محاسبه ها و انجام عملیات های منطقی روی داده ها توی پردازنده اصلی یا همون CPU هستش.

داده ها از کجا میان ؟
داده ها از main memory یا همون رم سیستم میان.
تا اونجا که خودتون در جریانید کامپیوتر ها باینری هستن پس اینطور در نظر بگیرید ما کلی صفر و یک توی رم داریم.

نکته ای که باید توجه کنید اینه کامپیوتر ذاتا فقط عدد میفهمه

اگه شما با هر زبان برنامه نویسی کار کرده باشید یک چیزی وجود داره به اسم انواع داده (data types)

هر زبان برنامه نویسی یک سری انواع داده اصلی رو میده.

اولین نوع داده ای که میشه اشاره کرد Boolean هستش. اینطوریه که اگه صفر بود false هستش و اگه غیر صفر بود true مثلا یک باشه true هستش
کامپیوتر هم اینو خیلی راحت میفهمه، بیسیک ترین نوع داده هستش که با یه بیت هم میشه نمایشش داد

انواع اعداد رو داریم مثلا int، short, long

اعداد اعشاری رو داریم مثل float و double

خب تا اینجا هر نوع تایپی که اشاره کردیم عدد بود و همچنین کل چیزی که CPU میفهمه اعداد هستش

ولی خب سوال اینجاست. ما که فقط اعداد نداریم مثلا چیزی به اسم رشته (String) رو داریم. پس چطور باهاش کار می کنیم؟

رشته چطوری ساخته میشه؟
رشته به این شکل ساخته میشه که میایم بر اساس هر حرف عددی رو تعریف میکنیم. اگه یادتون باشه چیزی به اسم جدول ascii codes داریم که توی این جدول مشخص شده مثلا A میشه 65
پس چیزی که توی حافظه برای رشته نوشتیم در واقع عدد هستش

اگه همه چی عدد هستش. چجوری داده های پیچیده تر رو میسازیم؟

برای ساخت داده های پیچیده تر میتونیم از composition یعنی ترکیب کردن استفاده کنیم. 
یعنی میایم چند تا نوع داده رو با هم ترکیب میکنیم یک نوع داده پیچیده تر رو میسازیم.

فرض کنید میخوایم اطلاعات دانش آموز رو ذخیره کنیم. برای اینکار نیازه که ما چند توع دیتا تایپ رو با هم ترکیب کنیم تا بتونیم دانشجو رو بسازیم. مثلا دانشجو نام داره که String هستش،‌کد دانشجویی داره و اطلاعات دیگه. پس چیزی که ما میسازیم به این

</div>

```Java
            name: str
Student     code: int
            age: int
```

<div dir="rtl">
تشکیل می شود. توی اینجا ما به Student میگیم Struct که البته توی زمان C بیشتر می شنوید.

Aggregation:

یک روش دیگه هم برای مدریت و ساخت انواع جدید، aggregation (البته چند روش دیگه هم داریم) هست. توی Aggregation یک سری از آبجکت ها، اشیا رو کنار هم قرار میدیم تا یک چیز بزرگ تری رو بسازیم

مثلا تعدادی دانشجو رو کنار هم قرار میدیم و کلاس رو میسازیم

این آبجکت هایی که کنار هم دیگه میذاریم خودشون بصورت مستقل شخصیت دارن مثلا شما دانشجو رو فرض کنید. بصورت جداگانه هم شخصیت داره اما حالا ما چیزی داریم به اسم کلاس که داخل خودش دانشجو هایی
که توی کلاس هستن رو داره. به این کار که ما آبجکت های مستقل رو کنار هم میذاریم میگن تجمیع و یا Aggregation کردن.

حالا وقتی که میایم آبجکت ها رو کنار هم قرار میدیم به ساختار و آرایشی نیاز داریم که بتونیم این آبجکت ها رو کنار همدیگه قرار بدیم. اینجاست که ساختمان داده ها (Data structures) به دادمون میرسه🥰

در واقع اینجا نیاز اینکه ما باید ساختار داده ای و یا ساختار های داده داشته باشیم حس شد و داستان ما از اینجا شروع میشه.

<br>
<h3>انواع ساختمان داده</h3>
ما انواع مختلفی از ساختمان داده داریم که هر کدومشون در جای مناسب کاربرد دارن. در ادامه چند نوع ساختمان داده رو بررسی میکنیم و مثال از نحوه پیاده
کردنش توی پایتون براتون میزنم.
<br>
<h3>ساختمان داده آرایه(Array)</h3> 
پایه ای ترین نوع ساختمان داده هستش.
توی آرایه ما می تونیم set کنیم چیزی رو اضافه کنیم و یا get کنیم و آبجکتی رو بگیریم و تمام.

مثلا:
</div>

```Java
[1, 2, 5, 9]

set(1, 9) ---> [1, 9, 5, 9]

get(0) -----> 1
```

<div dir="rtl">
همچنین باید lenght آرایه رو موقع تعریف کردنش مشخص کنیم که چقدر طول داره.

آرایه ها خیلی کاربردی هستن ولی یک سری محدودیت ها و معایبی رو دارن. مثلا:

شما باید موقع تعریف کردنش مشخص کنید که چقدر طول داره.
اگه بخوایم یک عنصری رو توی index مشخص شده جا بدیم در واقع insert کنیم، قابلیتش رو نداره یا اگه بخوایم عنصری رو از index مشخص پاک کنیم بازم قابلیتش رو نداره.

برای حل این مشکلات ساختمان داده ای به اسم Array list و یا تو بعضی از زبان های برنامه نویسی بهش «وکتور» میگیم که توی پایتون بهش لیست میگیم.

<h3>ساختمان داده Array List</h3>
ساختمان داده Array list رو میتونیم با استفاده از Array پیاده کنیم.

یک Array list این ویژگی هارو باید داشته باشه:

بتونیم insert, remove, add, get_size رو انجام بدیم.

همونطور که اشاره کردیم آرایه در ابتدا اینکه چقدر طول داشته باشه رو از ما میگیره و قابل تغییر دادن هم که نیسن. پس احتمالا حدس زدید کاری که انجام میدیم اینه که
توی Array list اول از همه بیشتر از فضایی که نیازه رو در نظر میگیریم و خالی قرار میدیمش.
بعد کاری که میکنیم اینه وقتی چیزی add میشه ما میایم تو آخر آرایه اون رو اضافه میکنیم.

اینکه آخر آرایه بلاک چندم هستش رو با استفاده از size که مشخص کردیم میفهمیم. یعنی مثلا اگه یک لیست با سه عنصر بوجود آوردیم سایزش میشه سه و اگه چیزی رو add کنیم با توجه به اینکه
سایز ما سه بوده پس توی size + 1 ذخیرش میکنیم.
پس در کل نحوه ساخت یک آرایه لیست به این صورت است.
  
توی Array list ما یک سری مشکلات رو هم داریم. مثلا خیلی از وقتا یا O(n)
مواجه میشویم. برای مثال اگه size لیست ما به اندازه طولی که مشخص کرده بودیم رسید. اونوقت باید بیایم کل داده رو توی یک Array دیگه که طول بزرگ تری دارد کپی کنیم و یا زمانی که index صفر را remove میکنیم اتفاقی که می افتد این است تمامی عناصر یک index
عقب تر می روند که کار ساده ای نیست.

نحوه پیاده سازی یک Array List رو بصورت عملی انجام نمیدم. بنظرم توضیحات کافیه


<h3>صف (Queue)</h3>
وقتی حرف از صف زده میشه همیشه یاد صف نونوایی بیوفتید. هر کی اول وارد شده، اولم نون میگیره. توی صف ما میگیم FIFO(First input first output)
کسی که اول وارد شده اول هم خارج میشه.
اما خب صف رو چجوری میتونیم پیادش کنیم؟

صف رو میتونیم با استفاده از Array list پیادش کنیم. در واقع میایم از دیزاین پترن Adapter استفاده میکنیم و لیست رو سبک و سنگینش میکنیم تا
برای ما کاربرد صف رو داشته باشه

صف یه سری متد ها رو باید داشته باشه. مثل:

متد add, take, head, tail, size

متد add برای اضافه کردن به صف، متد take برای گرفتن اولین نفر و برگردوندنش و حذف کردنش از صف، 
متد head برای نشون دادن اولین نفری که توی صفحه و متد tail برای نشون دادن آخرین نفری که توی صف قرار داره و متد size برای دیدن اینکه
صف ما حالا چند نفر منتظرن داخلش.

نحوه پیاده کردن یک صف ساده توی پایتون با استفاده از لیست:
</div>

```Python
from typing import Any


class Queue(list):

    def add(self, value) -> None:
        self.append(value)

    def size(self) -> int:
        return len(self)

    def get_first(self) -> Any:
        try:
            return self[0]
        except IndexError:
            raise IndexError('Queue index out of range')

    def get_last(self) -> Any:
        try:
            return self[-1]
        except IndexError:
            raise IndexError('Queue index out of range')

    def take(self) -> Any:
        first = self.get_first()
        del self[0]
        return first

    def head(self) -> Any:
        return self.get_first()

    def tail(self) -> Any:
        return self.get_last()
```

<div dir="rtl">
<h3>پشته (Stack)</h3>
پشته دقیقا برعکس صف هستش و یه جورایی ناعادلانست 😂

در پشته (Stack)
هر کی اول بره، اول بیرون نمیاد. هر کی آخر بره اول بیرون میاد. توی پشته میگیم LILO(Last input last output)
یعنی همون هر کی آخر بره اول بیرون میاد

یک سطح رو در نظر بگیرید که داخلش دیتا رو میریزیم. خب مشخصا وقتی میخوایم چیزی برداریم اونی که آخر وارد شده در دسترس هستش.

برای پیاده سازی پشته مثل صف دوباره از لیست استفاده می کنیم. متد هایی که نیازه داشته باشیم اینا هستن:

add, size, pop, top

متد add برای اضافه کردن توی پشته، متد size برای دیدن سایز، متد pop برای گرفتن و حذف کردن آخرین استفاده میشه و متد top برای دیدن 
اونی که آخر از همه وارد شد.

پیاده کردن یک پشته ساده با استفاده از لیست توی پایتون:

</div>


```Python
from typing import Any


class Stack(list):

    def add(self, value) -> None:
        self.append(value)

    def size(self) -> int:
        return len(self)

    def get_last(self) -> Any:
        try:
            return self[-1]
        except IndexError:
            raise IndexError('Stack index out of range')

    def pop(self) -> Any:
        try:
            return super().pop()
        except IndexError:
            raise IndexError('pop from empty stack.')

    def top(self) -> Any:
        return self.get_last()
```
