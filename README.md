# Nifty Hackathon

## SwapDAO: A Decentralized, Autonomous Protocol for Non-Fungible Digital Asset Backed Securities
# Introduction

The non-fungible token space has been rapidly increasing since its inception in 200x. The market capitalization of this space has grown from xyz to abc in a matter of n years. Since the launch of CryptoKitties, collectibles on the blockchain have captured millions of dollars in value. In February of 2018, a piece of digital art on the Ethereum blockchain sold for US $1 million.

# Overview of Non-Fungible Tokens

Properly explained, an ERC-721 non-fungible token (NFT) is a token on the Ethereum blockchain that is unique in the sense that it cannot be exchanged for another token of the same class. An NFT can be used to represent a collectible item in a game, an agreement between two individuals, or a unique asset such as a house. The tokenization of such assets creates an ecosystem with a massive value proposition as it allows for previously illiquid assets to be freely traded across international borders in a global, unified marketplace.

# The Value of Non-Fungible Tokens

Many folks in the digital asset space have surmised that people will seek to own NFTs purely for their unique and scarce traits. However, research regarding the psychology of collecting suggests that humans collect things more often for emotional purposes as opposed to monetary.

Crypto Kitties are being bought and sold primarily for the expected monetary gain of selling the asset at an appreciated future value. There is little emotion involved in the purchase of these assets. With that said, Non-Fungible Token’s will not be adopted on a wide scale based solely on their scarce and unique properties. One needs to develop a usability function for these assets that either increases the emotional response from the user or provides a utility that was not previously possible prior to this protocol standard.

# Why investing in NFT’s may be a good idea:

The implications of NFTs go well beyond digital cats. However, as exciting as this may be, the ripple effects of rapid growth in this area could be troublesome. The CryptoKitties mania took upwards of 16% of Ethereum transactions in December of 2017 and drastically slowed down the network. If NFTs continue to grow at a faster rate than Ethereum scaling solutions, one should expect to see skyrocketing TX fees and major network clog ups in the short term.

Investing in anticipation of NFT growth is particularly tough at present time. The obvious and unsatisfying answer is to buy ETH in anticipation of the increased demand in the network to pay elevated gas fees. However, the proper investable vertical exists yet. In the coming months, one should be on the lookout for novel projects working on custodial solutions for NFTs, consumer-friendly UIs for interacting with NFT’s, and developments in the marketplaces in which these unique assets can be exchanged.



# The Illiquidity of Non-Fungible Tokens

While NFTs are undoubtedly a growing asset class with a large amount of value, it remains relatively difficult to liquidate a non-fungible token as the marketplaces are in an even earlier stage of maturity than traditional, fungible cryptoassets such as Bitcoin and altcoins. There are only a handful of exchanges that provide the ability to buy and sell non-fungible tokens, and all of them are extremely illiquid and do not currently have APIs for algorithmic market makers. As a result, it is nearly impossible to offer a guarantee that a specific quantity of a specific NFT can be liquidated at a given price. Consequently, NFTs by themselves are highly volatile and make poor candidates for collateral. Because of the risk associated with the illiquidity of such NFTs, lenders are generally unwilling to offer loans collateralized by them. 

Syndication as a Means of Risk Mitigation

While one NFT can be relatively unpredictable in terms of price and liquidity, a sufficiently large set of NFTs will be hedged against the risk of individual tokens going to zero or becoming illiquid. As the NFT marketplace continues to grow rapidly, the overall market capitalization of NFTs will increase over time, and therefore the top performers in the space will offset the losses of the worst performers. This basket-holding strategy is commonly employed in traditional financial markets, where it is known as the index investing strategy. 

While many individuals and institutions would be hesitant to lend against a single, highly volatile digital asset with limited liquidity, a diversified index of a rapidly growing asset class would make for much more appealing collateral. 

We define the aggregate risk of a single NFT as β_0. We denote the total value of a portfolio as μ. On a daily basis, B_0 can range from negative 20% to positive 20% -- meaning the value of a $10 million portfolio can fall by as much as $2 million in a single day. 
	
 	 μ_new = μ_initial * ( 1 + β ) 

The one day Value at Risk (VaR)  for such a portfolio is defined on the interval:
	
	μ_initial * (β_min ) < VaR < μ_initial * ( β_max ) 

We represent the aggregate risk of a diversified index of NFTs as follows: 

	β_index = Σ(0 to n) [β_i * (μ_i / μ_total)] 

We posit that older, more established NFTs are less susceptible to large moves in their market price, as the hype associated with their projects has died down, whereas newer NFTs are more likely to undergo rapid price moves. Accordingly, we propose a dynamic portfolio allocation mechanism that favors holding a larger ratio of older, more liquid NFTs with a smaller ratio of newer, more volatile NFTs. 

[insert portfolio allocation model here]

# A Model for NFT-Collateralized Bonds

In order to allow holders of ERC-721 tokens to obtain liquidity from the value of their digital assets without sacrificing upside potential in the longer term, we propose a model for three classes of bonds, each backed by different pools of non-fungible tokens. Class A NFT Bonds have a maturity date one year from their creation, Class B NFT Bonds have a maturity date two years from their creation, and Class C NFT Bonds have a maturity date three years from their creation. 
The creation of an NFT bond begins with a group of Lenders, who post ETH into the bond’s liquidity pool. Once the liquidity pool has reached the target amount of ETH, Lenders will specify the following parameters:

