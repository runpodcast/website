+++
Description = "Auth.entication.orization. - Mid"
PublishDate = "2017-10-11T11:09:45-05:00"
date = "2017-10-11"
podcast_file = "post/0.1.2-auth-mid.mp3"
podcast_duration = "00:31:45"
podcast_bytes = "30484313" # the length of the episode in bytes
episode_image = "post/0.1.2-auth-session-oauth-jwts.png"
episode = "1"
title = "0.1.2 Auth/entication/orization Mid Level"
subtitle = "A tirade against JWTs for session, and a few other nuggets"
image = "post/0.1.2-auth-session-oauth-jwts.png"
aliases = ["/0.1.2"]
explicit = "no"
+++

More "authentication" and "authorization" talks, hear how much Aaron loves JWTs.

<!--more-->

We talk about several more angles on the authentication and authorization topic...

but I have a hard time thinking about anything besides Aaron's rants about JWTs.

We both agree that JWTs are elegant and effective means of passing information around.

Then Arron complains about how they are used as a replacement for Session data or a session id cookie/token.

He makes some great points.

JWT Pros:
* Trustable (there is a security encryption)
* Accessible (basically plain text JSON, encoded)
* Broadly accepted standard, lots of libs and tools now
* Allows intra-service token exchange, the systems only have to trust the encryption scheme, but do not need to share session tables.

JWT Cons:
* Un-expirable (can timeout, but can not log-out or force to expire)
* A fairly large payload over the wire, on every request (more than just an id)
* Doesn't really save you a DB lookup on the server, because you often will want to maintain a server session anyway, for secure data, or for payload too big to store in the JWT... and if you're doing that anyway, why not just use a normal server session?
