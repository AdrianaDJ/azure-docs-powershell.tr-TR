---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 9D4A68A8-0A39-4C9A-8EA6-391A5E7A0E25
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementRegion.md
ms.openlocfilehash: 172bd1490b105b942dc706afe9440030d39d5c49
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109261"
---
# <span data-ttu-id="3bd05-101">Add-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="3bd05-101">Add-AzApiManagementRegion</span></span>

## <span data-ttu-id="3bd05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3bd05-102">SYNOPSIS</span></span>
<span data-ttu-id="3bd05-103">Psapsananamı örneğine yeni dağıtım bölgeleri ekler.</span><span class="sxs-lookup"><span data-stu-id="3bd05-103">Adds new deployment regions to a PsApiManagement instance.</span></span>

## <span data-ttu-id="3bd05-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3bd05-104">SYNTAX</span></span>

```
Add-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> [-Sku <PsApiManagementSku>]
 [-Capacity <Int32>] [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3bd05-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3bd05-105">DESCRIPTION</span></span>
<span data-ttu-id="3bd05-106">**Add-Azapsananagementregion** cmdlet 'ı, **psapimanagementregion** türünde sağlanan **Microsoft. Azure. Commands. Apsananad. model** **AdditionalRegions**</span><span class="sxs-lookup"><span data-stu-id="3bd05-106">The **Add-AzApiManagementRegion** cmdlet adds new instance of type **PsApiManagementRegion** to the collection of **AdditionalRegions** of provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="3bd05-107">Bu cmdlet kendisiyle hiçbir şey dağıtmaz ancak bellekteki **Psapımana**</span><span class="sxs-lookup"><span data-stu-id="3bd05-107">This cmdlet does not deploy anything by itself but updates instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="3bd05-108">Bir API yönetiminin dağıtımını güncelleştirmek için, değiştirilmiş **Psapsananadınstance** öğesini ayarlanacak şekilde ayarlayın</span><span class="sxs-lookup"><span data-stu-id="3bd05-108">To update a deployment of an API Management pass the modified **PsApiManagement** Instance to Set-AzApiManagement.</span></span>

## <span data-ttu-id="3bd05-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3bd05-109">EXAMPLES</span></span>

### <span data-ttu-id="3bd05-110">Örnek 1: bir Psapsanana, bir örneğine yeni dağıtım bölgeleri ekleme</span><span class="sxs-lookup"><span data-stu-id="3bd05-110">Example 1: Add new deployment regions to a PsApiManagement instance</span></span>
```
PS C:\>Add-AzApiManagementRegion -ApiManagement $ApiManagement -Location "East US" -Sku "Premium" -Capacity 2
```

<span data-ttu-id="3bd05-111">Bu komut iki Premium SKU birimi ve Doğu ABD adlı bölgeyi **Psapımanadıman**</span><span class="sxs-lookup"><span data-stu-id="3bd05-111">This command adds two premium SKU units and the region named East US to the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="3bd05-112">Örnek 2: psapsananadın</span><span class="sxs-lookup"><span data-stu-id="3bd05-112">Example 2: Add new deployment regions to a PsApiManagement instance and then update deployment</span></span>
```powershell
PS C:\>$service = Get-AzApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi"
PS C:\>$service = Add-AzApiManagementRegion -ApiManagement $service -Location $secondarylocation -VirtualNetwork $additionalRegionVirtualNetwork
PS C:\>$service = Set-AzApiManagement -InputObject $service -PassThru
```

<span data-ttu-id="3bd05-113">Bu komut, **Psapsanananabir** nesne alır, Doğu ABD adlı bölge için ıkı Premium SKU birimi ekler ve ardından dağıtımı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="3bd05-113">This command gets a **PsApiManagement** object, adds two premium SKU units for the region named East US, and then updates deployment.</span></span>

## <span data-ttu-id="3bd05-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3bd05-114">PARAMETERS</span></span>

### <span data-ttu-id="3bd05-115">-Ucuz</span><span class="sxs-lookup"><span data-stu-id="3bd05-115">-ApiManagement</span></span>
<span data-ttu-id="3bd05-116">Bu cmdlet 'in ek dağıtım bölgelerini eklediği **Psapimana,** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3bd05-116">Specifies the **PsApiManagement** instance that this cmdlet adds additional deployment regions to.</span></span>

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

### <span data-ttu-id="3bd05-117">-Kapasite</span><span class="sxs-lookup"><span data-stu-id="3bd05-117">-Capacity</span></span>
<span data-ttu-id="3bd05-118">Dağıtım bölgesinin SKU kapasitesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3bd05-118">Specifies the SKU capacity of the deployment region.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bd05-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bd05-119">-DefaultProfile</span></span>
<span data-ttu-id="3bd05-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3bd05-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3bd05-121">-Konum</span><span class="sxs-lookup"><span data-stu-id="3bd05-121">-Location</span></span>
<span data-ttu-id="3bd05-122">API yönetim hizmeti için desteklenen bölge arasındaki yeni dağıtım bölgesinin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="3bd05-122">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="3bd05-123">Geçerli konumlar almak için, "Microsoft. Apsananae" Get-AzResourceProvider cmdlet 'ini kullanın. WHERE {$ _. ResourceTypes [0]. ResourceTypeName-EQ "hizmet"} | Select-Object konumları</span><span class="sxs-lookup"><span data-stu-id="3bd05-123">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bd05-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="3bd05-124">-Sku</span></span>
<span data-ttu-id="3bd05-125">Dağıtım bölgesinin katmanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3bd05-125">Specifies the tier of the deployment region.</span></span>
<span data-ttu-id="3bd05-126">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="3bd05-126">Valid values are:</span></span> 
- <span data-ttu-id="3bd05-127">İyle</span><span class="sxs-lookup"><span data-stu-id="3bd05-127">Developer</span></span>
- <span data-ttu-id="3bd05-128">Ardından</span><span class="sxs-lookup"><span data-stu-id="3bd05-128">Standard</span></span>
- <span data-ttu-id="3bd05-129">Min</span><span class="sxs-lookup"><span data-stu-id="3bd05-129">Premium</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Standard, Premium, Basic, Consumption

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bd05-130">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="3bd05-130">-VirtualNetwork</span></span>
<span data-ttu-id="3bd05-131">Sanal ağ yapılandırmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3bd05-131">Specifies a virtual network configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bd05-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bd05-132">CommonParameters</span></span>
<span data-ttu-id="3bd05-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3bd05-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bd05-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3bd05-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bd05-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3bd05-135">INPUTS</span></span>

### <span data-ttu-id="3bd05-136">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="3bd05-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="3bd05-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3bd05-137">OUTPUTS</span></span>

### <span data-ttu-id="3bd05-138">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="3bd05-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="3bd05-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3bd05-139">NOTES</span></span>
* <span data-ttu-id="3bd05-140">Cmdlet, güncelleştirilmiş **Psapsananadörneği** ardışık düzene yazar.</span><span class="sxs-lookup"><span data-stu-id="3bd05-140">The cmdlet writes updated **PsApiManagement** instance to pipeline.</span></span>

## <span data-ttu-id="3bd05-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3bd05-141">RELATED LINKS</span></span>

[<span data-ttu-id="3bd05-142">Remove-Azapsananagementregion</span><span class="sxs-lookup"><span data-stu-id="3bd05-142">Remove-AzApiManagementRegion</span></span>](./Remove-AzApiManagementRegion.md)

[<span data-ttu-id="3bd05-143">Güncelleştirme-Azapsananagementregion</span><span class="sxs-lookup"><span data-stu-id="3bd05-143">Update-AzApiManagementRegion</span></span>](./Update-AzApiManagementRegion.md)

[<span data-ttu-id="3bd05-144">Set-azapsanana</span><span class="sxs-lookup"><span data-stu-id="3bd05-144">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)


