local InterfaceManager = {}

InterfaceManager.Library = {}  -- สร้างตาราง Library หากยังไม่มี
InterfaceManager.Library.Themes = {}  -- สร้างตาราง Themes

-- ฟังก์ชันในการตั้งค่า Library
function InterfaceManager:SetLibrary(library)
    self.Library = library
    if not self.Library.Themes then
        self.Library.Themes = {}  -- ตรวจสอบว่า Library.Themes มีอยู่แล้วหรือยัง ถ้าไม่ให้สร้างใหม่
    end
end

-- ฟังก์ชันเพิ่มธีมใหม่
function InterfaceManager:AddCustomTheme(themeName, themeValues)
    -- ตรวจสอบว่า Library.Themes ถูกสร้างและเป็นตารางหรือไม่
    if type(self.Library.Themes) == "table" then
        self.Library.Themes[themeName] = themeValues  -- เพิ่มธีมใหม่ลงใน Library.Themes
    else
        warn("Library.Themes is not a valid table!")
    end
end

-- การใช้ฟังก์ชัน
InterfaceManager:SetLibrary({})  -- กำหนดให้ Library เป็นตารางใหม่
local customTheme = {
    BackgroundColor = Color3.fromRGB(30, 30, 30),
    TextColor = Color3.fromRGB(255, 255, 255)
}
InterfaceManager:AddCustomTheme("CustomDarkTheme", customTheme)

-- การตั้งค่าใช้ธีมที่เพิ่มมา
print(InterfaceManager.Library.Themes["CustomDarkTheme"].BackgroundColor)
