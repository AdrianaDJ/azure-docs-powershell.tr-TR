---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 164C5205-01BA-47BB-B780-D0B9AE614A4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagement.md
ms.openlocfilehash: 32e3bc6419ef94b177a06735654844d09ea04f3e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109252"
---
# <span data-ttu-id="bee89-101">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="bee89-101">New-AzApiManagement</span></span>

## <span data-ttu-id="bee89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bee89-102">SYNOPSIS</span></span>
<span data-ttu-id="bee89-103">Bir API yönetim dağıtımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bee89-103">Creates an API Management deployment.</span></span>

## <span data-ttu-id="bee89-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bee89-104">SYNTAX</span></span>

```
New-AzApiManagement -ResourceGroupName <String> -Name <String> -Location <String> -Organization <String>
 -AdminEmail <String> [-Sku <PsApiManagementSku>] [-Capacity <Int32>] [-VpnType <PsApiManagementVpnType>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-AdditionalRegions <PsApiManagementRegion[]>]
 [-CustomHostnameConfiguration <PsApiManagementCustomHostNameConfiguration[]>]
 [-SystemCertificateConfiguration <PsApiManagementSystemCertificate[]>]
 [-SslSetting <PsApiManagementSslSetting>] [-SystemAssignedIdentity] [-UserAssignedIdentity <String[]>]
 [-EnableClientCertificate] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bee89-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bee89-105">DESCRIPTION</span></span>
<span data-ttu-id="bee89-106">**Yeni-azın** cmdlet 'ı Azure API YÖNETIMINDE bir API yönetim dağıtımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bee89-106">The **New-AzApiManagement** cmdlet creates an API Management deployment in Azure API Management.</span></span>

## <span data-ttu-id="bee89-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bee89-107">EXAMPLES</span></span>

### <span data-ttu-id="bee89-108">Örnek 1: Geliştirici katmanı API yönetim hizmeti oluşturma</span><span class="sxs-lookup"><span data-stu-id="bee89-108">Example 1: Create a Developer tier API Management service</span></span>
```powershell
PS D:\> New-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi2" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com"


PublicIPAddresses                     : {104.43.240.65}
PrivateIPAddresses                    :
Id                                    : /subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/ContosoGroup02/providers/Microsoft.ApiManagement/service/ContosoApi2
Name                                  : ContosoApi2
Location                              : Central US
Sku                                   : Developer
Capacity                              : 1
CreatedTimeUtc                        : 2/24/2020 10:34:12 PM
ProvisioningState                     : Succeeded
RuntimeUrl                            : https://contosoapi2.azure-api.net
RuntimeRegionalUrl                    : https://contosoapi2-centralus-01.regional.azure-api.net
PortalUrl                             : https://contosoapi2.portal.azure-api.net
DeveloperPortalUrl                    : https://contosoapi2.developer.azure-api.net
ManagementApiUrl                      : https://contosoapi2.management.azure-api.net
ScmUrl                                : https://contosoapi2.scm.azure-api.net
PublisherEmail                        : admin@contoso.com
OrganizationName                      : Contoso
NotificationSenderEmail               : apimgmt-noreply@mail.windowsazure.com
VirtualNetwork                        :
VpnType                               : None
PortalCustomHostnameConfiguration     :
ProxyCustomHostnameConfiguration      : {contosoapi2.azure-api.net}
ManagementCustomHostnameConfiguration :
ScmCustomHostnameConfiguration        :
DeveloperPortalHostnameConfiguration  :
SystemCertificates                    :
Tags                                  : {}
AdditionalRegions                     : {}
SslSetting                            : Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSetting
Identity                              :
EnableClientCertificate               :
ResourceGroupName                     : ContosoGroup02
```

<span data-ttu-id="bee89-109">Bu komut bir geliştirici katmanı API yönetim hizmeti oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bee89-109">This command creates a Developer tier API Management service.</span></span>
<span data-ttu-id="bee89-110">Bu komut, organizasyonu ve yönetici adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bee89-110">The command specifies the organization and the administrator address.</span></span>
<span data-ttu-id="bee89-111">Komut *SKU* parametresini belirtmez.</span><span class="sxs-lookup"><span data-stu-id="bee89-111">The command does not specify the *SKU* parameter.</span></span>
<span data-ttu-id="bee89-112">Bu nedenle, cmdlet geliştirici varsayılan değerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="bee89-112">Therefore, the cmdlet uses the default value of Developer.</span></span>

### <span data-ttu-id="bee89-113">Örnek 2: üç birimli standart bir katman hizmeti oluşturma</span><span class="sxs-lookup"><span data-stu-id="bee89-113">Example 2: Create a Standard tier service that has three units</span></span>
```powershell
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com" -Sku Standard -Capacity 3
```

<span data-ttu-id="bee89-114">Bu komut, üç birimli bir standart katman API yönetim hizmeti oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bee89-114">This command creates a Standard tier API Management service that has three units.</span></span>

### <span data-ttu-id="bee89-115">Örnek 3: tüketim katmanı hizmeti oluşturma</span><span class="sxs-lookup"><span data-stu-id="bee89-115">Example 3: Create a Consumption tier service</span></span>
```powershell
PS D:\github\azure-powershell> New-AzApiManagement -ResourceGroupName Api-Default-North-Europe -Name consumptionskuservice -Location 'West Europe' -Sku Consumption -Organization microsoft -AdminEmail contoso@contoso.com -SystemAssignedIdentity -EnableClientCertificate

