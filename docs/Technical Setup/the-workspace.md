---
title: 'The LabelBox Workspace'
author: 'Darwin Jull'
date: '2024-11-07'
last_modified_date: '2024-11-12'
---

## The Workspace: 
The workspace contains all of your projects. There is one workspace per organization. A workspace can contain multiple projects: 
![Workspace Screenshot](/img/workspace_capture.png)

You can access the workspace by clicking on the "Annotate" tab on the left side of the page.

## Projects:
Each project represents an individual labelling task. Data rows are input into projects as batches, labelled once, reviewied, and then can be input into a different project or exported.

### Project Tabs:
When you select a project, you will notice there are multiple tabs at the top of the page. A summary of each tab is provided below:
**Overview-** Self-explanatory, provides a summary of the data in the project, the status of the workflow, and the annotations present in the project.

**Data Rows-** Allows you to view and search the data rows (for our purposes, videos). The "search your data" field is especially useful for finding data rows with specific properties, such as a specific label or a specific length.

**Workflow-** Displays the steps involved in the workflow for each project. You can click on a stage in a workflow to view information about that step, and start using it.

**Settings-** Provides several key functions for managing a project. One of the most useful functions it provides is managing the members in a project.

**Other Tabs-** During my time working on the project, I haven't had a use for the performance, issues, notifications, or automation pages. This may change in the future, but they appear to be more useful for large-scale projects and large organizations.

---

### Project "Ontologies":
There is exactly **one** ontology per project. An ontology is a labelling task. The labels (also referred to as annotations in LabelBox) are applied in the first step of a project. Once reviewed, they are applied to a data row.

Ontologies can be found in the "Schema" tab on the left side of the page.

Ontologies can share annotations. An example is provided below:
![Schema Capture](/img/schema_capture.png)

---

### Working With Multiple Projects:
Using multiple projects is a means of introducting multiple labelling steps. When I designed the workflow, I chose to use multiple projects since it will allow for data rows to be filtered based on labels applied to them. Practically, this was so that videos that are unusable are not included in longer labelling tasks. The SDK can be used to perform this tasks of filtering data rows and passing them between projects automatically. Below are some notes on these two tasks and how they are done.

**Filtering Data-** Data can be filtered before it is added to a batch. You can create this filter to exclude or include data rows with any property, including labels you have already applied. You can try this for yourself by using the "search your data" field in any project or in the catalog.

**Preserving Labels-** Once a label is applied to a data row, it will remain on the data row. This label will not show up in subsequent projects. I believe there is a way to keep labels visible and modifiable in subsequent projects, and involves changing a setting in the batch creation menu. If you want to keep labels visible in subsequent projects, I advise you investigate using the SDK to accomplish it.





