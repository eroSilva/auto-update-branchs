# Action to auto update branches

This workflow uses [actions/checkout@v2](https://github.com/actions/checkout) to update some branch when `main` receives new updates.


## How it works?

To validade action, we deploy two environments using [Netlify](https://www.netlify.com/), with `main` and `dev` branches.

**Main**  
https://auto-update-branches-prod.netlify.app/

**Dev**  
https://auto-update-branches-dev.netlify.app/

Always `main` branch is updated, a new branch `dev` will be genereted, based on `main` and pushed it to origin. This way, we guarantee that both environments will be updated, with the same code, automatically.


## Nice! I wanna test it. How can I do it?

Let's do it!  

First, open a new pull request, changing something in `index.html`.
![image](https://user-images.githubusercontent.com/9220300/116916125-4b2ceb80-ac23-11eb-9f11-eeee628f43fc.png)

Now, request a review from [@eroSilva](https://github.com/eroSilva).

When he approves your pull request, merge it. The both environments should be updated when deploy finished.

![Screen-Recording-2021-05-03-at-15 32 33](https://user-images.githubusercontent.com/9220300/116918058-d27b5e80-ac25-11eb-8d9a-1c8fe91bb996.gif)