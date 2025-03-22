# Shub.io UI Library V2
This documentation is for RedZ UI V2 Credit To REDzHUB

## Booting the RedZ UI V2 UI Library

## مهم تقرا الكود كامل وتحطه في السكربت الخاص بك وعشان تعرف كل شي 

```lua
loadstring(game:HttpGet(("https://raw.githubusercontent.com/S2EXE/Shub-ui/refs/heads/main/Src")))()
```




## اصنع نافذة
```lua
MakeWindow({
  Hub = {
    Title = "اسم السكربت هنا",
    Animation = "مرحبا بكم"
  },
  Key = {
    KeySystem = false,
    Title = "Key System",
    Description = "",
    KeyLink = "",
    Keys = {"1234"},
    Notifi = {
      Notifications = true,
      CorrectKey = "Running the Script...",
      Incorrectkey = "The key is incorrect",
      CopyKeyLink = "Copied to Clipboard"
    }
  }
})

--[[
  Hub = {
    Title = "shub" -- <string> عنوان السكربت
    Animation = "مرحبا" -- <string> تقدر تحط اي شيء

  Key = {
    KeySystem = <bollean> Adds a key system
    Title = "Key System" <string> Add a title to your key system
    Description = "" <string> Adds a description to your key system
    KeyLink = "" <string> Add the Link where you get the HUB key
    Keys = {"1234"} <table> Add the Keys
    Notifi = {
      Notifications = true <boolean> Add notifications to the key system
      CorrectKey = "Running the Script..." <string> notification when key is correct
      Incorrectkey = "The key is incorrect" <string> notification when key is incorrect
      CopyKeyLink = "Copied to Clipboard" <string> notification when key link is copied
    }
  }
]]
```

## MiniMize Button
```lua
MinimizeButton({
  Image = "",
  Size = {40, 40},
  Color = Color3.fromRGB(10, 10, 10),
  Corner = true,
  Stroke = false,
  StrokeColor = Color3.fromRGB(255, 0, 0)
})

--[[
  Image = "" <string> ايدي الصورة لزماتعرف خش قناتي على اليوتيوب
  Size = {40, 40} <table> حجم الزر
  Color = Color3.fromRGB(10, 10, 10) <Color3>  لون الزر
  Corner = true -- <boolean> اضافة زوايا للزر
  Stroke = false <boolean> Add a UIStroke
  StrokeColor = Color3.fromRGB(255, 0, 0) <Color3> لون ال UIStroke
]]
```

## اصنع نافذه
```lua
local Main = MakeTab({Name = "نافذة الرئيسية"})
--[[ 
  Name = "نافذة الرئيسية" <string> اسم النافذة
]]

```

## اصنع اشعار
```lua
MakeNotifi({
  Title = "عنوان الشعار",
  Text = "وصف الشعار",
  Time = 5
})

--[[
  Title = "REDz HUB" <string> عنوان الشعار
  Text = "Notification Testing" <string> وصف الشعار
  Time = 5 <number> مدة الشعار
]]
```

## اضافة قسم
```lua
local section = AddSection(Main, {"Test"})
--[[ 
  {"Test"} <table> اسم القسم
]]

```

## اضافة قسم
```lua
SetSection(section, "HI")
```

## اصنع زر
```lua
AddButton(Main, {
  Name = "اسم الزر",
  Callback = function()
    
  end
})

--[[
  Name = "Button Testing" <string> اسم الزر
  Callback = function()
    -- اضافة وظيفة 
  end
]]
```

## زر التبديل
```lua
local Toggle = AddToggle(Main, {
  Name = "زر التبديل",
  Default = false,
  Callback = function(Value)
    
  end
})

--[[
  Name = "Toggle Test" <string> اسم الزر
  Default = false <boolean> 
  Callback = function(Value)
    -- function of your checkbox
  end
]]
```

## اضافة زر تبديل ل الجوال
```lua
local MobileToggle = AddMobileToggle({
  Name = "",
  Visible = false,
  Callback = function(Value)
    
  end
})

MobileToggle.Visible = (false/true)

--[[
  Name = "Toggle" <string> اسم الزر
  Visible = false <boolean>  جعله مختفي او لا
  Callback = function()
    -- check box function
  end
]]
```