PublicIPAddresses                     :
PrivateIPAddresses                    :
Id                                    : /subscriptions/subid/resourceGroups/Api-Default-North-Europe/providers/Microsoft.ApiManagement/service/consumptionskuservice
Name                                  : consumptionskuservice
Location                              : West Europe
Sku                                   : Consumption
Capacity                              : 0
ProvisioningState                     : Succeeded
RuntimeUrl                            : https://consumptionskuservice.azure-api.net
PortalCustomHostnameConfiguration     :
ProxyCustomHostnameConfiguration      : {consumptionskuservice.azure-api.net}
ManagementCustomHostnameConfiguration :
ScmCustomHostnameConfiguration        :
DeveloperPortalHostnameConfiguration  :
SystemCertificates                    :
Tags                                  : {}
AdditionalRegions                     : {}
SslSetting                            : Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSetting
Identity                              : Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentity
EnableClientCertificate               : True
ResourceGroupName                     : Api-Default-North-Europe
```

<span data-ttu-id="bee89-116">Bu komut, Batı Avrupa 'da Istemci sertifikası etkinleştirilmiş bir tüketim katmanı API yönetim hizmeti oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bee89-116">This command creates a consumption tier API Management service with Client Certificate enabled in west Europe.</span></span>

### <span data-ttu-id="bee89-117">Örnek 4: dış sanal ağ için API yönetim hizmeti oluşturma</span><span class="sxs-lookup"><span data-stu-id="bee89-117">Example 4: Create an API Management service for an external virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="bee89-118">Bu komut, bir Azure sanal ağ alt ağında, Batı ABD 'deki ana bölgeyle birlikte dış bir ağ geçidi uç noktası içeren bir Premium katman API yönetim hizmeti oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bee89-118">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an external-facing gateway endpoint with a master region in the West US.</span></span>

### <span data-ttu-id="bee89-119">Örnek 5: iç sanal ağ için bir API yönetim hizmeti oluşturma</span><span class="sxs-lookup"><span data-stu-id="bee89-119">Example 5: Create an API Management service for an internal virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization "Contoso" -AdminEmail "admin@contoso.com" -VirtualNetwork $virtualNetwork -VpnType "Internal" -Sku "Premium"
```

<span data-ttu-id="bee89-120">Bu komut, bir Azure sanal ağ alt ağında, Batı ABD 'deki ana bölgeyle birlikte dahili bir ağ geçidi uç noktası içeren bir Premium katman API yönetim hizmeti oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bee89-120">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an internal-facing gateway endpoint with a master region in the West US.</span></span>

### <span data-ttu-id="bee89-121">Örnek 6: bir API yönetim hizmeti oluşturma ve TLS 1,0 protokolünü etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="bee89-121">Example 6: Create an API Management service and Enable TLS 1.0 protocol</span></span>
```powershell
PS C:\> $enableTls=@{"Tls10" = "True"}
PS C:\> $sslSetting = New-AzApiManagementSslSetting -FrontendProtocol $enableTls -BackendProtocol $enableTls
PS C:\> New-AzApiManagement -ResourceGroupName Api-Default-CentralUS -Name "testtlspowershell" -Sku Standard -Location "CentralUS" -Organization "Microsoft" -AdminEmail "bar@contoso.com" -SslSetting $sslSetting

PublicIPAddresses                     : {23.99.140.18}
PrivateIPAddresses                    :
Id                                    : /subscriptions/subid/resourceGroups/Api-Default-CentralUS/providers/Microsoft.ApiManagement/service/testtlspowershell
Name                                  : testtlspowershell
Location                              : Central US
Sku                                   : Standard
Capacity                              : 1
ProvisioningState                     : Succeeded
RuntimeUrl                            : https://testtlspowershell.azure-api.net
RuntimeRegionalUrl                    : https://testtlspowershell-centralus-01.regional.azure-api.net
PortalUrl                             : https://testtlspowershell.portal.azure-api.net
ManagementApiUrl                      : https://testtlspowershell.management.azure-api.net
ScmUrl                                : https://testtlspowershell.scm.azure-api.net
PublisherEmail                        : bar@contoso.com
OrganizationName                      : Microsoft
NotificationSenderEmail               : apimgmt-noreply@mail.windowsazure.com
VirtualNetwork                        :
VpnType                               : None
PortalCustomHostnameConfiguration     :
ProxyCustomHostnameConfiguration      : {testtlspowershell.azure-api.net}
ManagementCustomHostnameConfiguration :
ScmCustomHostnameConfiguration        :
DeveloperPortalHostnameConfiguration  :
SystemCertificates                    :
Tags                                  : {}
AdditionalRegions                     : {}
SslSetting                            : Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSetting
Identity                              :
EnableClientCertificate               :
ResourceGroupName                     : Api-Default-CentralUS
```

