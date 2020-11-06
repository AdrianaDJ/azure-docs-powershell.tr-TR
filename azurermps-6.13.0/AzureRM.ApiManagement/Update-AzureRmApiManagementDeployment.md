---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 56604912-53A0-496D-9BDC-472BCE45A6A2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/update-azurermapimanagementdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementDeployment.md
ms.openlocfilehash: f8f0273ab624cd81488734f9b84debc045f6fed2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587322"
---
# <span data-ttu-id="fba80-101">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="fba80-101">Update-AzureRmApiManagementDeployment</span></span>

## <span data-ttu-id="fba80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fba80-102">SYNOPSIS</span></span>
<span data-ttu-id="fba80-103">Bir API yönetim hizmetinin dağıtımını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="fba80-103">Updates deployment of an API Management Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fba80-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fba80-104">SYNTAX</span></span>

### <span data-ttu-id="fba80-105">UpdateSpecificService (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fba80-105">UpdateSpecificService (Default)</span></span>
```
Update-AzureRmApiManagementDeployment -ResourceGroupName <String> -Name <String> -Location <String>
 -Sku <PsApiManagementSku> -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-VpnType <PsApiManagementVpnType>]
 [-AdditionalRegions <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fba80-106">Updatefrompsapsananagementınstance</span><span class="sxs-lookup"><span data-stu-id="fba80-106">UpdateFromPsApiManagementInstance</span></span>
```
Update-AzureRmApiManagementDeployment -ApiManagement <PsApiManagement> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fba80-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="fba80-107">DESCRIPTION</span></span>
<span data-ttu-id="fba80-108">**Güncelleştirme-Azurermapımanagementdeployment** cmdlet 'i, bir API yönetim hizmetinin geçerli dağıtımlarını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="fba80-108">The **Update-AzureRmApiManagementDeployment** cmdlet updates current deployments of an API Management service.</span></span>

## <span data-ttu-id="fba80-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fba80-109">EXAMPLES</span></span>

### <span data-ttu-id="fba80-110">Örnek 1: bir anlık ileti örneğinin dağıtımını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="fba80-110">Example 1: Update a deployment of an ApiManagement instance</span></span>
```powershell
PS C:\>Update-AzureRmApiManagementDeployment -ResourceGroupName "Contoso" -Name "ContosoApi" -Sku "Standard" -Capacity 3
```

<span data-ttu-id="fba80-111">Bu komut, API yönetim örneğinin dağıtımını üç birim kapasite standardına göre güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="fba80-111">This command updates deployment of an API Management instance to a three unit capacity standard.</span></span>

### <span data-ttu-id="fba80-112">Örnek 2: bir anlık ileti alma ve yeniden boyutlandırma</span><span class="sxs-lookup"><span data-stu-id="fba80-112">Example 2: Get an ApiManagement instance and rescale it</span></span>
```powershell
PS C:\>$ApiManagement = Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi"
PS C:\> $ApiManagement.Sku = "Premium"
PS C:\> $ApiManagement.Capacity = 5
PS C:\> $ApiManagement.AddRegion("Central US", "Premium", 3)
PS C:\> Update-AzureRmApiManagementDeployment -ApiManagement $ApiManagement
```

<span data-ttu-id="fba80-113">Bu örnekte bir API yönetim örneği alınır, bunu beş Premium birime ölçeklendirir ve Premium bölgeye ek üç birim ekler.</span><span class="sxs-lookup"><span data-stu-id="fba80-113">This example gets an Api Management instance, scales it to five premium units and then adds an additional three units to the premium region.</span></span>

### <span data-ttu-id="fba80-114">Örnek 3: güncelleştirme dağıtımı (dış VNET)</span><span class="sxs-lookup"><span data-stu-id="fba80-114">Example 3: Update deployment (external VNET)</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-WestUS/providers/Microsoft.Network/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $virtualNetwork -VpnType "External"
```

<span data-ttu-id="fba80-115">Bu komut, var olan bir API yönetim dağıtımını güncelleştirir ve bir dış *Vpntype* 'a katılır.</span><span class="sxs-lookup"><span data-stu-id="fba80-115">This command updates an existing API Management deployment and joins to an external *VpnType*.</span></span>

### <span data-ttu-id="fba80-116">Örnek 4: güncelleştirme dağıtımı (iç VNET)</span><span class="sxs-lookup"><span data-stu-id="fba80-116">Example 4: Update deployment (internal VNET)</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-WestUS/providers/Microsoft.ClassicNetwork/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $virtualNetwork -VpnType "Internal"
```

