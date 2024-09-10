# Technical Debt Management Process

Technical Debt (TD) is a metaphor that expresses the immaturity of software artifacts and their impacts on maintenance activities and product evolution. As organizations become able to identify and understand the effects of Technical Debt, challenges arise when making investment decisions to pay it off. Although several theoretical and practical studies have been developed recently, studies that adapt the context and stakeholders objectives for Technical Debt Management (TDM) are still lacking.

This article aims to define and implement an incremental and evolutionary process of Technical Debt Management in software development, validated in a real industry application context. This study includes a new process to manage Technical Debt, which can be used to guide the company in the search for better results, periodically reviewing the practices and decisions adopted. The process provides guidelines that can be tailored for other organizations or contexts.

The Technical Debt Management Process proposed is presented in Figure below. It involves systematically applying procedures and practices to implement effective Technical Debt Management successfully. The process should be seen as iterative. It considers the context and the strategies to achieve the objectives. At each new iteration, or cycle, the results are evaluated, the objectives and the teams' capacity are reviewed to evolve in the Technical Debt Management goal. 

Each iteration starts with a Context activity that sets the ground for the others and ends with a Review activity that analyzes the results and prepares for the next iteration. Communication and monitoring is an activity that takes place along all the processes. Technical Debt Assessment is divided into Discovery, Analysis, Identification, and Measurement tasks. Technical Debt Repayment is divided into Prioritization and Payment tasks. TD Prevention is a continuous activity that the technical team must internalize.

<img src="TDMProcess.png" alt="drawing" width="1200"/>

## Activity: Context
In the definition of the context of the Technical Debt Management, the objectives, the scenario, the type of Technical Debt that will be managed, the stakeholders, and the criteria to achieve the objectives are described. This understanding is communicated to stakeholders to validate the information.

Different types of Technical Debt may require other forms of measures [1]. Technical Debt can occur in various artifacts throughout the product life cycle, having a distinct nature depending on when it is incurred and the activities with which it is associated [2]. A Technical Debt Management policy should be based on both the business context of a company and the technological environment in which it operates.

>:hammer: **Tasks**: 
>-	Define the objectives: the objectives may have different aspects, such improve the internal or external quality of the product, decreasing the development cost, decreasing the onboarding time for newly hired professionals, among others. It also can be applied to different technologies.
>-	Establish and strategy: the organization must devise its strategy to manage Technical Debt. A strategy has four pillars: mission, goal, strategy, and policies.
>-	Identify the opportunities and threats: for effective Technical Debt Management, it is essential to support decision-making by external and internal Technical Debt opportunities and threats related to the software product.
>-	Identify expected results: align the expected results with stakeholders' expectations. It is crucial to define key performance indicators to monitor the results during the monitoring of the Technical Debt Management.
>-	Select the technologies: consider the standards inherent the technologies that will be managed.
>-	Identify the impact on existing projects and processes: identify the teams and projects affected and the need for changes in the software development process.
>-	Define tools, resources, or standards: the context should foresee the study and implementation of new tools and standards needed for Technical Debt Management.
>-	Determine the extent of each cycle: determine a start and end period for performance analysis, then review the process for the next period.
>-	Identify risks: know the risks that may affect the objectives and decision-making, foreseeing strategies to mitigate and manage them.
>
>:outbox_tray: **Outcomes**: Technical Debt Management criteria, Goals, Strategies, Action Plans, Responsibles, List of Artifacts (e. g. PHP source code), Risks, KPIs, and Tools.
>
>:guardsman: **Responsible Role**: Technical Debt Manager.
>
>:busts_in_silhouette: **Other participant roles**: Sponsors, Managers and Team leads.

## Technical Debt Assessment
The Technical Debt assessment consists of Discovery, Analysis, Identification, and Measurement tasks. It is suggested to occur systematically and collaboratively with all stakeholders.

### Activity: Discovery
The purpose of the Technical Debt Discovery task is to recognize the types and the Technical Debt that are important to achieve the objectives of the context. Technical Debt Discovery can occur at any stage of the software life cycle. This is a critical activity once a Technical Debt not finding at this point will not be included in later analysis. This activity results must be aligned with the objectives and outcomes expected by the stakeholders, as defined in the previous step.

It is essential at this stage to rely on the experience and skills of the development team to detection the Technical Debts that are part of the context, independ if are not automatically recognized by the tools.

