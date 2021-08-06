1. ClickMe

on UptateScore
   if field "score" > 0
   then
      subtract 1 from field "score"
      save this stack
   else
      put "Game Over" into field "messagesField"
   end if
   if field "score" = 50
   then
      put "well done" into field "messagesField"
   end if
   
   if field "score" = 30
   then
      put "Good for you" into field "messagesField"
   end if
   if field "score" = 10
   then
      put "you're almost done" into field "messagesField"
   end if
end UptateScore

on changeMyLook
   if field "score" = 50
   then
      put image "blueEgg.png" of card "imageBank" into image "ClickMe"
   end if
   if field "score" = 10
   then
      put image "greenEgg.png" of card "imageBank" into image "ClickMe"
   end if
   if field "score" = 30
   then
      put image "purpleEgg.png" of card "imageBank" into image "ClickMe"
   end if
   if field "score" = 0
   then
      put image "chick.png" of card "imageBank" into image "ClickMe"
   end if
end changeMyLook

on ShrinkItDown
   set the locklocation of image "ClickMe" to false
   
   if field "score" = 60
   then
      set the width of image "ClickMe" to  240
      set the height of image "ClickMe" to  240
   end if
   
   if field "score" = 40
   then
      set the width of image "ClickMe" to  230
      set the height of image "ClickMe" to  230
   end if
   
   if field "score" = 20
   then
      set the width of image "ClickMe" to  220
      set the height of image "ClickMe" to  220
   end if
   
   
   if field "score" =750
   then
      set the width of image "ClickMe" to  280
      set the height of image "ClickMe" to  280
   end if
   
   
   if field "score" =500
   then
      set the width of image "ClickMe" to  270
      set the height of image "ClickMe" to  270
   end if
   
   
   if field "score" = 250
   then
      set the width of image "ClickMe" to  260
      set the height of image "ClickMe" to  260
   end if
   
   
   if field "score" = 110
   then
      set the width of image "ClickMe" to  250
      set the height of image "ClickMe" to  250
   end if
   
   set the locklocation of image "ClickMe" to true
end ShrinkItDown
   
   on mouseDown
      UptateScore
      changeMyLook
      ShrinkItDown
   end mouseDown

 2.StartOver

on startOver
   put 100 into field "score"
   put image "egg.png" of card "imageBank" into image "ClickMe"
   set the locklocation of image "ClickMe" to false
   set the width of image "ClickMe" to 300
   set the height of image "ClickMe" to 300
   set the locklocation of image "ClickMe" to true
end startOver

on mouseUp
   startOver
end mouseUp

3. SecondLevel

on MouseDown
   SecondLevel
end MouseDown

on SecondLevel
   put 1000 into field "score"
   put image "egg.png" of card "imageBank" into image "ClickMe"
   set the locklocation of image "ClickMe" to false
   set the width of image "ClickMe" to 300
   set the height of image "ClickMe" to 300
   set the locklocation of image "ClickMe" to true
end SecondLevel
