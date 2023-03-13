---
title: UI Overview
---

This page describes each of the pages in the Policy Manager UI. Some pages described here are only accessible to users with a [certain set of privileges](/policies/users/getting_started/policy_roles.html#policy-roles-overview-).

## Catalog

Catalog is the central place for viewing published templates available in your organization that can be applied to individual or multiple accounts. The policies in the Catalog are a combination of the [Flexera pre-built policies](../policy_list.html) along with any policies published by your organization. Users with `policy_publisher` role can choose to un-publish policy templates that they do not wish to make available to other users in the organization.

![policy_catalog.png](/img/policy_catalog.png)

## Dashboard

Dashboard provides a summary view of what is happening in the selected account. It shows important information about Applied Policies and Incidents to give you complete insights to take actions. Use the **Account selector drop-down** at the top of the page to change accounts, or the Organization Summary selection to see information from across the organization (only available to users with organization-level access to policy manager).

![policy_dashboard_v1.png](/img/governance-policy-dashboard.png)

## Applied Policies

This view shows all applied policies running in the account. Using the **Account selector drop-down** at the top of the page, you can switch between different accounts to see the applied policies in each account. You can choose to view complete details on the policy or take actions like updating the policy, terminating it or applying a similar one. Details on each of the actions available on an Applied Policy can be found below.

![policy_applied.png](/img/governance-applied-policy.png)

### Apply Similar

This action makes it seamless to quickly apply a similar policy in a different account or tweaking the input parameters for a new policy. Just click the actions menu and hit **Apply Similar** and the system will try to pre-fill input parameters from the original policy.

### Run Now

This action will trigger an evaluation immediately instead of waiting until the next scheduled evaluation time.

### View Log

This action, only available to certain users, shows a detailed log of the policy behavior. It includes details of all API calls, responses, and data used for evaluating and showing the policy data.

### Terminate

Terminates this applied policy, removing all information related to the policy, any incidents, and log information.

### Update Configuration

All (configuration options)[/policies/users/guides/apply_policy.html#common-policy-configuration-options-], except credentials, can be changed on a running policy. Select the applied policy from the `Applied Policies` screen with `Organizational Summary` selected in the account selector dropdown and click the **Edit** button. Updated policies will immediately evaluate after updating. For policies with no changes to frequency, an update will not effect their normal evaluation schedule.

If you don't see the **Edit** button, make sure you have `Organizational Summary` selected in the account selector dropdown.

If you don't have the [`Organizational Summary` option](/policies/users/getting_started/policy_roles.html#policy-roles-overview--access-levels-) in the account selector dropdown you are not able to update policy configurations. Instead, use the [`Apply Similar` action](#applied-policies--apply-similar-) to create a new applied policy.

If you need to change the [credentials]/policies/users/guides/credential_management.html) a policy is using, use the [`Apply Similar` action](#applied-policies--apply-similar-) to create a new applied policy.

![policy_update.png](/img/policy_update.png)

### Incidents

Similar to the Applied Policies page, this view shows all incidents generated by policies over time. You can see complete details on the Incident along with resources, actions, approvals and/or resolutions.

![policy_incidents.png](/img/policy_incidents.png)

## Templates

The view is for policy designers so they can upload Policy Templates for testing before publishing them to the Organization for wider use. To publish a policy template, you will need a special organization level role `policy_publisher`. For more information on custom policies, see [the policy developers guide](/policies/developers).

![policy_template.png](/img/policy_template.png)

### Policy Publishing Flow

Below diagram outlines how the policy engine works. Typically a policy developer will develop policy templates and test them by uploading to the **Templates** page. Once the policy template is ready to be published, `policy_publisher` can choose to publish it to the **Catalog** making it available to everyone in the organization.

![policy_interaction.png](/img/policy_interaction.png)

![policy_publish_step1.png.png](/img/policy_publish_step1.png)

![policy_publish_success.png](/img/policy_publish_success.png)
