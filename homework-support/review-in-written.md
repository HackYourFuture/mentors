##  Review process

1. When a new pull request comes in, add the GitHub label `homeworkN` (where `N` is 1, 2 or 3) and the label `to review` to the pull request.

2. Open your local (cloned) version of the module's HYF repository, say **JavaScript3** in VSCode (make sure that you run `npm install` after cloning).

3. Click on the GitHub Pull Request icon in the VSCode task bar and expand the **All** option. As shown in the picture below, you will see a list of the most recent Pull Requests for this repository.

4. Right-click on the pull request you want to review and select the **Checkout Pull Request** menu option. This will create a local branch in the local repository, e.g. `pr/veliataseven/273` as shown in the VSCode status bar here:

5. While the VSCode Github Pull Request extension allows local commenting on the pull request, it's recommended to do it online, directly in GitHub. To open the pull request in GitHub right-click again on the pull request in VSCode and select **Open Pull Request in GitHub**.

6. On the GitHub pull request page assign yourself as Assignee, and change the label `to review` to `review in progress`. This to ensure that fellow mentors helping out with reviews do not start on the same pull request. 

7. Now switch to the regular code window in VSCode by clicking on the Explorer icon in the VSCode task bar and start the actual review.

   > If the student installed additional dependencies in `package.json` you will need to run `npm install` again. For the JavaScript modules this should not be necessary.

8. If there are any unit tests as part of the repository, run them and review the results.

9. Run the code (in Node for a CLI app or in the browser with the console open for an HTML app) to ensure that it at least runs without run-time errors.

10. Go through the code on GitHub and insert comments in the pull request. When making the first comment select **Start a Review**, instead of making single comments. Note that for each single comment GitHub sends out an email notification to all repository watchers. It will only send out a single notification for a complete review.

11. Because the JavaScript modules lay the foundation for much of the rest of the curriculum, I tend to comment a lot:

   - Naming: avoid generic names such as `data`, `item`, `element` if more descriptive names are possible; use plurals for arrays and a corresponding singular for an element of that array; avoid cryptic or ambiguous abbreviations; verb-based names for functions, noun-based names for variables and parameters etc.
   - No nested named functions, pass all required data through the parameter list.
   - In general I try to bring across best practice programming style, and give the rationale for doing things in a particular way.

12. Point out fragments of code that do not work, or do not meet the requirements of the assignment. Students need to follow-up on these comments before their pull request can be approved.

13. Make recommendations on how things can be done better, more elegant, more efficient, etc. However don't consider these showstoppers for approving the pull request.

    > Before suggesting a non-trivial coding alternative to students, I try it out by modifying the code in the current branch and running it. When I'm satisfied I copy the relevant code snippet in a comment on GitHub and discard the local changes using the VSCode **Discard Changes** option.

14. When done select **Review changes** in the pull request, add an overall assessment in the comment box and either **Approve** or **Request changes**.

15. Finally, remove the label `review in progress` and either add the label `reviewed` in case the pull request was approved, or `needs work` if I requested changes.

16. Maybe the most important step: after the student implemented your feedback, check if their improvements are sufficient and if so, remove `needs work` and add the label`reviewed`
