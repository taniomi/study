file:: [fundamentals-of-data-engineering_1722554821038_0.pdf](../assets/fundamentals-of-data-engineering_1722554821038_0.pdf)
file-path:: ../assets/fundamentals-of-data-engineering_1722554821038_0.pdf

- Very often, data scientists struggled with basic problems that their background and training did not address—data collection, data cleansing, data access, data transformation, and data infrastructure. These are problems that data engineering aims to solve.
  ls-type:: annotation
  hl-page:: 19
  hl-color:: yellow
  id:: 66ac1ae1-e166-4491-8064-ea9f407dae9d
- We suggest that data novices read for high-level ideas and then look at materials in the Additional Resources section at the end of each chapter. On a second read through, note any unfamiliar terms and technologies. You can utilize Google, Wikipedia, blog posts, YouTube videos, and vendor sites to become familiar with new terms and fill gaps in your understanding.
  ls-type:: annotation
  hl-page:: 21
  hl-color:: yellow
  id:: 66ac1b23-5b35-4f4a-b56c-e372151f4b16
- Data engineering is one of the hottest fields in data and technology, and for a good reason. It builds the foundation for data science and analytics in production.
  ls-type:: annotation
  hl-page:: 29
  hl-color:: yellow
  id:: 66ac1b3a-975b-4e93-9deb-6d09d5f47f70
- a data engineer gets data, stores it, and prepares it for consumption by data scientists, analysts, and others.
  ls-type:: annotation
  hl-page:: 30
  hl-color:: yellow
  id:: 66ac1b49-05db-463c-824e-3b21c0c7795f
- Data engineering is the development, implementation, and maintenance of systems and processes that take in raw data and produce high-quality, consistent information that supports downstream use cases, such as analysis and machine learning. Data engi‐ neering is the intersection of security, data management, DataOps, data architecture, orchestration, and software engineering. A data engineer manages the data engineering lifecycle, beginning with getting data from source systems and ending with serving data for use cases, such as analysis or machine learning.
  ls-type:: annotation
  hl-page:: 30
  hl-color:: yellow
  id:: 66ac1b4e-43ec-4466-b179-a8c0876bbe87
- The data engineering lifecycle shifts the conversation away from technology and toward the data itself and the end goals that it must serve. The stages of the data engineering lifecycle are as follows:• Generation•• Storage•• Ingestion•• Transformation•• Serving• The data engineering lifecycle also has a notion of undercurrents—critical ideas across the entire lifecycle. These include security, data management, DataOps, data architec‐ ture, orchestration, and software engineering.
  ls-type:: annotation
  hl-page:: 31
  hl-color:: yellow
  id:: 66ac1be7-cd87-4e6a-bde4-0c1e6f0d8fa9
- The Oxford English Dictionary defines big data as “extremely large data sets that may be analyzed computationally to reveal patterns, trends, and associations, especially relating to human behavior and interactions.” Another famous and succinct descrip‐ tion of big data is the three Vs of data: velocity, variety, and volume.
  ls-type:: annotation
  hl-page:: 33
  hl-color:: yellow
  id:: 66ac1bfc-5a8d-4536-9dd2-e9430709572d