<span data-ttu-id="fba80-117">Bu komut, var olan bir API yönetim dağıtımını güncelleştirir ve bir iç *Vpntype* 'a katılır.</span><span class="sxs-lookup"><span data-stu-id="fba80-117">This command updates an existing API Management deployment and joins to an internal *VpnType*.</span></span>

## <span data-ttu-id="fba80-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fba80-118">PARAMETERS</span></span>

### <span data-ttu-id="fba80-119">-Additionalbölgelerle</span><span class="sxs-lookup"><span data-stu-id="fba80-119">-AdditionalRegions</span></span>
<span data-ttu-id="fba80-120">Azure API Yönetimi 'nin ek dağıtım bölgelerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fba80-120">Specifies additional deployment regions of Azure API Management.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion]
Parameter Sets: UpdateSpecificService
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fba80-121">-Ucuz</span><span class="sxs-lookup"><span data-stu-id="fba80-121">-ApiManagement</span></span>
<span data-ttu-id="fba80-122">Dağıtım yapılandırmasını almak için **Psapimana,** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fba80-122">Specifies the **PsApiManagement** instance to get deployment configuration from.</span></span>
<span data-ttu-id="fba80-123">Örnekte gerekli tüm değişiklikler varsa bu parametreyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="fba80-123">Use this parameter if the instance already has all the required changes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: UpdateFromPsApiManagementInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fba80-124">-Kapasite</span><span class="sxs-lookup"><span data-stu-id="fba80-124">-Capacity</span></span>
<span data-ttu-id="fba80-125">Ana Azure API Yönetimi dağıtım bölgesinin SKU kapasitesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fba80-125">Specifies the SKU capacity of the master Azure API Management deployment region.</span></span>

