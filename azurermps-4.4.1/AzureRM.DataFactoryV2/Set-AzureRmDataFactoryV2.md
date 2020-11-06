---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 8dc191223d5ec17856605c7640d324cc2ee3794e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595190"
---
# <span data-ttu-id="4a9e1-101">Set-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="4a9e1-101">Set-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="4a9e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a9e1-102">SYNOPSIS</span></span>
<span data-ttu-id="4a9e1-103">Veri fabrikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4a9e1-103">Creates a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a9e1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4a9e1-104">SYNTAX</span></span>

```
Set-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
[[-Tag] <Hashtable>] [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="4a9e1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4a9e1-105">DESCRIPTION</span></span>
<span data-ttu-id="4a9e1-106">**Set-AzureRmDataFactoryV2** cmdlet 'i belirtilen kaynak grubu adı ve konumuyla bir veri fabrikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4a9e1-106">The **Set-AzureRmDataFactoryV2** cmdlet creates a data factory with the specified resource group name and location.</span></span>

<span data-ttu-id="4a9e1-107">Bu işlemleri aşağıdaki sırada gerçekleştirin:</span><span class="sxs-lookup"><span data-stu-id="4a9e1-107">Perform these operations in the following order:</span></span>

        -- Create a data factory.
        -- Create linked services.
        -- Create datasets.
        -- Create a pipeline.

## <span data-ttu-id="4a9e1-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4a9e1-108">EXAMPLES</span></span>

### <span data-ttu-id="4a9e1-109">Örnek 1: Veri Fabrikası oluşturma</span><span class="sxs-lookup"><span data-stu-id="4a9e1-109">Example 1: Create a data factory</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF" -Location "WestUS"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded

```

<span data-ttu-id="4a9e1-110">Bu komut, WestUS konumunda ADF adlı kaynak grubunda WikiADF adlı bir veri fabrikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4a9e1-110">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="4a9e1-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4a9e1-111">PARAMETERS</span></span>

### <span data-ttu-id="4a9e1-112">-Onay</span><span class="sxs-lookup"><span data-stu-id="4a9e1-112">-Confirm</span></span>
<span data-ttu-id="4a9e1-113">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4a9e1-113">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a9e1-114">-Force</span><span class="sxs-lookup"><span data-stu-id="4a9e1-114">-Force</span></span>
<span data-ttu-id="4a9e1-115">Onay istemeden cmdlet 'i çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="4a9e1-115">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a9e1-116">-Konum</span><span class="sxs-lookup"><span data-stu-id="4a9e1-116">-Location</span></span>
<span data-ttu-id="4a9e1-117">Veri Fabrikası bu bölgede oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="4a9e1-117">The data factory is created in this region.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a9e1-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="4a9e1-118">-Name</span></span>
<span data-ttu-id="4a9e1-119">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="4a9e1-119">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a9e1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a9e1-120">-ResourceGroupName</span></span>
<span data-ttu-id="4a9e1-121">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="4a9e1-121">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a9e1-122">Etiketli</span><span class="sxs-lookup"><span data-stu-id="4a9e1-122">-Tag</span></span>
<span data-ttu-id="4a9e1-123">Veri Fabrikası 'nin etiketleri.</span><span class="sxs-lookup"><span data-stu-id="4a9e1-123">The tags of the data factory.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a9e1-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a9e1-124">-WhatIf</span></span>
<span data-ttu-id="4a9e1-125">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="4a9e1-125">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="4a9e1-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4a9e1-126">INPUTS</span></span>

### <span data-ttu-id="4a9e1-127">System. String</span><span class="sxs-lookup"><span data-stu-id="4a9e1-127">System.String</span></span>
<span data-ttu-id="4a9e1-128">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="4a9e1-128">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4a9e1-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4a9e1-129">OUTPUTS</span></span>

### <span data-ttu-id="4a9e1-130">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="4a9e1-130">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="4a9e1-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4a9e1-131">NOTES</span></span>
<span data-ttu-id="4a9e1-132">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="4a9e1-132">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="4a9e1-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4a9e1-133">RELATED LINKS</span></span>
[<span data-ttu-id="4a9e1-134">Get-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="4a9e1-134">Get-AzureRmDataFactoryV2</span></span>]()

[<span data-ttu-id="4a9e1-135">Remove-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="4a9e1-135">Remove-AzureRmDataFactoryV2</span></span>]()
