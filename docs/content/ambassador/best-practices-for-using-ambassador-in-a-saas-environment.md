---
slug: best-practices-for-using-ambassador-in-a-saas-environment
title: Best Practices for Using Ambassador in a SaaS Environment
authors: [undirected]
---


# Best Practices for Using Ambassador in a SaaS Environment

I'll never forget the day we decided to overhaul our cloud architecture, like trying to wrangle an octopus with ski mittens. It was a regular Tuesday morning at our bustling SaaS startup, and the revelation hit us like caffeine at 8:30 AM. "Why aren't we using Ambassador?" Colin, our CTO, exclaimed with a blend of frustration and inspiration. It was a strong coffee moment—people were running on zeal and technical adrenaline. It was transformative, really, once we realized how much potential there was in wielding this mighty tool.

Inset, then, into our narrative: the rollout of Ambassador. This tale isn't just about integrating a piece of tech; it's about empowering systems, enlightening pathways, and—dare I say—discovering joy in microservices. But let's not get ahead of ourselves. Here's the story, complete with human quirks and technical triumphs, served like a weekend brunch with friends.

## Setting the Stage

That pivotal day, much like any other, began with a lot of keyboard clacking and empty coffee mugs. Our SaaS platform was scaling, meaning our end-users expected more snappiness from our services than a Labrador expects treats. But snappiness often dies in translation between microservices—sad, yet true. Our just-barely-adequate solutions were tethering us like a kite on a windless day. Enter Ambassador.

For those of you who missed the memo—Ambassador is an open-source Kubernetes-native API gateway built on Envoy Proxy. It allows us to breathe life into our service meshes with configuration flexibility and routing wizardry. It's basically like having the traffic control superpowers of an airport air-traffic controller. Now, let’s dive into the nitty-gritty without using technical incantations that incite terror.

## Understanding the Value

Have you ever tried giving a presentation and ended up talking to plants at the back of the room, because everyone else was sleeping? Well, that was us trying to tell our story of service improvement, until Ambassador danced into our operations. What we needed was a bridge for our islands of code. Ambassador, in all its Kubernetes-loving glory, is the bridge builder.

By simplifying the intricate dance between microservices, Ambassador helped us improve deployment speed and reliability. Imagine, if you will, the service discovery capabilities that left us in awe—like a scene from a Spielberg movie, glowing with promise and devoid of technical apathy.

If you've been nodding along with a knowing smile, or an occasional wince, you're probably familiar with the chaos of scaling a SaaS platform. Improving integration with Ambassador is like discovering that your favorite song is number one on the charts—both gratifying and motivating.

## Best Practice #1: Simplified Configuration

Now, you might think configuring an API gateway is akin to plotting a transatlantic flight path armed only with a paper map. But with Ambassador? It's more like following the GPS in your pocket, only the GPS sometimes speaks in open-source dialects. Nonetheless, we discovered an easy-on-the-brain approach to configuration. Let me take you back to John’s Eureka moment—our DevOps sage.

One afternoon—propelled by snacks and determination—John whipped up a configuration that looked, well, tangible. By leveraging `YAML` files, we were able to create configurations that were not only human-readable but human-understandable. It was a tasteful alternative to arcane configurations. Here's a peek:

```yaml
apiVersion: getambassador.io/v2
kind:  Mapping
metadata:
  name:  sample-service
spec:
  prefix: /sample/
  service: sample-service.default
```

See, not rocket science, but it felt pretty close to art. Gone were the days of praying over our routing tables—now, we had structure.

## Best Practice #2: Rollouts Without a Mental Breakdown

Remember that time when Sandra, our tech lead, almost pulled out her hair trying to roll out a new service without downtime? Ambulances weren't called, but let's say stress levels were higher than average. But through the magic of Ambassador, zero-downtime rollouts became achievable dreams.

Utilizing the canary release capabilities, Ambassador allowed us to deploy new versions alongside older versions, like a well-choreographed ballet. Think of it as a peace treaty between time-tried stability and cutting-edge innovation. It was fabulous, and slightly intoxicating.

```yaml
apiVersion: getambassador.io/v1
kind:  Mapping
metadata:
  name:  canary-sample-service
spec:
  prefix: /sample/
  service: canary-sample-service.default
  weight: 10
```
With Ambassador managing our traffic shifts elegantly, we set a percentage of requests to the new service, letting us sleep better at night. Sometimes, in tech, peace of mind is the ultimate state of being.

## Best Practice #3: Service Observation and Debugging

One late while-the-nocturnal-creatures-stir evening, our delightful system decided to whisper sweet nothings and then shout '503 Errors' at us. Boy, was it a party. But instead of going down the spiraling rabbit hole of despair, Ambassador gifted us with the magic of observability. It was our software version of a secret decoder ring.

Ambassador's tracing and logging integrations offered insights that felt like spotting a long-lost friend across a room. We were able to utilize tracing headers with Envoy and integrate directly into our ELK stack for a central logging experience that practically sung us lullabies.

```yaml
---
apiVersion: getambassador.io/v1
kind:  TracingService
metadata:
  name:  tracing-service
spec:
  service:  "otel-collector:55678"
```

Through these traces, we mapped our entire request journey—each detour and every piggyback ride, captured for posterity. Debugging issues went from being frustrating laboratory experiments to actual, data-driven exploration.

## Best Practice #4: Secure and Performant

Ensuring performance and security isn't merely about ticking boxes; it's about creating an environment people trust and—dare I say—adore. Our security guru, Liz, was obsessed with encryption like a kid with candy, and rightly so. Her enthusiasm was infectious, and Ambassador's robust security protocols catered beautifully to her whims.

From mutual TLS to rate limiting, we locked down the access paths tighter than a secret club—yet user-experience remained frictionless. As intended processes unfolded without a hitch, we marveled at how effortlessly traffic was steered away from nasty potholes of vulnerability.

```yaml
---
apiVersion: getambassador.io/v1
kind:  Module
metadata:
  name:  tls
spec:
  config:
    server:
      enabled: true
      secret: ambassador-certs
```

Did we take bold strides toward hardened safety without sacrificing performance? You bet. And the resulting performance boost left us swanning through our release phases like co-conspirators in a grand heist.

## Embracing the Future

With Ambassador firmly integrated into our system's DNA, we embraced future challenges with the optimism of surfers catching the perfect wave. We began brainstorming new possibilities—could we automate even more? What about plugging in additional observability tools?

Our days of uncertainty were behind us, replaced by a newfound agility and poise. It was this sense of progress and sharpened toolkits that anchored us in a rapidly evolving tech ecosystem. Above all, we discovered our passion for using technology not just as a utility, but as a source of wonder and inspiration. We learned to trust our tools, our people—and most importantly, ourselves.

Through sharing our experiences, our hope is that more of you out there can find your stride in technological challenges, turning daunting tasks into stories worth telling. Let’s make those moments of enlightenment a shared adventure. May you find your Ambassador moments, fueled by collaborative spirit, boundless curiosity, and just a touch of mischief.