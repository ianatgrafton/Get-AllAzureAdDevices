# Get-AllAzureAdDevices
Get all devices from Azure AD (Entra ID) using mggraph

This script is taken from [https://o365reports.com/2023/04/18/get-azure-ad-devices-report-using-powershell/](url)

The script does not take piped input but requires command line input at runtime:
     * TenantID 
        is the TenantID required for certificate based authentication 
    * ClientID 
        is the CLientID required for certificate based authentication
    * CertificateThumbprint 
        is the thrumbprint of the certificate to be used for app only/cert based authentication
    * EnabledDevice
        if this parameter is specified then only enabled devices will be processed and exported
    * DisabledDevice 
        if this parameter is specified then only disabled devices will be processed and exported
    * InactiveDays <num of days> 
        exports the devices that have been inactive for the number of days specified e.g. .\GetAzureADDevicesReport.ps1 -InactiveDays 30
    * ManagedDevice
        if this parameter is specified then only managed devices are exported
    * DevicesWithBitlockerKey 
        if this parameter is specified then only devices with store bitlockerkeys are exported 
        *NOTE: this is not available when using Cert Based Auth* 
