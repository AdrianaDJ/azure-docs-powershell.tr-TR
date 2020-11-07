---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 164C5205-01BA-47BB-B780-D0B9AE614A4B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagement.md
ms.openlocfilehash: 98e90b4c8275028ab3e62e7383505775271e8d09
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762810"
---
# <span data-ttu-id="73acc-101">New-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="73acc-101">New-AzureRmApiManagement</span></span>

## <span data-ttu-id="73acc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73acc-102">SYNOPSIS</span></span>
<span data-ttu-id="73acc-103">Bir API yönetim dağıtımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="73acc-103">Creates an API Management deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73acc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="73acc-104">SYNTAX</span></span>

```
New-AzureRmApiManagement -ResourceGroupName <String> -Name <String> -Location <String> -Organization <String>
 -AdminEmail <String> [-Sku <PsApiManagementSku>] [-Capacity <Int32>] [-VpnType <PsApiManagementVpnType>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-AdditionalRegions <PsApiManagementRegion[]>]
 [-CustomHostnameConfiguration <PsApiManagementCustomHostNameConfiguration[]>]
 [-SystemCertificateConfiguration <PsApiManagementSystemCertificate[]>] [-AssignIdentity]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73acc-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="73acc-105">DESCRIPTION</span></span>
<span data-ttu-id="73acc-106">**Yeni-Azurermapsanana,** Azure API YÖNETIMINDE bir API yönetim dağıtımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="73acc-106">The **New-AzureRmApiManagement** cmdlet creates an API Management deployment in Azure API Management.</span></span>

## <span data-ttu-id="73acc-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="73acc-107">EXAMPLES</span></span>

### <span data-ttu-id="73acc-108">Örnek 1: Geliştirici katmanı API yönetim hizmeti oluşturma</span><span class="sxs-lookup"><span data-stu-id="73acc-108">Example 1: Create a Developer tier API Management service</span></span>
```powershell
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com"
```

<span data-ttu-id="73acc-109">Bu komut bir geliştirici katmanı API yönetim hizmeti oluşturur.</span><span class="sxs-lookup"><span data-stu-id="73acc-109">This command creates a Developer tier API Management service.</span></span>
<span data-ttu-id="73acc-110">Bu komut, organizasyonu ve yönetici adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="73acc-110">The command specifies the organization and the administrator address.</span></span>
<span data-ttu-id="73acc-111">Komut *SKU* parametresini belirtmez.</span><span class="sxs-lookup"><span data-stu-id="73acc-111">The command does not specify the *SKU* parameter.</span></span>
<span data-ttu-id="73acc-112">Bu nedenle, cmdlet geliştirici varsayılan değerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="73acc-112">Therefore, the cmdlet uses the default value of Developer.</span></span>

### <span data-ttu-id="73acc-113">Örnek 2: üç birimli standart bir katman hizmeti oluşturma</span><span class="sxs-lookup"><span data-stu-id="73acc-113">Example 2: Create a Standard tier service that has three units</span></span>
```powershell
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup02 -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com" -Sku Standard -Capacity 3
```

<span data-ttu-id="73acc-114">Bu komut, üç birimli bir standart katman API yönetim hizmeti oluşturur.</span><span class="sxs-lookup"><span data-stu-id="73acc-114">This command creates a Standard tier API Management service that has three units.</span></span>

### <span data-ttu-id="73acc-115">Örnek 3: dış sanal ağ için API yönetim hizmeti oluşturma</span><span class="sxs-lookup"><span data-stu-id="73acc-115">Example 3: Create an API Management service for an external virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="73acc-116">Bu komut, bir Azure sanal ağ alt ağında, Batı ABD 'deki ana bölgeyle birlikte dış bir ağ geçidi uç noktası içeren bir Premium katman API yönetim hizmeti oluşturur.</span><span class="sxs-lookup"><span data-stu-id="73acc-116">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an external-facing gateway endpoint with a master region in the West US.</span></span>

### <span data-ttu-id="73acc-117">Örnek 4: iç sanal ağ için bir API yönetim hizmeti oluşturma</span><span class="sxs-lookup"><span data-stu-id="73acc-117">Example 4: Create an API Management service for an internal virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization "Contoso" -AdminEmail "admin@contoso.com" -VirtualNetwork $virtualNetwork -VpnType "Internal" -Sku "Premium"
```

