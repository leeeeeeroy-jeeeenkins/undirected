---
slug: common-mistakes-to-avoid-when-using-ambassador
title: Common Mistakes to Avoid When Using Ambassador
authors: [undirected]
---


# Common Mistakes to Avoid When Using Ambassador

I'll never forget the time David roped me into using Ambassador for the first time. It was a sunny Saturday morning, the coffee was strong, and the possibilities seemed endless. "You'll love it," he said, with a twinkle in his eye that promised newfangled geekery beyond our wildest dreams. But we soon realized that the path of microservices nirvana was littered with traps, much like trying to chase a cat down a winding alley—not impossible, but definitely tricky. What follows is a mélange of our shared blunders and lessons, one code snippet at a time.

## Misunderstanding the Role of Ambassador

As we dove in, our first faux pas—ah, the memories!—was trying to make Ambassador do things it simply wasn't ever meant to do. It's not that we were optimistic coders, just that the ambiguity of its name made it feel like it could solve world hunger or, at the very least, orchestrate all our microservices issues effortlessly.

Ambassador, in its essence, is a Kubernetes-native API Gateway that handles all the inbound communication. It's like the friendly doorman of a fancy hotel, deciding which guests to let in and which ones might need a, shall we say, closer inspection. But, oh dear, trying to make it manage internal microservice communication was akin to asking our friendly doorman to also be the maître d'. Impossible—or very nearly so.

**Tip**: Focus on configuring Ambassador for managing external traffic first. Set up those mappings like Picasso with his paints, keeping your configurations clean and dedicated to edge responsibilities. Turns out, Ambassador serves up services to the outside world perfectly, as long as we don’t ask it to do more than it was designed for.

## Forgetting About Rate Limiting

One breezy afternoon, the kind where motivation wafts in through the window, we decided to test our once-fumbling but now-sophisticated Ambassador setup. David, our ever-enthusiastic debugging partner, leaned back in his chair and hit that 'enter' key with the flair of a conductor orchestrating a symphony. What followed was not quite melodic. Instead, it felt like being swallowed by a tidal wave of requests.

As it happens, we found that without the gentle hand of rate limiting, our APIs had decided the world needed to receive all its data at once—chaotic? Oh, yes.

**Tip**: Use Ambassador’s rate limiting to control traffic. Introduce it like you'd introduce a new pet to the family—with careful attention and thoughtful limits. It’s all about balancing an itsy-bitsy bit of concurrency so that the system isn't flooded.

```yaml
apiVersion: getambassador.io/v2
kind: RateLimitService
metadata:
  name: example
spec:
  service: "rate-limit:5000"
  timeout_ms: 2000
```

## Ignoring Security—A Rookie Mistake

One evening, under the dim glow of our monitors, with takeout boxes strewn about like an impromptu art installation, we realized an oversight that could have let anyone, and I mean anyone, waltz right through our API security. The culprit? Perimeter security was set to "nonexistent." If our APIs had had doors, they were wide open. It's the kind of oversight that keeps you awake at night, holding your takeout container like it's a ghostly reminder of your folly.

Using Ambassador involves securing communication, as one might secure the most precious secrets of the realm.

**Tip**: Embrace Ambassador’s authentication features with a whole-hearted hug. And don't forget TLS! You wouldn’t send your passwords through an unsecured channel, would you? Employ tools like OAuth and set your system gleaming with security aplomb.

```yaml
apiVersion: getambassador.io/v2
kind: Mapping
metadata:
  name: secure-backend
spec:
  prefix: /backend/
  service: backend
  host_regex: true
  jwt: 
    - provider: 
        issuer: "https://your.auth.server/issuer"
```

## Overcomplicating with Overzealous Mappings

As we found ourselves knee-deep in configurations, one particular snippet caught my eye. It was a labyrinthine block of mapping configurations, that woven wrongly spelled certain doom. It turns out, the more mappings you painstakingly create without understanding their purpose, the more likely you are to conjure chaos in your routing—who knew? Tumbling into the minutiae was akin to attempting to write a symphony with too many notes—it ends up just noise.

**Tip**: Keep your mappings concise and functional. Start simple; grow complexity as needs demand, not the other way around. Ambassador is happiest when clean and purposeful, like your evening wear on a cool Friday night.

```yaml
apiVersion: getambassador.io/v2
kind: Mapping
metadata:
  name: simple-backend
spec:
  prefix: /simple/
  service: simple-service
```

## Neglecting the Documentation

When the night was darkest, long after the pizza ran dry and David's energy drinks seemed more mistake than miracle, came the realization we should have started with documentation—not ended with it. It guided us as lost souls in a sea of self-inflicted misfortune.

The Ambassador documentation, much like a trusty compass or a wise friend, is there to get you back on track when your technology adventure veers off the expected path into the thicket of confusion and bug reports.

**Tip**: Always—like, really always—check Ambassador's documentation when you're lost, which is basically always going to be before you realize you need it. Documentation is the lifeboat we constantly forget we need until we’re adrift.

## Conclusion

As David fiddled with his last snippet, we marveled at how Ambassador had become less like an unfamiliar landscape and more akin to a cozy corner of our coding repertoire. Our journey was fraught with pitfalls, but in navigating them, we found understanding and a sense of camaraderie. 

Let us be your ship’s wheel through these treacherous waters; heed our lessons—avoid misunderstanding its limits, embrace security, manage traffic with care, keep mappings simple, and for all that's worth, read the documentation. Here’s to smooth sailing on your Ambassador endeavors. And remember: when everything fails, there's always coffee and an odd emergency pizza box nearby to comfort the soul.