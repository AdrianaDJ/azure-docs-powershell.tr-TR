---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 17D7EBD2-FE3F-4D24-A1AA-8C45B9B1FEF5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementRegion.md
ms.openlocfilehash: 8bacb26b4e30521ddd840d2a8081365ed9c4c6ad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587021"
---
# <span data-ttu-id="1f231-101">Remove-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="1f231-101">Remove-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="1f231-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f231-102">SYNOPSIS</span></span>
<span data-ttu-id="1f231-103">Psapsananaddeğerinden var olan bir dağıtım bölgesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1f231-103">Removes an existing deployment region from PsApiManagement instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f231-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1f231-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f231-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1f231-105">DESCRIPTION</span></span>
<span data-ttu-id="1f231-106">**Remove-Azurermapsananagementregion** cmdlet 'i, Microsoft. Azure. Commands. **Apsananad. model. psapsananad,** sağlanan bir **Additionalregion** koleksiyonundan **Microsoft. Azure. Commands**</span><span class="sxs-lookup"><span data-stu-id="1f231-106">The **Remove-AzureRmApiManagementRegion** cmdlet removes instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** from a collection of **AdditionalRegions** of provided the instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="1f231-107">Bu cmdlet, dağıtımı kendi başına değiştirmez ancak bellekteki **Psapımana**</span><span class="sxs-lookup"><span data-stu-id="1f231-107">This cmdlet does not modify deployment by itself but updates the instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="1f231-108">Bir API yönetiminin dağıtımını güncelleştirmek için, değiştirilmiş **Psapsananagementınstance** öğesini **güncelleştirmeye-Azurermapsananae** geçirin.</span><span class="sxs-lookup"><span data-stu-id="1f231-108">To update a deployment of an API Management, pass the modified **PsApiManagementInstance** to **Update-AzureRmApiManagement**.</span></span>

## <span data-ttu-id="1f231-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1f231-109">EXAMPLES</span></span>

### <span data-ttu-id="1f231-110">Örnek 1: psapsanana</span><span class="sxs-lookup"><span data-stu-id="1f231-110">Example 1: Remove a region from a PsApiManagement instance</span></span>
```
PS C:\>Remove-AzureRmApiManagementRegion -ApiManagement $ApiManagement -Location "East US"
```