<span data-ttu-id="bee89-122">Bu komut standart bir SKU API yönetim hizmeti oluşturur ve ön uç istemcisinde, anlık ağ geçidi ve arka uç istemci arasında TLS 1,0 ' i etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="bee89-122">This command creates a Standard SKU Api Management service and Enable TLS 1.0 on Frontend client to ApiManagement Gateway and Backend client between ApiManagement Gateway and Backend.</span></span>

## <span data-ttu-id="bee89-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bee89-123">PARAMETERS</span></span>

### <span data-ttu-id="bee89-124">-Additionalbölgelerle</span><span class="sxs-lookup"><span data-stu-id="bee89-124">-AdditionalRegions</span></span>
<span data-ttu-id="bee89-125">Azure API yönetimi için ek dağıtım bölgeleri.</span><span class="sxs-lookup"><span data-stu-id="bee89-125">Additional deployment regions of Azure API Management.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bee89-126">-AdminEmail</span><span class="sxs-lookup"><span data-stu-id="bee89-126">-AdminEmail</span></span>
<span data-ttu-id="bee89-127">API yönetim sisteminin gönderdiği tüm bildirimler için kaynak e-posta adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bee89-127">Specifies the originating email address for all notifications that the API Management system sends.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bee89-128">-Kapasite</span><span class="sxs-lookup"><span data-stu-id="bee89-128">-Capacity</span></span>
<span data-ttu-id="bee89-129">Azure API yönetim hizmetinin SKU kapasitesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bee89-129">Specifies the SKU capacity of the Azure API Management service.</span></span>
<span data-ttu-id="bee89-130">Varsayılan değer bir (1).</span><span class="sxs-lookup"><span data-stu-id="bee89-130">The default is one (1).</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bee89-131">-CustomHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="bee89-131">-CustomHostnameConfiguration</span></span>
<span data-ttu-id="bee89-132">Özel ana bilgisayar yapılandırmaları.</span><span class="sxs-lookup"><span data-stu-id="bee89-132">Custom hostname configurations.</span></span> <span data-ttu-id="bee89-133">Varsayılan değer $null.</span><span class="sxs-lookup"><span data-stu-id="bee89-133">Default value is $null.</span></span> <span data-ttu-id="bee89-134">$Null geçirmek varsayılan ana bilgisayar adını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="bee89-134">Passing $null will set the default hostname.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bee89-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bee89-135">-DefaultProfile</span></span>
<span data-ttu-id="bee89-136">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bee89-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bee89-137">-EnableClientCertificate</span><span class="sxs-lookup"><span data-stu-id="bee89-137">-EnableClientCertificate</span></span>
<span data-ttu-id="bee89-138">Bayrak yalnızca tüketim SKU 'SU için kullanılmak üzere kullanılır.</span><span class="sxs-lookup"><span data-stu-id="bee89-138">Flag only meant to be used for Consumption SKU ApiManagement Service.</span></span> <span data-ttu-id="bee89-139">Bu, ağ geçidine her isteğinde bir istemci sertifikası sunulmasını zorunlu tutar.</span><span class="sxs-lookup"><span data-stu-id="bee89-139">This enforces a client certificate to be presented on each request to the gateway.</span></span> <span data-ttu-id="bee89-140">Bu, ağ geçidinde ilkede sertifika kimliklerinin doğrulanmasını da olanaklı kılar.</span><span class="sxs-lookup"><span data-stu-id="bee89-140">This also enables the ability to authenticate the certificate in the policy on the gateway.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bee89-141">-Konum</span><span class="sxs-lookup"><span data-stu-id="bee89-141">-Location</span></span>
<span data-ttu-id="bee89-142">API Yönetim hizmetini oluşturacağınız konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="bee89-142">Specifies the location to create the Api Management service.</span></span>
<span data-ttu-id="bee89-143">Geçerli konumlar almak için, "Microsoft. Apsananae" Get-AzResourceProvider cmdlet 'ini kullanın. WHERE {$ _. ResourceTypes [0]. ResourceTypeName-EQ "hizmet"} | Select-Object konumları</span><span class="sxs-lookup"><span data-stu-id="bee89-143">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bee89-144">-Ad</span><span class="sxs-lookup"><span data-stu-id="bee89-144">-Name</span></span>
<span data-ttu-id="bee89-145">API yönetim dağıtımı için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="bee89-145">Specifies a name for the API Management deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bee89-146">-Kuruluş</span><span class="sxs-lookup"><span data-stu-id="bee89-146">-Organization</span></span>
<span data-ttu-id="bee89-147">Kuruluşun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bee89-147">Specifies the name of an organization.</span></span>
<span data-ttu-id="bee89-148">API Yönetimi, bu adresi Geliştirici Portalında e-posta bildirimlerinde kullanır.</span><span class="sxs-lookup"><span data-stu-id="bee89-148">API Management uses this address in the developer portal in email notifications.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bee89-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bee89-149">-ResourceGroupName</span></span>
<span data-ttu-id="bee89-150">Bu cmdlet 'in API yönetim dağıtımını oluşturduğu kaynak grubun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bee89-150">Specifies the name of the of resource group under which this cmdlet creates an API Management deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bee89-151">-SKU</span><span class="sxs-lookup"><span data-stu-id="bee89-151">-Sku</span></span>
<span data-ttu-id="bee89-152">API yönetim hizmetinin katmanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bee89-152">Specifies the tier of the API Management service.</span></span>
<span data-ttu-id="bee89-153">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="bee89-153">Valid values are:</span></span> 
- <span data-ttu-id="bee89-154">İyle</span><span class="sxs-lookup"><span data-stu-id="bee89-154">Developer</span></span> 
- <span data-ttu-id="bee89-155">Ardından</span><span class="sxs-lookup"><span data-stu-id="bee89-155">Standard</span></span> 
- <span data-ttu-id="bee89-156">Premium varsayılan geliştirici geliştirici.</span><span class="sxs-lookup"><span data-stu-id="bee89-156">Premium The default is Developer.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Basic, Standard, Premium, Consumption

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bee89-157">-SslSetting</span><span class="sxs-lookup"><span data-stu-id="bee89-157">-SslSetting</span></span>
<span data-ttu-id="bee89-158">Anlık hizmetin SSL ayarı.</span><span class="sxs-lookup"><span data-stu-id="bee89-158">The Ssl Setting of the ApiManagement Service.</span></span> <span data-ttu-id="bee89-159">Varsayılan değer $null</span><span class="sxs-lookup"><span data-stu-id="bee89-159">Default value is $null</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSetting
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bee89-160">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="bee89-160">-SystemAssignedIdentity</span></span>
<span data-ttu-id="bee89-161">Azure Keykasa gibi temel yönetim hizmetleri ile kullanmak için bu sunucu için bir Azure Active Directory kimliği oluşturun ve atayın.</span><span class="sxs-lookup"><span data-stu-id="bee89-161">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bee89-162">-SystemCertificateConfiguration</span><span class="sxs-lookup"><span data-stu-id="bee89-162">-SystemCertificateConfiguration</span></span>
<span data-ttu-id="bee89-163">Hizmete yüklenecek dahili CA tarafından verilen sertifikalar.</span><span class="sxs-lookup"><span data-stu-id="bee89-163">Certificates issued by Internal CA to be installed on the service.</span></span> <span data-ttu-id="bee89-164">Varsayılan değer $null.</span><span class="sxs-lookup"><span data-stu-id="bee89-164">Default value is $null.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bee89-165">Etiketli</span><span class="sxs-lookup"><span data-stu-id="bee89-165">-Tag</span></span>
<span data-ttu-id="bee89-166">Etiket sözlüğü.</span><span class="sxs-lookup"><span data-stu-id="bee89-166">Tags dictionary.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bee89-167">-Useratandidentity</span><span class="sxs-lookup"><span data-stu-id="bee89-167">-UserAssignedIdentity</span></span>
<span data-ttu-id="bee89-168">Azure Keykasa gibi temel yönetim hizmetleriyle kullanmak için Kullanıcı kimliklerini bu sunucuya atayın.</span><span class="sxs-lookup"><span data-stu-id="bee89-168">Assign User Identities to this server for use with key management services like Azure KeyVault.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bee89-169">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="bee89-169">-VirtualNetwork</span></span>
<span data-ttu-id="bee89-170">Master Azure API yönetim dağıtım bölgesinin sanal ağ yapılandırması.</span><span class="sxs-lookup"><span data-stu-id="bee89-170">Virtual Network Configuration of master Azure API Management deployment region.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bee89-171">-VpnType</span><span class="sxs-lookup"><span data-stu-id="bee89-171">-VpnType</span></span>
<span data-ttu-id="bee89-172">Sanal ağ 'ın sanal ağ türü.</span><span class="sxs-lookup"><span data-stu-id="bee89-172">Virtual Network Type of the ApiManagement Deployment.</span></span> <span data-ttu-id="bee89-173">Geçerli değerler</span><span class="sxs-lookup"><span data-stu-id="bee89-173">Valid Values are</span></span> 
- <span data-ttu-id="bee89-174">"None" (varsayılan değer.</span><span class="sxs-lookup"><span data-stu-id="bee89-174">"None" (Default Value.</span></span> <span data-ttu-id="bee89-175">Herhangi bir sanal ağın parçası değildir ")</span><span class="sxs-lookup"><span data-stu-id="bee89-175">ApiManagement is not part of any Virtual Network")</span></span>
- <span data-ttu-id="bee89-176">"Dış" (bir Internet 'e yönelik uç noktaya sahip bir sanal ağın içinde bir kuruluş)</span><span class="sxs-lookup"><span data-stu-id="bee89-176">"External" (ApiManagement Deployment is setup inside a Virtual Network having an Internet Facing Endpoint)</span></span>
- <span data-ttu-id="bee89-177">"İç" (bir sanal ağın iç uç noktasına sahip olduğu bir sanal ağ içinde, kuruluş)</span><span class="sxs-lookup"><span data-stu-id="bee89-177">"Internal" (ApiManagement Deployment is setup inside a Virtual Network having an Intranet Facing Endpoint)</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVpnType
Parameter Sets: (All)
Aliases:
Accepted values: None, External, Internal

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bee89-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bee89-178">CommonParameters</span></span>
<span data-ttu-id="bee89-179">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bee89-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bee89-180">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="bee89-180">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bee89-181">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bee89-181">INPUTS</span></span>

### <span data-ttu-id="bee89-182">System. String</span><span class="sxs-lookup"><span data-stu-id="bee89-182">System.String</span></span>

### <span data-ttu-id="bee89-183">System. Nullable ' 1 [[Microsoft. Azure. Commands. Apsananad. modeller. Psapsananagementsku, Microsoft. Azure. PowerShell. cmdlet. Apsananad, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="bee89-183">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="bee89-184">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="bee89-184">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="bee89-185">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="bee89-185">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

### <span data-ttu-id="bee89-186">System. Koleksiyonlar. Generic. Dictionary ' 2 [[System. String, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85din</span><span class="sxs-lookup"><span data-stu-id="bee89-186">System.Collections.Generic.Dictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="bee89-187">Microsoft. Azure. Commands. Apsananad. modeller. Psapsananagementregion []</span><span class="sxs-lookup"><span data-stu-id="bee89-187">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion[]</span></span>

### <span data-ttu-id="bee89-188">Microsoft. Azure. Commands. Apsananad. modeller. Psapsananagementcustomhostnameconfiguration []</span><span class="sxs-lookup"><span data-stu-id="bee89-188">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration[]</span></span>

### <span data-ttu-id="bee89-189">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="bee89-189">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate[]</span></span>

## <span data-ttu-id="bee89-190">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bee89-190">OUTPUTS</span></span>

### <span data-ttu-id="bee89-191">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="bee89-191">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="bee89-192">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bee89-192">NOTES</span></span>

## <span data-ttu-id="bee89-193">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bee89-193">RELATED LINKS</span></span>

[<span data-ttu-id="bee89-194">Yedek-azlı bir</span><span class="sxs-lookup"><span data-stu-id="bee89-194">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="bee89-195">Get-Azıbir</span><span class="sxs-lookup"><span data-stu-id="bee89-195">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="bee89-196">Set-azapsanana</span><span class="sxs-lookup"><span data-stu-id="bee89-196">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)

[<span data-ttu-id="bee89-197">Remove-azın</span><span class="sxs-lookup"><span data-stu-id="bee89-197">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="bee89-198">Geri yükleme-azbir</span><span class="sxs-lookup"><span data-stu-id="bee89-198">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


