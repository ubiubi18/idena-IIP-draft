 idena-IIP-draft

# IIP- : Higher Reward for early Submission of Flips 
by ubiubi / @audiodidakt314

# Abstract: 
 Only flips that are submitted with first 8 hours of each epoch should be rewarded. This will result in higher rewards for unique people and more AI-resistant flips.

# Motivation:

As long as there are no time-constraints submitting flips, big players have legit incentive to centralise their flip-production to be able to extract value more efficient and try to get it done as fast as possible. This leads also to bad practice. Story-template flips can be produced in two minutes and reach more often consensus than genuine flips that take much longer to produce. Unfortunately those repeating story-patterns are less AI-resistant. There are likely other undesirable strategies of big players that enfavor possible sybil attacks and are not covered by the report system. Introducing time-contraints to rewardable submission of flips will make it less profitable to centraly produce flips and favor solo-miners and family-pools over dishonest players.


# Technical specification:

If a flip has been submitted within the first 1440 blocks (about 8 hours) of  the epoch and if it does get qualified and is not reported by a majority, a basic flip reward  is payed. The basic reward is calculated based on how early in the epoch the flip was submitted. The later the flip is submitted, the lower the basic flip reward. The reduction factor k is calculated for each submitted flip as k = 1−t⁴ · 0.5, where t ∈ [0..1] is the amount of time that has passed from the start of the epoch to the moment of the submission until 1440 new blocks are mined. Flips can be also be submitted more than 1440 blocks into the new epoch, but the submitter will receive zero rewards for those flips.


# Rationale:

Even a centralised single human player that is able to create one flip every two minutes in a row would only be able to produce flips for up to 10 identities each hour, but not for hundreds of identites at once. That player would need to involve more real people instead, if the task was to create flips for hundreds of delegated identities fast. 

Unique people validating (semi-)unique identities are so far mainly required in two session tasks: reporting and solving flips. Those tasks cant be centralised or automatised and secure idenas semi-unique identity. No matter that they are only responsible for 25% of possible rewards in idenanetwork, while the other 75% of total rewards are extracted in tasks that are prone to centralisation. 

According to the block explorer human farms usualy produce flips in a row over the span of the whole epoch and the fastest of them use strategies like reusing flips or using story-templates to achieve that. Also the badest actors are most competitive to survive low marketcap, since their production costs each flip are smaller. 

Solo-miners and honest pools become faster unprofitable in flip production than dishonest players, so „free market“ logic unfortunately enfavors bad habits. 

The majority of unique people involved in idena flip-sessions  does not even have the chance to earn rewards and secure idena by producing flips! This can be deemed as a security risk alone and makes it at the same time cryptonomically less profitable to be a solo-miner, because big pools that centralise flip-production are faster in producing and submitting flips and thereby lower the median market value of that task. 

If we we start to reward only flips that are submitted on the first day of each epoch, big players will need to decide to involve more people to get it done in time or to loose flip rewards.
Involving more people will lift production costs for human farms substancially in favor of unique people, spread rewards to more people and make the production of AI-resistant semi-unique flips more likely. 

Story-templates can still be used in this setting, but the risk/profit ratio will be more undesirable for big players than it is now. Also it is less expensive to introduce more creative stories, if a farm has to involve and pay more people anyway. More farm workers beeing involved into flip production should also make it more realistic, that workers decide to turn into solo-miners.

There are several alternative approaches we could try to deal with bad habbits of centralised flip producers:

- Appeal for good will, teach them about implications of their behaviour

I think idena has an impressing history of teaching people about best practice. This was absolute worth it! Some big pools do a brilliant job in producing good flips that are sybil-resistant no matter that they are produced centrally. But at this point it seems unlikely that those big players with bad habbits will be unaware of their own worse performance. So appealing for more good will might be ineffective.

- Lower or even cut flip all flip rewards to zero

This is neither compatible with the upcoming incentive realignment of grading flips, nor is it desirable in context of staking, because it will make it more expensive for late adopters to collect the required idna for their stake just with work.

- Hope for flip grading to solve the issue

Flip grading is great but wont cover every aspect of centralised flip production. There will allways be undesirable patterns possible in flip production that are not instantly visible for the flip reporting committee. 

The block explorer indicates: Solo-miners need up to 8 minutes in median to create and submit a flip while big pools with centralised flip-production are much faster. The biggest human farm seems to need only like 2 minutes each flip. At the same time there is no indication that multiple people are involved in its creation, otherwise there would be times where several identities of a pool post flips within less than 2 or 3 blocks at the same time. But there is nearly no evidence of such events in the block explorer. This is an indication that most often centralised flip production is indeed done manually by one person at a time. 

It may seem more user-friendly to give honest people as much time as possible to come up with good flips instead of producing them in a hurry, it may also seem convenient to outsource the process of flipproduction to people or centralised players who know how to do it better and faster – but lowering and optimising the production costs of big players ultimately hurts a small player more than the risk of loosing a few flip rewards due to the lack of time. If people have about eight rewardable submission hours, that should in most cases be enough time to arrange a submission. If people dont find the time, they will still have their staking rewards, which will outweight the potential flip rewards losses in most cases.


# Backwards Compatibility 

should be similar to the change that introduced a reduction factor over time to the invitation rewards

# Reference Implementation 

the proposal leans to the reduction factor of the invitation reward fund, which is proven to work just fine: https://docs.idena.io/docs/wp/economics#invitation-reward-fund

# Security Considerations:

This IIP might be opposed by a majority of eligable identities onchain, because pools that are bigger than a family will have problems to cover the time limitation, while pools smaller than that as well as unique solo miners might not all see the neccessity and oppose it as well for fearing to loose more rewards. 

If implemented right now at those market conditions, it likely would result in an even faster decline of network size in short term, because many pools would need to rearange their strategy or even question their whole profitability of their operations under new conditions. Some of them could shut down operations and sell, while at the same time some solo-miners would feel frustrated about not finding the time for flip production and loosing even those rewards.

Also it is undesirable to loose too many farms, they are managed by competent people who understand idena and that do a hell of a job in introducing idena to new humans. It should not be the goal to shut all pools down, just because a few of them have bad habbits.

But i think the medium term benefits should outweight that risk. 

The task of solving flips secures itself with a time-limit against sybil-attacks, the task of producing flips should do the same. Centralisation of flip-production poses a constant security risk, because it is prone to AI-recognition and other abuse. For better sybil-resistance flips need to be produced as semi-unique as possible. As more people are involved in producing flips, as more unique creativity can be involved without additional costs, which will probably be recognisable much harder for possible AI-assistance in solving flips.
