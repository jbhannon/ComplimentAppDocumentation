# Compliment Giver Documentation

Here is where I will document the creation of my Compliment Giver App.

In general, each section below will be comprised of various journal-like entries as I develop my app.

## Table of Contents

- [Introduction](#introduction)
- [Technical Documentation](#technical-documentation)
	- [Failures](#failures)
	- [Google Sheets to PHP](#google-sheets-to-php)
	- [PHP to Unity](#php-to-unity)
	- [Save System](#save-system)
- [Art Documentation](#art-documentation)
- [User Guide](#user-guide)
- [Postmortem](#postmortem)


## Introduction

The first work I did for this project was to complete the assignment [_Project Proposal 1_](documentationFiles/projectProposal1.pdf) which was a first draft of my idea for the project I will create in this course (completed January 26th).
Below I will display my current answers to the various questions.

> ___What is your overall idea?___

> I want to make a small compliment-giving app using Unity.
I want to build an app that connects to a google sheet that someone else can fill with custom complements for the app user.
The ideal use of the app would be two users having the app and swapping URLs to separate google sheets and then filling each other’s sheets with compliments.

> ___What tool(s) do you hope to learn (or become more proficient at) over the course of this
project?___

> Unity 2D, C#, Photoshop, Adobe Illustrator

> ___How familiar are you with your chosen tools?___

> I’m familiar with Unity 3D, around 3 years of experience, but I have little to no experience Unity 2D.
C# I have a decent amount of experience, about 2 years, but I have never connected to an online source via C#.
I have about a year and a half of experience in Photoshop and Illustrator.

> ___How proficient do you expect to become via using your tools by the end of the semester?___

> Unity in general and especially Unity 2D can be quite complicated and more so can be learned best by trying out completely different projects.
With this app, I’m going out of my comfort zone so I can hopefully learn a new area of Unity.
I have done no online calls using C#, so I hope to become well-versed in this technique to use it on  later projects.
I can always be growing in Photoshop and Illustrator, especially in new and better methods/in their integration into Unity.

> ___What do you imagine your final project deliverable(s) will be based off the tool(s) you
use to create it?___

> The submission will be an app.
I will make an APK which can only be used by androids, so to let everyone experience the app I will also make a windows (standalone) build so you can use the app on your computer by just clicking the .exe, and a video taking you through the app to explain it.

> ___Do you think your stated final deliverable(s) are fair?___

> I think this is very fair. I am branching out into a space that I am not confident in
and don’t quite know how exactly to get it accomplished yet. Unity is notoriously
finicky and will take many hours of research and many tries to complete the main
mechanics of my app and that’s not including the art to make the app look better.

> ___Who is your target user group?___

> My target user group is rather broad. I think that couples within the 16-30 range
would enjoy the app the most as I intend it, which is almost gamifying love and
affection. I do think, however that some not in relationships may enjoy this app to
use with friends.

> ___Why are they your chosen target user group?___

> My main target group (16 – 30 and in a relationship) comes from the original 
concept of this app being used to better the communication between couples. I think
that in order to experience this app as it was intended the target group would need a
phone with the ability to use this app, the desire to use an app to communicate, and
a S.O. to communicate with via this app. Therefore, I think around 16 – 30 and in a
relationship is the user group that will best utilize this app

> ___What is your motivation for creating this project?___

> My motivation comes honestly from my semi-long-distance relationship and
wanting to still feel connected to my S.O. in a more personal way than just a random
compliment generator especially when either of us is busy.

> ___What is your purpose?___

> Good communication is a key to success in healthy relationship and ‘Words of
Affirmation’ is one of the most common languages of love/affection. With this app I
hope to give couples another avenue to express their love/affection and to receive
that love/affection when one or the other is busy or they just need a pick-me-up.

> ___What are your initial plans on how to tackle doing research for your project?___

> The hardest part of this project will be to get unity to pull, save, and then access .csv
files from google sheets so that’s where I will start. I plan on making a simple unity
scene that pulls a .csv from google sheets and displays the text in a UI text box. I
know that it is possible, so I have that going for me, I just need to find the right
tutorials and edit them for my specific purposes.

> ___What outcomes are you hoping for and/or foresee taking place?___

> Well I hope to get at least a beta out by Valentines’ Day to give to my S.O. to test out
but ultimately I hope to make at least an APK to post online so that my friends and 
anyone who wants to use the app can enjoy it and better their relationships or
friendships.

## Technical Documentation

#### Failures

#### Google Sheets to PHP
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

#### PHP to Unity
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

#### Save System
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

## Art Documentation

## User Guide

## Postmortem
