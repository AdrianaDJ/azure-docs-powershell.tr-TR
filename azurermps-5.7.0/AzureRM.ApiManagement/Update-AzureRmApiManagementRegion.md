---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: 5B7B285A-6418-44D7-BD78-E14AFFAA7765
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/update-azurermapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementRegion.md
ms.openlocfilehash: d6c97ac0fc948ba3ee4f86a2e657a1386c693f73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764041"
---
# <span data-ttu-id="1b592-101">Update-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="1b592-101">Update-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="1b592-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b592-102">SYNOPSIS</span></span>
<span data-ttu-id="1b592-103">Psapımanadörneği örneğinde varolan dağıtım bölgesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="1b592-103">Updates existing deployment region in PsApiManagement instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b592-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1b592-104">SYNTAX</span></span>

```
Update-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> -Sku <PsApiManagementSku>
 -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1b592-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1b592-105">DESCRIPTION</span></span>
<span data-ttu-id="1b592-106">**Update-Azurermapsananagementregion** cmdlet 'ı, **Microsoft. Azure. Commands. Apsananamedid. model. Psapsananad,** sağlanan bir örnek **Addiregion** nesneleri koleksiyonunda **Microsoft. Azure. Commands**</span><span class="sxs-lookup"><span data-stu-id="1b592-106">The **Update-AzureRmApiManagementRegion** cmdlet updates an existing instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** in a collection of **AdditionalRegions** objects of a provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="1b592-107">Bu cmdlet hiçbir şey dağıtmaz ancak bellekteki bir **Psapımanadın** örneğini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="1b592-107">This cmdlet does not deploy anything but updates an instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="1b592-108">Bir API yönetiminin dağıtımını güncelleştirmek için, değiştirilmiş **Psapsananagementınstance** 'ı Update-AzureRmApiManagementDeployment cmdlet 'ine kullanın.</span><span class="sxs-lookup"><span data-stu-id="1b592-108">To update a deployment of an API Management use the modified **PsApiManagementInstance** to the Update-AzureRmApiManagementDeployment cmdlet.</span></span>

## <span data-ttu-id="1b592-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1b592-109">EXAMPLES</span></span>

## <span data-ttu-id="1b592-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1b592-110">PARAMETERS</span></span>

### <span data-ttu-id="1b592-111">-Ucuz</span><span class="sxs-lookup"><span data-stu-id="1b592-111">-ApiManagement</span></span>
<span data-ttu-id="1b592-112">Var olan bir dağıtım bölgesini güncelleştirmek için **Psapimana,** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1b592-112">Specifies the **PsApiManagement** instance to update an existing deployment region in.</span></span>

```yaml
Type: PsApiManagement
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1b592-113">-Kapasite</span><span class="sxs-lookup"><span data-stu-id="1b592-113">-Capacity</span></span>
<span data-ttu-id="1b592-114">Dağıtım bölgesi için yeni SKU kapasite değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1b592-114">Specifies the new SKU capacity value for the deployment region.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b592-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b592-115">-DefaultProfile</span></span>
<span data-ttu-id="1b592-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1b592-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b592-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="1b592-117">-Location</span></span>
<span data-ttu-id="1b592-118">Güncelleştirilecek dağıtım bölgesinin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1b592-118">Specifies the location of the deployment region to update.</span></span>

<span data-ttu-id="1b592-119">API yönetim hizmeti için desteklenen bölge arasındaki yeni dağıtım bölgesinin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1b592-119">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="1b592-120">Geçerli konumlar almak için, "Microsoft. Apsananae" Get-AzureRmResourceProvider cmdlet 'ini kullanın. WHERE {$ _. ResourceTypes [0]. ResourceTypeName-EQ "hizmet"} | Select-Object konumları</span><span class="sxs-lookup"><span data-stu-id="1b592-120">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b592-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="1b592-121">-Sku</span></span>
<span data-ttu-id="1b592-122">Dağıtım bölgesi için yeni katman değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1b592-122">Specifies the new tier value for the deployment region.</span></span>

<span data-ttu-id="1b592-123">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="1b592-123">Valid values are:</span></span>

- <span data-ttu-id="1b592-124">İyle</span><span class="sxs-lookup"><span data-stu-id="1b592-124">Developer</span></span>
- <span data-ttu-id="1b592-125">Ardından</span><span class="sxs-lookup"><span data-stu-id="1b592-125">Standard</span></span>
- <span data-ttu-id="1b592-126">Min</span><span class="sxs-lookup"><span data-stu-id="1b592-126">Premium</span></span>

```yaml
Type: PsApiManagementSku
Parameter Sets: (All)
Aliases: 
Accepted values: Developer, Standard, Premium

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b592-127">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="1b592-127">-VirtualNetwork</span></span>
<span data-ttu-id="1b592-128">Dağıtım bölgesi için sanal ağ yapılandırmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1b592-128">Specifies a virtual network configuration for the deployment region.</span></span>
<span data-ttu-id="1b592-129">$Null geçirmek, bölgenin sanal ağ yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1b592-129">Passing $null will remove virtual network configuration for the region.</span></span>

```yaml
Type: PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b592-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b592-130">CommonParameters</span></span>
<span data-ttu-id="1b592-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1b592-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b592-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b592-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b592-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1b592-133">INPUTS</span></span>

### <span data-ttu-id="1b592-134">Bağış</span><span class="sxs-lookup"><span data-stu-id="1b592-134">PsApiManagement</span></span>
<span data-ttu-id="1b592-135">Parametre ' Apsananadeğeri ', ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="1b592-135">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="1b592-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1b592-136">OUTPUTS</span></span>

### <span data-ttu-id="1b592-137">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="1b592-137">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="1b592-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1b592-138">NOTES</span></span>

## <span data-ttu-id="1b592-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1b592-139">RELATED LINKS</span></span>

[<span data-ttu-id="1b592-140">Add-Azurermapımanagementregion</span><span class="sxs-lookup"><span data-stu-id="1b592-140">Add-AzureRmApiManagementRegion</span></span>](./Add-AzureRmApiManagementRegion.md)

[<span data-ttu-id="1b592-141">Remove-Azurermapımanagementregion</span><span class="sxs-lookup"><span data-stu-id="1b592-141">Remove-AzureRmApiManagementRegion</span></span>](./Remove-AzureRmApiManagementRegion.md)

[<span data-ttu-id="1b592-142">Güncelleştirme-Azurermapımanagementdeployment</span><span class="sxs-lookup"><span data-stu-id="1b592-142">Update-AzureRmApiManagementDeployment</span></span>](./Update-AzureRmApiManagementDeployment.md)