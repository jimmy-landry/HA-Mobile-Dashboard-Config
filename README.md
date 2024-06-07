# Home Assistant Mobile Dashboard
A mobile Home Assistant dashboard inspired by LE0N's Rounded theme
> I'm not creative enough to give this a name. Yes, I know I could just name it "Rounded dashboard based off LE0N's dashboard," but that sounds too basic. Personally, I think Home Assistant Mobile Dashboard has a nice ring to it, don't you?

**Beginners Warning:** This repo is pretty much a dump of my config and will require some work to get working on your end. As a result, I'm assuming you have some basic YAML knowledge and will be able to troubleshoot basic issues and errors, as your dashboard will likely be freaking out with all kinds of errors after pasting in my code. Sorry in advance 😜

---

## You'll need the following custom repos:
_All these can be installed via HACS._
- [Layout Card](https://github.com/thomasloven/lovelace-layout-card)
- [Button Card](https://github.com/custom-cards/button-card)
- [Card Mod](https://github.com/thomasloven/lovelace-card-mod)
- [My Cards Bundle](https://github.com/AnthonMS/my-cards)
- [Swipe Card](https://github.com/bramkragten/swipe-card)
- [Vertical Stack-In Card](https://github.com/ofekashery/vertical-stack-in-card)
- [Mushroom Cards](https://github.com/piitaya/lovelace-mushroom)
- [Mini Graph Card](https://github.com/kalkih/mini-graph-card)
- [Timer Bar Card](https://github.com/rianadon/timer-bar-card)
- [Custom Brand Icons](https://github.com/elax46/custom-brand-icons) (optional but recommended, gives you more icon choices)

---

**Credit where credit is due (once again):** Of course, I need to give credit to LE0N and his amazing work with his [Rounded dashboard and theme](https://community.home-assistant.io/t/rounded-dashboard-guide/543043). I went through 4 different mobile dashboards within about 7 months before I settled on his, and I think I'll be sticking with it for quite a while. The layout of this dashboard is very heavily based off his, and the theme is pretty much identical. I used a lot of his custom button cards as well as created a few of my own. 

---

## There's a few things you need to do before you paste in the YAML file so LISTEN UP:
**Step 1:** Copy the weather_icons folder into your config/www folder. This is **required** for the weather card on the main page.

<img width="431" alt="Screenshot 2024-06-02 at 8 53 41 AM" src="https://github.com/jimmy-landry/HA-Mobile-Dashboard-Config/assets/121106900/ea1b0489-436e-4385-adad-a085e4cad05d">

This thing right up here ⬆

**Step 2:** Import the Rounded theme file:
- 2.1: Navigate to the _rounded.yaml_ theme file and choose _Copy raw file_.
<img width="288" alt="Screenshot 2024-06-04 at 9 17 19 PM" src="https://github.com/jimmy-landry/HA-Mobile-Dashboard-Config/assets/121106900/5c325602-dffa-4663-a88a-87a57558fe9e">

- 2.2: Access your Home Assistant configuration.yaml file and add the following lines if you don't already have them:

```
frontend:
  themes: !include_dir_merge_named themes
```
- 2.3: Create a new folder inside the _config_ directory named "themes" (yes, it's case sensitive).
- 2.4: Inside that folder, create a new file, name it _rounded.yaml_, and paste in the rounded.yaml file that you copied earlier.
- 2.5: Save the file and restart Home Assistant.

**Step 3:** Ensure you can access and use the new Rounded theme via your profile.

<img width="740" alt="Screenshot 2024-06-04 at 9 25 38 PM" src="https://github.com/jimmy-landry/HA-Mobile-Dashboard-Config/assets/121106900/15280cd9-923b-4a76-8a10-5be9f19c60f9">


> oh and don't mind me having like 50 themes on my instance

If you don't see it, repeat step 2 and make sure you named the folders and files correctly.

## Time to import the actual dashboard...

- Open the _mobile_dash_redacted_master.yaml_ file and choose Copy raw file.
- In Home Assistant, go to Settings > Dashboards and create a new dashboard from scratch.

<img width="451" alt="Screenshot 2024-06-04 at 9 39 23 PM" src="https://github.com/jimmy-landry/HA-Mobile-Dashboard-Config/assets/121106900/743ba45d-0e25-41bb-b7ce-26e4f86e785c">

- Open the dashboard followed by the Raw config editor as shown below:
  
![raw config editor 001](https://github.com/jimmy-landry/HA-Mobile-Dashboard-Config/assets/121106900/65f5621e-0d04-4fef-8d2e-855023db4fdb)

- Delete any existing lines and then paste in the YAML file that you copied earlier. There should be ~5100 lines.
- Save the file and exit the raw config editor.

From here, you should be able to begin clicking through each of the cards and replacing my entities with yours.

## DON'T OPEN AN ISSUE UNTIL YOU READ THIS!!!
**MY HOME ASSISTANT ENTITIES ARE NOT THE SAME AS YOUR HOME ASSISTANT ENTITIES.** This means that you'll be seeing a bunch of errors with stuff like "Entity not found" and "ButtonCardJSTError" on pretty much every card. But don't panic. Edit each of the cards and replace each of my entities with your entities, or delete the card entirely if you don't want it. Even better, feel free to modify any of the cards to your liking. I made all the YAML available to you for a reason.

If you've tried basic troubleshooting and are still seeing errors and don't know what they mean, _then_ feel free to drop a comment on YouTube or open an issue. I'll be more than happy to help you out.

