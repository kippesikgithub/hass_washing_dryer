# hass_washing_dryer
How to use Power monitoring for HA notifications on Washing machine and Dryer

## Explanation
The issues we had: Washing machine/Dryer does not give a sound or notification when done.
Using power measuring to determine when the Washing Machine or Dryer is finished.

# Howto
- Create Needed template sensors
- Determine the amount of Watts when the washing machine or dryer has finished
- Check if result is as expected
- Telegram or HA notification integration

## HA Config
![image](https://user-images.githubusercontent.com/100353268/212078202-74f94be3-b3cc-416c-8946-ece0da431f2b.png)
Creating a status entity for the Washing machine, dryer and dishwasher. With the delay_off you can controll the moment you get the notification.

## Node Red example telegram message
![image](https://user-images.githubusercontent.com/100353268/212079142-fb10d5be-9866-4a84-81dc-e3b7b56c12f9.png)
Based on the status entity we created in the step above, we create a message the moment the entity gets the status 'off'.