<span data-ttu-id="73acc-118">Bu komut, bir Azure sanal ağ alt ağında, Batı ABD 'deki ana bölgeyle birlikte dahili bir ağ geçidi uç noktası içeren bir Premium katman API yönetim hizmeti oluşturur.</span><span class="sxs-lookup"><span data-stu-id="73acc-118">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an internal-facing gateway endpoint with a master region in the West US.</span></span>

## <span data-ttu-id="73acc-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="73acc-119">PARAMETERS</span></span>

### <span data-ttu-id="73acc-120">-Additionalbölgelerle</span><span class="sxs-lookup"><span data-stu-id="73acc-120">-AdditionalRegions</span></span>
<span data-ttu-id="73acc-121">Azure API yönetimi için ek dağıtım bölgeleri.</span><span class="sxs-lookup"><span data-stu-id="73acc-121">Additional deployment regions of Azure API Management.</span></span>

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

### <span data-ttu-id="73acc-122">-AdminEmail</span><span class="sxs-lookup"><span data-stu-id="73acc-122">-AdminEmail</span></span>
<span data-ttu-id="73acc-123">API yönetim sisteminin gönderdiği tüm bildirimler için kaynak e-posta adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="73acc-123">Specifies the originating email address for all notifications that the API Management system sends.</span></span>

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

### <span data-ttu-id="73acc-124">-Atama kimliği</span><span class="sxs-lookup"><span data-stu-id="73acc-124">-AssignIdentity</span></span>
<span data-ttu-id="73acc-125">Azure Keykasa gibi temel yönetim hizmetleri ile kullanmak için bu sunucu için bir Azure Active Directory kimliği oluşturun ve atayın.</span><span class="sxs-lookup"><span data-stu-id="73acc-125">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="73acc-126">-Kapasite</span><span class="sxs-lookup"><span data-stu-id="73acc-126">-Capacity</span></span>
<span data-ttu-id="73acc-127">Azure API yönetim hizmetinin SKU kapasitesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="73acc-127">Specifies the SKU capacity of the Azure API Management service.</span></span>
<span data-ttu-id="73acc-128">Varsayılan değer bir (1).</span><span class="sxs-lookup"><span data-stu-id="73acc-128">The default is one (1).</span></span>

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

### <span data-ttu-id="73acc-129">-CustomHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="73acc-129">-CustomHostnameConfiguration</span></span>
<span data-ttu-id="73acc-130">Özel ana bilgisayar yapılandırmaları.</span><span class="sxs-lookup"><span data-stu-id="73acc-130">Custom hostname configurations.</span></span> <span data-ttu-id="73acc-131">Varsayılan değer $null.</span><span class="sxs-lookup"><span data-stu-id="73acc-131">Default value is $null.</span></span> <span data-ttu-id="73acc-132">$Null geçirmek varsayılan ana bilgisayar adını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="73acc-132">Passing $null will set the default hostname.</span></span>

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

### <span data-ttu-id="73acc-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73acc-133">-DefaultProfile</span></span>
<span data-ttu-id="73acc-134">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="73acc-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73acc-135">-Konum</span><span class="sxs-lookup"><span data-stu-id="73acc-135">-Location</span></span>
<span data-ttu-id="73acc-136">API Yönetim hizmetini oluşturacağınız konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="73acc-136">Specifies the location to create the Api Management service.</span></span>
<span data-ttu-id="73acc-137">Geçerli konumlar almak için, "Microsoft. Apsananae" Get-AzureRmResourceProvider cmdlet 'ini kullanın. WHERE {$ _. ResourceTypes [0]. ResourceTypeName-EQ "hizmet"} | Select-Object konumları</span><span class="sxs-lookup"><span data-stu-id="73acc-137">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="73acc-138">-Ad</span><span class="sxs-lookup"><span data-stu-id="73acc-138">-Name</span></span>
<span data-ttu-id="73acc-139">API yönetim dağıtımı için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="73acc-139">Specifies a name for the API Management deployment.</span></span>

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

