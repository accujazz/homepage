---
title: "Making group competition flow x100 more simple and efficient"
date: 2021-01-16T16:57:54+03:00
---

Our team was working on a tournament platform for competitive video games. The players could browse tournaments for the games they play, find what they like, register to play and record scores. The app helped to manage tournament participants, score recording, pair competitors against each other and determined which players would advance to the next stages based on a set of tournament rules.

The player could join a tournament either as individual competitor or as part of the team. We had a pretty complex flow for team tournaments and quickly saw in the session recordings that it wasn't working. For some users it could take for up to 30(!) minutes to join the tournament. 

And no surprise why if we list all the steps our imaginary player Mike would need to complete in order to register for a team competition:

- Mike lands on a tournament page with an intent to join a team tournament
- First he needs to create an account filling all the required fields
- Then Mike clicks on "Join" button again only to find out that he needs to have a team, cause only team owners can join team tournaments
- This is not a given but let's for a moment assume that Mike regularly plays his favourite game with his friends as part of the same team
- Thankfully there is a "Create new team" button in the message. 
- Mike clicks it and is presented with a form that asks Mike to come up with team name, upload a team avatar, write something in the description, select team size. Not all the fields are required. But still a lot of work. Arghhh!
- After the team is created Mike needs to invite his friends to it. He can send invites via email or just copy an invite link and send it to his friends.
- Mike tries again to join the tournament but he still can't. Tournament requires the teams of 4 people in size and Mike's friends haven't yet responded to his invitation.
- Mike pings his mates in chat, waits till they sign up for the site and join his team. He refreshes the team members page to check if all the members are in.
- Finally Mike returns to the tournament page clicks Join and is able to register for the competition.

Honestly, what an embarrassing experience! This must be fixed. 

Thankfully we have a group events pattern that after the pandemic experience of 2020 is familiar and used by millions of people. We spend our days in group video calls and not all of them have a built in contact list. This is especially relevant for new products cause your friends are not there. But it is still pretty easy to organize a meeting. You create a new call, copy the invite link and send it the way you like. Everybody who has a link can join. New meeting with another group of people? Simple. New invite link.

There is nothing stopping team tournaments to work the same way and Mike's flow would simplify drastically:

- Mike sign ups for the service
- Mike clicks to join the team tournament. It doesn't matter if he already has a team or not.
- Mike receives an invite-link and sends it to his friends.
- When enough players sign up and join with this link the team is formed and can play in a competition.
- Every player has a history of who he played with and can join future tournaments selecting one of the previous groups or by grabbing an invite link.

![Tournament team flow](/img/posts/tournament-team-flow.png)

We have simplified the user flow increasing the conversion to tournament participations, got rid of unnecessary entities and screens that were needed to support the "Team" model and reduced the codebase making it easier to support and add new features.

In retrospect the solution seems obvious and simple but simplicity is never a given, it takes work to achieve. People tend to overthink and overcomplicate things.