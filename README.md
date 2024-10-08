# Legacy DB Modernization Kata

An architectural kata to practice modernizing legacy DB-based systems, for scalability and/or for scaling teams.

# The context 

You just arrived at a company. This company is a few years old and runs a marketplace for selling Minecraft creations between creators (sellers) and players (customers). The business is growing fast and the system originally built doesn’t seem to be ready for more extreme growth.

You’ve been on Reddit recently, and it didn’t go well with too many visitors at the same time, and the system slowed down and you lost many sales. The investors expressed concerns for the ability to scale the current system, and that’s why you’re here. 

Meanwhile, the product managers request  new features to improve the conversion rate, like adding multiple images and videos to the items, and consequently and automatically add them to the related bundles as well. 

# The system 

Here is the DB schema in one picture:

![The DB schema shown in Azimutt](https://github.com/cyriux/LegacyDBModernizationKata/blob/main/DB_schema.png) 

It's a typical system built on top of a DB.

**A detailled description of the DB tables of the system can be found in this repository in various forms.**

The sequence of operations goes like this, in a nutshell:

- A Seller puts Items for sale.
- A Customer then orders items and/or bundles.
- The system contacts the PSP (Payment Service Provider) and updates the Order and Payment entities.
- If the payment is successful, then a Payment confirmation is generated.
- Watermarked Items are created for the customer.
- A Download Limit is created.
- Additionally, an Invoice is generated, reportings are generated, and popularity for the items and the seller are updated.

![The DB schema shown in Azimutt](https://github.com/cyriux/LegacyDBModernizationKata/blob/main/sequence-diagram.png) 


# The game

3 iterations (20mn each), with a short debrief after each where you’re facing technical experts and managers having the power to approve budgets. 

1. Discovery: discuss what’s right, what’s wrong there, and mention potentiel ideas of next moves.
1. Propositions: Propose changes to apply to the system, why they’re needed and the consequences. You may use the ADR structure. 
1. Planing: Propose the practical trajectory to actually change the system and explain why it’s the best way to move.