## اضافة شريط تمرير
```lua
local Slider = AddSlider(Main, {
  Name = "Slider Test",
  MinValue = 10,
  MaxValue = 100,
  Default = 25,
  Increase = 1,
  Callback = function(Value)
    
  end
})

--[[
  Name = "Slider teste" <string> اسم الشريط
  MinValue = 10 <number> لالاقل قيمة
  MaxValue = 100 <number> الاعلى قيمة
  Default = 25 <number> الوسط
  Increase = 1 <number> القيمة التي تزداد وفقًا لموضع المؤشر
  Callback = function(Value)
    slider function
  end
]]
```

## إنشاء رابط مفتاح
```lua
AddKeybind(Main, {
  Name = "Keybind Test",
  KeyCode = "E",
  Default = false,
  Callback = function(Value)
    
  end
})

--[[
  Name = "Keybind teste" <string> اسم الرابط
  KeyCode = "E" <string> المفتاح
  Default = false <boolean> القيمة الافتراضية (ستعمل هذه كمربع اختيار)
  Callback = function(Value)
    -- keyboard shortcut function
  end
]]
```

## انشاء زر كتابي
```lua
AddTextBox(Main, {
  Name = "TextBox Test",
  Default = "",
  PlaceholderText = "hub",
  ClearText = true,
  Callback = function(Value)
    
  end
})

--[[
  Name = "TextBox Test" <string> اسم الزر
  Default = "" <string> خليها كذا
  PlaceholderText = "hub" <string> الشي الي بيظهر في الزر نفسه
  ClearText = true <boolean> 
  Callback = function(Value)
    -- text box function
  end
]]
```

## قائيمة صغيرة
```lua
local Dropdown = AddDropdown(Main, {
  Name = "Dropdown Test",
  Options = {"1", "2", "3"},
  Default = "2",
  Callback = function(Value)
    
  end
})

--[[
  Name = "Dropdown teste" <string> الاسم
  Options = {"1", "2", "3"} <table> اوبشنز
  Default = "2" <string> الختيار الظاهر قبل فتح القائمة
  Callback = function(Value)
    -- dropdown menu function
  end
]]
```

## انشاء محدد اللون
```lua
AddColorPicker(Main, {
  Name = "Color Picker Test",
  Default = Color3.fromRGB(255, 255, 0),
  Callback = function(Value)
    
  end
})

--[[
  Name = "Color picker teste" <string> مدري شسمه
  Default = Color3.fromRGB(255, 255, 0) <Color3> Sets the default color of the color sector
  Callback = function(Value)
    -- color sector function
  end
]]
```

## انشاء برغراف
```lua
local Paragraph = AddParagraph(Main, {"اسم البرقراف", "hello"})

--[[
  <string> Paragraph 
  <string> description of the Paragraph
]]
```
## بروغراف جديد
```lua
SetParagraph(Paragraph, {"Paragraph", ":>"})

--[[
  <string> new Paragraph Name
  <string> New Paragraph description
]]
```

## ليبل انشاء
```lua
local Label = AddTextLabel(Main, "زي البرغراف بس اصغر :)")

--[[
  <string> Text
]]
```

## ليبل جديد
```lua
SetLabel(Label, "New Text")

--[[
  <string> new Text
]]
```

## صورة
```lua
local Image = AddImageLabel(Main, {
  Name = "صورة جميلة",
  Image = "rbxassetid://"
})

--[[
  Name = "Cool Image" <string> اسم الصورة
  Image = "rbxassetid://" <string> ايدي
]]
```
## صورة جديدة
```lua
SetImage(Image, "rbxassetid://")

--[[
  <string> صورة جديدة
]]
```

## حذف النافذة
```lua
DestroyScript()
```
## متنوع

## ديسكور 
```lua
AddDiscord(Main, {
    DiscordLink = "",
    DiscordIcon = "rbxassetid://",
    DiscordTitle = "",
    })

--[[
AddDiscord(Main, {
    DiscordLink = "",<string> رابط الديسكورد او تيليجرام
    DiscordIcon = "rbxassetid://",<string> ايدي الصورة
    DiscordTitle = "",<string> وصف (اختياري)
    })
  --]]
```

## تحديث زر التبديل
```lua
UpdateToggle(Toggle, true)
```

## تحديث شريط التمرير
```lua
UpdateSlider(Slider, 25)

--[[
  <number> new slider value
]]
```

## تحديث القائمة المنسدلة
```lua
UpdateDropdown(Dropdown, {"", "", ""})

--[[
  {" ", "", ""} <table> اسماؤ الابشنز
]]
```