>:hammer: **Tasks**:
>-	Choose the Technical Debt type: identify which types of Technical Debt can be related to the artifacts in the context;
>-	Discovery the Technical Debt: Technical Debt discovery is a procedure to identify the characteristics of artifacts that hinder the evolution and maintenance of the software and that are outside the standard defined in the context (e.g. poor desing, performance, outdated documentation). Suggested tools for this task are meetings, brainstorming, and interviews with stakeholders and experts;
>-	Use automated tools: it is important to use automated tools to collect data and information to enable the discovery of Technical Debts that are appropriate to the context. For example, the use of automated tools: SonarQube has several rules for identifying Technical Debts, using this type of tool contributes to this activity.
>
>:outbox_tray: **Outcomes**: Technical Debt list (e. g. Design Debt: Complex code, Coding pattern violation).
>
>:guardsman: **Responsible Role**: Technical Debt Manager.
>
>:busts_in_silhouette: **Other participant roles**: Technical and product experts.

### Activity: Analysis
The Analysis task involves developing a deep understanding of each Technical Debt discovered. Technical Debt Analysis provides the information that will be the basis for decision making and the levels of detail that will be used in the Technical Debt Identification.

In this activity, for each Technical Debt a set of elements that define the Technical Debt is recorded. 

To understand the features of the Technical Debt, the management context is considered to define the purpose of the analysis. The analysis can be carried out with various levels of detail and complexity and can be qualitative or quantitative, depending on the purpose of the analysis.

In the analysis, the common characteristics of each Technical Debt are understood and documented, which will be used in the next activities. The common characteristics help in the management of large quantities of Technical Debt Items, because these scenarios require a lot of effort making it unfeasible to identify the particular characteristics of each Technical Debt Item. The information extracted in this activity can help in the creation of Technical Debt prevention strategies. In this step the tools that will be used in the Technical Debt Management are selected and validated.

>:hammer: **Tasks**:
>-	Registration of the Technical Debt: in this task you must complement the Technical Debt registration with relevant information that will be used in the next activities. We highlight the following information: detailed description of the Technical Debt, example of how to identify the Technical Debt; compliant solution; artifacts to which the Technical Debt applies; specific parameters (e. g. convention, suspicious, bad-practice);
>-	Define default characteristics:
>    -	Impact: is a rating of the importance of Technical Debt to the context;
>    -	Effects: identify the negative implications or consequences of Technical Debt. This information can assist in prioritizing Technical Debt Items;
>    -	Cause: identify the reasons or motives that led to the existence of Technical Debt;
>    -	Principal estimation: cost estimate to eliminate a Technical Debt Item.
>-	Tool approval: there are several tools available to support Technical Debt Management activities (e. g. Sonar Qube, Fixbugs, CAST, Jira). The selected tools should go through a validation and approval process, where one should know in detail the purpose and the results that can be used in Technical Debt Management.
>
>:outbox_tray: **Outcomes**: Technical Debt documentation done, Cause list, Effect list, Impact list, Tools approved.
>
>:guardsman: **Responsible Role**: Technical Debt Manager.
>
>:busts_in_silhouette: **Other participant roles**: Technical and Product experts.

### Activity: Identification
The Technical Debt Items are identified and documented in this step. Previous steps provide an understanding of the Technical Debt and the environment (e.g., where the Technical Debt Items reside) established when the context was considered.

The results of the Technical Debt Identification must be accessible, communicated, and validated with all the stakeholders. A good practice is to use automated static source code analysis tools to find the Technical Debt Items.

>:hammer: **Tasks**:
>-	Identify the Technical Debt Items: in this task the Technical Debt Items are identified and registered. The Technical Debt Item must have a reference of the artifact where it was found. The Technical Debt Items can be identified manually or automatically by previously approved tools;
>-	Update the characteristics: initially the Technical Debt Item receives the standard characteristics defined for the Technical Debt, these characteristics must be reviewed and updated;
>-	Responsible party: the Technical Debt Item must have a responsible party that has the commitment to monitor or delete the Technical Debt Item, initially the responsible party for the Technical Debt Item is defined as being the same responsible party for the artifact. The suggested responsible parties for a Technical Debt Item are: team, project, leader, and developer.
>
>:outbox_tray: **Outcomes**: Technical Debt Items list.
>
>:guardsman: **Responsible Role**: Technical Debt Manager.
>
>:busts_in_silhouette: **Other participant roles**: Artifact responsible.

### Activity: Measurement
In the Technical Debt Measurement activity the Technical Debt values are determined and the planned results are transformed into Technical Debt payment targets. In this activity the values of the principal and interest of the Technical Debt Item are reviewed and estimated. 

