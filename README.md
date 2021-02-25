# self_driving_car
This is your own self driving car where your own Tesla can go left, right, and forward with just 60 lines of python your self driving car will be up and running.
I have done it by using Pycharm which is an python code editor.
For the code I have used a pip (python installation package) which is **pip install pygame**.
I have installed the same both packages in the terminal.
After installing the packages in the terminal you have to download some images which I will give in different files.
At the first I have imported the package pygame.
After that I have initiated pygame.
Then I have created a variable called window and I have entered the value as pygame.display.set_mode((1200, 400)).
Then we have created another variable called track and entered the value as pygame.image.load('track6.png').
Then for the car to show up we have created another variable and entered the value as pygame.image.load('tesla.png').
Then I have wrote car = pygame.transform.scale(car, (30, 60)) this code we have put for the scaling for the car.
Then we have created another variable called car_x this variable we have created for the x means horizontal position of the car and we have stored the value as 155.
Then we have created another variable called car_y this variable we have created for the y means vertical position of the car and we have  stored the value as 300.
Then we have created another variable called as focal_dis and stored it's value as 25.
Then again we have created another variable called cam_x_offset and stored the value as 0.
Then we have created another variable called cam_y_offset and the value we have stored in it is 0.
Then we have to put the car facing up or our self-driving car will go backward!! so to put the car in the direction of up we write the code as direction = 'up'.
Then we make a variable called drive and make the value as True.
Then we have created another variable called clock nd then we have stored the value as pygame.time.Clock().
Then we get a while loop and we write it as while drive inside this while loop we have made a for loop which is for event in pygame.event.get(): and then inside that we have made an if loop which is if event.type == pygame.Quit: inside this if loop we have told the drive = false.
Then we have wrote some code just some lines below of the for loop we created and the code these clock.tick(60) and then we have wrote cam_x = car_x + cam_x_offset + 15 and then after that is cam_y = car_y + cam_y_offset + 15 then we have written as up_px = window.get_at((cam_x, cam_y - focal dis))[0] and then the same down_px = window.get_at((cam_x, cam_y - focal dis))[0] and then for the right right_px = window.get_at((cam_x + focal dis, cam_y))[0] and then to print that we have wrote print(up_px, right_px, down_px).
Then we have wrote some code for the directions of the car so it is if direction == 'up' and up_px != 255 and right_px == 255: and then inside it we have wrote direction = 'right' and then cam_x_offset = 30 and then after that we are gonna write car = pygame.transform.rotate(car, -90).
Then we have created another set of code that is elif direction == 'right' and right_px != 255 and down_px == 255: and inside this I have wrote direction = 'down' and then car_x = car_x + 30 and after that cam_x_offset = 0 and then cam_y_offset = 30 and then at the last car = pygame.transform.rotate(car, -90).
After that we have created another set of code which is elif direction == 'down' and down_px != 255 and right_px == 255: and then inside this I have wrote some few lines of code which are direction = 'right'and then car_y = car_y + 30and after that cam_x_offset = 30and then we have wrote cam_y_offset = 0and then at the last I have wrote car = pygame.transform.rotate(car, 90).
Again we have created another set of code which are elif direction == 'right' and right_px != 255 and up_px == 255: and then inside this I have wrote some lines of code which are direction = 'up'and then car_x = car_x + 30 and after that cam_x_offset = 0 and then we have wrote car = pygame.transform.rotate(car, 90).
Then some small set of code I have written which are if direction == 'up' and up_px == 255: and inside this I have written car_y = car_y - 2.
Then this is another small set of code which is elif direction == 'right' and right_px == 255: and inside this I have written car_x = car_x + 2.
Then here is the last small set of code elif direction == 'down' and down_px == 255: and inside this I have written car_y = car_y + 2.
Then I have written window.blit(track, (0, 0)).
Then after this I have written window.blit(car, (car_x, car_y)).
And after that at the last I have written pygame.draw.circle(window, (0, 255, 0), (cam_x, cam_y), 5, 5).
Then at last to run and update your code this is the last line you have to write which is pygame.display.update().
Here your Self Driving car is ready now don't buy Tesla and with just 60 lines of python your self driving car is ready enjoy!!!
