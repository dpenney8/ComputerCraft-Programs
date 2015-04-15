	

function sweep() 
              leftHook()
			  Strafe()
			  rightHook()
			  Strafe()
end

function Strafe() 
            local i = 0
			repeat
               local success, data = turtle.inspectDown()
			   if success == false then
			    turtle.select(1)
				turtle.placeDown()
				turtle.forward()
			   end
			   if data.metadata == 7 then
			    turtle.digDown()
			    turtle.select(1)
				turtle.placeDown()
				turtle.forward()
			   end
			   if success == true and data.metadata ~= 7 then
			       turtle.forward()
			   end
			   i = i + 1
			until i == 7
end

function leftHook()
                 turtle.turnLeft()
                 turtle.forward()
				 turtle.turnLeft()
                 local success, data = turtle.inspectDown()
				 if data.metadata == 7 then
			    turtle.digDown()
			    turtle.select(1)
				turtle.placeDown()
			   end
			   
			   
end

function rightHook()
				  turtle.turnRight()
				  turtle.forward()
				  turtle.turnRight()
				  local success, data = turtle.inspectDown()
				 if data.metadata == 7 then
			    turtle.digDown()
			    turtle.select(1)
				turtle.placeDown()
				
			   end
			   
end

function Refuel()
              turtle.forward()
              turtle.suckDown()
			  turtle.select(16)
			  turtle.refuel(5)
end			  

function home()
			  turtle.turnLeft()
			  local t = 0
			  repeat
			  turtle.forward()
			  t = t + 1
			  until t == 7
			  turtle.turnRight()
			  turtle.select(5)
			  turtle.drop(turtle.getItemCount() - 1)
			  turtle.select(6)
			  turtle.drop(turtle.getItemCount() - 1)
			  turtle.turnLeft()
			  turtle.select(1)
			  turtle.drop(turtle.getItemCount() - 10)
			  turtle.select(2)
			  turtle.drop(turtle.getItemCount() - 10)
			  turtle.turnLeft()
			  
end

turtle.forward()
Strafe()
local r = 1
repeat
      sweep()
      r = r + 1
until r == 4	  
leftHook()
Strafe()
Refuel()
home()					  
