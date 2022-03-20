
Writing a blog post is hard; writing a technical blog post with step-by-step instructions is even harder.

But writing step-by-step instructions in a community blog, where many authors -- each with different voices and styles -- write in a consistent manner is practically impossible.

Unless, that is, if you have a style guide.

Follow these guidelines to help you create clear, easy-to-follow instructions, whether you're writing simple, single-step procedures or complex procedures that consist of multiple steps.

## Key concepts

- **People don't read, they scan:** make it easy for your audience to follow instructions by using **bullets**, **highlighting** important elements, adding **headings** and **screenshots** to help them.
- **Be accessible:** make sure that your instructions make sense to those who may have a visual, motility or cognitive impairment. Avoid instructions that require the audience to see, use a mouse, or be able to tell what is *above*, *below*, *right* and *left*, for example
- **Write for a global audience:** contrary to what some people might think, we don't all live in the Seattle area, speak English as a first language, or read text from left to right. Your perspective is only your own, and may not reflect your audience's perspective.

## Complex procedures

Complex instructions often consist of multiple steps formatted as a numbered list. For multiple-step procedures in numbered lists:

- Format procedures consistently so readers can find them easily by scanning.
- Use heading to help readers find instructions quickly. Use the heading to tell readers what the instructions will help them do.  

    **Examples**  

    > ### To add an account  
    >
    > or
    >
    >### Add an account

    Choose one phrasing style for the headings, and write them all the same way (in parallel structure).
- Use a separate numbered entry for each step. It's OK to combine short steps that occur in the same place in the UI.
- Use the numbered sequence Markdown syntax:

    ```markdown
    1. Label every step as step one
    1. That way, you don't have to renumber them all if you move steps around
    1. Or add or remove steps
    ```

    which will be rendered as follows:

    > 1. Label every step as step one
    > 1. That way, you don't have to renumber them all if you move steps around
    > 1. Or add or remove steps

- Most of the time, include actions that finalize a step, such as OK or Apply buttons; Don't assume your readers know to **Save** or select **OK**.
- Use complete sentences.
- Use [imperative verb forms](https://docs.microsoft.com/style-guide/grammar/verbs) (e.g. **Select this**, **To do *x***). In instructions, tell your audience what to do.

- Use consistent sentence structures. For example, always use a phrase when you need to tell the reader where to start. The rest of the time, start each sentence with a verb.  

    **Examples**  
    > On the ribbon, go to the **Design** tab.  
    > Open Photos.  
    > For **Alignment**, choose **Left**.

- Capitalize the first word in each step.

- Use a period after each step.  

    **Exception**  
    When instructing readers to type input that doesn't include end punctuation, don’t use a period. Try to format the text so that the user input appears on a new line.

- Limit a procedure to seven steps, and preferably fewer. Try to fit all the steps on the same screen.
  
    **Examples**

    > ### To remove API access
    >
    > 1. In the **API access**, select the permission you wish to remove.
    > 1. From the toolbar, select **Remove access**. When prompted to confirm, select **Remove**.

## Single-step procedures

If you're using a consistent format for step-by-step instructions, use the same format for single-step instructions, but replace the number with a bullet.  

**Example**

> ### To play an app
>
> - Select an app and select **Play** from the toolbar or the context menu.

## Tips for writing steps

Make sure the reader knows where the action should take place before you describe the action.

- If the instruction appears in the same UI where the action occurs, it’s usually not necessary to provide location details.
- If you need to make sure the reader begins in the right place, provide a brief phrase at the beginning of the step.  

    **Example**  
    > On the **Design** tab, select **Header Row**.

- If there’s a chance of confusion, provide an introductory step.  

    **Example**  
    > On the ribbon, go to the **Design** tab.

## Simple instructions with right angle brackets

Abbreviate simple sequences by using right angle brackets. Include a space before and after each bracket, and don't make the brackets bold.

**Example**

> Select **Accounts** > **Other accounts** > **Add an account**.


### Accessibility tip

Screen readers may skip over brackets and read instructions such as **Menu** > **Go To** > **Folders** as *Menu Go To Folders,* which might confuse readers. Please take this into consideration when writing your instructions.

---
This document is based on [the Microsoft style guide](https://docs.microsoft.com/style-guide/procedures-instructions/writing-step-by-step-instructions)
