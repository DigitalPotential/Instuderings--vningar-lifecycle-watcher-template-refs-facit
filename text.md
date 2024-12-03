Lifecycle Hooks
3:25:02
first of all I want you to grab a cup of coffee because I'm going to be showing you a lot of slides right here okay so
3:25:08
trust me it's not that much difficult topic but it has a lot of missing pieces and everything is just floating around
3:25:15
so what in the word is a life cycle Hooks and why you should care about that so life cycle hooks are a special
3:25:20
methods provided by wujs that allow you to execute code at a different stages of
3:25:25
a compounded life cycle these hooks provide developer with the ability to perform action or respond to events at a
3:25:32
specific point during the creation updating destruction of a view component
3:25:37
so before we jump into what actually are a life cycle hooks first of all we we have to learn about these two concept
3:25:43
which is called the mounting and unmounting or Mount or unmount so what is a mounting or Mount and why should
3:25:50
care about that so mounting means when a component is being created and inserted into the Dom and unmounting means when a
3:25:57
component is being removed from the Dom okay so I want you to just keep that in mind and now let's begin our journey
3:26:04
with a lot of slides so yeah first of all we are going to be talking about the on before life
3:26:10
cycle hooks so it just a hook to be called right before the component is being mounted so what is a mounted when
3:26:17
a component is created and inserted to the Dom so when this component is called the component has finished setting up
3:26:24
its reactive state but no Dom nodes have been created yet and it is about to execute the Dom render effect for the
3:26:30
first time so that was the first one now the next one we have is the on mounted I want you to keep in mind this teed
3:26:37
because we have another concept you know what I'm just getting a sid track so so now I want you to just keep in mind that
3:26:43
the next one we have is a on mounted with teed so on mounted is used for executing logic or action after the
3:26:50
component has been mounted to the Dom this Hook is particularly useful for test that should occur when the
3:26:57
component is ready to interact with the user such as fetching the data setting up a listener or performing initial
3:27:03
calculations okay the next one we have is a on before update and it registered the hook to be called right before the
3:27:09
component is about to update his D Tree due to the reactive State changes and this hook can be used to access the Dome
3:27:15
State before the view updates the Dome and it is also safe to modify a component State inside this hook okay so
3:27:22
yeah you can even take a screenshot of that because I know that will not stick to your brain sometime if I'm working with a
3:27:29
view app and I want to do something so I do search a lot about these uh life cycle hooks so yeah that's totally
3:27:35
normal if you are not getting it at first time so the next one we have is on updated this one well come on this one
3:27:42
is on before update and this one is on updated right here so on updated register call back to be called after
3:27:48
the component has updated the Dom tree due to the reactive State changes and
3:27:53
this Hook is called after any Dom updates of the component which can be caused by different state changes
3:28:00
because multiple State changes can be bed into a single render cycle for performance reasons the next one we have
3:28:06
is a on before unmounted okay so now we are talking about the deleting stuff so Reg ex ra hook to be called right before
3:28:13
a component instance is to be unmounted like removed so when this Hook is called
3:28:18
the component instance is still fully functional okay the next one we have is unmounted right here and register a call
3:28:24
back to be called after the component has been unmounted use this hook to clean up manually created side effect
3:28:31
such as the timers Dom event listeners or Server Connection okay so yeah that was a huge list of life cycle Hooks and
3:28:39
now let's just write some sort of a code then you'll get get to know what I'm talking about so for this example I already created this component which is
3:28:44
a life cycle component and I already imported that and I just render that right here and I don't have anything
3:28:50
special inside there but I just only have this H1 right here so now let's just start working with our life cycle
3:28:56
hooks right here okay so what I'm going to do is that I'm going to be importing a lot of stuff from my VJs so what are
3:29:02
the things I would need right here so the first thing which I would do is that I'm going to be getting the Riff then the on before Mount then the on Mount t
3:29:11
then we would also need the on before update not mounted but update right here
3:29:18
and we will also need the on updated right here and also the on before
3:29:23
unmounted and finally we're going to be importing this un like on unmounted right here so if I sve my file so it's
3:29:29
going to Auto format there right here and now what I'm going to do is that I'm going to just create one message right
3:29:35
here is going to be equals to empty string or you know not empty string but hello uh we would be fine right here
3:29:42
okay so what I'm going to do is that I'm going to just remove this H1 from here and I'm going to just write a paragraph
3:29:48
tag right here and I'm going to just render my message and now if I save my file so here you can see we are now
3:29:53
getting where hello View and also I'm going to be just creating a button and which will just say like update the
3:29:58
message right here so if I save my file and here you can see we have this update message button and everything is working
3:30:05
a okay so I'm going to just right click on that and go to my console and now let's just start using all of these HS
3:30:11
right here and trust me we have like a lot more hooks than that but in this specific section we're going to be just
3:30:17
learning about these okay so yeah now let's just start working with that so the first thing which I want to do is
3:30:22
that I want to start from the life cycle hooks Right Here and Now what I'm going
3:30:28
to do is that I'm going to be starting from the first one which will be on before Mount R here and it's going to
3:30:33
take the Callback function I mean like all of that life cycle will take a callback function so now in this case I'm going to be just logging to the
3:30:40
console like comp component is about and here is the keyword about right here
3:30:46
about to be mounted right here so now if i s my file and here you can see if I just refreshed it so it's going to gives
3:30:52
us that component is about to be mounted right here okay so it is not already
3:30:58
mounted but it is about to be mounted so it's going to gives us that uh message right here so now the next life cycle
3:31:04
hook which we are going to be using is this on mounted and here we are going to be also passing this Arrow function and
3:31:10
we are going to be just writing where console. log it's going to say like component component has been mounted
3:31:16
right here so here the keyword is has been mounted so if I sell my file and I
3:31:22
don't know okay that's because of that errors so now if I sell my file and now if I refresh that so here you can see
3:31:28
it's going to first of all gives us this message right here like component is about to be mounted and then it's going
3:31:33
to gives us that component has been mounted so what if I change the order of that so if I cut that from here and if I
3:31:40
put right here at the top and I put this second one at the bottom so what do you think will be the result of that so if I
3:31:46
save my file and it refreshed that so here you can see the result will be totally the same so it's going to give
3:31:52
us like component is about to be mounted which is this second one right here because it's not going to wait for a
3:31:58
component to be mounted it's going to gives us that result first and then when the component successfully mounted then
3:32:04
it's going to gives us the result of this unmounted right here so I'm going to just cut that from here and now let me just put that right here back so now
3:32:11
if I save that and that was supremely easy like this one is not going to wait for a component to be mounted it's going
3:32:17
to giv us every single thing which you write right here before even the component mounted and then when the
3:32:23
component successfully mounted so I mean like when the component successfully render to the Dom so then it's going to
3:32:28
gives a St result Right Here and Now underneath that we're going to be working with the on
3:32:33
before um what do we call it on before mounted word or not mounted on before
3:32:38
updated right here so I'm going to just loog to the Al that component is about to update about to update right here
3:32:47
okay so it is not already updated but it is about to be updated so for this hook to work first of all we're going to have
3:32:53
to provide some sort of updation or yeah we have to update something then this H is going to be working so what I'm going
3:32:59
to do is there I'm going to just uh attach the event handler right here so I'm going to just say when somebody clicks on there so we're going to be
3:33:05
calling this function which is update message function now let me just copy there and now let me just create that right here here so C update message and
3:33:13
this is going to be the arrow function and we're not going to be doing anything crazy but we are going to be getting that message which we've created right
3:33:19
here above which is just saying like hello view we are now getting the value of that and we are just uh changing that
3:33:24
to something else like updated miss m a s a g e yeah or no not M A but m e s a g
3:33:33
e okay so now if i s my file and here you can see we have the button right here so first of all it's going to gives
3:33:38
us this result right here like component is about to be mounted then component has been mounted but now if I click on
3:33:45
this button so here you can see that content will be updated successfully right here and it's going to also gives us that component is about to be mounted
3:33:52
or about to mount right here so it's not going to wait for a component to be mounted so it's going to give us all of
3:33:58
their result when the component is about to be mounted and now the next one we
3:34:03
have is when the component successfully update so we are going to be using that on update and here we are going to be
3:34:10
passing call function right here so if I just write like cons log and component
3:34:15
has been um yeah has been updated there we go so now if I sell my file and now
3:34:21
if I refresh it right here so Watch What Happens so if I click on this button right here so it's going to gives us
3:34:27
that two results right here the first one will say that component is about to update I did I just say mounted I meant
3:34:34
update I don't know what I said but anyways you get the idea so component is about to update and here we are going to
3:34:41
be getting that component has successfully updated right here in this case so this one is not going to wait
3:34:46
for a component to be update so it's going to give us all of the logic which we're going to be putting right here
3:34:51
okay so I'm going to cut that from here let me just put that at the bottom so that you can see all of the life cycle
3:34:56
hooks so this one is not going to wait for a component to be updated and this one is wa for a component to be
3:35:02
successfully updated and then it's going to give us the result which we put right here inside this unupdated life cycle
3:35:07
hook right here so the final two we have is the on before unmount and we have the on unmounted right here so to give you
3:35:15
the example of that we're going to have to destroy something inside our component so we cannot destroy something
3:35:20
right here but we're going to have to put some conditional statement for that so the first thing which I want to do is
3:35:25
that I'm going to just write like on before unmount right here and inside that I'm going to be just logging to the
3:35:31
console that component is about to be unmounted right here okay so now I'm
3:35:38
going to save my file and now if I refresh then nothing is going to happen so for that I'm going to have to go to
3:35:44
my fjs right here and I'm going to have to write some sort of a logic right here so I'm going to first of all get my refi
3:35:50
and I'm going to just get there from The View and now let me just try like show hide or something like that and here
3:35:56
inside this RI I'm going to be passing the true and now and now I'm going to be passing this component conditionally so
3:36:03
I'm going to just say like we if and here I'm going to be passing this show hide right here okay so show hide and
3:36:09
now we are going to be just generating some button and it's going to say that uh I don't know come on show/hide and
3:36:16
here we're going to be passing when somebody clicks on this button so what do you want to do we just want to show
3:36:21
hide and now it's going to be equals to not show hide right here so now if I save my file and now if I refresh that
3:36:28
so here you can see we have this show hide button right here so anytime I click on this button so it's going to
3:36:33
hide the UI I mean like it's going to totally remove that component from here and it's going to gives us that
3:36:39
component is a about to be unmounted and you already guessed it that we use unmounted when the component is
3:36:46
destroyed okay so now let me just show you there let me just go ahead and refresh there I'm going to go to my elements Tab and here you can see we
3:36:52
have this hello VI right here and in this case we're using the V if right here if you were using the V show this
3:36:58
will not work right here so you know let me just show you there so here you can see we have this hello view right here
3:37:04
but if I click on this button and here you can see that hello view is totally gone from this UI on the other hand if I
3:37:11
were using the V show right here so if I save there and refresh and now you know what let me just God damn it let me just
3:37:18
click on that and here you can see we have this VI I like we have this hello view right here but now if I click on
3:37:25
that nothing is happening right here but if I go to my console we are now getting just the component has been updated but
3:37:32
we are not getting the result of uh component has been unmounted right here okay so also keep that in mind so I'm
3:37:39
going to just change that to VF right here save my file and now let me just talk to you about the final life cycle
3:37:45
hook right here which will be the on unmounted right here so when the component is successfully removed from
3:37:51
the Dom so for that we're going to be just showing to the user like component uh component has been unmounted right
3:37:58
here so if I save my file and now if I refresh that and here you can see first of all it's going to give us these two
3:38:03
results and now if I click on that so first of all it's going to gives us that component is about to be unmounted and
3:38:09
then it's going to gives us that component has been mounted right here okay so yeah that was all of the life
3:38:15
cycle hooks which I wanted to show you right here and trust me there are a lot more and you're not going to be using
3:38:21
them that often so that's why I did not include them in this list so yeah that was it about a life cycle hooks in VJs
Watchers
3:38:29
so now let's talk about a Watchers in VJs so what in the world are Watchers and why you should care about that so
3:38:34
Watcher or Watchers allow us to reactively watch for a changes in the specific property or expression and
3:38:41
perform some custom logic when the property or expression changes so Watchers are a part of a ugs reactivity
3:38:48
system which enables the framework to automatically update the Dom when the underline data changes okay so that was
3:38:54
just a actual definition of what a Watchers is and now how the syntax of a watcher is going to be looking like this
3:39:01
is how the syntax of a watcher looks like so first of all we would have word Watchers method uh which we are going to
3:39:06
be importing manually from the VJs and then we are going to be providing The Source then the Callback function and
3:39:12
this one is optional but yeah if you care about this so you can read the documentation about that because I'm not going to be showing you this one so how
3:39:19
that's going to look like like what in the word is a source so you can provide the ref you can provide the reactive
3:39:25
object you can also specify the array or you can even specify the getter function I'm not going to go into that much
3:39:31
craziness but I'm going to just show you how you're going to be working with a few of them then the next one we have is
3:39:37
a cak function and so the C function is called when whenever some data changes right here so it's going to give us
3:39:43
access to the new value it's going to also gives us access to the previous value or you can say the older value
3:39:48
right here which I'm going to show you in action in a few seconds and then the final one this is totally optional but
3:39:54
if you care about that you can go to your documentation and you can learn more about that because I'm not going to be showing you this one right here so it
3:40:00
also supports the immediate deep flush and on track and on trigger right here
3:40:06
something which you will not use that much but yeah these are some like awful
3:40:11
topics which I'm not going to be explaining in this course okay so now I'm going to go ahead and write some code then you'll get to know what I'm
3:40:17
talking about and now I'm going to just delete that stuff from this component
3:40:22
and I'm going to be also deleting these stuff from this component as well and now let me just rename this component
3:40:27
but before I do I'm going to have to remove this uh stuff from this fjs app component as well so first of all I'm
3:40:35
going to just give this component a name of like a basic component would be fine or basic Watcher I guess I'm going to
3:40:41
just stick with the basic component and now let me just import it right here inside uh this app right here this app
3:40:48
component so now let me just import there I'm going to be importing this component from let's just go ahead and
3:40:53
go to my components and go to the basic component yeah basic component and now let me just render that right here so
3:40:59
now I'm going to save that and here I'm going to have to write something so that I can see something right here so
3:41:04
something now let me just save my file and refresh that so it's going to gives us there something right here so I'm
3:41:10
going to just close this one out and now let's just work with the basic component of Watchers so like how in the word we
3:41:16
are going to be watching for the changes and all of that kind of stuff so the first thing which I want to do is that I want to provide some sort of a
3:41:22
reactivity so that we can watch for some changes okay so let me just zoom in a bit and I'm going to be importing two
3:41:28
things the first thing I'm going to be importing is a riff and the second one we are going to be importing is the Watcher or watch whatever you want to
3:41:35
call that and we're going to be importing that from the VJs and now let me just write a cons Miss message it's
3:41:40
going to be equals to the rep and I'm going to just say like hello comma View and now let's just also write an input
3:41:47
text right here it's going to be equals to the ref of totally empty string right here okay so now I'm going to go ahead
3:41:54
and remove this H1 and you know what I'm going to just write a div in this case and now let me just write H1 and now let
3:41:59
me just render my message right here and I'm going to be also providing the input field we don't need that types and stuff
3:42:05
but I'm going to also provide the view model right here and I'm going to just say that take um this input text right
3:42:12
here so anything we write inside there will be also shown inside this message right here which I'm going to show you in a few seconds and now here I'm going
3:42:19
to just say like placeholder and type something dot dot dot now let me just go back and here now if you sell our file
3:42:26
and here you can see we have our hello view right here and now let me just right click on then go to my inspect element and go to my console we don't
3:42:34
have nothing inside there and now let's just watch for a changes right here now let me just write a comment like watch
3:42:41
for changes uh in input text and update
3:42:46
message accordingly so how we are going to be using that we are going to be using this watch method which we are
3:42:52
already importing right here and the first thing which we have to do is that we have to provide the source and as I
3:42:58
said that you can provide the source as a ref you can provide the array you can provide the reactive object you can also
3:43:03
P the gor function but in this case I'm going to be passing the source as this input text right here so now let me just
3:43:09
P that and the next thing which I'm going to pass is this Arrow function you can create this function like separately
3:43:14
you can create it right here and then you can pass it here if you want it to but in my case I'm going to be using the
3:43:20
es6 and I'm going to just provide a new value first of all come on new value H
3:43:26
new value there we go and then the old value right here so you guys can see everything a bit better and now inside
3:43:32
there uh I'm going to just write a comment like you can perform some logic
3:43:37
here when input input text uh changes there we go so which kind of logic we
3:43:44
can perform I'm going to just write a message. value right here and I'm going to just say like you typed uh this
3:43:50
content right here which is a new value right here so now let me just write that I like now let me just save my file and
3:43:57
now let's just check it out and here you can see I have this input field if I start typing something like hell you
3:44:02
know something right here so here you can see it's going to give us that you type something right here which is
3:44:08
totally a okay but I'm also going to loog to the console my new value and also I'm going to loog to the console my
3:44:15
old value as well okay so now if I save my file and now if I refresh that and I'm going to just write a okay so if I
3:44:23
just write a so it is not giving us the older value I don't know why oh that's
3:44:28
because we have empty string right here but if I just write something like uh I don't know if I just write apple right
3:44:34
here send my file and refresh that so it's going to give us that Apple but if I just remove that so here you can can
3:44:39
see the older value was Apple and I just removed that from this input field so that's why we are now getting this empty
3:44:46
input field right here but if I type something like I don't know maybe D so here you can see this is the new value
3:44:52
and the older value is now totally removed right here so this is how we going to be using the Watcher for watch
3:44:58
for all of our changes and it's going to giv us the new value and also the older value as well so that was just a basic
3:45:05
example now I'm going to just remove that and now let me just give you one more example which will be the reactive
3:45:12
object. view right here in this case we're going to be passing the reactive object so I'm going to just go ahead and
3:45:18
comment this line out and I'm going to also comment this line out as well so you know what I'm going to copy all of that content and now let me just place
3:45:25
it right here and I'm going to just remove that and I just say like hello and now let me just remove that from
3:45:30
here and first of all we're going to have to import that component so import the reactive object and now let me just
3:45:37
copy that and render that right here inside or app so now if I save that and refresh that so here you can see we're
3:45:43
now getting this hello right here which is totally expected right here so the first thing which I want to do is that I
3:45:49
wanted to get a few things so I'm going to first of all get the reactive because in this case we're going to be working
3:45:55
with the reactive object okay so the next thing which I want to do is that I also wanted to get the watch so that we
3:46:00
can watch forward changes and we are going to be getting there from the VJs and now I'm going to just create my
3:46:06
initial State word here so I'm going to just give a name of like St and here we going to be creating our reactive uh I
3:46:11
mean like we are going to be providing a value for our reactive which will be a username and currently I'm going to be passing my Alex uh brother I'm going to
3:46:20
faing this Alex person right here okay so now I'm going to just remove that oh you know let me just create that and I'm
3:46:26
going to be just getting St down username right here and now let me just create a button and it's going to just
3:46:32
say like change name right here so if I save that and here you can see we have this Alex right here and we also have
3:46:38
this button so everything thing is totally working a okay but what I want to do is that I want to just change this
3:46:45
name right here so so I'm going to just write a click event handler right here and it is going to just say state.
3:46:51
change or you know not change name but username and it's going to be equals to Jordan right here so if I save that and
3:46:57
refresh and now if I click on that so here you can see it's going to change that name to Jordan right here which is
3:47:03
totally expected right here so now let's just use or watch method right here so
3:47:09
what I want to do is that I'm going to just write a watch but here I'm going to just write a few comments right here I'm
3:47:15
going to just go back and now let me just place this comment right here so here we can't provide a specific
3:47:21
property of object we have to provide the entire object otherwise going to
3:47:26
give us some error inside a console okay so yeah that was just the error which I want you to keep in mind when we are
3:47:32
working with the reactive and also the Watchers okay so here if I just write like I don't know St uh do username
3:47:39
right here and now here in this case I'm going to be just writing like a new value and also the old value and here
3:47:46
inside there I'm going to just loog to the console like uh new value and here let me just pass my come on what the
3:47:52
hell new value and also let me just duplicate there and provide my old value right here and here I'm going to also
3:47:58
say like all value right here so if I save my file and now if I refresh that and here you can see we are going to be
3:48:04
getting this error inside a console which is going to just say like uh invalid watch source andex a uh watch
3:48:11
Source can only be a get effect function a ref a reactive object or array right
3:48:17
here so you cannot provide the actual value of this usern name right here you're going to have to pass this entire
3:48:23
State object so I'm going to just remove that from here and now if I save that and refresh that and here you can see
3:48:29
everything will work totally the same and there is one more catch which you have to keep in mind the first catch was
3:48:36
that you cannot provide dot something right right here like you have to provide the entire object the second
3:48:42
catch is if you're using an object both the new and the old value will be the same okay so now if I sell my file and
3:48:50
now if I click on this change name right here so here you can see the name is successfully changed but now let me just
3:48:56
show you the console so here you can see we have the username which is set to Jordan and we also have the username
3:49:03
which is also set to Jordan right here we have the order value which is set to Jordan and we also have the new value
3:49:09
which which is also said to Jordan right here okay so yeah that's a bit of bug
3:49:14
and to solve this bug we're going to be using something called the getter function okay so yeah I'm going to just
3:49:20
remove that from here and to solve this issue let me just provide that comment for you so now to solve this issue if
3:49:27
you want to get the old value and the new value separately so for that we'll have to pass the getter function and
3:49:34
here we have to specify the actual object or State Property Okay so so not
3:49:39
the object but the state property okay so how that's going to look like I'm going to just remove there and we are
3:49:45
going to be only passing the getter function right here when we want the older value and also the newer value
3:49:50
right here at once so for that we're going to be passing the gter function so how that's going to look like this is
3:49:55
how it's going to look like so you can create your function like separately and you can past the reference off there but
3:50:00
in my case I'm going to be just writing my arrow function right here because this is supremely easy and yeah I'm
3:50:06
going to be just getting the state. username right here in this case so now if I save that and here you can see we
3:50:12
are now passing this getter function right here and yeah it will totally give us the older value and it's going to
3:50:19
also gives us the newer value right here so now if I refresh that and now if I click on the change names new value
3:50:25
which you can see right here is Jordan but the older value was Alex right here so that's cool but now in some situation
3:50:32
we would want to pass multiple sources so how in the what we are going to be doing there so now I'm going to just
3:50:38
close there and now for that I'm going to be creating a separate component I'm going to give a name of like multi come
3:50:44
on m t l e multiple multiple sources there we go
3:50:49
view okay and I'm going to just copy there and now let me just go ahead and comment this line out and now let me
3:50:56
just import that component right here from where from my components folder and
3:51:01
now let me just pass that right here and I'm going to be just passing it right here so now let me just save that and we
3:51:07
will not see anything because we don't have anything okay let me just copy some cont oh God damn it there's a lot of
3:51:13
content so I'm going to have to write script setup and then we have to WR a
3:51:19
template part come on template and now let's just close oh my God what the hell are you doing hosan so now let's just
3:51:26
save there we will still see nothing uhuh what's up bro what's up to resolve
3:51:33
the component multiple sources don't we have nothing inside there what's going on I'm not Hello this let's just save
3:51:39
that refresh it you know I'm going to have to do that manually so let's just remove that and con multiple source and
3:51:47
here you got now let's just save there and here you can see we are now getting our hello right here which is totally
3:51:54
amazing so yeah that's cool but now let's just pass multiple sources right here so the first thing which I want to
3:52:00
do is that I wanted to get my ref and also the watch as well from my VJs not W
3:52:08
but VJs yes now let me just create an initial state of a username which will be set to rep and I'm going to be just
3:52:14
passing a Jordan right here Jordan and then I'm going to be also creating for a counter as well so the counter will be
3:52:20
set to zero okay so now let me just render all of that content right here so we can see something so now let me just
3:52:26
pass this H1 right here and username now let's just duplicate there and past the counter and now underneath that we're
3:52:33
going to be just providing the event listeners right here so we have a change name and we also have uh what do we call
3:52:40
it increment counter okay so God damn it what the hell am I doing today what's
3:52:46
wrong with my hands let me just write this click Handler right here and first of all I'm
3:52:52
going to be passing the username it's going to be equals to not like that it's going to be equals to hosan we are just
3:52:58
changing the username and now let's just increment or counter by one so now if I save that and now here we're going to be
3:53:05
using the Watcher so now let me just past the Watcher or watch and now if you want to pass multiple data like multiple
3:53:12
sources like if you want to pass the username and also the counter so for that you're going to have to first of all write array and then you have to
3:53:19
pass your sources right here so now let me just write a username and also the count and also the counter as well let
3:53:26
me just provide a comma and new value and also the old value as well and here
3:53:32
we are going to be just logging to the console first of all the new value and then uh we are going to be passing uh
3:53:39
you know let me just write a new value let's just duplicate that an old value and here we have to just P the old value
3:53:45
right here so now let me just sa my file and now here you can see we have a Jordan right here and we also have the
3:53:51
zero initial state of the counter and here I can also write counter or count
3:53:58
other okay so yeah everything is working a okay let me just go back and now if I
3:54:03
click on the change name so it's going to gives us the new value and also the old value right here so the new value we
3:54:10
have is hosan as for the username and we have a zero how that's because we're not
3:54:15
changing that you know let me just zoom in a bit uh let's just zoom in a bit like that and here you can see we have a
3:54:22
new value of hen we are just only changing hus I mean like we are only changing the username and we are not
3:54:28
changing this counter right here so the new value for the username is going to be hus and the new value for the counter
3:54:35
or count will be set to zero so now for this one the older value was Jordan and
3:54:41
also the count value was zero right here okay so let's suppose if I just click on
3:54:46
the counter instead let me just click on the increment counter okay what's up ah
3:54:51
we are providing a account I'm going to have to copy that and put a counter and
3:54:57
now let's just refresh that and now let me just click on there and here you can see we are now successfully incrementing
3:55:02
our counter right here which is totally a okay and that was it about Watchers in
3:55:08
wjs so now let's talk about our template ref injs so this is not the ref which we've been using so far in our course
Template Ref
3:55:14
for the reactivity this is something else so what in the world is a template refi and why you should care about that
3:55:20
so a template refi is a way to create a reference to a child component element or a Dom element within a template and
3:55:27
this allow you to access and manipulate the reference object directly in your component's logic and refs are commonly
3:55:34
used to interact with child components trigger imperative action or excess property propes and methods of the Dom
3:55:41
element okay so yeah that was just the actual definition of what a ref is so now let me just write some code and then
3:55:47
you'll get to know what I'm talking about so I already have that component and now I'm going to delete almost every
3:55:53
single thing from it okay so I'm going to just say like hello or something like that now let me just go ahead and remove
3:55:59
almost all of that Imports and all of that kind of stuff and now I'm going to just REM oh you know I'm going to just
3:56:07
remove both of these components and I'm going to rename this component to the basic ref. view right here okay so now
3:56:14
let me just copy that and now let me just import it inside my app so I'm going to be importing it by using my
3:56:19
basic rev and let me just go ahead and go to my components folder and now let me just execute that right in come on
3:56:27
right in here so now let me just save that and here you can see we are now getting that hellow right here inside
3:56:34
our browser right here okay so everything is working poly a okay but now I'm going to first of all go ahead
3:56:41
and import a few things the first thing I'm going to be importing is the on mounted right here and the second thing
3:56:47
I'm going to be importing this ref okay so I'm going to just write like cons my ref and it's going to be equals to the
3:56:53
ref and we are going to be passing just empty string right here okay and the next thing which I want to do is that
3:56:58
I'm going to just remove that H1 from here and I'm going to be creating a div and inside this div I'm going to be creating my input field right here and
3:57:05
let me just pass my placeholder right here like place holder enter your name
3:57:10
or lowercase name right here and the next thing which I'm going to do is that I'm going to be passing that ref and
3:57:18
here we are going to be passing some sort of a value so this ref is known as a compound ref which is used for the
3:57:23
reactivity and this ref is used for the reference right here okay and this is known as a template ref okay so now
3:57:30
inside that what I'm going to do is that I'm going to be passing my refer here which we've already created right here
3:57:36
okay so yeah that's that but but what I want to do is that I'm going to log to the console like conso log my riff and
3:57:43
here we're going to be logging to the console this value right here so what do you think will be the result of that so if I save my file and now if I refresh
3:57:50
that and here you can see we are not getting anything but if I just type something inside there like I don't know
3:57:56
my own name or something like that and now if I save that and here you can see it's going to gives us the value right
3:58:01
here it's not going to giv us the reference it's going to gives us the value right here on the other hand if I
3:58:07
use this console log inside this unmounted right here so if I just write like unmounted and inside there if I
3:58:13
just use like console oh you know let me just copy that from here and now let me just place that right here and now if I
3:58:18
save that and refresh that so it's going to give us reference to that object right here here you can see that we are
3:58:25
now providing that my ref and we are passing that ref as the template ref right here or you can say the initial
3:58:32
reactivity stand to the template refi right here okay so here you can see if you are not using this on M counted
3:58:38
right here so it's going to gives us that my reference. value is going to gives us that value which we currently
3:58:44
store inside this reactivity state right here but if you use that inside the on
3:58:50
mounted so it's going to gives us reference to this uh input field right here so now we can do anything we want
3:58:55
to do with that so how can you go about doing that I'm going to just comment this line out and I'm going to be also
3:59:00
removing this Huzan from here as well and I don't want to do nothing else but I'm going to just write like my ref
3:59:06
which we have this ref right here okay I just want to select that I mean like that's already been selected right here
3:59:12
but I want to do something with that input field right here so I'm not going to do anything crazy but I'm going to
3:59:17
just get the value of there and we are going to be just using the focus method on there so focus and now if i s there
3:59:24
and now if I just refresh and here you can see I did not click on this input field right here but it is already
3:59:30
focused so now let me just click somewhere else and now if I refresh there so here you can see it's going to
3:59:35
gives us that Focus automatically and why is there that's because of this line of code right here so we already have
3:59:42
access for this input field right here by using this template refi right here
3:59:47
and now we can do whatever we want to do with that so that's just the first logic I just did and now I can just change the
3:59:53
value of the I can do whatever I want to do with that like my ref do value and we
3:59:58
are going to be also using yet again value right here okay so this one will gives us that value which we have right
4:00:06
here as this reference right here but now if you want to get the value inside this input field so for that we're going
4:00:11
to have to write this dot value once again and now it's going to be equals to like something else or something like
4:00:17
that and now if I sve my file and refresh that and here you can see by default it's going to be a focus and
4:00:23
it's going to also gives us that something else right here so if I just refresh there come on so if I so if I
4:00:29
just refresh there and here you can see it's going to gives us the focus there and it's going to also gives us that something else right here okay so yeah
4:00:36
this is how we are going to be referencing to the HTML element this is how we are going to be what do we call
4:00:41
it this is how we are going to be uh doing something which you want to do with that okay so that was the first
4:00:47
example now I'm going to just close it right here now the next example I want to give you is that how in theorder we're going to be working with a ref by
4:00:53
using a functions so what I want to do is that I want to create a separate uh component right here I'm going to give a
4:00:59
name of like function ref. View and I'm going to go ahead and go to this
4:01:04
component let me just copy then let me just place that right here I'm going to almost every single thing from this
4:01:11
component right here and I'm going to just proide this H1 of something right here s my file and now I'm going to
4:01:16
comment or you know what I'm going to just comment this line out and I'm going to import my function ref right here
4:01:23
let's just copy it let me just comment this line out and place it right here Sam file and refresh that so here you
4:01:28
can see it's going to giv us there something from this function like function ref component right here okay
4:01:33
so yeah now the next thing which I want to do is that I want to remove that from here and I'm I'm going to just select
4:01:39
this is uh initial value right here okay so what I want to do is I want to create
4:01:46
a separate function and I want to reference that function for this H1 right here so how in the we're going to
4:01:51
be doing that well you know let me just attach that function right away so to attach that function we're going to be
4:01:56
either using this we uh bind right here or we can use the shorthand right here which is this column and we are going to
4:02:03
be using the ref and here we have to pass some sort of a function so in my case I'm going to give a name of like my
4:02:08
ref FK right here I guess that's going to be fine now let me just copy that and here we can do whatever we want to do
4:02:15
with that so I'm going to just create that my ref function and here it's going to take some sort of element and now
4:02:20
inside there we're going to be just log into the console like element. text content right here come on text content
4:02:28
so now let me just save that and here you can see let me just refresh that right here and here you can see it's
4:02:34
going to gives us that initial value right here why is that that's because we are using a template ri right here and
4:02:41
we are ping that element right here and that element will gives us that text content right here so if I just remove
4:02:46
that and save my f and refresh that so it's going to gives us access to this H1 right here okay so yeah now we can
4:02:53
access that uh text content we can do whatever you want to do with that so you know what let me just write a comment
4:02:59
right here like uh reading text content right here and next we are going to be
4:03:04
just doing like uh element. text content and now let's just change that content to something else like text change come
4:03:11
on text change or something like that now if I save my file and here you can see if I just refreshed there it's going
4:03:17
to change this initial text to uh text change right here and it's going to also give us like this is a initial value
4:03:23
inside a console and now I'm going to also just style there so I'm going to just use like element. style. color and
4:03:30
it's going to be just equals to some sort of a red color or Crimson would be fine so now if I save there and now if I
4:03:36
refresh there so here you can see it's going to also attach this crimson color right here so yeah this is how we are
4:03:42
going to be passing a function as a reference element to our um what do we call it is a reference oh God damn it I
4:03:49
kind of forgot the name of that uh as a template Rift there we go it's a
4:03:55
template Rift to our element there we go kind of lost my mind today but anyways
4:04:01
I'm just have I'm going to have to just record this video as soon as possible next we're going to be learning about
4:04:06
how we are going to be using a ref with component so I'm going to be just writing like ref component. right here
4:04:13
and inside that um you know what before I do that I'm going to also create yet
4:04:18
another component which will be uh my component right here so my component.
4:04:24
view so that we can use this my component inside this ref component right here so I'm going to go ahead and
4:04:30
go to my component right here and I'm going to what the hell I have to do that manually and let's just write oh
4:04:39
what was that let me just write a template once again and yeah now let's just start working with that but I'm
4:04:45
going to have to write H1 of something I guess and then we are going to be just
4:04:50
getting into this uh setup script right here and first of all we're going to have to get the ref right here from the
4:04:57
VJs so now let me just save that and underneath there we are going to be creating our initial St so cost count is
4:05:04
going to be equals to this R and we're going to be passing 10 value right here so then we're going to be creating two
4:05:09
functions so cons increment it's going to be equals to this Arrow function and this going to allows us to just change
4:05:15
the value of that counter to + one and then we have a decrement function so now let me just change the name of that to
4:05:22
decrement and there you have it okay so I forgot to include these arrows now let
4:05:27
me just do that and finally we just have to use these functions somewhere so first of all I'm going to be using that
4:05:33
count so now let me just P my count and I'm going to be also creating a of plus
4:05:38
and also for minus and now let me just attach my click event handlers and increment function and also the
4:05:45
decrement function so like we only have this counter component right here but
4:05:50
yeah now if you want to use a rep with this component so first of all I'm going to go back and here I'm going to just place these comments right here so when
4:05:57
using a script setup which we are using right here so that component is private
4:06:03
by default right here so a parent referencing to a child won't be able to access anything from that component so
4:06:09
first we have to expose all of the properties and methods then we would be able to use them in our parent component
4:06:15
so to expose them for that we're going to be using this defined expose right here to expose our data for our parent
4:06:22
component uh to use so I'm going to just remove that from here and now let me just uh expose that data right here so
4:06:28
I'm going to just zoom in a bit and here we are going to be exposing our data to be used inside our parent component so
4:06:34
for that we're going to be using like Define come on Define uh not a but find expose right here and
4:06:41
we are going to be passing the count we're going to be also passing the increment right here and also the decr
4:06:47
so now if you s our file now we can successfully use all of these stuff inside our ref word here so to use that
4:06:53
word here first of all we're going to have to write uh our script and setup and then we have to write come on what
4:07:00
the hell then we have to write template and opening and closing tag and now what
4:07:05
I want to do is that I'm going to be importing my component so now let me just import my component right here I'm
4:07:12
going to copy that and now let me just place that component right here sell my file but I'm going to also create a
4:07:17
reference right here inside this component as well and I'm going to be also getting the unmounted right here so
4:07:24
not unmounted but unmounted so now let me just get on mounted and I'm going to be also getting the refi from there and
4:07:30
now let me just create my reference and it's going to be equals to the ref object and here we're going to be passing the null value and when this
4:07:37
component mounts so then we wanted to get access to our component right here so now let me just use like my ref and
4:07:44
then do value which I just show you a few seconds ago so now let me just copy that and here we are going to be passing
4:07:51
that as a template refi right here so now let me just use my ref I mean like ref and here we're going to be passing
4:07:56
my ref right here so now if I save this file and I'm pretty much sure that I did
4:08:02
not import this component right here yep I didn't so now let me just comment this line out and run and import come on let
4:08:09
me just import uh ref component right here I'm going to copy that and now let me just comment this line out and place
4:08:16
that right here so now let me just refresh that and here you can see it's going to give us that count and
4:08:22
increment and decrement buttons right here but I'm going to right click on that and go to my inspect area I don't
4:08:27
know why I just closed and now let me just refresh that right here and then I'm going to just expand there then I'm
4:08:33
going to go to the Target then I'm going to go to the Target one more time so here you can can see we have this count method I mean like that count right here
4:08:40
and we also have the increment I mean like I don't what the hell am I saying we have a decrement uh what do we call
4:08:46
decrement method right here and we also have a increment method right here so yeah this is how we are going to be accessing our component right here but
4:08:54
now if I click on that we can successfully increment that and decrement that right here so everything
4:08:59
is working okay and this is how we are going to be using the template R in VJs so now let's talk about ASN component in