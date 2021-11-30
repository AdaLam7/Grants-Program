# DOT PAY

- **Project Name:** DOT PAY
- **Team Name:** Crypto Pay Lab (CPL)
- **Payment Address:**  3CnxDH6myTaK6MVy3SawVF2FC6FdgfK8pj （BTC address）
- **[Level]:** 2


### Overview

DotPay is a platform that supports paid tasks to complete open source projects on Github.

Our mission is:
- Attract more Github developers, especially who are not familiar with blockchain to expand the user-number of Polkadot ecosystem.
- Earn DOT tokens by completing open source tasks to encourage Github developers to communicate, cooperate and innovate with each other.


### Project Details

Page 1: task list
![image](https://user-images.githubusercontent.com/94216827/142724732-b7675c28-bfbb-492d-9f9e-e7ba53c9f4a0.png)


Page 2: Configure Github webhook
![image](https://user-images.githubusercontent.com/94216827/142724798-20a0409d-195a-47b9-ba3b-01c6c647eab5.png)


Page 3: Recharge
![image](https://user-images.githubusercontent.com/94216827/142724518-a22d1760-eeb8-4399-b0ac-e04348002beb.png)


Page 4: Creat tasks and trigger the payment 
![image](https://user-images.githubusercontent.com/94216827/142757369-7bb816ae-b834-4a80-a562-8bb21da0624f.png)



Page 5: You can withdraw  DOT tokens from the exclusive account of our platform to your other wallets (such as Polka Wallet , MetaMask ,etc)
![image](https://user-images.githubusercontent.com/94216827/142724667-f216d119-b44a-4f46-9501-18e38a35ca82.png)



### Flow-process diagram


![image](https://user-images.githubusercontent.com/94216827/142736787-f9bdb340-8703-48b5-9b5a-24dd70f42f08.png)

DotPay is a payment platform, you can initiate open source tasks and paid with DOT tokens  (for example, you can initiate paid collaboration tasks when you encounter difficulties in architecture construction, requirements analysis, document construction and testing). Those who complete the tasks as required can receive tokens after the task initiator verifies that the tasks are completed

The specific process is as follows:
1. Alice recharge Dot tokens on the platform.
2. Alice initiates paid open source tasks on the Github (such as the task about architecture construction, requirements analysis, document construction, development and testing, etc )
3. Bob accepted this task on Github and completed it!
4. Alice clicks on the payment instruction.
Github receives the instruction and trigger the webhook to contact Bob by email and other notification methods to notify that 10 DOT tokens have been put into our platform
Exclusive account Wallet.
5. trigger on chain transfer.
6. Bob withdraws 10 DOT tokens from our platform to his wallet(such as Polkawallet or MetaMask)



### Data models / API specifications of the core functionality


> Create tasks

```
{
  "id": "issue id",
  "name": "issue name",
  "repo": "paritytech/substrate",
  "author": "gavofyork",
  "pay": "10DOT",
  "describe": "issue overview",
  "createTime": "",
  "updataTime": "",
}
```

> Apply task

```
{
   "issueID": "issue id",
   "applier": "Bob",
   "applyTime": ""
}
```

> Payment

Command line in issue reply: `/pay Bob 10DOT`

```
{
   "id": "payment id",
   "from": "Alice",
   "to": "Bob",
   "amount": "10DOT",
   "RMKS": "Alice pay bob",
}
```



### An overview of the technology stack to be used

* Font-end, typescipt,react
* Backend, golang,Rust
* Devops, github action, kubenretes
* Search, MeiliSearch



### Key Functions

0. User management
    - Using github OAuth2 login, user group management. 
    
1. Email / Issue informal
    - Imformal user to withdraw their DOT tokens.

2. Webhook sever
    - Github webhook management, listen events and trigger payment.

3. Transfer module
    - Transfer by calling the API of the chain.

4. Recharge / Withdraw
    - User recharge DOT tokens if they want to pay others on Github.
    - User withdraw  DOT tokens to their own wallet.

5. Issue search
    - Users can find and filter paid collaboration tasks that meet their requirements in the issue search form.

6. Payment secrect management 
    - Create it on DotPay website and config it to github secrect to pay user DOT.



### Ecosystem Fit

As far as I am concerned, there are no similar projects in Polkadot  ecosystem. 
Maybe we have some similarities with gitcoin, there are still many differences ,dotpay will focus on open-source payment collaboration, deep integration with GitHub, closer to end-users，what's more important is we prefer to realize open source payment cooperation in Polkadot ecosystem. As we all know Polkadot offers flexible cross-chain interoperation functionality with a large user base and volume expectation, and as a mainstream cryptocurrency with high market value, DOT tokens is easier for developers to accept and be recognized，and we also believe that we will attract more Github developers especially who not familiar with blockchain to join and expand the user-number of Polkadot ecosystem.


## Team :busts_in_silhouette:


### Team members 

We will pleased to offer github accounts, LinkedIn and any other information in private.

All team members can contact privately for any specific information.

* Richard Fang: team leader, core developer

* Fugen Wang: Background development
  - responsible for the development of the website background.

* Yang Li: 
  - Responsible for front-end development.

* Peng Qiao: Rust developer 
  - Responsible for back-end development, relevant development of blockchain, payment task management module, and docking API and key management module on the chain.

 
* Wei Zhang: 
  - Responsible for operation, promotion in the open source community after the website is launched, and attracting open source projects to use our services.
 
* AdaLam:  PD/PMO  
  - Responsible for product design and project schedule management.
 
 
 
### Team's Experience


* Richard Fang:
    - As an expert in the field of cloud computing in one of the biggested Internet listed companies with 7 years of rich working  experience. 
    - The author of a well-known cloud native project which has more than 5K stars and 4k paid enterprise users. 

* Fugen Wang:
   - CEO of an Internet start-up company and manages more than a dozen employees with 7 years working experience.
  
* Yang Li:
   - Andriod/IOS front-end engineer with 5 years working experience.
 
* Peng Qiao: 
   - A core member of AI Research Institute wich is one of the top AI listed companies in China with 5 years working experience.
 
* Wei Zhang:
   - An advertising director, one of the top AI listed companies in China with 7 years of rich working experience.
 
* AdaLam: PD/PMO
  - Familiar with product design and project schedule management.


### Contact

- **Contact Name:**  AdaLam
- **Contact Email:** adalamlzy@gmail.com
- **Website:**  comming soon 

- **Contact Name:** Richard Fang
- **Contact Email:** lamelegdog@gmail.com

### Legal Structure

we will be pleased to offer specific information in private.


### Team Code Repos

https://github.com/bytepayment 

https://github.com/bytepayment/bytepay  


### Team LinkedIn Profiles

we have provided in private through Google Form.


## Development Roadmap :nut_and_bolt:

### Overview

* **Total Estimated Duration:** 16 weeks
* **Full-time equivalent (FTE):**  3
* **Total Costs:**  48,000 USD

### Milestone 1 — Product design & Develop documents
* **Estimated Duration:** 2 weeks
* **FTE:**  2.5
* **Costs:**  8,000 USD

1. website PRD 
2. Provide design documents
3. Website home page

### Milestone 2 — Core module development
* **Estimated Duration:** 4 weeks
* **FTE:**  4
* **Costs:**  10,000 USD

1. task management
2. Task creation and transfer module development completed
3. Source code / Accessible pages but not fully functional

| Number | Deliverable | Specification |
| ------------- | ------------- | ------------- |
| 0 | License | Apache 2.0 |
| 1 | User management | Using github OAuth2 login |
| 2 | Payment Secrect management | create it on page and config it to github secrect to pay user DOT.|
| 3 | Recharge module | User recharge DOT if they want to pay others on git.|
| 4 | Withdraw module | User withdraw there dot to their own wallet.|
| 5 | Github webhook management | listen hook and triggle payment.|
| 6 | Email imformal module | imformal user to withdraw their DOT.|
| 7 | Email imformal module | imformal user to withdraw their DOT.|
| 8 | Documents & Test website | You can try the test website.|

### Milestone 3 — Development
* **Estimated Duration:** 4 weeks
* **FTE:**  4
* **Costs:** 10,000 USD

1.  Core functions are basically available
2.  Source code / documentation / basic available website

### Milestone 4 — Tests
* **Estimated Duration:** 2 weeks
* **FTE:**  2
* **Costs:** 10,000 USD

1. Automated test cases and test reports
2. All functions of the website are completed

### Milestone 5 — Production & Promoted Products
* **Estimated Duration:** 2 weeks
* **FTE:**  3
* **Costs:** 10,000 USD 

1. GitHub contribution data analysis, according to the contribution of each developer to allocate rewards.
The function that can be experienced at this time is that the employer only needs to fill in the total amount of the reward, and all the contributors will automatically receive the reward. 
2. Spending analysis graph, employers can see the reward pie chart of each contributor.


## Development Status

https://github.com/bytepayment/bytepay

We have developed the webhook event processing module.
The following is a brief description of what the repository contains。
Including GitHub webhook server，it can listen to GitHub events, handle some specific instructions in the issue, and extend the instruction processor。

## Future Plans

-  About our future plan, we will support more payment scenarios, such as website recharge VIP and online payment to buy goods after completing this grant.
-  And then, we are going to support more platforms to expand the number of users, not only completing paid tasks on Github , but also on Telegram, Discord, Twitter, etc,
   and We also have an idea that cross-chain cooperation with other project.
-  After that, We will launch our own Polkadot para-chain tokens and the open source developers will receive  tokens by completing the paid tasks on Github.
