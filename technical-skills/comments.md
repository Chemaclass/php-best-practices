[Back to technical skills](../technical-skills)

# Comments

When we think about comments in code, we have in mind comments that explain what code is doing. The problem with comments is that they are not always updated. Very often the code is changed but the old comments remain the same. So, the comments don’t reflect the code anymore.

In time, code is moved from one location to another, it is refactored, split, and moved. Even if the code location is changed, the old comments remain in the same location. In time, we end up with comments that don’t reflect reality and the code around them.

The hardest thing to do is to educate developers and make them understand that comments are part of the code. And, the moment the code is changed, the same thing should happen with the comments. But because of time pressure or indifference, we end up with outdated comments that don’t reflect reality anymore.

We need to think of comments like documentation. It is an expensive artifact that needs to be maintained. Because of this we should add comments only in location where it is necessary and code itself cannot express what is happening there.

## Bad example of comments

### Ugly code
Often comments are used in locations where code is ugly, and they are used to ‘fix’ the code. Don’t try to make a code more beautiful by adding comments. When you have an ugly code you should refactor it and write it in a way that expresses what you are doing there.

### Code explanation
When you have a code that cannot be understood, then comments are not the solution. Try to rewrite the code or rename fields and other elements in a way that the reader will understand the action that you are doing there.

In many cases, you can extract a method with a mindful name. The reader will understand very easily what is happening there based on the methods and fields name.

### Mumbling
Adding comments into the code only because you think that is necessary is a bad thing. Often it happens that somebody adds comments in code only because he thinks that it is good, without a real background. In the end we end up with a lot of comments that are not useful and make code more difficult to read and understand.

### Redundant
When you have a good name for your field or method, you no longer need a comment that describes what the scope of that field or method is. For example a method that is named “SendEmail” doesn’t need any additional comments when it is called. It is clear from the name of the method that an email is send.

Another good example is a field called ‘vatValueForCurrentOrder’. From the name of the field it is pretty clear what value is stored in this field. You don’t need a comment that says “The value for the current order is stored”. The comment in this case doesn’t add valuable information.

### Misleading, Mandated and Noise
In many cases, developers don’t express what they intended to do. Because of this you can end up with a comment that says that an email is sent to the customer, but you end up debugging and trying to understand why the email is not sent.

In the end you realize that the method that is called under that comment doesn’t send an email, only constructs the email object.

Usually in big companies and projects you end up with rules that require each method and class to have comments. You end up with a lot of comments that don’t add a real value. They are added by developers only because it is required. For example a property called “Id” had the following comment “Gets, sets the id of the current object”. No useful information is added by this comment, only additional 3 lines of comments that pollute the code.

What about commenting a constructor – “Construct an instance of object Foo”. Come on, it is clear what the scope of a constructor is. In general, constructors should never be commented.

### Journal
30 years ago, when source control wasn't used on every project maybe it was a good idea to write in the code the journal of code changes (when, what, why, who – changed the code). But now, with source control and other tracking mechanisms, there is no point to do this.

Using a source control system you can see and track all the changes that happen on the code.

Position markers

Try to avoid using position markers into your code. For example adding `/////////` into the code to find more easily a specific part of the code.

## Good example of comments

Yes, there are cases when comments are useful and can add value to our code.

### Legal and Informative
There are cases when you need to add a comment because of the legal reason. The code can be under specific license terms and this needs to be specified. In this case you should add a comment that specifies this thing, but without adding all the license terms to it. You can point from the comment to a specific document or url link that describes the license terms. You don’t want to have 200 lines of comments with this information.

There are cases when a comment can add value to a code. For example when we give more information about what is returned by a method. Be careful, there are cases when a good name of a method can remove the necessity of comments related to return value.

###  Intention and Clarification
A comment is always useful to express an intention. It is not important to comment what we have done in the code, because the reader can see the code itself. It is more important to explain what we wanted to do in the code.

There are cases when we cannot express exactly what our intention is. Because of this we need to add comments that add more clarification and explain why we didn't take a specific action. Maybe there is a bug in an external library that we had to avoid, or the client had an odd request.

### Amplification and Warning
There are times when we know that some lines of code are very important, and without them the application could crash, for example. In these cases, comments could warn other developers about the importance of those lines of code.

A good example is a mutex variable that is used to access a shared resource. Maybe not all developers would understand the importance of that mutex, and a warning is needed.

### API Documentation
All public API intended to be used by external clients and developers should be documented very well. Since they will not be able to see the implementation, the naming of different functions and classes in combination with comments should express very clear what the purpose of each method is and how it should be called.

## References

### Books

* **Clean Code** ([Amazon](https://www.amazon.de/-/en/dp/0132350882/)) [English] by Robert C. Martin

### Other links

 * [Todaysoftmag](https://www.todaysoftmag.com/article/1120/clean-code-comments-and-formatting) about comments
