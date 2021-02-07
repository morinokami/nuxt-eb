# nuxt-eb

Nuxt.js deployed to Elastic Beanstalk

```sh
$ yarn create nuxt-app nuxt-eb
? Project name: nuxt-eb
? Programming language: JavaScript
? Package manager: Yarn
? UI framework: None
? Nuxt.js modules: (Press <space> to select, <a> to toggle all, <i> to invert selection)
? Linting tools: (Press <space> to select, <a> to toggle all, <i> to invert selection)
? Testing framework: None
? Rendering mode: Universal (SSR / SSG)
? Deployment target: Server (Node.js hosting)
? Development tools: (Press <space> to select, <a> to toggle all, <i> to invert selection)
? What is your GitHub username? shinya fujino
? Version control system: Git
$ cd nuxt-eb
$ vim package.json
$ cat package.json
{
  "name": "nuxt-eb",
  "version": "1.0.0",
  "private": true,
  "scripts": {
    "dev": "nuxt",
    "build": "nuxt build",
    "start:dev": "nuxt start",
    "start": "nuxt start --port $PORT",
    "generate": "nuxt generate"
  },
  "dependencies": {
    "core-js": "^3.8.3",
    "nuxt": "^2.14.12"
  },
  "devDependencies": {}
}
$ vim .ebignore
$ cat .ebignore
node_modules

# Other stuffs
$ git add .
$ git commit -m "Initial commit"
$ yarn build
$ yarn start:dev
$ eb init

Select a default region
1) us-east-1 : US East (N. Virginia)
2) us-west-1 : US West (N. California)
3) us-west-2 : US West (Oregon)
4) eu-west-1 : EU (Ireland)
5) eu-central-1 : EU (Frankfurt)
6) ap-south-1 : Asia Pacific (Mumbai)
7) ap-southeast-1 : Asia Pacific (Singapore)
8) ap-southeast-2 : Asia Pacific (Sydney)
9) ap-northeast-1 : Asia Pacific (Tokyo)
10) ap-northeast-2 : Asia Pacific (Seoul)
11) sa-east-1 : South America (Sao Paulo)
12) cn-north-1 : China (Beijing)
13) cn-northwest-1 : China (Ningxia)
14) us-east-2 : US East (Ohio)
15) ca-central-1 : Canada (Central)
16) eu-west-2 : EU (London)
17) eu-west-3 : EU (Paris)
18) eu-north-1 : EU (Stockholm)
19) eu-south-1 : EU (Milano)
20) ap-east-1 : Asia Pacific (Hong Kong)
21) me-south-1 : Middle East (Bahrain)
22) af-south-1 : Africa (Cape Town)
(default is 3): 9


Enter Application Name
(default is "nuxt-eb"):
Application nuxt-eb has been created.

It appears you are using Node.js. Is this correct?
(Y/n):
Select a platform branch.
1) Node.js 12 running on 64bit Amazon Linux 2
2) Node.js 10 running on 64bit Amazon Linux 2
3) Node.js running on 64bit Amazon Linux
(default is 1):

Do you wish to continue with CodeCommit? (Y/n): n
Do you want to set up SSH for your instances?
(Y/n): n
$ eb create
Enter Environment Name
(default is nuxt-eb-dev):
Enter DNS CNAME prefix
(default is nuxt-eb-dev):

Select a load balancer type
1) classic
2) application
3) network
(default is 2):
$ eb open
$ eb terminate
```

- [Elastic Beanstalk concepts](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/concepts.html)
- [Install the EB CLI](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/eb-cli3-install.html)
- [Deploying an Express application to Elastic Beanstalk](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/create_deploy_nodejs_express.html)
- [Configuring your application's dependencies](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/nodejs-platform-dependencies.html)
- [Configuring the proxy server](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/nodejs-platform-proxy.html)