<span data-ttu-id="1f231-111">Bu komut, **Psapsananadus** ÖRNEĞINDEKI Doğu US adındaki bölgeyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1f231-111">This command removes the region named East US from the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="1f231-112">Örnek 2: bir dizi komutu kullanarak psapsanana</span><span class="sxs-lookup"><span data-stu-id="1f231-112">Example 2: Remove a region from a PsApiManagement instance using a series of commands</span></span>
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name ContosoApi | Remove-AzureRmApiManagementRegion -Location "East US" | Update-AzureRmApiManagementDeployment
```

<span data-ttu-id="1f231-113">İlk komut, contoso adlı bir kaynak grubundan Contosoapı adlı kaynak grubundan bir **Psapsananadörneği** alır.</span><span class="sxs-lookup"><span data-stu-id="1f231-113">This first command gets an instance of **PsApiManagement** from the resource group named Contoso named ContosoApi.</span></span>
<span data-ttu-id="1f231-114">Son komutu daha sonra o örnekten Doğu ABD adlı bölgeyi kaldırır ve dağıtımı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="1f231-114">The final command then removes the region named East US from that instance then updates the deployment.</span></span>

## <span data-ttu-id="1f231-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1f231-115">PARAMETERS</span></span>

### <span data-ttu-id="1f231-116">-Ucuz</span><span class="sxs-lookup"><span data-stu-id="1f231-116">-ApiManagement</span></span>
<span data-ttu-id="1f231-117">Bu cmdlet 'in ek dağıtım bölgesini kaldırdığı **Psapimanadörneği** 'ni belirtir.</span><span class="sxs-lookup"><span data-stu-id="1f231-117">Specifies the **PsApiManagement** instance that this cmdlet removes the additional deployment region from.</span></span>

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

### <span data-ttu-id="1f231-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="1f231-118">-Location</span></span>
<span data-ttu-id="1f231-119">Bu cmdlet 'in kaldırıldığı bölgenin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1f231-119">Specifies the location of the region that this cmdlet removes.</span></span>

<span data-ttu-id="1f231-120">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="1f231-120">Valid values are:</span></span> 

- <span data-ttu-id="1f231-121">Kuzey Orta ABD</span><span class="sxs-lookup"><span data-stu-id="1f231-121">North Central US</span></span>
- <span data-ttu-id="1f231-122">Güney Orta ABD</span><span class="sxs-lookup"><span data-stu-id="1f231-122">South Central US</span></span>
- <span data-ttu-id="1f231-123">Orta ABD</span><span class="sxs-lookup"><span data-stu-id="1f231-123">Central US</span></span>
- <span data-ttu-id="1f231-124">Batı Avrupa</span><span class="sxs-lookup"><span data-stu-id="1f231-124">West Europe</span></span>
- <span data-ttu-id="1f231-125">Kuzey Avrupa</span><span class="sxs-lookup"><span data-stu-id="1f231-125">North Europe</span></span>
- <span data-ttu-id="1f231-126">Batı ABD</span><span class="sxs-lookup"><span data-stu-id="1f231-126">West US</span></span>
- <span data-ttu-id="1f231-127">Doğu ABD</span><span class="sxs-lookup"><span data-stu-id="1f231-127">East US</span></span>
- <span data-ttu-id="1f231-128">Doğu ABD 2</span><span class="sxs-lookup"><span data-stu-id="1f231-128">East US 2</span></span>
- <span data-ttu-id="1f231-129">Japon Doğu</span><span class="sxs-lookup"><span data-stu-id="1f231-129">Japan East</span></span>
- <span data-ttu-id="1f231-130">Japon Batı</span><span class="sxs-lookup"><span data-stu-id="1f231-130">Japan West</span></span>
- <span data-ttu-id="1f231-131">Brezilya Güney</span><span class="sxs-lookup"><span data-stu-id="1f231-131">Brazil South</span></span>
- <span data-ttu-id="1f231-132">Güneydoğu Asya</span><span class="sxs-lookup"><span data-stu-id="1f231-132">Southeast Asia</span></span>
- <span data-ttu-id="1f231-133">Doğu Asya</span><span class="sxs-lookup"><span data-stu-id="1f231-133">East Asia</span></span>
- <span data-ttu-id="1f231-134">Avustralya Doğu</span><span class="sxs-lookup"><span data-stu-id="1f231-134">Australia East</span></span>
- <span data-ttu-id="1f231-135">Avustralya Güneydoğu</span><span class="sxs-lookup"><span data-stu-id="1f231-135">Australia Southeast</span></span>

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

### <span data-ttu-id="1f231-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f231-136">-DefaultProfile</span></span>
<span data-ttu-id="1f231-137">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1f231-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f231-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f231-138">CommonParameters</span></span>
<span data-ttu-id="1f231-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1f231-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f231-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f231-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f231-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1f231-141">INPUTS</span></span>

### <span data-ttu-id="1f231-142">Bağış</span><span class="sxs-lookup"><span data-stu-id="1f231-142">PsApiManagement</span></span>
<span data-ttu-id="1f231-143">Parametre ' Apsananadeğeri ', ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="1f231-143">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="1f231-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1f231-144">OUTPUTS</span></span>

### <span data-ttu-id="1f231-145">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="1f231-145">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="1f231-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1f231-146">NOTES</span></span>

## <span data-ttu-id="1f231-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1f231-147">RELATED LINKS</span></span>

[<span data-ttu-id="1f231-148">Add-Azurermapımanagementregion</span><span class="sxs-lookup"><span data-stu-id="1f231-148">Add-AzureRmApiManagementRegion</span></span>](./Add-AzureRmApiManagementRegion.md)

[<span data-ttu-id="1f231-149">Güncelleştirme-azurermapsanana</span><span class="sxs-lookup"><span data-stu-id="1f231-149">Update-AzureRmApiManagementRegion</span></span>](./Update-AzureRmApiManagementRegion.md)