### <span data-ttu-id="73acc-140">-Kuruluş</span><span class="sxs-lookup"><span data-stu-id="73acc-140">-Organization</span></span>
<span data-ttu-id="73acc-141">Kuruluşun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="73acc-141">Specifies the name of an organization.</span></span>
<span data-ttu-id="73acc-142">API Yönetimi, bu adresi Geliştirici Portalında e-posta bildirimlerinde kullanır.</span><span class="sxs-lookup"><span data-stu-id="73acc-142">API Management uses this address in the developer portal in email notifications.</span></span>

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

### <span data-ttu-id="73acc-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73acc-143">-ResourceGroupName</span></span>
<span data-ttu-id="73acc-144">Bu cmdlet 'in API yönetim dağıtımını oluşturduğu kaynak grubun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="73acc-144">Specifies the name of the of resource group under which this cmdlet creates an API Management deployment.</span></span>

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

### <span data-ttu-id="73acc-145">-SKU</span><span class="sxs-lookup"><span data-stu-id="73acc-145">-Sku</span></span>
<span data-ttu-id="73acc-146">API yönetim hizmetinin katmanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="73acc-146">Specifies the tier of the API Management service.</span></span>
<span data-ttu-id="73acc-147">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="73acc-147">Valid values are:</span></span> 
- <span data-ttu-id="73acc-148">İyle</span><span class="sxs-lookup"><span data-stu-id="73acc-148">Developer</span></span> 
- <span data-ttu-id="73acc-149">Ardından</span><span class="sxs-lookup"><span data-stu-id="73acc-149">Standard</span></span> 
- <span data-ttu-id="73acc-150">Premium varsayılan geliştirici geliştirici.</span><span class="sxs-lookup"><span data-stu-id="73acc-150">Premium The default is Developer.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73acc-151">-SystemCertificateConfiguration</span><span class="sxs-lookup"><span data-stu-id="73acc-151">-SystemCertificateConfiguration</span></span>
<span data-ttu-id="73acc-152">Hizmete yüklenecek dahili CA tarafından verilen sertifikalar.</span><span class="sxs-lookup"><span data-stu-id="73acc-152">Certificates issued by Internal CA to be installed on the service.</span></span> <span data-ttu-id="73acc-153">Varsayılan değer $null.</span><span class="sxs-lookup"><span data-stu-id="73acc-153">Default value is $null.</span></span>

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

### <span data-ttu-id="73acc-154">Etiketli</span><span class="sxs-lookup"><span data-stu-id="73acc-154">-Tag</span></span>
<span data-ttu-id="73acc-155">Etiket sözlüğü.</span><span class="sxs-lookup"><span data-stu-id="73acc-155">Tags dictionary.</span></span>

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

### <span data-ttu-id="73acc-156">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="73acc-156">-VirtualNetwork</span></span>
<span data-ttu-id="73acc-157">Master Azure API yönetim dağıtım bölgesinin sanal ağ yapılandırması.</span><span class="sxs-lookup"><span data-stu-id="73acc-157">Virtual Network Configuration of master Azure API Management deployment region.</span></span>

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

