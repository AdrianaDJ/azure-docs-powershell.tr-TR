---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5B7B285A-6418-44D7-BD78-E14AFFAA7765
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementRegion.md
ms.openlocfilehash: 29dd6d1938228d3e76c0393ca27f49a3a9fe2564
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587009"
---
# <span data-ttu-id="9a5c1-101">Update-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="9a5c1-101">Update-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="9a5c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a5c1-102">SYNOPSIS</span></span>
<span data-ttu-id="9a5c1-103">Psapımanadörneği örneğinde varolan dağıtım bölgesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="9a5c1-103">Updates existing deployment region in PsApiManagement instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a5c1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9a5c1-104">SYNTAX</span></span>

```
Update-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> -Sku <PsApiManagementSku>
 -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9a5c1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9a5c1-105">DESCRIPTION</span></span>
<span data-ttu-id="9a5c1-106">**Update-Azurermapsananagementregion** cmdlet 'ı, **Microsoft. Azure. Commands. Apsananamedid. model. Psapsananad,** sağlanan bir örnek **Addiregion** nesneleri koleksiyonunda **Microsoft. Azure. Commands**</span><span class="sxs-lookup"><span data-stu-id="9a5c1-106">The **Update-AzureRmApiManagementRegion** cmdlet updates an existing instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** in a collection of **AdditionalRegions** objects of a provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="9a5c1-107">Bu cmdlet hiçbir şey dağıtmaz ancak bellekteki bir **Psapımanadın** örneğini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="9a5c1-107">This cmdlet does not deploy anything but updates an instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="9a5c1-108">Bir API yönetiminin dağıtımını güncelleştirmek için, değiştirilmiş **Psapsananagementınstance** 'ı Update-AzureRmApiManagementDeployment cmdlet 'ine kullanın.</span><span class="sxs-lookup"><span data-stu-id="9a5c1-108">To update a deployment of an API Management use the modified **PsApiManagementInstance** to the Update-AzureRmApiManagementDeployment cmdlet.</span></span>

## <span data-ttu-id="9a5c1-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9a5c1-109">EXAMPLES</span></span>

## <span data-ttu-id="9a5c1-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9a5c1-110">PARAMETERS</span></span>

### <span data-ttu-id="9a5c1-111">-Ucuz</span><span class="sxs-lookup"><span data-stu-id="9a5c1-111">-ApiManagement</span></span>
<span data-ttu-id="9a5c1-112">Var olan bir dağıtım bölgesini güncelleştirmek için **Psapimana,** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9a5c1-112">Specifies the **PsApiManagement** instance to update an existing deployment region in.</span></span>

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

### <span data-ttu-id="9a5c1-113">-Kapasite</span><span class="sxs-lookup"><span data-stu-id="9a5c1-113">-Capacity</span></span>
<span data-ttu-id="9a5c1-114">Dağıtım bölgesi için yeni SKU kapasite değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9a5c1-114">Specifies the new SKU capacity value for the deployment region.</span></span>

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

### <span data-ttu-id="9a5c1-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="9a5c1-115">-Location</span></span>
<span data-ttu-id="9a5c1-116">Güncelleştirilecek dağıtım bölgesinin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="9a5c1-116">Specifies the location of the deployment region to update.</span></span>

<span data-ttu-id="9a5c1-117">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="9a5c1-117">Valid values are:</span></span>

- <span data-ttu-id="9a5c1-118">Kuzey Orta ABD</span><span class="sxs-lookup"><span data-stu-id="9a5c1-118">North Central US</span></span>
- <span data-ttu-id="9a5c1-119">Güney Orta ABD</span><span class="sxs-lookup"><span data-stu-id="9a5c1-119">South Central US</span></span>
- <span data-ttu-id="9a5c1-120">Orta ABD</span><span class="sxs-lookup"><span data-stu-id="9a5c1-120">Central US</span></span>
- <span data-ttu-id="9a5c1-121">Batı Avrupa</span><span class="sxs-lookup"><span data-stu-id="9a5c1-121">West Europe</span></span>
- <span data-ttu-id="9a5c1-122">Kuzey Avrupa</span><span class="sxs-lookup"><span data-stu-id="9a5c1-122">North Europe</span></span>
- <span data-ttu-id="9a5c1-123">Batı ABD</span><span class="sxs-lookup"><span data-stu-id="9a5c1-123">West US</span></span>
- <span data-ttu-id="9a5c1-124">Doğu ABD</span><span class="sxs-lookup"><span data-stu-id="9a5c1-124">East US</span></span>
- <span data-ttu-id="9a5c1-125">Doğu ABD 2</span><span class="sxs-lookup"><span data-stu-id="9a5c1-125">East US 2</span></span>
- <span data-ttu-id="9a5c1-126">Japon Doğu</span><span class="sxs-lookup"><span data-stu-id="9a5c1-126">Japan East</span></span>
- <span data-ttu-id="9a5c1-127">Japon Batı</span><span class="sxs-lookup"><span data-stu-id="9a5c1-127">Japan West</span></span>
- <span data-ttu-id="9a5c1-128">Brezilya Güney</span><span class="sxs-lookup"><span data-stu-id="9a5c1-128">Brazil South</span></span>
- <span data-ttu-id="9a5c1-129">Güneydoğu Asya</span><span class="sxs-lookup"><span data-stu-id="9a5c1-129">Southeast Asia</span></span>
- <span data-ttu-id="9a5c1-130">Doğu Asya</span><span class="sxs-lookup"><span data-stu-id="9a5c1-130">East Asia</span></span>
- <span data-ttu-id="9a5c1-131">Avustralya Doğu</span><span class="sxs-lookup"><span data-stu-id="9a5c1-131">Australia East</span></span>
- <span data-ttu-id="9a5c1-132">Avustralya Güneydoğu</span><span class="sxs-lookup"><span data-stu-id="9a5c1-132">Australia Southeast</span></span>

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

### <span data-ttu-id="9a5c1-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="9a5c1-133">-Sku</span></span>
<span data-ttu-id="9a5c1-134">Dağıtım bölgesi için yeni katman değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9a5c1-134">Specifies the new tier value for the deployment region.</span></span>

<span data-ttu-id="9a5c1-135">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="9a5c1-135">Valid values are:</span></span>

- <span data-ttu-id="9a5c1-136">İyle</span><span class="sxs-lookup"><span data-stu-id="9a5c1-136">Developer</span></span>
- <span data-ttu-id="9a5c1-137">Ardından</span><span class="sxs-lookup"><span data-stu-id="9a5c1-137">Standard</span></span>
- <span data-ttu-id="9a5c1-138">Min</span><span class="sxs-lookup"><span data-stu-id="9a5c1-138">Premium</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku
Parameter Sets: (All)
Aliases: 
Accepted values: Developer, Standard, Premium

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a5c1-139">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9a5c1-139">-VirtualNetwork</span></span>
<span data-ttu-id="9a5c1-140">Dağıtım bölgesi için sanal ağ yapılandırmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9a5c1-140">Specifies a virtual network configuration for the deployment region.</span></span>
<span data-ttu-id="9a5c1-141">$Null geçirmek, bölgenin sanal ağ yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9a5c1-141">Passing $null will remove virtual network configuration for the region.</span></span>

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

### <span data-ttu-id="9a5c1-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a5c1-142">-DefaultProfile</span></span>
<span data-ttu-id="9a5c1-143">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9a5c1-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a5c1-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a5c1-144">CommonParameters</span></span>
<span data-ttu-id="9a5c1-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9a5c1-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a5c1-146">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a5c1-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a5c1-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9a5c1-147">INPUTS</span></span>

### <span data-ttu-id="9a5c1-148">Bağış</span><span class="sxs-lookup"><span data-stu-id="9a5c1-148">PsApiManagement</span></span>
<span data-ttu-id="9a5c1-149">Parametre ' Apsananadeğeri ', ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="9a5c1-149">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="9a5c1-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9a5c1-150">OUTPUTS</span></span>

### <span data-ttu-id="9a5c1-151">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="9a5c1-151">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="9a5c1-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9a5c1-152">NOTES</span></span>

## <span data-ttu-id="9a5c1-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9a5c1-153">RELATED LINKS</span></span>

[<span data-ttu-id="9a5c1-154">Add-Azurermapımanagementregion</span><span class="sxs-lookup"><span data-stu-id="9a5c1-154">Add-AzureRmApiManagementRegion</span></span>](./Add-AzureRmApiManagementRegion.md)

[<span data-ttu-id="9a5c1-155">Remove-Azurermapımanagementregion</span><span class="sxs-lookup"><span data-stu-id="9a5c1-155">Remove-AzureRmApiManagementRegion</span></span>](./Remove-AzureRmApiManagementRegion.md)

[<span data-ttu-id="9a5c1-156">Güncelleştirme-Azurermapımanagementdeployment</span><span class="sxs-lookup"><span data-stu-id="9a5c1-156">Update-AzureRmApiManagementDeployment</span></span>](./Update-AzureRmApiManagementDeployment.md)
