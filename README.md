# Regular Expressions
regular expressions is a way to search through a string of text in order to do things such as validation or get certain pieces of the text and more in an advanced way.

# Email validation
This regular expression matches any email

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

# Table of Contents

- [Email Validation](#email)
- [Validation In JavaScript](#validation)

# Email Validation
The regex is delimited with word boundaries, making it able to extract email addresses from large blocks of text

It looks for any combination of upper and lowercase letter and numbers and a few special characters

This is then followed with an @ symbol which will then follow the TLD after this

Few rules include that a special character cannot appear as the first or last character of the email address or be repeated.

# Validation in Java Script

function ValidateEmail(inputText)
{
	var mailformat = /^[a-zA-Z0-9.!#$%&’*+/=?^_`{|}~-]+@[a-zA-Z0-9-]+(?:\.[a-zA-Z0-9-]+)*$/
	if(inputText.value.match(mailformat))
	{
		alert("This is not a valid email address");
		return false;
		}
}
