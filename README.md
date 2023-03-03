# user-removal-based-on-attribute

The script starts by defining an array of AD groups to process. You can modify this array to include the groups that you want to manage. The script then loops over each group in the array and retrieves a list of members for that group. It checks each member’s attributes (country, city, and office location) to determine if they should be removed from the group.

If a member’s attribute matches one of the specified values (in this case, Estonia or Tallinn), the script outputs a message to indicate that the member will be removed from the group. It then uses the Remove-ADPrincipalGroupMembership cmdlet to remove the member from the group.

To use this script in your own environment, you’ll need to modify the group names and attribute values to match your AD setup. You may also want to modify the output message or add additional checks for other attributes.

This PowerShell script provides a convenient way to manage AD group membership based on user attributes. With a little tweaking, you can use it to automate the process of adding or removing users from groups based on specific criteria.
