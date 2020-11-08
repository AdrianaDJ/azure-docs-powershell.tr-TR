---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 17D7EBD2-FE3F-4D24-A1AA-8C45B9B1FEF5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementRegion.md
ms.openlocfilehash: 70816b054acc7667d2246ea72901c65890f9389e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266142"
---
# <span data-ttu-id="7bda9-101">Remove-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="7bda9-101">Remove-AzApiManagementRegion</span></span>

## <span data-ttu-id="7bda9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7bda9-102">SYNOPSIS</span></span>
<span data-ttu-id="7bda9-103">Psapsananaddeğerinden var olan bir dağıtım bölgesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7bda9-103">Removes an existing deployment region from PsApiManagement instance.</span></span>

## <span data-ttu-id="7bda9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7bda9-104">SYNTAX</span></span>

```
Remove-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7bda9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7bda9-105">DESCRIPTION</span></span>
<span data-ttu-id="7bda9-106">**Remove-Azapsananagementregion** cmdlet 'i, sağlanan bir **additionalregion** koleksiyonundan Microsoft. Azure. Commands. Apsananad. model. **Psapsananagementregion** , Microsoft **. Azure. Commands**</span><span class="sxs-lookup"><span data-stu-id="7bda9-106">The **Remove-AzApiManagementRegion** cmdlet removes instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** from a collection of **AdditionalRegions** of provided the instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="7bda9-107">Bu cmdlet, dağıtımı kendi başına değiştirmez ancak bellekteki **Psapımana**</span><span class="sxs-lookup"><span data-stu-id="7bda9-107">This cmdlet does not modify deployment by itself but updates the instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="7bda9-108">Bir API yönetiminin dağıtımını güncelleştirmek için, değiştirilmiş **Psapsananagementınstance** 'ı **set-azapsananae** olarak geçirin.</span><span class="sxs-lookup"><span data-stu-id="7bda9-108">To update a deployment of an API Management, pass the modified **PsApiManagementInstance** to **Set-AzApiManagement**.</span></span>

## <span data-ttu-id="7bda9-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7bda9-109">EXAMPLES</span></span>

### <span data-ttu-id="7bda9-110">Örnek 1: psapsanana</span><span class="sxs-lookup"><span data-stu-id="7bda9-110">Example 1: Remove a region from a PsApiManagement instance</span></span>
```
PS C:\>Remove-AzApiManagementRegion -ApiManagement $ApiManagement -Location "East US"
```

<span data-ttu-id="7bda9-111">Bu komut, **Psapsananadus** ÖRNEĞINDEKI Doğu US adındaki bölgeyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7bda9-111">This command removes the region named East US from the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="7bda9-112">Örnek 2: bir dizi komutu kullanarak psapsanana</span><span class="sxs-lookup"><span data-stu-id="7bda9-112">Example 2: Remove a region from a PsApiManagement instance using a series of commands</span></span>
```
PS C:\>Get-AzApiManagement -ResourceGroupName "Contoso" -Name ContosoApi | Remove-AzApiManagementRegion -Location "East US" | Set-AzApiManagement
```

<span data-ttu-id="7bda9-113">İlk komut, contoso adlı bir kaynak grubundan Contosoapı adlı kaynak grubundan bir **Psapsananadörneği** alır.</span><span class="sxs-lookup"><span data-stu-id="7bda9-113">This first command gets an instance of **PsApiManagement** from the resource group named Contoso named ContosoApi.</span></span>
<span data-ttu-id="7bda9-114">Son komutu daha sonra o örnekten Doğu ABD adlı bölgeyi kaldırır ve dağıtımı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="7bda9-114">The final command then removes the region named East US from that instance then updates the deployment.</span></span>

## <span data-ttu-id="7bda9-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7bda9-115">PARAMETERS</span></span>

### <span data-ttu-id="7bda9-116">-Ucuz</span><span class="sxs-lookup"><span data-stu-id="7bda9-116">-ApiManagement</span></span>
<span data-ttu-id="7bda9-117">Bu cmdlet 'in ek dağıtım bölgesini kaldırdığı **Psapimanadörneği** 'ni belirtir.</span><span class="sxs-lookup"><span data-stu-id="7bda9-117">Specifies the **PsApiManagement** instance that this cmdlet removes the additional deployment region from.</span></span>

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

### <span data-ttu-id="7bda9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bda9-118">-DefaultProfile</span></span>

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

### <span data-ttu-id="7bda9-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="7bda9-119">-Location</span></span>
<span data-ttu-id="7bda9-120">Bu cmdlet 'in kaldırıldığı bölgenin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="7bda9-120">Specifies the location of the region that this cmdlet removes.</span></span>
<span data-ttu-id="7bda9-121">API yönetim hizmeti için desteklenen bölge arasındaki yeni dağıtım bölgesinin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="7bda9-121">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="7bda9-122">Geçerli konumlar almak için, "Microsoft. Apsananae" Get-AzResourceProvider cmdlet 'ini kullanın. WHERE {$ _. ResourceTypes [0]. ResourceTypeName-EQ "hizmet"} | Select-Object konumları</span><span class="sxs-lookup"><span data-stu-id="7bda9-122">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="7bda9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bda9-123">CommonParameters</span></span>
<span data-ttu-id="7bda9-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7bda9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bda9-125">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7bda9-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bda9-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7bda9-126">INPUTS</span></span>

### <span data-ttu-id="7bda9-127">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="7bda9-127">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

### <span data-ttu-id="7bda9-128">System. String</span><span class="sxs-lookup"><span data-stu-id="7bda9-128">System.String</span></span>

## <span data-ttu-id="7bda9-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7bda9-129">OUTPUTS</span></span>

### <span data-ttu-id="7bda9-130">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="7bda9-130">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="7bda9-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7bda9-131">NOTES</span></span>

## <span data-ttu-id="7bda9-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7bda9-132">RELATED LINKS</span></span>

[<span data-ttu-id="7bda9-133">Add-Azapsananagementregion</span><span class="sxs-lookup"><span data-stu-id="7bda9-133">Add-AzApiManagementRegion</span></span>](./Add-AzApiManagementRegion.md)

[<span data-ttu-id="7bda9-134">Güncelleştirme-Azapsananagementregion</span><span class="sxs-lookup"><span data-stu-id="7bda9-134">Update-AzApiManagementRegion</span></span>](./Update-AzApiManagementRegion.md)