The Technical Debt Measurement activity seeks to generate values that fit the needs of the decision makers. The measurements generated in this activity can be used to evaluate the Technical Debt Management process, because it is possible to use the values from the beginning of the process as a basis for evaluating the evolution in the Technical Debt payment.

The information generated in this activity is used in decision-making, mainly about which Technical Debt needs actions and initiatives and how the Technical Debt will be controlled and decreased.

>:hammer: **Tasks**:
>-	Principal estimation: starting from the principal value suggested in Analysis Technical Debt, in this task the principal estimation per item of Technical Debt is reviewed;
>-	Interest estimation: given the difficulty in obtaining a precise value for the current or expected interest, interest information can be estimated. The estimated value for interest can be either quantitative, using historical data of the artifact to calculate an approximate value for maintainability, or qualitative in the form of a rating (e. g. Very High, High, Medium, Low, Very Low);
>-	Targets: in this task you define the targets for decreasing the amount of Technical Debt. This target can be defined based on the resources available for the payment of Technical Debt and the estimated principal value.
>
>:outbox_tray: **Outcomes**: Updated Technical Debt Items list, Target.
>
>:guardsman: **Responsible Role**: Technical Debt Manager.
>
>:busts_in_silhouette: **Other participant roles**: Sponsors, Managers and Team Leads.

## Technical Debt Repayment
Technical Debt Repayment refers to the activities carried out to support decision-making about the most appropriate time to eliminate items from the debt. 

### Activity: Prioritization
Technical Debt prioritization is about deciding which Technical Debt Items are to be repaid first and which items will be delayed until later releases [4]. Prioritization should provide information to support decision-making about which Technical Debt Item should be paid.

The output of this activity should be a list of Technical Debt Items eligible for payment.

>:hammer: **Task**:
>-	Prioritization: arrange the Technical Debt Items in order of importance for the context. Important in this task to consider the available resources when selecting candidate Technical Debt Items for payment.
>
>:outbox_tray: **Outcomes**: Technical Debt Items list for payment.
>
>:guardsman: **Responsible Role**: Technical Debt Manager.
>
>:busts_in_silhouette: **Other participant roles**: Team Leads, Artifact responsible.

### Activity: Payment 
The Payment activity involves the selection and implementation of one or more actions to change the current situation of Technical Debt. The choice of the most appropriate actions consists of analyzing the efforts, resources, and benefits generated to achieve the objectives.

Technical Debt payment actions can be manual or automatic, using approved tools in the Analysis activity.

>:hammer: **Task**:
>-	Eliminate Technical Debt Item: for the prioritized Technical Debt Items, tasks are generated where resources and deadlines are defined to eliminate them.
>
>:outbox_tray: **Outcomes**: Updated Technical Debt Items list.
>
>:guardsman: **Responsible Role**: Technical Debt Manager.
>
>:busts_in_silhouette: **Other participant roles**: Team Leads, Artifact responsible.

## Activity: Prevention
The Technical Debt prevention activity acts within the software development process, with actions to prevent the appearance of Technical Debt.Prevention refers to activities whose objective is to prevent the occurrence of Technical Debt [3]. Technical Debt Prevention can be seen as one of the most influential activities of the Technical Debt Management that a development team can conduct. When the development team has set up mandatory coding standards, assisted with, e.g., code reviews and Definition of Done practice, the amount of Technical Debt that gets to the code base may decrease. When Technical Debt is prevented as much as possible, it also helps other Technical Debt Management activities. In addition, setting up Technical Debt prevention practices helps catch inexperienced developers’ ‘not-so-good’ solutions [3].

>:hammer: **Tasks**:
>-	Identify potential problems: review the software development activities that are part of the Technical Debt Management context, to propose changes to avoid the appearance of Technical Debt;
>-	Create preventive actions: analyze the causes and create actions to intervene the appearance of Technical Debt (e. g. training, coding tools).
>
>:outbox_tray: **Outcomes**: Action plan, Change in the Software development process.
>
>:guardsman: **Responsible Role**: Technical Debt Manager.
>
>:busts_in_silhouette: **Other participant roles**: Managers and team leads.

## Activity: Review
The Review activity has the purpose of evolving the Technical Debt Management process. The Technical Debt Management process must be periodically reviewed, however the need to review the management process can be identified during the monitoring and critical analysis activity. 

After Review activity, must return to the Context because the objectives and management needs may change over time.

