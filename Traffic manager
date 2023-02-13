Connect-AzAccount
$profile_name = "BluegreenTrafficManager"
$endpoint_name_1 = "Blue"
$endpoint_name_2 = "Green"
$endpoint_status_1 = (Get-AzTrafficManagerEndpoint -Name $endpoint_name_1 -ProfileName $profile_name).EndpointStatus
$endpoint_status_2 = (Get-AzTrafficManagerEndpoint -Name $endpoint_name_2 -ProfileName $profile_name).EndpointStatus
Write-Output "The status of the Traffic Manager endpoint $endpoint_name_1 is: $endpoint_status_1"

if ($endpoint_status_1 -eq "Enabled") {
    Write-Output "The endpoint is healthy and actively receiving traffic."
}
elseif ($endpoint_status_1 -eq "Disabled") {
    Write-Output "The endpoint is not receiving traffic and should be checked."
}
elseif ($endpoint_status_1 -eq "Deleting") {
    Write-Output "The endpoint is being deleted and should not receive traffic."
}
else {
    Write-Output "The endpoint status is not recognized and should be checked."
}
Write-Output "The status of the Traffic Manager endpoint $endpoint_name_2 is: $endpoint_status_2"

if ($endpoint_status_2 -eq "Enabled") {
    Write-Output "The endpoint is healthy and actively receiving traffic."
}
elseif ($endpoint_status_2 -eq "Disabled") {
    Write-Output "The endpoint is not receiving traffic and should be checked."
}
elseif ($endpoint_status_2 -eq "Deleting") {
    Write-Output "The endpoint is being deleted and should not receive traffic."
}
else {
    Write-Output "The endpoint status is not recognized and should be checked."
}
