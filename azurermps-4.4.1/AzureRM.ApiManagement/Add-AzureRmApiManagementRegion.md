---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 9D4A68A8-0A39-4C9A-8EA6-391A5E7A0E25
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementRegion.md
ms.openlocfilehash: 7edf16a6970f831235f76c64ef5cb5181a49bf98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593860"
---
# <span data-ttu-id="2e844-101">Add-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="2e844-101">Add-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="2e844-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e844-102">SYNOPSIS</span></span>
<span data-ttu-id="2e844-103">Psapsananamı örneğine yeni dağıtım bölgeleri ekler.</span><span class="sxs-lookup"><span data-stu-id="2e844-103">Adds new deployment regions to a PsApiManagement instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e844-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2e844-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> [-Sku <PsApiManagementSku>]
 [-Capacity <Int32>] [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e844-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2e844-105">DESCRIPTION</span></span>
<span data-ttu-id="2e844-106">**Add-Azurermapsananagementregion** cmdlet 'ı, **psapsananagementregion** türünde sağlanan **Microsoft. Azure. Commands. Apsananad. model** **AdditionalRegions**</span><span class="sxs-lookup"><span data-stu-id="2e844-106">The **Add-AzureRmApiManagementRegion** cmdlet adds new instance of type **PsApiManagementRegion** to the collection of **AdditionalRegions** of provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="2e844-107">Bu cmdlet kendisiyle hiçbir şey dağıtmaz ancak bellekteki **Psapımana**</span><span class="sxs-lookup"><span data-stu-id="2e844-107">This cmdlet does not deploy anything by itself but updates instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="2e844-108">API yönetiminin dağıtımını güncelleştirmek için, değiştirilmiş **Psapımanadınstance** öğesini Update-Azurermapsananagementdeployment öğesine geçirin.</span><span class="sxs-lookup"><span data-stu-id="2e844-108">To update a deployment of an API Management pass the modified **PsApiManagement** Instance to Update-AzureRmApiManagementDeployment.</span></span>

## <span data-ttu-id="2e844-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2e844-109">EXAMPLES</span></span>

### <span data-ttu-id="2e844-110">Örnek 1: bir Psapsanana, bir örneğine yeni dağıtım bölgeleri ekleme</span><span class="sxs-lookup"><span data-stu-id="2e844-110">Example 1: Add new deployment regions to a PsApiManagement instance</span></span>
```
PS C:\>Add-AzureRmApiManagementRegion -ApiManagement $ApiManagement -Location "East US" -Sku "Premium" -Capacity 2
```

<span data-ttu-id="2e844-111">Bu komut iki Premium SKU birimi ve Doğu ABD adlı bölgeyi **Psapımanadıman**</span><span class="sxs-lookup"><span data-stu-id="2e844-111">This command adds two premium SKU units and the region named East US to the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="2e844-112">Örnek 2: psapsananadın</span><span class="sxs-lookup"><span data-stu-id="2e844-112">Example 2: Add new deployment regions to a PsApiManagement instance and then update deployment</span></span>
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi" | Add-AzureRmApiManagementRegion -Location "East US" -Sku "Premium" -Capacity 2 | Update-AzureRmApiManagementDeployment
```

<span data-ttu-id="2e844-113">Bu komut, **Psapsanananabir** nesne alır, Doğu ABD adlı bölge için ıkı Premium SKU birimi ekler ve ardından dağıtımı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="2e844-113">This command gets a **PsApiManagement** object, adds two premium SKU units for the region named East US, and then updates deployment.</span></span>

## <span data-ttu-id="2e844-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2e844-114">PARAMETERS</span></span>

### <span data-ttu-id="2e844-115">-Ucuz</span><span class="sxs-lookup"><span data-stu-id="2e844-115">-ApiManagement</span></span>
<span data-ttu-id="2e844-116">Bu cmdlet 'in ek dağıtım bölgelerini eklediği **Psapimana,** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2e844-116">Specifies the **PsApiManagement** instance that this cmdlet adds additional deployment regions to.</span></span>

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

### <span data-ttu-id="2e844-117">-Kapasite</span><span class="sxs-lookup"><span data-stu-id="2e844-117">-Capacity</span></span>
<span data-ttu-id="2e844-118">Dağıtım bölgesinin SKU kapasitesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2e844-118">Specifies the SKU capacity of the deployment region.</span></span>

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

### <span data-ttu-id="2e844-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="2e844-119">-Location</span></span>
<span data-ttu-id="2e844-120">Yeni dağıtım bölgesinin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="2e844-120">Specifies the location of the new deployment region.</span></span>

<span data-ttu-id="2e844-121">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="2e844-121">Valid values are:</span></span> 

- <span data-ttu-id="2e844-122">Kuzey Orta ABD</span><span class="sxs-lookup"><span data-stu-id="2e844-122">North Central US</span></span>
- <span data-ttu-id="2e844-123">Güney Orta ABD</span><span class="sxs-lookup"><span data-stu-id="2e844-123">South Central US</span></span>
- <span data-ttu-id="2e844-124">Orta ABD</span><span class="sxs-lookup"><span data-stu-id="2e844-124">Central US</span></span>
- <span data-ttu-id="2e844-125">Batı Avrupa</span><span class="sxs-lookup"><span data-stu-id="2e844-125">West Europe</span></span>
- <span data-ttu-id="2e844-126">Kuzey Avrupa</span><span class="sxs-lookup"><span data-stu-id="2e844-126">North Europe</span></span>
- <span data-ttu-id="2e844-127">Batı ABD</span><span class="sxs-lookup"><span data-stu-id="2e844-127">West US</span></span>
- <span data-ttu-id="2e844-128">Doğu ABD</span><span class="sxs-lookup"><span data-stu-id="2e844-128">East US</span></span>
- <span data-ttu-id="2e844-129">Doğu ABD 2</span><span class="sxs-lookup"><span data-stu-id="2e844-129">East US 2</span></span>
- <span data-ttu-id="2e844-130">Japon Doğu</span><span class="sxs-lookup"><span data-stu-id="2e844-130">Japan East</span></span>
- <span data-ttu-id="2e844-131">Japon Batı</span><span class="sxs-lookup"><span data-stu-id="2e844-131">Japan West</span></span>
- <span data-ttu-id="2e844-132">Brezilya Güney</span><span class="sxs-lookup"><span data-stu-id="2e844-132">Brazil South</span></span>
- <span data-ttu-id="2e844-133">Güneydoğu Asya</span><span class="sxs-lookup"><span data-stu-id="2e844-133">Southeast Asia</span></span>
- <span data-ttu-id="2e844-134">Doğu Asya</span><span class="sxs-lookup"><span data-stu-id="2e844-134">East Asia</span></span>
- <span data-ttu-id="2e844-135">Avustralya Doğu</span><span class="sxs-lookup"><span data-stu-id="2e844-135">Australia East</span></span>
- <span data-ttu-id="2e844-136">Avustralya Güneydoğu</span><span class="sxs-lookup"><span data-stu-id="2e844-136">Australia Southeast</span></span>

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

### <span data-ttu-id="2e844-137">-SKU</span><span class="sxs-lookup"><span data-stu-id="2e844-137">-Sku</span></span>
<span data-ttu-id="2e844-138">Dağıtım bölgesinin katmanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2e844-138">Specifies the tier of the deployment region.</span></span>
<span data-ttu-id="2e844-139">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="2e844-139">Valid values are:</span></span> 

- <span data-ttu-id="2e844-140">İyle</span><span class="sxs-lookup"><span data-stu-id="2e844-140">Developer</span></span>
- <span data-ttu-id="2e844-141">Ardından</span><span class="sxs-lookup"><span data-stu-id="2e844-141">Standard</span></span>
- <span data-ttu-id="2e844-142">Min</span><span class="sxs-lookup"><span data-stu-id="2e844-142">Premium</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases: 
Accepted values: Developer, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e844-143">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2e844-143">-VirtualNetwork</span></span>
<span data-ttu-id="2e844-144">Sanal ağ yapılandırmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2e844-144">Specifies a virtual network configuration.</span></span>

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

### <span data-ttu-id="2e844-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e844-145">-DefaultProfile</span></span>
<span data-ttu-id="2e844-146">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2e844-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e844-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e844-147">CommonParameters</span></span>
<span data-ttu-id="2e844-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2e844-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e844-149">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e844-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e844-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2e844-150">INPUTS</span></span>

### <span data-ttu-id="2e844-151">Bağış</span><span class="sxs-lookup"><span data-stu-id="2e844-151">PsApiManagement</span></span>
<span data-ttu-id="2e844-152">Parametre ' Apsananadeğeri ', ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="2e844-152">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="2e844-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2e844-153">OUTPUTS</span></span>

### <span data-ttu-id="2e844-154">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="2e844-154">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="2e844-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2e844-155">NOTES</span></span>
* <span data-ttu-id="2e844-156">Cmdlet, güncelleştirilmiş **Psapsananadörneği** ardışık düzene yazar.</span><span class="sxs-lookup"><span data-stu-id="2e844-156">The cmdlet writes updated **PsApiManagement** instance to pipeline.</span></span>

## <span data-ttu-id="2e844-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2e844-157">RELATED LINKS</span></span>

[<span data-ttu-id="2e844-158">Remove-Azurermapımanagementregion</span><span class="sxs-lookup"><span data-stu-id="2e844-158">Remove-AzureRmApiManagementRegion</span></span>](./Remove-AzureRmApiManagementRegion.md)

[<span data-ttu-id="2e844-159">Güncelleştirme-azurermapsanana</span><span class="sxs-lookup"><span data-stu-id="2e844-159">Update-AzureRmApiManagementRegion</span></span>](./Update-AzureRmApiManagementRegion.md)

[<span data-ttu-id="2e844-160">Güncelleştirme-Azurermapımanagementdeployment</span><span class="sxs-lookup"><span data-stu-id="2e844-160">Update-AzureRmApiManagementDeployment</span></span>](./Update-AzureRmApiManagementDeployment.md)

