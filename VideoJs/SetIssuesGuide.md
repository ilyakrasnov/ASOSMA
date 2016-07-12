## Step 1: Search for duplicate issues

    if a duplicate issue is found
        --> label `duplicate`
        --> reference the duplicate issue (e.g. "This appears to be a duplicate. See #123")
        --> close this issue

## Step 2: What kind of issue is it?

### Case: Pull request

    --> say "Thank you! This will be reviewed by other contributors as soon as possible. 
        Please be sure all tests are passing in all targeted browsers (IE8+)."

We have a separate process for managing pull requests.

### Case: Non-core project related
Common non-core issues include:
[Plugins](https://github.com/videojs/video.js/wiki/Plugins), 
[Flash Player](https://github.com/videojs/video-js-swf), 
[Videojs.com Website](https://github.com/videojs/videojs.com)

    --> ask them to submit an issue on the specific project  
    --> close issue

### Case: Feature/Enhancement Request

    if it's already supported through the core or a plugin
        --> link to the docs, source code, or plugin
        --> close the issue
    else if the use case is not as clear as possible
        --> label `needs: more info`
        --> ask for more info about the use case and examples if relevant
    else
        --> label `feature`
        --> ping any contributors you think should weigh in
        if it's covered in or related to the HTML5 video spec (link below)
            --> link to the related part of the spec

See [HTML5 Video spec](http://www.whatwg.org/specs/web-apps/current-work/multipage/the-video-element.html)

### Case: Bug Report
    --> Respond with bug report first response (see below)
    if any specific info is needed and missing
        --> label `needs: more info`
        --> ask for them to fill in any missing details
    if it can be verified
        --> label `bug`
        --> say "I can confirm this" (or something like it)
        --> link to your own example if available
    if there is any other relevant info
        --> link to it, mention it

[Bug report first response](#wiki-bug-report-first-response)

### Case: Question (general)

    --> search for any answered duplicate StackOverflow questions (search link below)
    if an answered question is found
        --> label `duplicate`
        --> link to the answer (click "share" in the answer to get a link)
        --> close the issue
    else
        --> label `question`
        if you can answer the question *quickly*
            --> answer it
            --> close the issue
        else if more info is needed
            --> label `needs: more info`
            --> ask for the info that's needed
        else
            --> label 'needs: addressing'
            if you can answer it but not quickly
                --> say 'I've read this but it's going to take more time to answer'
            else if you need help from someone
                --> say 'Need help with this one'
                --> ping any contributors you think my be able to answer
        if the question seems user-specific
            --> close the issue

See [answered StackOverflow Video.js questions](http://stackoverflow.com/search?q=%5Bvideo.js%5D+answers%3A1)

[StackOverflow](http://stackoverflow.com/questions/tagged/video.js) is better for questions, but it's fine if they're asked in the issues. We're just more liberal about closing question issues sooner so they don't clutter the issue list. All watchers will still get emails for closed question responses.

## Boilerplates

### Closing a general question:

```
> ### Why was this closed?

> This issue was closed because it does't require any direct changes to Video.js core. The conversation can continue, but I need to close this to keep the open issue list focused on development.

> This question may be better fit for [Stack Overflow](http://stackoverflow.com/questions/tagged/video.js) or IRC (#videojs), where you're most likely to get a quick response. If you do post to Stack Overflow or if a post already exists, please link to it here.

> Cheers!  
> @heff
```

### Bug report first response

```
> ### What's next?

> Thanks for submitting a bug report! Another contributor will address this as soon as possible. In the mean time, please make sure the following details are available.

> What did you do? (steps to reproduce)  
> What happened? (actual results)  
> What should have happened? (expected results)  
> What version of Video.js, and any plugins used?  
> What browsers and platforms does this occur/not occur on?  
> Is there a link to an example online?  
> Can a reduced test case be created? (e.g. [a jsbin](http://jsbin.com/axedog/9999/edit) or [JSFiddle (if Flash is involved)](http://jsfiddle.net/heff/zzXfb/)) 
```

### Feature request first response

```
> ### What's next?

> Thanks for submitting a feature request! Another contributor will address this as soon as possible. In the mean time, please make sure the following details are available.

> - Describe the feature/enhancement (please be as detailed as possible so it's clear who, why, and how it would be used).
> - Are there any existing documentation/specs?
> - Are there any existing examples?
```

### Pull request first response

<pre>
> ### What's next?

> Thanks for the contribution! A core member will review this as soon as possible. In the mean time, please make sure any related issues have been mentioned. 

> The following checklist can be added to the pull request description to track progress through the requirements.

```
### To finish
- [ ] Change confirmed (issue # or reviewer:___)
- [ ] Tests written  
- [ ] Feature implemented  
- [ ] Example created (e.g. [jsbin](http://jsbin.com/axedog/9999/edit))  
- [ ] Docs/guides updated  
```
</pre>
