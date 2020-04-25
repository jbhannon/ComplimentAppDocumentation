

# Compliment Giver Documentation

Here is where I will document the creation of my Compliment Giver App.

In general, each section below will be comprised of various journal-like entries as I develop my app.

## Table of Contents

- [Introduction](#introduction)
	- [Project Proposal](#project-proposal)
	- [Project Proposal Feedback](#project-proposal-feedback)
	- [Gant Chart](#gant-chart)
- [Technical Process](#technical-process)
	- [Failures](#failures)
	- [A New Approach](#a-new-approach)
	- [Google Sheets to PHP](#google-sheets-to-php)
	- [PHP to Unity](#php-to-unity)
	- [Random Compliments](#random-compliments)
	- [Save System](#save-system)
- [Mid-semester Check-in](#mid-semester-check-in)
- [COVID-19](#covid-19)
- [Art Process](#art-process)
	- [Heart](#heart)
	- [Border](#border)
	- [Settings](#settings)
	- [Font](#font)
	- [In Game](#in-game)
- [User Guide](#user-guide)
- [Postmortem](#postmortem)
- [Sources](#sources)


## Introduction

### Project Proposal

The first work I did for this project was to complete the assignment [_Project Proposal 1_](documentationFiles/projectProposal1.pdf) which was a first draft of my idea for the project I will create in this course (completed January 26th).
Below I will display my current answers to the various questions.

> ___What is your overall idea?___
> 
> I want to make a small compliment-giving app using Unity.
I want to build an app that connects to a google sheet that someone else can fill with custom complements for the app user.
The ideal use of the app would be two users having the app and swapping URLs to separate google sheets and then filling each other’s sheets with compliments.

> ___What tool(s) do you hope to learn (or become more proficient at) over the course of this
project?___
> 
> Unity 2D, C#, Photoshop, Adobe Illustrator

> ___How familiar are you with your chosen tools?___
> 
> I’m familiar with Unity 3D, around 3 years of experience, but I have little to no experience Unity 2D.
C# I have a decent amount of experience, about 2 years, but I have never connected to an online source via C#.
I have about a year and a half of experience in Photoshop and Illustrator.

> ___How proficient do you expect to become via using your tools by the end of the semester?___
> 
> Unity in general and especially Unity 2D can be quite complicated and more so can be learned best by trying out completely different projects.
With this app, I’m going out of my comfort zone so I can hopefully learn a new area of Unity.
I have done no online calls using C#, so I hope to become well-versed in this technique to use it on  later projects.
I can always be growing in Photoshop and Illustrator, especially in new and better methods/in their integration into Unity.

> ___What do you imagine your final project deliverable(s) will be based off the tool(s) you
use to create it?___
> 
> The submission will be an app.
I will make an APK which can only be used by androids, so to let everyone experience the app I will also make a windows (standalone) build so you can use the app on your computer by just clicking the .exe, and a video taking you through the app to explain it.

> ___Do you think your stated final deliverable(s) are fair?___
> 
> I think this is very fair. I am branching out into a space that I am not confident in
and don’t quite know how exactly to get it accomplished yet. Unity is notoriously
finicky and will take many hours of research and many tries to complete the main
mechanics of my app and that’s not including the art to make the app look better.

> ___Who is your target user group?___
> 
> My target user group is rather broad. I think that couples within the 16-30 range
would enjoy the app the most as I intend it, which is almost gamifying love and
affection. I do think, however that some not in relationships may enjoy this app to
use with friends.

> ___Why are they your chosen target user group?___
> 
> My main target group (16 – 30 and in a relationship) comes from the original 
concept of this app being used to better the communication between couples. I think
that in order to experience this app as it was intended the target group would need a
phone with the ability to use this app, the desire to use an app to communicate, and
a S.O. to communicate with via this app. Therefore, I think around 16 – 30 and in a
relationship is the user group that will best utilize this app

> ___What is your motivation for creating this project?___
> 
> My motivation comes honestly from my semi-long-distance relationship and
wanting to still feel connected to my S.O. in a more personal way than just a random
compliment generator especially when either of us is busy.

> ___What is your purpose?___
> 
> Good communication is a key to success in healthy relationship and ‘Words of
Affirmation’ is one of the most common languages of love/affection. With this app I
hope to give couples another avenue to express their love/affection and to receive
that love/affection when one or the other is busy or they just need a pick-me-up.

> ___What are your initial plans on how to tackle doing research for your project?___
> 
> The hardest part of this project will be to get unity to pull, save, and then access .csv
files from google sheets so that’s where I will start. I plan on making a simple unity
scene that pulls a .csv from google sheets and displays the text in a UI text box. I
know that it is possible, so I have that going for me, I just need to find the right
tutorials and edit them for my specific purposes.

> ___What outcomes are you hoping for and/or foresee taking place?___
> 
> Well I hope to get at least a beta out by Valentines’ Day to give to my S.O. to test out
but ultimately I hope to make at least an APK to post online so that my friends and 
anyone who wants to use the app can enjoy it and better their relationships or
friendships.

### Project Proposal Feedback

After completing my project proposal, I received and documented feedback from my peers. I will document it below:

I answered 5 questions for each peer. The questions were:

> 1) ___Can your classmate re-articulate back to you what your project is mainly about in 45 seconds to 1 minute?___
> 2) ___Do they think your project goals sound feasible?___
> 3) ___Do they think your multimedia tool goals sound feasible?___
> 4) ___Are there any multimedia tools they could suggest to you to help you in your project?___
> 5) ___What would they like to see you add, drop, and/or change about your project? Why?___

The responses were as follows:

<table>
<tr>
<td>
<b>Emilie Holtz</b>
</td>
<td>
	
1) Yes, she was accurate
			
2) Project sounds feasible

3) Multimedia tools sound feasible

4) No recommendations for multimedia tools

5) Add seasonal or changing content, keep UI fresh

</td>
</tr>

<tr>
<td>
<b>Logan Couch</b>
</td>
<td>
	
1) Yes, he understood the concept well enough to repeat it back

2) He thinks the project sounds achievable and not too small

3) He thinks the technologies used sound feasible

4) He didn’t have any recommendations for the multimedia tools

5) He recommended perhaps adding sound effects to make it more fun and game-like

</td>
</tr>
<tr>
<td>
<b>Diana Eakhshiyar</b>
</td>
<td>
	
1) She was a little confused about what’s being shared, it was my mistake as I emphasized too much on the documents and not on the app itself.

2) Goal sounds feasible

3) Tools sound feasible

4) No tools suggested

5) She suggested adding more art and making the app feel very loving

</td>
</tr>
</table>

I took their comments and used them to better shape my proposal and re-prioritize the way I would delegate my time for different parts of the project.

### Gant Chart

With the knowledge I gained from the creation of my project proposal and with the feedback I gained from my peers, I needed to create a schedule that I would try to follow in order to stay on track to complete my project in time.

To do this, I created a Gant Chart (template provided by my lab AI: Dinesh Ramaswamy) to attempt to manage my time.

![Gant Chart](images/gant.PNG)

As you can note in the chart above, I made a conscious decision to work on the technical aspects of my project first.
I did this because I wanted to be sure that I could get my core functions to work before spending time beautifying.
For this reason, I allotted up until week 9 (right before spring break) to get all technical aspects completed so that I can rest over spring break and polish when I get back.
I also saved a lot of time at the end of the semester for unforeseen setbacks and a lot of time for polishing so I did not run out of time.

Now with all pre-planning complete, I'm ready to start the production of my project.

## Technical Process

Here is where I will document the first half of the creation of this project: the technical process

### Failures

I started this process by trying to get my hardest mechanic out of the way: how to get information from google sheets into my app. The first thing that came to mind was to try different plugins from the [Unity Asset Store](https://assetstore.unity.com/) that would help me access the Google Sheets API. I wasted about 3 weeks trying these different methods, all of which failed.

![Google Sheets Try 1](images/googleSheetsTry1.PNG)
My first plugin I attempted to use was [Google Sheets to Unity](https://assetstore.unity.com/packages/tools/utilities/google-sheets-to-unity-73410). This package was great for certain needs, but not for me. This package optimized the time spent with large groups by allowing information to be stored in google sheets then pulled into the Unity Editor. The problem for me, is that I need this plugin to work in real-time on people's apps, not just in the Unity Editor. So I had to scrap that Unity Project entirely to start over.

![Google Sheets Try 2](images/googleSheetsTry2.PNG)
My second plugin I attempted was [XlsxParser](https://assetstore.unity.com/packages/tools/input-management/xlsxparser-80712) which was a plugin designed to parse through spreadsheets. This worked a little for me. I would download my google sheet as a spreadsheet then import it into unity, then use the package to read the sheet and display the different rows of compliments. My problem was that I needed this to work for any given google sheet and I couldn't figure out a way to get a spreadsheet download from any given google sheet so I gave up on this method too and scrapped this Unity project as well.

![Google Sheets Try 3](images/googleSheetsTry3.PNG)
My third and final plugin I attempted to use was [MetaSheets Free](https://assetstore.unity.com/packages/tools/utilities/metasheets-free-94656) which I thought would assist in integrating the xlsx files into my project, and the plugin did work to an extent. The plugin would look at xlsx documents and help coding in visual studio by giving helpful code snippets and column names. Again, I ran into the issue that this only helped me if I could find a way to download xlsx documents and save them from google sheets.

### A New Approach

So none of the plugins that I was using worked out for me, so it was time to choose a new approach.
For my capstone project (my final project-based course for my Informatics degree) I needed to access a database while using Unity in real-time and I stumbled upon the use of calling a website with C#, writing that website in PHP to access a database and display certain needed information, then using C# to read and parse through that PHP page to use in-game.

This got me thinking about whether PHP can access Google Sheets and print out entries which, turns out, it can! This gave me the idea of how I would get my core functionality into my game.

I would write PHP code to parse through a given URL and display the columns.
I would then write C# code that would be able to construct a website URL to view, then parse through the content on that page and separate the content into individual compliments.

Now let's get into how I actually developed this functionality!


### Google Sheets to PHP

So I began by writing the PHP code that I would need to access Google Sheets, parse through a page, then display each of the entries separated by new lines.
I used this page -> [Google Sheets to PHP Tutorial](https://community.spiceworks.com/topic/1290489-use-google-spreadsheet-as-data-source-for-webpage) to understand the way that I properly access and parse through a Google Sheet and then edited the code slightly so that I would easily be able to parse through the lines inside of Unity.

Also required to make this work, I had to publish my example Google Sheet page and get the *.csv* share link.
This means that I will have to include some sort of setup instructions for the users so they know how to use the app.

Here's the first iteration of my PHP code (URL is hard-coded for testing):

```PHP
$spreadsheet_url="https://docs.google.com/spreadsheets/d/e/2PACX-1vSHvNJFikAJRxgf2V1Uf2yvMUHq56xKQjlIsVLBBM11gdE6-pKRy2ZpybwLyhn-Ew31bfnUraKdFOYi/pub?gid=0&single=true&output=csv";

if(!ini_set('default_socket_timeout', 15)) echo "<!-- unable to change socket timeout -->";

if (($handle = fopen($spreadsheet_url, "r")) !== FALSE) {
    while (($data = fgetcsv($handle, 1000, ",")) !== FALSE) {
		echo $data[0] . "\n";
    }
    fclose($handle);
}
else
    die("Problem reading csv");
```

### PHP to Unity

Now that I had a web-page that was accessing and displaying the entries from a Google Sheet, I could now use Unity's UnityWebRequest class to access and parse through that web-page.
This was the code that I was already familiar with through my work on my capstone project, but here is the original tutorial I used to learn this functionality -> [PHP to Unity Tutorial](https://wiki.unity3d.com/index.php/Server_Side_Highscores).

The code (written in C#) goes to a given URL (my PHP url), checks whether there's a connection issue, if there's not, will create an empty list of strings and fill it with each item in the downloaded text (if it's not empty).
This means that I now have all of the compliments from a given Google Sheet now saved as a list in Unity.

Here's the C# I used to download and save each compliment into a list:
```C#
 IEnumerator Display()
    {
        UnityWebRequest complimentsGet = UnityWebRequest.Get(url);
        yield return complimentsGet.SendWebRequest();

        if (complimentsGet.isNetworkError)
        {
            Debug.Log("Error: " + complimentsGet.error);
        }
        else
        {
            if (complimentsGet.downloadHandler.text == "")
            {
                Debug.Log("No Entries Found");
            }
            else
            {
                List<string> compliments = new List<string>();
                foreach (string st in complimentsGet.downloadHandler.text.Split('\n'))
                {
                    if (st != "")
                    {
                        compliments.Add(st);
                    }
                }
                this.GetComponent<ComplimentList>().compliments = compliments;
                this.GetComponent<ComplimentList>().SaveList();
            }
        }
    }
```

### Random Compliments

I then had to expand on this code in order to display each compliment randomly.
I started by just choosing a random item on each click of a button, but this meant that I got a lot of repeated compliments in a row and it took very long to get through the whole list.

To solve this, I made my own code that would ensure that we would iterate through the list of compliments randomly and we would not have repeats.
My solution was to create a new list, fill it with the compliments, then each time that the code was run, a random compliment from that new list would be used and deleted, then when that list became empty we would fill it once again with all compliments.
This means that all compliments will be seen before seeing repeats.

The code that I created to randomly choose compliments to display is shown below:

```C#
public class ComplimentList : MonoBehaviour
{
    public List<string> compliments = new List<string>();
    public List<string> UnusedCompliments = new List<string>();
    public GameObject ComplimentText;

    public void Display() {
        if (compliments.Count != 1) {
            if (UnusedCompliments.Count == 0) {
                UnusedCompliments = new List<string>(compliments);
            } 
            int nextCompliment = Random.Range(0, UnusedCompliments.Count);
            ComplimentText.GetComponent<TextMeshProUGUI>().text = UnusedCompliments[nextCompliment];
            UnusedCompliments.RemoveAt(nextCompliment);
        }
        
    }

    public void SaveList()
    {
        SaveSystem.SaveList(this);
        UnusedCompliments = new List<string>();
        Display();
    }

    public void LoadList()
    {
        ComplimentData data = SaveSystem.LoadList();

        if (!(data is null)) {
            compliments = data.compliments;
            Display();
        }
        
    }
}
```

### Save System

You may have noticed in the last code snippet that I included save/load functions.
This is because I wanted to be sure that users didn't have to re-download the Google Sheet they were using every time they opened the app.

To solve this problem, I integrated a save/load system that I became familiar with in my capstone project.
The original tutorial I used to learn how to save/load was this video by Brackeys -> [Unity Save/Load System](https://www.youtube.com/watch?v=XOjd_qU2Ido).

The two code snippets (below) take a list of strings, serialize the list (turn it into 1s and 0s) then save that file as "compliments.fun" into any device.
To load, the code takes that "compliments.fun" file, de-serialize it, then sets the list of complements to the list found in the saved file.

I also made it so that every time you grab data from a Google Sheet the system saves that list of compliments, and every time the program is started it tries to load an existing list of compliments.
This means that the compliments would be consistently found on every use of the app.

Here is my save/load code (written in C#):

```C#
[System.Serializable]
public class ComplimentData
{
    public List<string> compliments;

    public ComplimentData (ComplimentList list) {
        compliments = list.compliments;
    }
}
```
```C#
public static class SaveSystem
{

    public static void SaveList(ComplimentList list)
    {
        BinaryFormatter formatter = new BinaryFormatter();
        string path = Application.persistentDataPath + "/compliments.fun";
        FileStream stream = new FileStream(path, FileMode.Create);

        ComplimentData data = new ComplimentData(list);

        formatter.Serialize(stream, data);
        stream.Close();
    }

    public static ComplimentData LoadList()
    {
        string path = Application.persistentDataPath + "/compliments.fun";
        if (File.Exists(path))
        {
            BinaryFormatter formatter = new BinaryFormatter();
            FileStream stream = new FileStream(path, FileMode.Open);

            ComplimentData data = formatter.Deserialize(stream) as ComplimentData;

            stream.Close();

            return data;
        }
        else
        {
            Debug.Log("Save file not found in " + path);
            return null;
        }
    }

}
```
## Mid-semester Check-in

On February 26th we had a PowerPoint explaining where we were due to show our peers and get input about our current accomplishments and where to go from here.
You can find the presentation link here -> [Compliment App Check In PowerPoint](documentationFiles/ComplimentAppCheckIn.pptx)

I thought now would be a good time in my documentation to also do a quick summary of where I stand.

I now have all my functionality built into my app that I'll need, the only remaining tasks are to beautify my UI.

Here you can see compliments being displayed, you can place in a new Sheet URL, refresh your compliments, and get a new random compliment:

![Check In image 1](images/checkIn1.PNG)

Here is what my example Google Sheet looks like, all compliments are just listed down the first column:

![Check In image 2](images/checkIn2.PNG)

And here is what the inspector looks like inside of Unity.
Notice that each compliment is it's own item.
Also notice that I have two lists, one to store the compliments, one to choose from:

![Check In image 3](images/checkIn3.PNG)

## COVID-19

Here is where I was in my process of creating this app when COVID-19 caused a great disruption in my life. I spent the extended spring break locked in a single room, only exiting to quickly get food from the store and come back. When school started back up, I only lasted about a week before having a mental breakdown and subsequently traveling back home to quarantine with my family.

These shifts in my mental state and my environment severely impacted my work ethic so I wasn't able to complete as much as I intended to. Along with that, I also lost access to a mac (which I needed to build this app onto my phone) and lost access to any powerful computers (which caused a much slower process and a lot of computer crashes)

Overall, COVID-19 caused me to scale back my project a bit for the back half. I'll now discuss that back half of the project below.

## Art Process

Below I will go through each of the art assets that I created for the app, and then I will discuss how they all came together to create the aesthetics of the game.

### Heart

The first thing that I wanted to create was the custom button that users would be pressing for each new compliment. From the research that I conducted during lab time, I knew that users wanted the graphics to be centered more around love than platonic friendship. Knowing that, I really leaned into the lovey-dovey graphics and made a big heart button to press.

I created the heart with Adobe Illustrator by making a curve that looked like one side of a heart then flipped it horizontally. I took that heart shape and created many different sizes of concentric hearts. I then added some squiggly subdivisions so I could shade to make the heart look 3D.

Here's what the heart looked like with just lines:

<img src="images/heart_process2.png" height="500px"/>

I then filled in the heart with different shades of red to add shape:

<img src="images/heart_process1.png" height="500px"/>

Here is the heart asset that I ended up creating:

<img src="images/heart.png" height="500px"/>

### Border

Similar to the heart button, I really wanted to lean into the lovey-dovey feeling of the app, and I knew I wanted to add a border to the application. I also knew that Unity allows you to import a sprite and define a border and corners that can then be tiled.

So I set out to create a border that was intertwining, giving the feeling of love and togetherness. I experimented with this for a while but finally decided on a pattern of lines. I then gave those lines a border and expanded the object. I also put hearts wherever the lines met

Here's what I came up with:

<img src="images/border_process2.png" height="500px"/>

I then added color to the lines and borders, making sure that I was staying with the color palette that I had earlier defined with my heart button.

Here's what I came up with:

<img src="images/border_process1.png" height="500px"/>

And here's how the exported asset came out:

<img src="images/border.png" height="500px"/>

### Settings

So with a good portion of my art done, I now needed a couple UI icons for the settings menu and the exit button (to get out of the settings menu). I knew that I had to keep these pretty minimalist to match the rest of the app, so I messed around for a bit until I discovered a way to make the cog icon. I took 4 rectangles and rotated them to look like an X and a + put together, I then combined them with a large circle and then cut a smaller circle out of the middle.

While I was at it, I also created an X out of just two of the rectangles combined together.

Here's what it looked like without color:

<img src="images/settings_process2.png" height="500px"/>

I knew that I could change white to any color within unity, so I decided to keep the fill of these icons white so they would be able to be customized in the game. I also thought dark gray borders would go with any color that I ended up deciding to go with in Unity.

Here's what they looked like with color:

<img src="images/settings_process1.png" height="500px"/>

So here's what the settings cog looked like exported:

<img src="images/settings.png" height="500px"/>

And here's what the X looked like exported:

<img src="images/x.png" height="500px"/>

### Font

I needed a cutsie font to use in game so I went looking online for a free font to use. I ended up finding the font called [Words of Love](https://www.1001fonts.com/words-of-love-font.html) by Pizzadude.

![Words of Love](images/wordsOfLove1.png)

I thought the characters where really cute and would be perfect in the game. Sadly, there were no numbers in this font and they just turned into stars, but this was a sacrifice I was willing to make for such a cute font.

Here's what the characters looked like:

![Words of Love Characters](images/wordsOfLove2.png)


### In Game

The button was pretty easy to put in, all it was was an image that was a ray-cast target (allows users to press it) and a button component which allowed me to tell the program what to do when I pressed the heart.

I also implemented the border, which involved putting the image as the background of a panel, telling it to tile the edges, then adjusting how many times it would repeat.

Here's the setup for my border:

![In-game 3](images/inGame3.png)

I then put all of these items together with the initial setup that I already displayed earlier in the documentation. I had to re-place the button, reorganize the hierarchy, etc.

Here's what the hierarchy now looked like:

![In-game 2](images/inGame2.png)

And here's what the actual in-game view looks like now:

![In-game 1](images/inGame1.png)

## User Guide

Luckily, the way I setup this app, it's rather easy to use.  I even created a little graphic in the app to explain how to set it up:

![In-game 4](images/inGame4.png)

So here are the steps:

 1. Create a Google Sheet and fill the left-most column with compliments*
 2. Go to File > Publish to the Web
 3. Set the drop-downs to the entire document as .csv
 4. You then will either give that link to someone else using the app or paste it yourself

Once you hit "Refresh Database" the app will take a moment to contact the sheet, download, and save the compliments.

Now that it's setup, every time you hit the heart a new compliment will be given to you!

**each compliment has to be longer than one character or it won't be added*

## Postmortem

Here is the postmortem I wrote for the end of this porject. You can also find the .pdf here: [Reflection Paper](documentationFiles/ReflectionPaper.pdf)

> This project, the Compliment App is all providing human connection, even when you cannot be there physically. It is all about finding that one person that keeps you happy and being able to get asynchronous affection from them. I have a hard time with depression many times stemming from a feeling of not being seen or acknowledged, and many times what I need is to feel some sort of affection, usually words of affirmation if I can’t have physical contact. Though one of the issues with living like this is that you cannot always get someone else’s attention when you need it. We also have to realize here that it is selfish to rely on others to set aside time to give you affection when they have busy lives and are probably struggling with many of the same issues that we are. So, with the creation of this app, it was important to me that I created a way to provide a way to give and receive affection asynchronously, allowing the users to receive affection at any time.
> 
> Also important to me was human connection and a way to surpass distance. I did not want to just create a random compliment generator, I wanted to make sure that people were getting customized messages. What better way to get customized compliments than to receive them from someone who knows the intended user? I also wanted a way for the users to receive compliments from any distance. What is so weird is that all of this was my internal reasoning at the beginning of the semester, and then COVID-19 came along and multiplied all these needs by 10. I think we are all feeling negative impacts of social distancing which makes the need for affection and affirmation that much more important. Personally, I have missed my significant other for the duration of entering self-isolation and have greatly needed some way to stay connected, even when we are both busy with schoolwork.
> 
> Admittedly, a lot of my motivation for this project was to satisfy my needs, but in constructing the project, I put a lot of thought into who would be using this app. I wanted to make sure that anyone who wanted to use the app could, and that it would be easy and convenient for them to setup a connection through the app. Knowing that I would be trying to assist those that don’t live with their significant other, I knew that my target audience would most likely be young adults. Knowing this, it allowed me to create the product around this target group. I know that almost every young adult has a smartphone and would be able to download this app onto their phones. I also knew that I had a little bit of leeway with the setup (having them go through google sheets and setup a spreadsheet with the compliments and exchange URLs), knowing that they probably have a bit of technical competence to be able to do these steps.
> 
> So that is why I ended up choosing to develop a mobile app, but I could have coded in many different coding environments, but I chose to produce my app in Unity. I am very comfortable with Unity (not really Unity2D) but there were more reasons than just that. Unity provides so many built-in functions and features that make very interactive apps. The code is just in C# which I was able to manage, but the art was greatly helped by Unity. I was able to add an interactable custom button, a scaling border, particle effects for the button, sounds on the button, etc. All these features through Unity allowed me to make my app more and more interactive, which was one of my goals when laying out my project to begin with.
> 
> As for the pros/cons for my application, I think that a lot of my planning paid off when it came to platform and usability. I think that this app is very accessible, and very convenient to use, I think there are a lot of pros to the asynchronous features of the app, and I think that there’s pros to the compliments being user-generated. For all of the reasons I listed above, it was important that this app was able to be used at any time, and that it would be incredibly easy for the users to do so, and I think all of these goals were achieved. As for the cons, I think that the asynchronous nature of the app can kind of be a disadvantage. It is easy to set up this app and then forget about it, on both sides. For the user, they can forget that the app is there, because it is not an in-grown reaction to go to this app when they need affection. As for the person creating and maintaining the database, it is easy for them to completely forget about the google sheet and stop updating it. It also takes quite a while to get into google drive in the first place, and then to edit a spreadsheet would seem like a large task that many people might just choose not to do because of the time commitment.
> 
> I think the strongest aspect of this app is the code supporting it. I had the most time to work on this, and it was the backbone of my idea. Everything from php pull requests, to the list structure that makes sure you see the full list of compliments before repeating, to the save/load features are very strong features. All of these were strong coding choices that I stand by. As for the weaknesses, I think I could have made some better art/particle effects and a better tutorial. I think I could have also added some more features so you can save you favorite compliments, etc. But the second half of this project was severely limited by COVID-19. I think they are still not terrible, just not exactly what I envisioned.
> 
> So, now that the project is done and I am turning it in, how do I feel? Honestly, my gut reaction is to be upset about not achieving everything I set out to achieve, being a perfectionist, but I’m working on being kinder to myself, so I think that in the end I’m proud of myself. I know how hard this semester was, and putting that in perspective, I think the project was a success. I am looking forward to getting access to a Mac so I can download this app onto mine and my significant other’s phones 😊
> 
> As for the documentation, I am very proud of this deliverable. I chose to create and maintain the documentation on GitHub which is very structured (which was an advantage and disadvantage) but it ended up looking great. The way I structured the documentation, it is very easy to follow, and I was able to access it from anywhere which made editing it very easy to do. I also think that I provided a lot of written explanation for every aspect on my app, hopefully successfully providing my internal monologue for the entire process. I hope that you find it helpful and that you enjoy reading through it (and using my app for that matter).


## Sources

- [Google Sheets to PHP Tutorial](https://community.spiceworks.com/topic/1290489-use-google-spreadsheet-as-data-source-for-webpage)
- [PHP to Unity Tutorial](https://wiki.unity3d.com/index.php/Server_Side_Highscores)
- [Unity Save/Load System](https://www.youtube.com/watch?v=XOjd_qU2Ido)
- [Words of Love](https://www.1001fonts.com/words-of-love-font.html) by Pizzadude
