---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 56604912-53A0-496D-9BDC-472BCE45A6A2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementDeployment.md
ms.openlocfilehash: e4170dbe2a1ac4ed8ad39bdb7a5db6d7174555e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587012"
---
# <span data-ttu-id="04e4f-101">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="04e4f-101">Update-AzureRmApiManagementDeployment</span></span>

## <span data-ttu-id="04e4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04e4f-102">SYNOPSIS</span></span>
<span data-ttu-id="04e4f-103">Bir API yönetim hizmetinin dağıtımını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="04e4f-103">Updates deployment of an API Management Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="04e4f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="04e4f-104">SYNTAX</span></span>

### <span data-ttu-id="04e4f-105">Belirli API yönetim hizmeti (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="04e4f-105">Specific API Management service (Default)</span></span>
```
Update-AzureRmApiManagementDeployment -ResourceGroupName <String> -Name <String> -Location <String>
 -Sku <PsApiManagementSku> -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-VpnType <PsApiManagementVpnType>]
 [-AdditionalRegions <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="04e4f-106">Psapsananamı örneğinden Güncelleştir</span><span class="sxs-lookup"><span data-stu-id="04e4f-106">Update from PsApiManagement instance</span></span>
```
Update-AzureRmApiManagementDeployment -ApiManagement <PsApiManagement> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04e4f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="04e4f-107">DESCRIPTION</span></span>
<span data-ttu-id="04e4f-108">**Güncelleştirme-Azurermapımanagementdeployment** cmdlet 'i, bir API yönetim hizmetinin geçerli dağıtımlarını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="04e4f-108">The **Update-AzureRmApiManagementDeployment** cmdlet updates current deployments of an API Management service.</span></span>

## <span data-ttu-id="04e4f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="04e4f-109">EXAMPLES</span></span>

### <span data-ttu-id="04e4f-110">Örnek 1: bir anlık ileti örneğinin dağıtımını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="04e4f-110">Example 1: Update a deployment of an ApiManagement instance</span></span>
```
PS C:\>Update-AzureRmApiManagementDeployment -ResourceGroupName "Contoso" -Name "ContosoApi" -Sku "Standard" -Capacity 3
```

<span data-ttu-id="04e4f-111">Bu komut, API yönetim örneğinin dağıtımını üç birim kapasite standardına göre güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="04e4f-111">This command updates deployment of an API Management instance to a three unit capacity standard.</span></span>

### <span data-ttu-id="04e4f-112">Örnek 2: bir anlık ileti alma ve yeniden boyutlandırma</span><span class="sxs-lookup"><span data-stu-id="04e4f-112">Example 2: Get an ApiManagement instance and rescale it</span></span>
```
PS C:\>$ApiManagement = Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi"
PS C:\> $ApiManagement.Sku = "Premium"
PS C:\> $ApiManagement.Capacity = 5
PS C:\> $ApiManagement.AddRegion("Central US", "Premium", 3)
PS C:\> Update-AzureRmApiManagementDeployment -ApiManagement $ApiManagement
```

<span data-ttu-id="04e4f-113">Bu örnekte bir API yönetim örneği alınır, bunu beş Premium birime ölçeklendirir ve Premium bölgeye ek üç birim ekler.</span><span class="sxs-lookup"><span data-stu-id="04e4f-113">This example gets an Api Management instance, scales it to five premium units and then adds an additional three units to the premium region.</span></span>

### <span data-ttu-id="04e4f-114">Örnek 3: güncelleştirme dağıtımı (dış VNET)</span><span class="sxs-lookup"><span data-stu-id="04e4f-114">Example 3: Update deployment (external VNET)</span></span>
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-West-US/providers/Microsoft.ClassicNetwork/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $virtualNetwork -VpnType "External"
```

<span data-ttu-id="04e4f-115">Bu komut, var olan bir API yönetim dağıtımını güncelleştirir ve bir dış *Vpntype* 'a katılır.</span><span class="sxs-lookup"><span data-stu-id="04e4f-115">This command updates an existing API Management deployment and joins to an external *VpnType*.</span></span>

### <span data-ttu-id="04e4f-116">Örnek 4: güncelleştirme dağıtımı (iç VNET)</span><span class="sxs-lookup"><span data-stu-id="04e4f-116">Example 4: Update deployment (internal VNET)</span></span>
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-West-US/providers/Microsoft.ClassicNetwork/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $virtualNetwork -VpnType "Internal"
```

<span data-ttu-id="04e4f-117">Bu komut, var olan bir API yönetim dağıtımını güncelleştirir ve bir iç *Vpntype* 'a katılır.</span><span class="sxs-lookup"><span data-stu-id="04e4f-117">This command updates an existing API Management deployment and joins to an internal *VpnType*.</span></span>

