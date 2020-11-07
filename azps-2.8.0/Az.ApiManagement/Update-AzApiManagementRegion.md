---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5B7B285A-6418-44D7-BD78-E14AFFAA7765
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/update-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementRegion.md
ms.openlocfilehash: 7fa565eb16ced9e9146b219d7850354e499ef06e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753389"
---
# <span data-ttu-id="a2310-101">Update-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="a2310-101">Update-AzApiManagementRegion</span></span>

## <span data-ttu-id="a2310-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2310-102">SYNOPSIS</span></span>
<span data-ttu-id="a2310-103">Psapımanadörneği örneğinde varolan dağıtım bölgesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="a2310-103">Updates existing deployment region in PsApiManagement instance.</span></span>

## <span data-ttu-id="a2310-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a2310-104">SYNTAX</span></span>

```
Update-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> -Sku <PsApiManagementSku>
 -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a2310-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a2310-105">DESCRIPTION</span></span>
<span data-ttu-id="a2310-106">**Update-Azapsananagementregion** cmdlet 'i, Microsoft. **Azure. Commands. Apsananamedid. model. Psapsananad,** sağlanan bir örnek **Addiregion** nesneleri koleksiyonunda **Microsoft. Azure. Commands**</span><span class="sxs-lookup"><span data-stu-id="a2310-106">The **Update-AzApiManagementRegion** cmdlet updates an existing instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** in a collection of **AdditionalRegions** objects of a provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="a2310-107">Bu cmdlet hiçbir şey dağıtmaz ancak bellekteki bir **Psapımanadın** örneğini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="a2310-107">This cmdlet does not deploy anything but updates an instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="a2310-108">Bir API yönetiminin dağıtımını güncelleştirmek için, değiştirilmiş **Psapsananagementınstance** 'ı Set-AzApiManagement cmdlet 'ine kullanın.</span><span class="sxs-lookup"><span data-stu-id="a2310-108">To update a deployment of an API Management use the modified **PsApiManagementInstance** to the Set-AzApiManagement cmdlet.</span></span>

## <span data-ttu-id="a2310-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a2310-109">EXAMPLES</span></span>

### <span data-ttu-id="a2310-110">Örnek 1: psapsanan</span><span class="sxs-lookup"><span data-stu-id="a2310-110">Example 1: Increases capacity of Additional Region in a PsApiManagement instance</span></span>
```powershell
PS C:\>$apimService = Get-AzApiManagement -ResourceGroupName $resourceGroupName -Name $apiManagementName
PS C:\>$apimService = Update-AzApiManagementRegion -ApiManagement $apimService -Location "North Central US" -Capacity 2 -Sku Premium
PS C:\>$apimService = Set-AzApiManagement -InputObject $apimService -PassThru
```

<span data-ttu-id="a2310-111">Bu komut, Güney Merkezi ABD ve Kuzey Merkezi ABD 'de bölgeleri bulunan API Yönetimi Premium SKU hizmetini alır.</span><span class="sxs-lookup"><span data-stu-id="a2310-111">This command gets the API Management Premium SKU service, having regions in South Central US and North Central US.</span></span> <span data-ttu-id="a2310-112">Ardından, **set-Azapsanana'i** kullanarak Kuzey Merkezi bölge kapasitesini 2 ile arttırır.</span><span class="sxs-lookup"><span data-stu-id="a2310-112">It then increases the Capacity of the North Central US region to 2 using the **Set-AzApiManagement**.</span></span> <span data-ttu-id="a2310-113">Sonraki cmdlet **kümesi-Azapda** yapılandırma değişikliği API Yönetim hizmetine uygulanır.</span><span class="sxs-lookup"><span data-stu-id="a2310-113">The next cmdlet **Set-AzApiManagement** applies the configuration change to the Api Management service.</span></span>

## <span data-ttu-id="a2310-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a2310-114">PARAMETERS</span></span>

### <span data-ttu-id="a2310-115">-Ucuz</span><span class="sxs-lookup"><span data-stu-id="a2310-115">-ApiManagement</span></span>
<span data-ttu-id="a2310-116">Var olan bir dağıtım bölgesini güncelleştirmek için **Psapimana,** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2310-116">Specifies the **PsApiManagement** instance to update an existing deployment region in.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2310-117">-Kapasite</span><span class="sxs-lookup"><span data-stu-id="a2310-117">-Capacity</span></span>
<span data-ttu-id="a2310-118">Dağıtım bölgesi için yeni SKU kapasite değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2310-118">Specifies the new SKU capacity value for the deployment region.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2310-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2310-119">-DefaultProfile</span></span>
<span data-ttu-id="a2310-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a2310-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2310-121">-Konum</span><span class="sxs-lookup"><span data-stu-id="a2310-121">-Location</span></span>
<span data-ttu-id="a2310-122">Güncelleştirilecek dağıtım bölgesinin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2310-122">Specifies the location of the deployment region to update.</span></span>
<span data-ttu-id="a2310-123">API yönetim hizmeti için desteklenen bölge arasındaki yeni dağıtım bölgesinin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2310-123">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="a2310-124">Geçerli konumlar almak için, "Microsoft. Apsananae" Get-AzResourceProvider cmdlet 'ini kullanın. WHERE {$ _. ResourceTypes [0]. ResourceTypeName-EQ "hizmet"} | Select-Object konumları</span><span class="sxs-lookup"><span data-stu-id="a2310-124">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="a2310-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="a2310-125">-Sku</span></span>
<span data-ttu-id="a2310-126">Dağıtım bölgesi için yeni katman değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2310-126">Specifies the new tier value for the deployment region.</span></span>
<span data-ttu-id="a2310-127">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="a2310-127">Valid values are:</span></span>
- <span data-ttu-id="a2310-128">İyle</span><span class="sxs-lookup"><span data-stu-id="a2310-128">Developer</span></span>
- <span data-ttu-id="a2310-129">Ardından</span><span class="sxs-lookup"><span data-stu-id="a2310-129">Standard</span></span>
- <span data-ttu-id="a2310-130">Min</span><span class="sxs-lookup"><span data-stu-id="a2310-130">Premium</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Standard, Premium, Basic, Consumption

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2310-131">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a2310-131">-VirtualNetwork</span></span>
<span data-ttu-id="a2310-132">Dağıtım bölgesi için sanal ağ yapılandırmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2310-132">Specifies a virtual network configuration for the deployment region.</span></span>
<span data-ttu-id="a2310-133">$Null geçirmek, bölgenin sanal ağ yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a2310-133">Passing $null will remove virtual network configuration for the region.</span></span>

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

### <span data-ttu-id="a2310-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2310-134">CommonParameters</span></span>
<span data-ttu-id="a2310-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a2310-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2310-136">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a2310-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2310-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a2310-137">INPUTS</span></span>

### <span data-ttu-id="a2310-138">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="a2310-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

### <span data-ttu-id="a2310-139">System. String</span><span class="sxs-lookup"><span data-stu-id="a2310-139">System.String</span></span>

### <span data-ttu-id="a2310-140">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="a2310-140">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku</span></span>

### <span data-ttu-id="a2310-141">System. Int32</span><span class="sxs-lookup"><span data-stu-id="a2310-141">System.Int32</span></span>

### <span data-ttu-id="a2310-142">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="a2310-142">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="a2310-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a2310-143">OUTPUTS</span></span>

### <span data-ttu-id="a2310-144">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="a2310-144">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="a2310-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a2310-145">NOTES</span></span>

## <span data-ttu-id="a2310-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a2310-146">RELATED LINKS</span></span>

[<span data-ttu-id="a2310-147">Add-Azapsananagementregion</span><span class="sxs-lookup"><span data-stu-id="a2310-147">Add-AzApiManagementRegion</span></span>](./Add-AzApiManagementRegion.md)

[<span data-ttu-id="a2310-148">Remove-Azapsananagementregion</span><span class="sxs-lookup"><span data-stu-id="a2310-148">Remove-AzApiManagementRegion</span></span>](./Remove-AzApiManagementRegion.md)

[<span data-ttu-id="a2310-149">Set-azapsanana</span><span class="sxs-lookup"><span data-stu-id="a2310-149">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)
