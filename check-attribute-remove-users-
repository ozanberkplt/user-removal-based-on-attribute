$groups = @("Group1","Group2","Group3")
foreach ($group in $groups) {
  $members = Get-ADGroupMember -Identity $group | Get-ADUser -Properties co,l,physicalDeliveryOfficeName
  
  foreach ($member in $members) {
    if ($member.co -eq "Estonia" -or $member.l -eq "Tallinn" -or $member.physicalDeliveryOfficeName -eq "Tallinn") { 
      Write-Output "$($member.Name) is from $group and has 'Estonia or 'Tallinn' in their attributes. Removing from the group..."
     Remove-ADPrincipalGroupMembership -Identity $member -MemberOf $group -Confirm:$false
    }
  }
}