```yaml
Type: System.Int32
Parameter Sets: UpdateSpecificService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fba80-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fba80-126">-DefaultProfile</span></span>
<span data-ttu-id="fba80-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fba80-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fba80-128">-Konum</span><span class="sxs-lookup"><span data-stu-id="fba80-128">-Location</span></span>
<span data-ttu-id="fba80-129">Master API Yönetimi dağıtım bölgesinin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="fba80-129">Specifies the location of the master API Management deployment region.</span></span>
<span data-ttu-id="fba80-130">Geçerli konumlar almak için, "Microsoft. Apsananae" Get-AzureRmResourceProvider cmdlet 'ini kullanın. WHERE {$ _. ResourceTypes [0]. ResourceTypeName-EQ "hizmet"} | Select-Object konumları</span><span class="sxs-lookup"><span data-stu-id="fba80-130">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateSpecificService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fba80-131">-Ad</span><span class="sxs-lookup"><span data-stu-id="fba80-131">-Name</span></span>
<span data-ttu-id="fba80-132">Bu cmdlet 'in güncelleştirdiği API yönetiminin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fba80-132">Specifies the name of API Management that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateSpecificService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fba80-133">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="fba80-133">-PassThru</span></span>
<span data-ttu-id="fba80-134">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="fba80-134">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fba80-135">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="fba80-135">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fba80-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fba80-136">-ResourceGroupName</span></span>
<span data-ttu-id="fba80-137">API yönetiminin altında bulunduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fba80-137">Specifies the name of resource group under which API Management exists.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateSpecificService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fba80-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="fba80-138">-Sku</span></span>
<span data-ttu-id="fba80-139">Ana Azure API Yönetimi dağıtım bölgesinin katmanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fba80-139">Specifies the tier of the master Azure API Management deployment region.</span></span>
<span data-ttu-id="fba80-140">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="fba80-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fba80-141">İyle</span><span class="sxs-lookup"><span data-stu-id="fba80-141">Developer</span></span>
- <span data-ttu-id="fba80-142">Ardından</span><span class="sxs-lookup"><span data-stu-id="fba80-142">Standard</span></span>
- <span data-ttu-id="fba80-143">Min</span><span class="sxs-lookup"><span data-stu-id="fba80-143">Premium</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku
Parameter Sets: UpdateSpecificService
Aliases:
Accepted values: Developer, Standard, Premium, Basic

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fba80-144">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fba80-144">-VirtualNetwork</span></span>
<span data-ttu-id="fba80-145">Ana Azure API Yönetimi dağıtım bölgesinin sanal ağ yapılandırmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fba80-145">Specifies the Virtual Network configuration of the master Azure API Management deployment region.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: UpdateSpecificService
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fba80-146">-VpnType</span><span class="sxs-lookup"><span data-stu-id="fba80-146">-VpnType</span></span>
<span data-ttu-id="fba80-147">API yönetim dağıtımının sanal ağ türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="fba80-147">Specifies the virtual network Type of the API Management deployment.</span></span>
<span data-ttu-id="fba80-148">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="fba80-148">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fba80-149">Yabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fba80-149">None.</span></span>
<span data-ttu-id="fba80-150">API yönetim dağıtımı hiçbir sanal ağın parçası değildir.</span><span class="sxs-lookup"><span data-stu-id="fba80-150">The API Management deployment is not part of any Virtual Network.</span></span>
<span data-ttu-id="fba80-151">Bu varsayılan değerdir.</span><span class="sxs-lookup"><span data-stu-id="fba80-151">This is the default value.</span></span> 
- <span data-ttu-id="fba80-152">External.</span><span class="sxs-lookup"><span data-stu-id="fba80-152">External.</span></span>
<span data-ttu-id="fba80-153">API yönetim dağıtımında dış bir açık sanal adres vardır.</span><span class="sxs-lookup"><span data-stu-id="fba80-153">The API Management deployment has an external facing virtual address.</span></span> 
- <span data-ttu-id="fba80-154">Ýç.</span><span class="sxs-lookup"><span data-stu-id="fba80-154">Internal.</span></span>
<span data-ttu-id="fba80-155">API yönetim dağıtımında, bir intranete bağlanan sanal adres vardır.</span><span class="sxs-lookup"><span data-stu-id="fba80-155">The API Management deployment has an intranet facing virtual address.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVpnType
Parameter Sets: UpdateSpecificService
Aliases:
Accepted values: None, External, Internal

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fba80-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fba80-156">CommonParameters</span></span>
<span data-ttu-id="fba80-157">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fba80-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fba80-158">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fba80-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fba80-159">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fba80-159">INPUTS</span></span>

### <span data-ttu-id="fba80-160">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="fba80-160">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>
<span data-ttu-id="fba80-161">Parametreler: Apsananad(ByValue)</span><span class="sxs-lookup"><span data-stu-id="fba80-161">Parameters: ApiManagement (ByValue)</span></span>

### <span data-ttu-id="fba80-162">System. String</span><span class="sxs-lookup"><span data-stu-id="fba80-162">System.String</span></span>

### <span data-ttu-id="fba80-163">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="fba80-163">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku</span></span>

### <span data-ttu-id="fba80-164">System. Int32</span><span class="sxs-lookup"><span data-stu-id="fba80-164">System.Int32</span></span>

### <span data-ttu-id="fba80-165">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="fba80-165">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

### <span data-ttu-id="fba80-166">Microsoft. Azure. Commands. apsananad</span><span class="sxs-lookup"><span data-stu-id="fba80-166">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVpnType</span></span>

### <span data-ttu-id="fba80-167">System. Koleksiyonlar. Generic. IList ' 1 [[Microsoft. Azure. Commands. Apsananad. modeller. Psapsananagementregion, Microsoft. Azure. Commands. Apsananad, Version = 6.1.2.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="fba80-167">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion, Microsoft.Azure.Commands.ApiManagement, Version=6.1.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="fba80-168">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fba80-168">OUTPUTS</span></span>

### <span data-ttu-id="fba80-169">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="fba80-169">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="fba80-170">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fba80-170">NOTES</span></span>

## <span data-ttu-id="fba80-171">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fba80-171">RELATED LINKS</span></span>

[<span data-ttu-id="fba80-172">Get-azurermapı</span><span class="sxs-lookup"><span data-stu-id="fba80-172">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)