## <span data-ttu-id="04e4f-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="04e4f-118">PARAMETERS</span></span>

### <span data-ttu-id="04e4f-119">-Additionalbölgelerle</span><span class="sxs-lookup"><span data-stu-id="04e4f-119">-AdditionalRegions</span></span>
<span data-ttu-id="04e4f-120">Azure API Yönetimi 'nin ek dağıtım bölgelerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="04e4f-120">Specifies additional deployment regions of Azure API Management.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion]
Parameter Sets: Specific API Management service
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04e4f-121">-Ucuz</span><span class="sxs-lookup"><span data-stu-id="04e4f-121">-ApiManagement</span></span>
<span data-ttu-id="04e4f-122">Dağıtım yapılandırmasını almak için **Psapimana,** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="04e4f-122">Specifies the **PsApiManagement** instance to get deployment configuration from.</span></span>
<span data-ttu-id="04e4f-123">Örnekte gerekli tüm değişiklikler varsa bu parametreyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="04e4f-123">Use this parameter if the instance already has all the required changes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: Update from PsApiManagement instance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="04e4f-124">-Kapasite</span><span class="sxs-lookup"><span data-stu-id="04e4f-124">-Capacity</span></span>
<span data-ttu-id="04e4f-125">Ana Azure API Yönetimi dağıtım bölgesinin SKU kapasitesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="04e4f-125">Specifies the SKU capacity of the master Azure API Management deployment region.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Specific API Management service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04e4f-126">-Konum</span><span class="sxs-lookup"><span data-stu-id="04e4f-126">-Location</span></span>
<span data-ttu-id="04e4f-127">Master API Yönetimi dağıtım bölgesinin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="04e4f-127">Specifies the location of the master API Management deployment region.</span></span>

<span data-ttu-id="04e4f-128">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="04e4f-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="04e4f-129">Kuzey Orta ABD</span><span class="sxs-lookup"><span data-stu-id="04e4f-129">North Central US</span></span>
- <span data-ttu-id="04e4f-130">Güney Orta ABD</span><span class="sxs-lookup"><span data-stu-id="04e4f-130">South Central US</span></span>
- <span data-ttu-id="04e4f-131">Orta ABD</span><span class="sxs-lookup"><span data-stu-id="04e4f-131">Central US</span></span>
- <span data-ttu-id="04e4f-132">Batı Avrupa</span><span class="sxs-lookup"><span data-stu-id="04e4f-132">West Europe</span></span>
- <span data-ttu-id="04e4f-133">Kuzey Avrupa</span><span class="sxs-lookup"><span data-stu-id="04e4f-133">North Europe</span></span>
- <span data-ttu-id="04e4f-134">Batı ABD</span><span class="sxs-lookup"><span data-stu-id="04e4f-134">West US</span></span>
- <span data-ttu-id="04e4f-135">Doğu ABD</span><span class="sxs-lookup"><span data-stu-id="04e4f-135">East US</span></span>
- <span data-ttu-id="04e4f-136">Doğu ABD 2</span><span class="sxs-lookup"><span data-stu-id="04e4f-136">East US 2</span></span>
- <span data-ttu-id="04e4f-137">Japon Doğu</span><span class="sxs-lookup"><span data-stu-id="04e4f-137">Japan East</span></span>
- <span data-ttu-id="04e4f-138">Japon Batı</span><span class="sxs-lookup"><span data-stu-id="04e4f-138">Japan West</span></span>
- <span data-ttu-id="04e4f-139">Brezilya Güney</span><span class="sxs-lookup"><span data-stu-id="04e4f-139">Brazil South</span></span>
- <span data-ttu-id="04e4f-140">Güneydoğu Asya</span><span class="sxs-lookup"><span data-stu-id="04e4f-140">Southeast Asia</span></span>
- <span data-ttu-id="04e4f-141">Doğu Asya</span><span class="sxs-lookup"><span data-stu-id="04e4f-141">East Asia</span></span>
- <span data-ttu-id="04e4f-142">Avustralya Doğu</span><span class="sxs-lookup"><span data-stu-id="04e4f-142">Australia East</span></span>
- <span data-ttu-id="04e4f-143">Avustralya Güneydoğu</span><span class="sxs-lookup"><span data-stu-id="04e4f-143">Australia Southeast</span></span>

