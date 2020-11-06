---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2.md
ms.openlocfilehash: b5e5d42ba114da87daa3fa3effb15d3ad8bab22c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586901"
---
# <span data-ttu-id="a4bea-101">Set-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="a4bea-101">Set-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="a4bea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4bea-102">SYNOPSIS</span></span>
<span data-ttu-id="a4bea-103">Veri fabrikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a4bea-103">Creates a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4bea-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a4bea-104">SYNTAX</span></span>

```
Set-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a4bea-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a4bea-105">DESCRIPTION</span></span>
<span data-ttu-id="a4bea-106">**Set-AzureRmDataFactoryV2** cmdlet 'i belirtilen kaynak grubu adı ve konumuyla bir veri fabrikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a4bea-106">The **Set-AzureRmDataFactoryV2** cmdlet creates a data factory with the specified resource group name and location.</span></span>

<span data-ttu-id="a4bea-107">Bu işlemleri aşağıdaki sırada gerçekleştirin:</span><span class="sxs-lookup"><span data-stu-id="a4bea-107">Perform these operations in the following order:</span></span>

        -- Create a data factory.
        -- Create linked services.
        -- Create datasets.
        -- Create a pipeline.

## <span data-ttu-id="a4bea-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a4bea-108">EXAMPLES</span></span>

### <span data-ttu-id="a4bea-109">Örnek 1: Veri Fabrikası oluşturma</span><span class="sxs-lookup"><span data-stu-id="a4bea-109">Example 1: Create a data factory</span></span>
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

<span data-ttu-id="a4bea-110">Bu komut, WestUS konumunda ADF adlı kaynak grubunda WikiADF adlı bir veri fabrikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a4bea-110">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="a4bea-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a4bea-111">PARAMETERS</span></span>

### <span data-ttu-id="a4bea-112">-Onay</span><span class="sxs-lookup"><span data-stu-id="a4bea-112">-Confirm</span></span>
<span data-ttu-id="a4bea-113">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a4bea-113">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4bea-114">-Force</span><span class="sxs-lookup"><span data-stu-id="a4bea-114">-Force</span></span>
<span data-ttu-id="a4bea-115">Onay istemeden cmdlet 'i çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="a4bea-115">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="a4bea-116">-Konum</span><span class="sxs-lookup"><span data-stu-id="a4bea-116">-Location</span></span>
<span data-ttu-id="a4bea-117">Veri Fabrikası bu bölgede oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="a4bea-117">The data factory is created in this region.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4bea-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="a4bea-118">-Name</span></span>
<span data-ttu-id="a4bea-119">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="a4bea-119">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4bea-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4bea-120">-ResourceGroupName</span></span>
<span data-ttu-id="a4bea-121">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="a4bea-121">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4bea-122">Etiketli</span><span class="sxs-lookup"><span data-stu-id="a4bea-122">-Tag</span></span>
<span data-ttu-id="a4bea-123">Veri Fabrikası 'nin etiketleri.</span><span class="sxs-lookup"><span data-stu-id="a4bea-123">The tags of the data factory.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4bea-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4bea-124">-WhatIf</span></span>
<span data-ttu-id="a4bea-125">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="a4bea-125">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4bea-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4bea-126">-DefaultProfile</span></span>
<span data-ttu-id="a4bea-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a4bea-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4bea-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4bea-128">CommonParameters</span></span>
<span data-ttu-id="a4bea-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a4bea-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4bea-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4bea-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4bea-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a4bea-131">INPUTS</span></span>

### <span data-ttu-id="a4bea-132">System. String</span><span class="sxs-lookup"><span data-stu-id="a4bea-132">System.String</span></span>
<span data-ttu-id="a4bea-133">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a4bea-133">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a4bea-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a4bea-134">OUTPUTS</span></span>

### <span data-ttu-id="a4bea-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="a4bea-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="a4bea-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a4bea-136">NOTES</span></span>
<span data-ttu-id="a4bea-137">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="a4bea-137">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="a4bea-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a4bea-138">RELATED LINKS</span></span>

[<span data-ttu-id="a4bea-139">Get-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="a4bea-139">Get-AzureRmDataFactoryV2</span></span>]()

[<span data-ttu-id="a4bea-140">Remove-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="a4bea-140">Remove-AzureRmDataFactoryV2</span></span>]()
