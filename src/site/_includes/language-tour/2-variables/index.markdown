Here's an example of creating a variable and assigning a value to it:

{% highlight dart %}
var name = 'Bob';
{% endhighlight %}

Variables are references. The variable named `name` contains a reference
to a String object with a value of "Bob".

#### Default value

Uninitialized variables have an initial value of `null`. This includes numbers,
which are also objects.

{% highlight dart %}
int lineCount;
assert(lineCount == null); // Variables (even numbers) are initially null.
{% endhighlight %}

#### Optional types

You have the option of adding static types to your variable declarations:

{% highlight dart %}
String name = 'Bob';
{% endhighlight %}

Adding types is a way to clearly express your intent.
Tools like compilers and editors can use these types to
help you, by providing early warnings for bugs and code completion.

<aside markdown="1">
  <div class="alert alert-info">
    <strong>Note:</strong>
    This chapter follows the
    <a href="/articles/style-guide/#type-annotations">style guide recommendation</a>
    of using <strong>var</strong>, rather than type annotations, for local variables.
  </div>
</aside>

#### final

If you never intend to change a variable, use `final` instead of var or in
addition to a type. Once a `final` variable is set, it can't be changed.

{% highlight dart %}
final name = 'Bob'; // Or: final String name = 'Bob';
name = 'Alice';     // ERROR
{% endhighlight %}

#### Summary

Although Dart variables are optionally typed,
we generally recommend using types
because they make your intent clear.
Variables can be marked as `final`, locking the value. Uninitialized variables
have an initial value of `null`.
