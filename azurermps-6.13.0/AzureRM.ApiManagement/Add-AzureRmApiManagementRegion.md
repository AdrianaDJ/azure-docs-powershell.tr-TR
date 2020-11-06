---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 9D4A68A8-0A39-4C9A-8EA6-391A5E7A0E25
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/add-azurermapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementRegion.md
ms.openlocfilehash: 9ea4b734eba1ed1a37a72e756c32acc3d6ad2a32
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591479"
---
# <span data-ttu-id="00ad2-101">Add-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="00ad2-101">Add-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="00ad2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00ad2-102">SYNOPSIS</span></span>
<span data-ttu-id="00ad2-103">Psapsananamı örneğine yeni dağıtım bölgeleri ekler.</span><span class="sxs-lookup"><span data-stu-id="00ad2-103">Adds new deployment regions to a PsApiManagement instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00ad2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="00ad2-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> [-Sku <PsApiManagementSku>]
 [-Capacity <Int32>] [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00ad2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="00ad2-105">DESCRIPTION</span></span>
<span data-ttu-id="00ad2-106">**Add-Azurermapsananagementregion** cmdlet 'ı, **psapsananagementregion** türünde sağlanan **Microsoft. Azure. Commands. Apsananad. model** **AdditionalRegions**</span><span class="sxs-lookup"><span data-stu-id="00ad2-106">The **Add-AzureRmApiManagementRegion** cmdlet adds new instance of type **PsApiManagementRegion** to the collection of **AdditionalRegions** of provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="00ad2-107">Bu cmdlet kendisiyle hiçbir şey dağıtmaz ancak bellekteki **Psapımana**</span><span class="sxs-lookup"><span data-stu-id="00ad2-107">This cmdlet does not deploy anything by itself but updates instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="00ad2-108">API yönetiminin dağıtımını güncelleştirmek için, değiştirilmiş **Psapımanadınstance** öğesini Update-Azurermapsananagementdeployment öğesine geçirin.</span><span class="sxs-lookup"><span data-stu-id="00ad2-108">To update a deployment of an API Management pass the modified **PsApiManagement** Instance to Update-AzureRmApiManagementDeployment.</span></span>

## <span data-ttu-id="00ad2-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="00ad2-109">EXAMPLES</span></span>

### <span data-ttu-id="00ad2-110">Örnek 1: bir Psapsanana, bir örneğine yeni dağıtım bölgeleri ekleme</span><span class="sxs-lookup"><span data-stu-id="00ad2-110">Example 1: Add new deployment regions to a PsApiManagement instance</span></span>
```
PS C:\>Add-AzureRmApiManagementRegion -ApiManagement $ApiManagement -Location "East US" -Sku "Premium" -Capacity 2
```

<span data-ttu-id="00ad2-111">Bu komut iki Premium SKU birimi ve Doğu ABD adlı bölgeyi **Psapımanadıman**</span><span class="sxs-lookup"><span data-stu-id="00ad2-111">This command adds two premium SKU units and the region named East US to the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="00ad2-112">Örnek 2: psapsananadın</span><span class="sxs-lookup"><span data-stu-id="00ad2-112">Example 2: Add new deployment regions to a PsApiManagement instance and then update deployment</span></span>
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi" | Add-AzureRmApiManagementRegion -Location "East US" -Sku "Premium" -Capacity 2 | Update-AzureRmApiManagementDeployment
```

<span data-ttu-id="00ad2-113">Bu komut, **Psapsanananabir** nesne alır, Doğu ABD adlı bölge için ıkı Premium SKU birimi ekler ve ardından dağıtımı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="00ad2-113">This command gets a **PsApiManagement** object, adds two premium SKU units for the region named East US, and then updates deployment.</span></span>

## <span data-ttu-id="00ad2-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="00ad2-114">PARAMETERS</span></span>

### <span data-ttu-id="00ad2-115">-Ucuz</span><span class="sxs-lookup"><span data-stu-id="00ad2-115">-ApiManagement</span></span>
<span data-ttu-id="00ad2-116">Bu cmdlet 'in ek dağıtım bölgelerini eklediği **Psapimana,** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="00ad2-116">Specifies the **PsApiManagement** instance that this cmdlet adds additional deployment regions to.</span></span>

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

### <span data-ttu-id="00ad2-117">-Kapasite</span><span class="sxs-lookup"><span data-stu-id="00ad2-117">-Capacity</span></span>
<span data-ttu-id="00ad2-118">Dağıtım bölgesinin SKU kapasitesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="00ad2-118">Specifies the SKU capacity of the deployment region.</span></span>

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

### <span data-ttu-id="00ad2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00ad2-119">-DefaultProfile</span></span>
<span data-ttu-id="00ad2-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="00ad2-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00ad2-121">-Konum</span><span class="sxs-lookup"><span data-stu-id="00ad2-121">-Location</span></span>
<span data-ttu-id="00ad2-122">API yönetim hizmeti için desteklenen bölge arasındaki yeni dağıtım bölgesinin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="00ad2-122">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="00ad2-123">Geçerli konumlar almak için, "Microsoft. Apsananae" Get-AzureRmResourceProvider cmdlet 'ini kullanın. WHERE {$ _. ResourceTypes [0]. ResourceTypeName-EQ "hizmet"} | Select-Object konumları</span><span class="sxs-lookup"><span data-stu-id="00ad2-123">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="00ad2-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="00ad2-124">-Sku</span></span>
<span data-ttu-id="00ad2-125">Dağıtım bölgesinin katmanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="00ad2-125">Specifies the tier of the deployment region.</span></span>
<span data-ttu-id="00ad2-126">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="00ad2-126">Valid values are:</span></span> 
- <span data-ttu-id="00ad2-127">İyle</span><span class="sxs-lookup"><span data-stu-id="00ad2-127">Developer</span></span>
- <span data-ttu-id="00ad2-128">Ardından</span><span class="sxs-lookup"><span data-stu-id="00ad2-128">Standard</span></span>
- <span data-ttu-id="00ad2-129">Min</span><span class="sxs-lookup"><span data-stu-id="00ad2-129">Premium</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Standard, Premium, Basic

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00ad2-130">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="00ad2-130">-VirtualNetwork</span></span>
<span data-ttu-id="00ad2-131">Sanal ağ yapılandırmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="00ad2-131">Specifies a virtual network configuration.</span></span>

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

### <span data-ttu-id="00ad2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00ad2-132">CommonParameters</span></span>
<span data-ttu-id="00ad2-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="00ad2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00ad2-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00ad2-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00ad2-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="00ad2-135">INPUTS</span></span>

### <span data-ttu-id="00ad2-136">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="00ad2-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>
<span data-ttu-id="00ad2-137">Parametreler: Apsananad(ByValue)</span><span class="sxs-lookup"><span data-stu-id="00ad2-137">Parameters: ApiManagement (ByValue)</span></span>

## <span data-ttu-id="00ad2-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="00ad2-138">OUTPUTS</span></span>

### <span data-ttu-id="00ad2-139">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="00ad2-139">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="00ad2-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="00ad2-140">NOTES</span></span>
* <span data-ttu-id="00ad2-141">Cmdlet, güncelleştirilmiş **Psapsananadörneği** ardışık düzene yazar.</span><span class="sxs-lookup"><span data-stu-id="00ad2-141">The cmdlet writes updated **PsApiManagement** instance to pipeline.</span></span>

## <span data-ttu-id="00ad2-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="00ad2-142">RELATED LINKS</span></span>

[<span data-ttu-id="00ad2-143">Remove-Azurermapımanagementregion</span><span class="sxs-lookup"><span data-stu-id="00ad2-143">Remove-AzureRmApiManagementRegion</span></span>](./Remove-AzureRmApiManagementRegion.md)

[<span data-ttu-id="00ad2-144">Güncelleştirme-azurermapsanana</span><span class="sxs-lookup"><span data-stu-id="00ad2-144">Update-AzureRmApiManagementRegion</span></span>](./Update-AzureRmApiManagementRegion.md)

[<span data-ttu-id="00ad2-145">Güncelleştirme-Azurermapımanagementdeployment</span><span class="sxs-lookup"><span data-stu-id="00ad2-145">Update-AzureRmApiManagementDeployment</span></span>](./Update-AzureRmApiManagementDeployment.md)


