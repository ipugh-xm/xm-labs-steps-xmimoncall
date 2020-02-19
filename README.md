# xmimoncall Steps

This step can put a user on call in a group on a shift.


---------

<kbd>
  <img src="https://github.com/xmatters/xMatters-Labs/raw/master/media/disclaimer.png">
</kbd>

---------

# Files

* [xmimoncallSteps.zip](xmimoncallSteps.zip) - Workflow zip file with the step and example flow
* [xm.png](/xm.png) - xMatters logo

# How it works
This step puts the user who called it on call for a specified shift and on a specified team.


# Installation

## xMatters Setup
1. Download the [xmimoncallSteps.zip](xmimoncallSteps.zip) file onto your local computer
2. Navigate to the Developer tab of your xMatters instance
3. Click Import, and select the zip file you just downloaded


## Usage
The **xmimoncall** step is now available in your custom steps. So navigate to the appropriate canvas so you can add the step there. If you'd like to experiment with it, the **xmimoncall** workflow has a canvas that can be triggered via HTTP call. 

### Inputs
| Name  | Required? | Min | Max | Help Text | Default Value | Multiline |
| ----- | ----------| --- | --- | --------- | ------------- | --------- |
| user_name  | Yes | 0 | 2000 | Name of user to put on call  | | No |
| group_sep_character  | Yes | 0 | 2000 | The character to separate the groups | ',' | No |
| groups  | Yes | 0 | 2000 | Groups separated by group_sep_character | | No |
| shifts  | Yes | 0 | 2000 | Shift to put on call for | 'Default Group' | No |


### Outputs

| Name | Description |
| ---- | ----------  |
| result | 'success' or 'failure' depending on 100% success or not |
| rejected_groups | Groups failed to put user on call for |


## Example
This is an example of a slack slash command calling **xmimoncall** to put the user who called it on call.

<kbd>
	<img src="/media/ExampleFlow.png">
</kbd>

