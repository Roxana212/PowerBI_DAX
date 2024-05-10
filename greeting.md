Welcome Txt = 
VAR Hour = HOUR(NOW())
VAR Greetings = 
SWITCH(
    TRUE(), 
    Hour >= 0 && Hour < 5, "Good Night", 
    Hour >= 5 && Hour < 12, "Good Morning", 
    Hour >= 12 && Hour < 18, "Good Afternoon", 
    Hour >= 18 && Hour < 24, "Good Evening"
)
RETURN 
Greetings & " " & SELECTEDVALUE(dimUser[FirstName])

