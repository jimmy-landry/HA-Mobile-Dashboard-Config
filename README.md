# Home Assistant Mobile Dashboard
A mobile Home Assistant dashboard inspired by LE0N's Rounded theme

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://github.com/jimmy-landry/HA-Mobile-Dashboard-Config/assets/121106900/187080a2-5615-4c68-b3f9-d3718bc00c34">
  <source media="(prefers-color-scheme: light)" srcset="https://github.com/jimmy-landry/HA-Mobile-Dashboard-Config/assets/121106900/da6df125-bd12-41f8-af0c-0246c3891d67">
  <img alt="Shows a black logo in light color mode and a white one in dark color mode." src="https://github.com/jimmy-landry/HA-Mobile-Dashboard-Config/assets/121106900/187080a2-5615-4c68-b3f9-d3718bc00c34">
</picture>

> No, I'm not creative enough to give this a name. Yes, I know I could just name it "Rounded dashboard based off LE0N's dashboard," but that's a bit of a mouthful. Personally, I think Home Assistant Mobile Dashboard has a nice ring to it, don't you?

**Beginners Warning:** This repo is pretty much a dump of my config and will require some work to get working on your end. As a result, I'm assuming you have some basic YAML knowledge and will be able to troubleshoot basic issues and errors, because your dashboard will likely be freaking out with all kinds of errors after pasting in my code. Sorry in advance 😜

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

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://github.com/jimmy-landry/HA-Mobile-Dashboard-Config/assets/121106900/9c0d50d9-9546-4862-bd0f-b7385bed2145">
  <source media="(prefers-color-scheme: light)" srcset="https://github.com/jimmy-landry/HA-Mobile-Dashboard-Config/assets/121106900/fa14e902-7571-4428-bdf3-3349487c99ca">
  <img width="438" img alt="Navigate to the rounded.yaml file and choose Copy raw file." src="https://github.com/jimmy-landry/HA-Mobile-Dashboard-Config/assets/121106900/8f8c3d71-f568-4f5b-8870-4abdb8dc36ac">
</picture>

This thing right up here ⬆

**Step 2:** Import the Rounded theme file:
- 2.1: Navigate to the _rounded.yaml_ theme file and choose _Copy raw file_.

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://github.com/jimmy-landry/HA-Mobile-Dashboard-Config/assets/121106900/2f6fe260-14da-4bce-b042-b997b17d9a6a">
  <source media="(prefers-color-scheme: light)" srcset="https://github.com/jimmy-landry/HA-Mobile-Dashboard-Config/assets/121106900/8f8c3d71-f568-4f5b-8870-4abdb8dc36ac">
  <img width="288" img alt="Navigate to the rounded.yaml file and choose Copy raw file." src="https://github.com/jimmy-landry/HA-Mobile-Dashboard-Config/assets/121106900/8f8c3d71-f568-4f5b-8870-4abdb8dc36ac">
</picture>

- 2.2: Access your Home Assistant configuration.yaml file and add the following lines if you don't already have them:

```
frontend:
  themes: !include_dir_merge_named themes
```
- 2.3: Create a new folder inside the _config_ directory named "themes" (yes, it's case sensitive).
- 2.4: Inside that folder, create a new file, name it _rounded.yaml_, and paste in the rounded.yaml file that you copied earlier.
- 2.5: Save the file and restart Home Assistant.

**Step 3:** Ensure you can access and use the new Rounded theme via your profile.

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://github.com/jimmy-landry/HA-Mobile-Dashboard-Config/assets/121106900/6e29ce64-9ee9-4bd8-bb6b-e3c631eb663f">
  <source media="(prefers-color-scheme: light)" srcset="https://github.com/jimmy-landry/HA-Mobile-Dashboard-Config/assets/121106900/11f9c021-3b0c-4333-b343-ca1f1bc9135a">
  <img alt="Ensure you can access and use the new Rounded theme via your profile." src="https://github.com/jimmy-landry/HA-Mobile-Dashboard-Config/assets/121106900/d78857b8-904d-44c1-8064-94cf9bf96542">
</picture>


> oh and don't mind me having like 50 themes on my instance

If you don't see it, repeat step 2 and make sure you named the folders and files correctly.

## Time to import the actual dashboard...

- Open the _mobile_dash_redacted_master.yaml_ file and choose Copy raw file.
- In Home Assistant, go to Settings > Dashboards and create a new dashboard from scratch.

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://github.com/jimmy-landry/HA-Mobile-Dashboard-Config/assets/121106900/f68308ea-9d1e-46aa-98da-3c2fdbbafeb9">
  <source media="(prefers-color-scheme: light)" srcset="https://github.com/jimmy-landry/HA-Mobile-Dashboard-Config/assets/121106900/75bc7ce5-cfce-4c5c-93da-0f546d9af6eb">
  <img width="432" img alt="Create a new dashboard from scratch" src="https://github.com/jimmy-landry/HA-Mobile-Dashboard-Config/assets/121106900/8f8c3d71-f568-4f5b-8870-4abdb8dc36ac">
</picture>

- Open the dashboard and access the raw configuration editor:

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://github.com/jimmy-landry/HA-Mobile-Dashboard-Config/assets/121106900/104ff1e1-c04f-41e6-8ba2-41323ebc460e">
  <source media="(prefers-color-scheme: light)" srcset="https://github.com/jimmy-landry/HA-Mobile-Dashboard-Config/assets/121106900/a690855e-adb0-4402-8e9e-ed079a67c391">
  <img width="418" img alt="Access the raw config editor" src="https://github.com/jimmy-landry/HA-Mobile-Dashboard-Config/assets/121106900/8f8c3d71-f568-4f5b-8870-4abdb8dc36ac">
</picture>

- Delete any existing lines and then paste in the YAML file that you copied earlier. There should be ~5100 lines.
- Save the file and exit the raw config editor.

From here, you should be able to begin clicking through each of the cards and replacing my entities with yours.

## DON'T OPEN AN ISSUE UNTIL YOU READ THIS!!!
**MY HOME ASSISTANT ENTITIES ARE NOT THE SAME AS YOUR HOME ASSISTANT ENTITIES.** This means that you'll be seeing a bunch of errors with stuff like "Entity not found" and "ButtonCardJSTError" on pretty much every card. But don't panic. Edit each of the cards and replace each of my entities with your entities, or delete the card entirely if you don't want it. Even better, feel free to modify any of the cards to your liking. I made all the YAML available to you for a reason.

These errors say different things but all mean the same thing (the entity doesn't exist):
- Entity not found
- Entity not available
- ButtonCardJSTError
- Undefined is not an object
- _The card just doesn't show up at all_

If you've tried basic troubleshooting and are still seeing errors and don't know what they mean, _then_ feel free to drop a comment on YouTube or open an issue. I'll be more than happy to help you out.

And don't forget to drop a star on this repo if you like this dashboard! 😀
