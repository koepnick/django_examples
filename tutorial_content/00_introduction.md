# Introduction

Hi!

This tutorial is going to follow my own personal preferences for project development and deployment. 

Generally, it's:

![](images/00_workflow.png)

## Assumptions

For the sake of our collective sanity, let’s go over some basic project assumptions:

There will be a project root **and** and Django root. The project root is the base of this repository, the Django root is a subdirectory named for the Django application.

If that seems redundant, you are not alone.

So pick a spot on your filesystem. Create a directory. If you’re feeling bold you can even initialize a Git repository there. Henceforth, that directory will be referred to as: `${PROJECT_ROOT}`. The Django application that we’ll be building soon will be in a subdirectory to be known as `${DJANGO_ROOT}`.

## Build Environment

So now we’re nice and comfortable in our `${PROJECT_ROOT}` directory. But it’s dreadfully empty.

And we all know that we should never, **ever** let our project libraries commingle with our operating system libraries. So choose one of:

1) You’re feeling pragmatic and want to use what is generally seen as the simplest solution: `virtualenv --prompt='.:: Pantry Manager ::.' -p python3 .environment`¹ ²
   * This uses `pip` and create a new subdirectory named `.environment` to house the dependencies that you’ll be needing.

2) You like new things and are willing to dive into the documentation for projects that may have less presence on Stack Exchange: `poetry new 'Pantry-Manager'`
    * Poetry is my new favorite package manager, but it still hasn’t reached critical mass. This is what I use for my own projects.

3) You value speed and sanity over bleeding-edge packages: `conda create -n 'Pantry Manager'`
    * It’s Conda. Their package solution finder is smarter than most people I know.

> Note: I’m intentionally not going over any further details because any Pythonista following along should *already* be familiar with whichever package manager they prefer.

I’ll be using Option #1 from here on out. Primarily for the sake of the majority who already know it. But also because it is the most generic
and it’s easier to take instructions meant for it and fiddle with them to get analogs in Poetry and Conda.

For those who chose Option #1, you can do a sanity check by running: 

```
$> source .enviornment/bin/activate
.:: Pantry Manager ::.

.:: Pantry Manager::. $> which python
/path/to/your/project/.environment/bin/python
```


**Every** command and installation in the rest of this document will assume that you’re properly in your development environment!

# :warning: READ THIS :warning:

I **cannot** emphasize this enough: Installing arbitrary packages into your operating system’s Python environment will end in tears. Using, for example, `pip install --user blahblahblah` is tolerable for some multipurpose libraries. Using `sudo pip install blahblahblah` will make you question your life decisions.³

---

¹ If using a rolling release distribution (like Arch, Manjaro, etc.), it is very important to ensure that your base Python binary is stable. My preference is to download and compile a specific Python binary to `/opt/python/3.x` and use that for virtual environments. 

² The `-p` option is a purely cosemetic quality-of-life enhancer to show when you're operating within a virtual environment

³ Your operating systme may expect specific versions of various Python libraries. By using `sudo` and forcefully overwriting those libraries, the operating system may be unable to update or perform other seemingly mundane tasks.