>:hammer: **Tasks**:
>-	Identify lessons learned: extract the knowledge acquired in the previous steps that can be used in the next cycle of the Technical Debt Management;
>-	Approve the revision: align with stakeholders the objectives of the need for the revision of the Technical Debt Management.
>
>:outbox_tray: **Outcomes**: Lesson learned, Review approved.
>
>:guardsman: **Responsible Role**: Technical Debt Manager.
>
>:busts_in_silhouette: **Other participant roles**: Managers and Team leads.

## Activity: Communication and monitoring
Communication takes place in all activities of Technical Debt Management, as it must ensure that all those responsible and stakeholders understand the rationale and reasons on which decisions are made.

Communication should ensure that the objectives are understood, inform and raise awareness of those involved, communicate the decisions and criteria used, facilitate the exchange of information, gather different points of view, and obtain feedback and suggestions.

The monitoring of Technical Debt Items should be planned together with the Technical Debt Management process. The monitoring activity occurs during the evolution or maintenance of the software. The monitoring can be periodic or a notice when updating or changing the source code.

During the monitoring, the critical and periodic analysis of the management process and the progress of actions must occur. The use of automated tools and websites or wikis, with updated information available to interested parties, helps in the monitoring and control activity of Technical Debt.

>:hammer: **Tasks**:
>-	Periodically monitor the Technical Debt: the Technical Debt should be periodically analyzed and monitored along with those responsible. This monitoring can be done with periodic meetings where those responsible should report the status of the payment tasks of Technical Debt, emphasizing points of attention and deliveries that were performed (or should have been);
>-	Spot management: generate relevant information for managers and stakeholders, allowing the monitoring of indicators, status and trends of Technical Debt. One of the practices of view management can be the creation of online dashboards;
>-	Monitoring preventive actions: this task should verify and notify those responsible of the progress of Technical Debt's preventive actions.
>
>:outbox_tray: **Outcomes**: Meeting, Reports, Dashboard, Feedback.
>
>:guardsman: **Responsible Role**: Technical Debt Manager.
>
>:busts_in_silhouette: **Other participant roles**: Stakeholders.

## Strategies and tools
From our experience, we compiled the following guidelines to make an effective and efficient Technical Debt Management:
1.	Commitment and support: the effectiveness of Technical Debt Management depends on the commitment of the team and the support of stakeholders, especially senior management;
2.	Integration to the software development process: Technical Debt Management should be treated as an integral part of the software development process instead of a project with a deadline. Monitoring should be continuous; 
3.	Team skills: Technical Debt Management needs qualified people with technical knowledge and several skills to identify the Technical Debt and properly guide the actions. The best professionals must be allocated to such tasks;
4.	Improvement in information: Technical Debt Management can be based on historical and current information and future expectations. It is essential that the data is available to all and presented in a way that all stakeholders understand the origin and transformation of the data;
5.	Tailored process: the objectives for Technical Debt Management should be personalized and adherent to the organizational context;
6.	Resource allocation: it is convenient for those responsible for resources to ensure appropriate resources for Technical Debt payment. This means qualified people, proper tools, documented processes, and procedures;
7.	Training and knowledge transfer: changes in procedures and new guidelines for software development should be passed on to all those involved, ensuring technical capacity for activities execution. It is important to seek training in standards and good practices of development within the context of Technical Debt Management;
8.	Attention to the dynamics: the Technical Debt can appear or disappear as the source code or context changes. Technical Debt Management should be aware to detect, recognize, and answer to these changes accordingly;
9.	Change of culture: Technical Debt Management can cause changes in how software is developed. These changes can cause initial discomfort in the development team and need support from stakeholders;
10.	Continuous improvement: the behavior and culture of developers significantly influence continuous improvement through learning and experiences acquired in the Technical Debt Management process. Technical Debt Management is a lifelong commitment.



### References
[1] 	Y. Guo and C. Seaman, “A Portfolio Approach to Technical Debt Management”,  MTD '11: Proceedings of the 2nd Workshop on Managing Technical Debt, 2011.

[2] 	H. Ghanbari, T. Besker, A. Martini and J. Bosch, “Looking for Peace of Mind? Manage your (Technical) Debt. An Exploratory Field Study”, 2017 ACM/IEEE International Symposium on Empirical Software Engineering and Measurement (ESEM), 2017.

[3] 	J. Yli-Huumo, A. Maglyas and K. Smolander, “How do software development teams manage technical debt? - An empirical study”, Journal of Systems and Software, 2016.

[4] 	Z. Li, P. Avgeriou and P. Liang, “A systematic mapping study on technical debt and its management”, Journal of Systems and Software, 2015. 
