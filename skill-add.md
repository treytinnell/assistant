---

copyright:
  years: 2015, 2019
lastupdated: "2019-11-12"

subcollection: assistant

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:deprecated: .deprecated}
{:important: .important}
{:note: .note}
{:tip: .tip}
{:pre: .pre}
{:codeblock: .codeblock}
{:screen: .screen}
{:javascript: .ph data-hd-programlang='javascript'}
{:java: .ph data-hd-programlang='java'}
{:python: .ph data-hd-programlang='python'}
{:swift: .ph data-hd-programlang='swift'}

# Creating a skill
{: #skill-add}

Customize your assistant by adding to it the skills it needs to satisfy your customers' goals.
{: shortdesc}

You can create the following type of skill:

- **Dialog skill**: Uses Watson natural language processing and machine learning technologies to understand user questions and requests, and respond to them with answers that are authored by you.

- **Search skill** ![Plus or Premium plan only](images/plus.png): For a given user query, uses the {{site.data.keyword.discoveryfull}} service to search a data source of your self-service content and return an answer.

  Only users of Plus or Premium plans can create this type of skill.
  
  Typically, you create a skill of each type first. Then, as you build a dialog for the dialog skill, you decide when to initiate the search skill. For some questions or requests, a hard-coded or programmatically-derived response (that is defined in the dialog skill) is sufficient. For others, you might want to provide a more robust response by returning a full passage of related information (that is extracted from an external data source by using the search skill).

## Create the skill
{: #skill-add-task}

You can add one skill of each skill type to an assistant.

To create a skill, complete the following step:

1.  Click the **Skills** icon ![Skills menu icon](images/nav-skills-icon.png), and then click **Create skill**.

1.  Choose the type of skill to create, and then click **Next**.

    Follow the remaining steps in the appropriate procedure to complete the skill creation process.

      - [Dialog Skill](/docs/services/assistant?topic=assistant-skill-dialog-add)
      - [Search Skill](/docs/services/assistant?topic=assistant-skill-search-add)

## Skill limits
{: #skill-add-limits}

The number of skills you can create depends on your {{site.data.keyword.conversationshort}} plan type. Any sample dialog skills that are available for you to use do not count toward your limit unless you use them. A skill version does not count as a skill.

| Plan     | Maximum number of skills of each type per service instance |
|------------------|----------------------------:|
| Premium          |                          50 |
| Plus             |                          50 |
| Standard         |                          20 |
| Lite`*`, Plus Trial |                        5 |
{: caption="Plan details" caption-side="top"}

`*` After 30 days of inactivity, an unused skill in a Lite plan service instance might be deleted to free up space.

## Deleting a skill
{: #skill-add-delete}

You can delete any skill that you can access, unless it is being used by an assistant. If it is in use, you must remove it from the assistant that is using it before you can delete it.

Be sure to check with anyone else who might be using the skill before you delete it.
{: tip}

To delete a skill, complete the following steps:

1.  Find out whether the skill is being used by any assistants. From the Skills page, find the tile for the skill that you want to delete. The **Assistants** field lists the assistants that currently use the skill.

1.  If the skill you want to delete is associated with an assistant, then remove it from the assistant by completing the following steps:

    - Check with the owner of the assistant that is using the skill before you remove the skill from it.
    - Open the Assistants page, and then click to open the assistant tile.
    - Find the tile for the skill that you want to delete. Click the ![open and close list of options](images/kabob-beta.png) icon, and then choose **Remove**.
    - Repeat the previous steps for any other assistants that use the skill.
    - Return to the Skills page and find the tile for the skill that you want to delete.

1.  Click the ![open and close list of options](images/kabob-beta.png) icon, and then choose **Delete**. Confirm the deletion.