```yaml
Type: System.String
Parameter Sets: Specific API Management service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04e4f-144">-Ad</span><span class="sxs-lookup"><span data-stu-id="04e4f-144">-Name</span></span>
<span data-ttu-id="04e4f-145">Bu cmdlet 'in güncelleştirdiği API yönetiminin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="04e4f-145">Specifies the name of API Management that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific API Management service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04e4f-146">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="04e4f-146">-PassThru</span></span>
<span data-ttu-id="04e4f-147">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="04e4f-147">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="04e4f-148">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="04e4f-148">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="04e4f-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04e4f-149">-ResourceGroupName</span></span>
<span data-ttu-id="04e4f-150">API yönetiminin altında bulunduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="04e4f-150">Specifies the name of resource group under which API Management exists.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific API Management service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04e4f-151">-SKU</span><span class="sxs-lookup"><span data-stu-id="04e4f-151">-Sku</span></span>
<span data-ttu-id="04e4f-152">Ana Azure API Yönetimi dağıtım bölgesinin katmanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="04e4f-152">Specifies the tier of the master Azure API Management deployment region.</span></span>

<span data-ttu-id="04e4f-153">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="04e4f-153">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="04e4f-154">İyle</span><span class="sxs-lookup"><span data-stu-id="04e4f-154">Developer</span></span>
- <span data-ttu-id="04e4f-155">Ardından</span><span class="sxs-lookup"><span data-stu-id="04e4f-155">Standard</span></span>
- <span data-ttu-id="04e4f-156">Min</span><span class="sxs-lookup"><span data-stu-id="04e4f-156">Premium</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku
Parameter Sets: Specific API Management service
Aliases: 
Accepted values: Developer, Standard, Premium

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04e4f-157">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="04e4f-157">-VirtualNetwork</span></span>
<span data-ttu-id="04e4f-158">Ana Azure API Yönetimi dağıtım bölgesinin sanal ağ yapılandırmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="04e4f-158">Specifies the Virtual Network configuration of the master Azure API Management deployment region.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: Specific API Management service
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04e4f-159">-VpnType</span><span class="sxs-lookup"><span data-stu-id="04e4f-159">-VpnType</span></span>
<span data-ttu-id="04e4f-160">API yönetim dağıtımının sanal ağ türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="04e4f-160">Specifies the virtual network Type of the API Management deployment.</span></span>
<span data-ttu-id="04e4f-161">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="04e4f-161">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="04e4f-162">Yabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="04e4f-162">None.</span></span>
<span data-ttu-id="04e4f-163">API yönetim dağıtımı hiçbir sanal ağın parçası değildir.</span><span class="sxs-lookup"><span data-stu-id="04e4f-163">The API Management deployment is not part of any Virtual Network.</span></span>
<span data-ttu-id="04e4f-164">Bu varsayılan değerdir.</span><span class="sxs-lookup"><span data-stu-id="04e4f-164">This is the default value.</span></span> 
- <span data-ttu-id="04e4f-165">External.</span><span class="sxs-lookup"><span data-stu-id="04e4f-165">External.</span></span>
<span data-ttu-id="04e4f-166">API yönetim dağıtımında dış bir açık sanal adres vardır.</span><span class="sxs-lookup"><span data-stu-id="04e4f-166">The API Management deployment has an external facing virtual address.</span></span> 
- <span data-ttu-id="04e4f-167">Ýç.</span><span class="sxs-lookup"><span data-stu-id="04e4f-167">Internal.</span></span>
<span data-ttu-id="04e4f-168">API yönetim dağıtımında, bir intranete bağlanan sanal adres vardır.</span><span class="sxs-lookup"><span data-stu-id="04e4f-168">The API Management deployment has an intranet facing virtual address.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVpnType
Parameter Sets: Specific API Management service
Aliases: 
Accepted values: None, External, Internal

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04e4f-169">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04e4f-169">-DefaultProfile</span></span>
<span data-ttu-id="04e4f-170">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="04e4f-170">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04e4f-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04e4f-171">CommonParameters</span></span>
<span data-ttu-id="04e4f-172">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="04e4f-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04e4f-173">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04e4f-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04e4f-174">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="04e4f-174">INPUTS</span></span>

### <span data-ttu-id="04e4f-175">Bağış</span><span class="sxs-lookup"><span data-stu-id="04e4f-175">PsApiManagement</span></span>
<span data-ttu-id="04e4f-176">Parametre ' Apsananadeğeri ', ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="04e4f-176">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="04e4f-177">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="04e4f-177">OUTPUTS</span></span>

### <span data-ttu-id="04e4f-178">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="04e4f-178">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="04e4f-179">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="04e4f-179">NOTES</span></span>

## <span data-ttu-id="04e4f-180">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="04e4f-180">RELATED LINKS</span></span>

[<span data-ttu-id="04e4f-181">Get-azurermapı</span><span class="sxs-lookup"><span data-stu-id="04e4f-181">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)