### <span data-ttu-id="73acc-158">-VpnType</span><span class="sxs-lookup"><span data-stu-id="73acc-158">-VpnType</span></span>
<span data-ttu-id="73acc-159">Sanal ağ 'ın sanal ağ türü.</span><span class="sxs-lookup"><span data-stu-id="73acc-159">Virtual Network Type of the ApiManagement Deployment.</span></span> <span data-ttu-id="73acc-160">Geçerli değerler</span><span class="sxs-lookup"><span data-stu-id="73acc-160">Valid Values are</span></span> 
- <span data-ttu-id="73acc-161">"None" (varsayılan değer.</span><span class="sxs-lookup"><span data-stu-id="73acc-161">"None" (Default Value.</span></span> <span data-ttu-id="73acc-162">Herhangi bir sanal ağın parçası değildir ")</span><span class="sxs-lookup"><span data-stu-id="73acc-162">ApiManagement is not part of any Virtual Network")</span></span>
- <span data-ttu-id="73acc-163">"Dış" (bir Internet 'e yönelik uç noktaya sahip bir sanal ağın içinde bir kuruluş)</span><span class="sxs-lookup"><span data-stu-id="73acc-163">"External" (ApiManagement Deployment is setup inside a Virtual Network having an Internet Facing Endpoint)</span></span>
- <span data-ttu-id="73acc-164">"İç" (bir sanal ağın iç uç noktasına sahip olduğu bir sanal ağ içinde, kuruluş)</span><span class="sxs-lookup"><span data-stu-id="73acc-164">"Internal" (ApiManagement Deployment is setup inside a Virtual Network having an Intranet Facing Endpoint)</span></span>

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

### <span data-ttu-id="73acc-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73acc-165">CommonParameters</span></span>
<span data-ttu-id="73acc-166">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="73acc-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73acc-167">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73acc-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73acc-168">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="73acc-168">INPUTS</span></span>

### <span data-ttu-id="73acc-169">System. String</span><span class="sxs-lookup"><span data-stu-id="73acc-169">System.String</span></span>

### <span data-ttu-id="73acc-170">System. Nullable ' 1 [[Microsoft. Azure. Commands. Apsananamedi. model. Psapsananagementsku, Microsoft. Azure. Commands. Apsananad, Version = 6.1.2.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="73acc-170">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku, Microsoft.Azure.Commands.ApiManagement, Version=6.1.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="73acc-171">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="73acc-171">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="73acc-172">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="73acc-172">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

### <span data-ttu-id="73acc-173">System. Koleksiyonlar. Generic. Dictionary ' 2 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089], [System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="73acc-173">System.Collections.Generic.Dictionary\`2[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089],[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="73acc-174">Microsoft. Azure. Commands. Apsananad. modeller. Psapsananagementregion []</span><span class="sxs-lookup"><span data-stu-id="73acc-174">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion[]</span></span>

### <span data-ttu-id="73acc-175">Microsoft. Azure. Commands. Apsananad. modeller. Psapsananagementcustomhostnameconfiguration []</span><span class="sxs-lookup"><span data-stu-id="73acc-175">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration[]</span></span>

### <span data-ttu-id="73acc-176">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="73acc-176">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate[]</span></span>

## <span data-ttu-id="73acc-177">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="73acc-177">OUTPUTS</span></span>

### <span data-ttu-id="73acc-178">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="73acc-178">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="73acc-179">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="73acc-179">NOTES</span></span>

## <span data-ttu-id="73acc-180">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="73acc-180">RELATED LINKS</span></span>

[<span data-ttu-id="73acc-181">Yedek-azurermapı</span><span class="sxs-lookup"><span data-stu-id="73acc-181">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="73acc-182">Get-azurermapı</span><span class="sxs-lookup"><span data-stu-id="73acc-182">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="73acc-183">Set-azurermapsanana</span><span class="sxs-lookup"><span data-stu-id="73acc-183">Set-AzureRmApiManagement</span></span>](./Set-AzureRmApiManagement.md)

[<span data-ttu-id="73acc-184">Remove-azurermapsanana</span><span class="sxs-lookup"><span data-stu-id="73acc-184">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)

[<span data-ttu-id="73acc-185">Geri yükleme-azurermapı</span><span class="sxs-lookup"><span data-stu-id="73acc-185">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