- infinitely scalable storage systems (Amazon Simple Storage Service, or S3), highly scalable NoSQL databases (Amazon DynamoDB
  ls-type:: annotation
  hl-page:: 33
  hl-color:: yellow
  id:: 66ac1c07-b466-44c2-addc-4464131a297d
- Amazon elected to offer these services for internal and external consumption through Amazon Web Services (AWS), becoming the first popular public cloud. AWS created an ultra-flexible pay-as-you-go resource marketplace by virtualizing and reselling vast pools of commodity hardware. Instead of purchasing hardware for a data center, developers could simply rent compute and storage from AWS.
  ls-type:: annotation
  hl-page:: 33
  hl-color:: yellow
  id:: 66ac1c0d-397c-4257-860a-ce65f12864f6
- Today, data is moving faster than ever and growing ever larger, but big data process‐ ing has become so accessible that it no longer merits a separate term; every company aims to solve its data problems, regardless of actual data size. Big data engineers are now simply data engineers.
  ls-type:: annotation
  hl-page:: 35
  hl-color:: yellow
  id:: 66ac1c23-dd90-45c1-9b21-dcdf92563ec1
- Data engineering is increasingly a discipline of interoperation, and connecting various technologies like LEGO bricks, to serve ultimate business goals.
  ls-type:: annotation
  hl-page:: 36
  hl-color:: yellow
  id:: 66ac1c35-d39b-436b-aebe-96338399ac8f
- While data engineers maintain skills in low-level data programming and use these as required, they increasingly find their role focused on things higher in the value chain: security, data management, DataOps, data architecture, orchestration, and general data lifecycle management.
  ls-type:: annotation
  hl-page:: 36
  hl-color:: yellow
  id:: 66ac1c45-ee2d-4bc0-89b1-3524d51d15b5
- We view the present as a golden age of data lifecycle management. Data engineers managing the data engineering lifecycle have better tools and techniques than ever before.
  ls-type:: annotation
  hl-page:: 37
  hl-color:: yellow
  id:: 66ac1c53-f2f8-45f4-be62-ecb61039f849
- Although many data scientists are eager to build and tune ML models, the reality is an estimated 70% to 80% of their time is spent toiling in the bottom three parts of the hierarchy—gathering data, cleaning data, processing data—and only a tiny slice of their time on analysis and ML. Rogati argues that companies need to build a solid data foundation (the bottom three levels of the hierarchy) before tackling areas such as AI and ML.
  ls-type:: annotation
  hl-page:: 38
  hl-color:: yellow
  id:: 66ac1c5c-6c1c-4389-86ab-3d7b3e6fbd53
- The skill set of a data engineer encompasses the “undercurrents” of data engineering: security, data management, DataOps, data architecture, and software engineering. This skill set requires an understanding of how to evaluate data tools and how they fit together across the data engineering lifecycle. It’s also critical to know how data is produced in source systems and how analysts and data scientists will consume and create value after processing and curating data. Finally, a data engineer juggles a lot of complex moving parts and must constantly optimize along the axes of cost, agility, scalability, simplicity, reuse, and interoperability
  ls-type:: annotation
  hl-page:: 39
  hl-color:: yellow
  id:: 66ac1c76-d703-4d34-b900-64ef65d066af
- Modern data tools considerably abstract and simplify workflows. As a result, data engineers are now focused on balancing the simplest and most cost-effective, best-of-breed services that deliver value to the business. The data engineer is also expected to create agile data architectures that evolve as new trends emerge.
  ls-type:: annotation
  hl-page:: 39
  hl-color:: yellow
  id:: 66ac1c8e-9aec-43a6-9dba-6fae3d2d5ec9
- What are some things a data engineer does not do? A data engineer typically does not directly build ML models, create reports or dashboards, perform data analysis, build key performance indicators (KPIs), or develop software applications.
  ls-type:: annotation
  hl-page:: 39
  hl-color:: yellow
  id:: 66ac1c95-02dd-412e-8be6-c2e405db2e51
- We half-jokingly call ourselves “recovering data scientists”, mainly from personal experience with being involved in premature data science projects without adequate data maturity or data engineering support.
  ls-type:: annotation
  hl-page:: 40
  hl-color:: yellow
  id:: 66ac1ca6-038c-41e1-a78d-a02eb740c4e9
- A data engineer’s goal is to move fast, get traction, and add value.
  ls-type:: annotation
  hl-page:: 40
  hl-color:: yellow
  id:: 66ac1cc2-a025-4edd-bbec-f1c6f436a24d
- People entering data engineering arrive with varying backgrounds in education, career, and skill set. Everyone entering the field should expect to invest a significant amount of time in self-study. Reading this book is a good starting point; one of the primary goals of this book is to give you a foundation for the knowledge and skills we think are necessary to succeed as a data engineer.
  ls-type:: annotation
  hl-page:: 43
  hl-color:: yellow
  id:: 66ac1cd5-c65f-46e6-ab0e-25f4785e9558
- By definition, a data engineer must understand both data and technology. With respect to data, this entails knowing about various best practices around data management. On the technology end, a data engineer must be aware of various options for tools, their interplay, and their trade-offs. This requires a good understanding of software engineering, DataOps, and data architecture.
  ls-type:: annotation
  hl-page:: 43
  hl-color:: yellow
  id:: 66ac1cdb-41ca-47b3-9a4f-3fb6230a2b1c
- Zooming out, a data engineer must also understand the requirements of data con‐ sumers (data analysts and data scientists) and the broader implications of data across the organization. Data engineering is a holistic practice; the best data engineers view their responsibilities through business and technical lenses.
  ls-type:: annotation
  hl-page:: 44
  hl-color:: yellow
  id:: 66ac1ce4-664a-4fb5-97da-28a657f83f76
- Know how to communicate with nontechnical and technical people.
  ls-type:: annotation
  hl-page:: 44
  hl-color:: yellow
  id:: 66ac1cea-0693-4d24-a120-296949f4e56a
- Learn continuously.
  ls-type:: annotation
  hl-page:: 44
  hl-color:: yellow
  id:: 66ac1cef-0b79-44e7-bf0e-0fa3efcd9d06
- What languages should a data engineer know? We divide data engineering program‐ ming languages into primary and secondary categories. At the time of this writing, the primary languages of data engineering are SQL, Python, a Java Virtual Machine(JVM) language (usually Java or Scala), and bash:
  ls-type:: annotation
  hl-page:: 46
  hl-color:: yellow
  id:: 66ac1d01-be23-4306-8e4e-97580edfb587
- Given that time is a primary constraint for data engineering team throughput, engi‐ neers should embrace tools that combine simplicity and high productivity.
  ls-type:: annotation
  hl-page:: 47
  hl-color:: yellow
  id:: 66ac1d0c-322b-4b04-a174-22eb0a7f18c6
- Keeping Pace in a Fast-Moving Field Once a new technology rolls over you, if you’re not part of the steamroller, you’re part of the road.—Stewart Brand How do you keep your skills sharp in a rapidly changing field like data engineering? Should you focus on the latest tools or deep dive into fundamentals? Here’s our advice: focus on the fundamentals to understand what’s not going to change; pay attention to ongoing developments to know where the field is going. New paradigms and practices are introduced all the time, and it’s incumbent on you to stay current. Strive to understand how new technologies will be helpful in the lifecycle.
  ls-type:: annotation
  hl-page:: 47
  hl-color:: yellow
  id:: 66ac1d12-a99a-4419-9821-56f13f498c15
- Type A data engineers A stands for abstraction.
  ls-type:: annotation
  hl-page:: 48
  hl-color:: yellow
  id:: 66ac1d19-6bdf-4a1d-8185-9bc637056ea3
- Type B data engineers B stands for build.
  ls-type:: annotation
  hl-page:: 48
  hl-color:: yellow
  id:: 66ac1d1f-f784-48ca-bf64-6c7791cd908f
- Type A and type B data engineers may work in the same company and may even be the same person!
  ls-type:: annotation
  hl-page:: 48
  hl-color:: yellow
  id:: 66ac1d26-602d-470a-be84-2f3a835923e4
- The data engineer is a hub between data producers, such as software engineers, data architects, and DevOps or site-reliability engineers (SREs), and data consumers, such as data analysts, data scientists, and ML engineers. In addition, data engineers will interact with those in operational roles, such as DevOps engineers.
  ls-type:: annotation
  hl-page:: 50
  hl-color:: yellow
  id:: 66ac1d3a-cd0b-4026-b4e1-af5bfe7ee3b5
- To be successful as a data engineer, you need to understand the data architecture you’re using or designing and the source systems producing the data you’ll need.
  ls-type:: annotation
  hl-page:: 51
  hl-color:: yellow
  id:: 66ac1d43-b9b6-444f-bbc5-cc209ea90ea8
- Depending on the company’s data maturity and size, a data engineer may overlap with or assume the responsibilities of a data architect. Therefore, a data engineer should have a good understanding of architecture best practices and approaches.
  ls-type:: annotation
  hl-page:: 51
  hl-color:: yellow
  id:: 66ac1d48-7453-429b-8f73-c77ab6e83fbf
- A data engineer should work together with software engineers to understand the applications that generate data, the volume, frequency, and format of the generated data, and anything else that will impact the data engineering lifecycle, such as data security and regulatory compliance
  ls-type:: annotation
  hl-page:: 52
  hl-color:: yellow
  id:: 66ac1d52-d31c-4dae-aa20-d1388ad88805
- A data engineer should work together with software engineers to understand the applications that generate data, the volume, frequency, and format of the generated data, and anything else that will impact the data engineering lifecycle, such as data security and regulatory compliance.
  ls-type:: annotation
  hl-page:: 52
  hl-color:: yellow
  id:: 66ac1eca-2056-43f4-a84e-94333a728035
- Data scientists build forward-looking models to make predictions and recommendations. These models are then evaluated on live data to provide value in various ways
  ls-type:: annotation
  hl-page:: 52
  hl-color:: yellow
  id:: 66ac1ed0-834c-425b-b540-be174bbb6551
- According to common industry folklore, data scientists spend 70% to 80% of their time collecting, cleaning, and preparing data.12 In our experience, these numbers often reflect immature data science and data engineering practices.
  ls-type:: annotation
  hl-page:: 52
  hl-color:: yellow
  id:: 66ac1ed8-754b-4012-a9bc-1a6d6fc9f2d7
- The need for production-ready data science is a significant driver behind the emer‐ gence of the data engineering profession. Data engineers should help data scientists to enable a path to production. In fact, we (the authors) moved from data science to data engineering after recognizing this fundamental need. Data engineers work to provide the data automation and scale that make data science more efficient.
  ls-type:: annotation
  hl-page:: 53
  hl-color:: yellow
  id:: 66ac1ee4-535b-43b7-a83c-e6185068e57f
- Data analysts (or business analysts) seek to understand business per‐ formance and trends. Whereas data scientists are forward-looking, a data analyst typically focuses on the past or present.
  ls-type:: annotation
  hl-page:: 53
  hl-color:: yellow
  id:: 66ac1ee9-baff-4c82-8d23-3adc43d1ea49
- ML engineers often have advanced working knowledge of ML and deep learning techniques and frameworks such as PyTorch or TensorFlow.
  ls-type:: annotation
  hl-page:: 53
  hl-color:: yellow
  id:: 66ac1eef-3866-43e0-8559-963d84bb9193
- A chief information officer (CIO) is the senior C-suite executive responsible for information technology within an organization; it is an internal-facing role. A CIO must possess deep knowledge of information technology and business processes—either alone is insufficien
  ls-type:: annotation
  hl-page:: 55
  hl-color:: yellow
  id:: 66ac1ef9-8afd-4127-bdcf-c97cc75c3445
- A chief technology officer (CTO) is similar to a CIO but faces outward. A CTO owns the key technological strategy and architectures for externalfacing applications, such as mobile, web apps, and IoT—all critical data sources for data engineers
  ls-type:: annotation
  hl-page:: 55
  hl-color:: yellow
  id:: 66ac1efe-f0df-4a1d-832d-045e2419beba
- The CDO is respon‐ sible for a company’s data assets and strategy. CDOs are focused on data’s business utility but should have a strong technical grounding.
  ls-type:: annotation
  hl-page:: 55
  hl-color:: yellow
  id:: 66ac1f04-480e-4b01-88a5-258ca2488bed
- Companies don’t hire engineers simply to hack on code in isola‐ tion. To be worthy of their title, engineers should develop a deep understanding of the problems they’re tasked with solving, the technology tools at their disposal, and the people they work with and serve.
  ls-type:: annotation
  hl-page:: 57
  hl-color:: yellow
  id:: 66ac1f0c-06d9-4fe2-992e-a04129cab183
- Chapter 1 of What Is Data Engineering? by Lewis Gavin (O’Reilly)
  ls-type:: annotation
  hl-page:: 58
  hl-color:: yellow
  id:: 66ac1f24-d8d5-4b1b-a2cb-fa8e2282a00b
- “The Downfall of the Data Engineer” by Maxime Beauchemin
  ls-type:: annotation
  hl-page:: 58
  hl-color:: yellow
  id:: 66ac1f2a-f967-4d14-840c-b411dd201202
- “The Rise of the Data Engineer” by Maxime Beauchemin
  ls-type:: annotation
  hl-page:: 58
  hl-color:: yellow
  id:: 66ac1f30-0d49-45b1-864a-fbc2ef66cfd0
- Because of increased technical abstraction, data engineers will increasingly become data lifecycle engineers, thinking and operating in terms of the principles of data lifecycle management.
  ls-type:: annotation
  hl-page:: 59
  hl-color:: yellow
  id:: 66ac1f3d-3062-4c17-b93e-d6048564d04e
- We begin the data engineering lifecycle by getting data from source systems and storing it. Next, we transform the data and then proceed to our central goal, serving data to analysts, data scientists, ML engineers, and others. In reality, storage occurs throughout the lifecycle as data flows from beginning to end—hence, the diagram shows the storage “stage” as a foundation that underpins other stages.
  ls-type:: annotation
  hl-page:: 60
  hl-color:: yellow
  id:: 66ac1f44-e2dd-4aa9-a63f-3e664e7a9e9b