1. Accepted ERC-721 Tokens 
2. Collateral Requirement
3. Maintenance Margin
4. Portfolio Allocation Rules 
5. Premium
6. Maturity Date

Lenders specify the Accepted ERC-721 Tokens, as a list of tokens they are willing to offer collateralized loans against. These tokens will generally be the most valuable or the most liquid, in order to protect the lenders against the risk of collateral devaluation. Next, they will specify the Collateral Requirement, or the minimum multiple of value borrowed required to be posted as collateral for a loan. In exchanges that offered leveraged trading, it is not uncommon for this number to be 0.2 or even 0.01, meaning the ability for one to borrow 100 times the amount one posts as collateral. Because NFTs are a nascent asset class with limited liquidity, we will set the default Collateral Requirement as 1.75. This means that in order to borrow 100 ETH, a Borrower would need to post Accepted ERC-721 Tokens worth 175 ETH as collateral. The next parameter is the Maintenance Margin, which is the maximum amount of value the collateral can lose with respect to the Collateral Requirement before a Borrower is margin called, which we set to 0.25 by default. This means that if the market value of a Borrower’s collateral falls below 1.5 (1.75 - 0.25) times the remaining balance of the loan, the Borrower will be prompted to post more collateral in any Accepted ERC-721 Token in order to meet the Collateral Requirement. For example, if Alice has 50 ETH remaining in her loan, and the value of her collateral drops to 70 ETH, she will be prompted to post collateral worth 17.5 ETH in order to bring the total value of her collateral to 87.5 ETH, the Collateral Requirement for her loan. If she cannot post this collateral, her collateral will be sold on the market for and proceeds from the sale will be returned to the liquidity pool of the bond. Lenders specify Portfolio Allocation Rules, which dictate the target ratio of the Accepted ERC-721 Tokens, which depends on the collective risk profile of the Lenders. Lenders with a lower risk appetite might want to only accept Gen 0 CryptoKitties, while Lenders with a greater risk tolerance may choose to accept 20% Gen 0 CryptoKitties and 80% of a recently launched NFT. Lastly, Lenders specify a Premium, which is the interest rate that Borrowers will pay on the ETH that they borrow. Borrowers make monthly payments until the maturity date of the bond, at which point they will have paid off the principal amount borrowed in addition to interest accrued over the lifespan of the bond, as calculated from the Premium. In the event that a Borrower chooses to pay off his loan early, he must still pay the interest that he would have accrued over the entire duration of the bond. 

When a Borrower is looking to borrow ETH from the liquidity pool, he or she firstly posts the Collateral Requirement in Accepted ERC-721 Tokens. Next, an ERC-721 token representing the loan and the Borrower’s collateral is issued to the Borrower, along with the requested amount of ETH. Borrowers make monthly payments towards repayment of their loans until the bond’s maturity date. This means that all loans must be initialized 

Price Discovery of ERC-721 Tokens
In order to calculate the value of tokens in the network along with the penalty fee generated if a borrower earns a strike was determined by a price discovery mechanism. Using Oracle services as means to pull third party party data into the blockchain. Although the solution was sound, we disliked the central point of failure of an ORacle and didn’t want to rely on third party providers. While ideating how to solve the problem that was so integral to our product, we took notice of 0x and the 0xChanger use of 0xChanger will help us constantly retrieve accurate pricing of our ERC20 token as well as make the experience more seamless for our users. 

# Providing Liquidity to ERC-721 using ERC-20 

Beyond solving the problem of price discovery, 0x offers “our Company” network another highly desirable property: liquidity. Since the penalty fee requires users to possess a native token, it would be suboptimal to require them to move to third party marketplaces when they want to bring their tokens out of the system. In addition to providing an efficient price discovery mechanism, integration with the 0xChanger contract allows the “Company” network to provide “always open” liquidity tokens to its users. With the 0xChanger contract, users will not be required to interact with third-party markets in order to acquire the ERC20 tokens they need to pay to receive/expend their funds, or convert rewards to denomination tokens, and can instead convert our ERC20 token.,

# Preserving Upside Potential Whilst Mitigating Drawdown

# Decentralized Governance 

The network is designed with the goal of being fully autonomous and self-sustaining at some point in the future. To accomplish this goal the “Team” is building the dApp to be as isolated from central control as possible while still maintaining safety guarantees. During the initial launch and for the first few periods of production, the team will maintain the ability to upgrade the network if Solidity is updated or more optimized processes are devised. Eventually this central control will be transitioned to the community and a decentralized governance tool will be put into place. 

Governance of NFT funds will be handled in a decentralized fashion. We will be using quadratic voting to ensure an optimal level of decentralization. Quadratic voting is a system of buying votes, where each additional vote costs twice as much as the one before it. In other words, money buys votes, but with strong diminishing returns. 

Vitalik proposed a variant on this he calls “quadratic coin lock voting” where N coins let you make N * k votes by locking up those coins for a time period of k². This is a nice modification because it aligns incentives over time: more voting power requires living with your decisions for longer (In a tokenized world with little friction of entering or leaving a community, this is especially important).
 
In summary, Quadratic Voting is a voting scheme for electing one out of two candidates which departs from the concept of one person, one vote and instead allows each eligible voter to cast multiple votes for any single candidate, thereby expressing the magnitude of his or her preference for the selected decision. After the election, the total revenue is reallocated among the voters according to a refund rule: perhaps each voter get an equal share of the election revenue.
 






