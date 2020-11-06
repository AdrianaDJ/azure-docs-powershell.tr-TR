---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2.md
ms.openlocfilehash: c50023cefbae9a9ba341eba22f40a421c37d12c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590330"
---
# <span data-ttu-id="ec642-101">Set-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ec642-101">Set-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="ec642-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec642-102">SYNOPSIS</span></span>
<span data-ttu-id="ec642-103">Veri fabrikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ec642-103">Creates a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec642-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ec642-104">SYNTAX</span></span>

```
Set-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ec642-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ec642-105">DESCRIPTION</span></span>
<span data-ttu-id="ec642-106">**Set-AzureRmDataFactoryV2** cmdlet 'i belirtilen kaynak grubu adı ve konumuyla bir veri fabrikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ec642-106">The **Set-AzureRmDataFactoryV2** cmdlet creates a data factory with the specified resource group name and location.</span></span>
<span data-ttu-id="ec642-107">Bu işlemleri aşağıdaki sırada gerçekleştirin:--Veri Fabrikası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ec642-107">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="ec642-108">--Bağlantılı hizmetler oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ec642-108">-- Create linked services.</span></span>
<span data-ttu-id="ec642-109">--Veri kümeleri oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ec642-109">-- Create datasets.</span></span>
<span data-ttu-id="ec642-110">--Ardışık düzen oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ec642-110">-- Create a pipeline.</span></span>

## <span data-ttu-id="ec642-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ec642-111">EXAMPLES</span></span>

### <span data-ttu-id="ec642-112">Örnek 1: Veri Fabrikası oluşturma</span><span class="sxs-lookup"><span data-stu-id="ec642-112">Example 1: Create a data factory</span></span>
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

<span data-ttu-id="ec642-113">Bu komut, WestUS konumunda ADF adlı kaynak grubunda WikiADF adlı bir veri fabrikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ec642-113">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="ec642-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ec642-114">PARAMETERS</span></span>

### <span data-ttu-id="ec642-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec642-115">-DefaultProfile</span></span>
<span data-ttu-id="ec642-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ec642-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec642-117">-Force</span><span class="sxs-lookup"><span data-stu-id="ec642-117">-Force</span></span>
<span data-ttu-id="ec642-118">Onay istemeden cmdlet 'i çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="ec642-118">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="ec642-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="ec642-119">-Location</span></span>
<span data-ttu-id="ec642-120">Veri Fabrikası bu bölgede oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="ec642-120">The data factory is created in this region.</span></span>

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

### <span data-ttu-id="ec642-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="ec642-121">-Name</span></span>
<span data-ttu-id="ec642-122">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="ec642-122">The data factory name.</span></span>

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

### <span data-ttu-id="ec642-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec642-123">-ResourceGroupName</span></span>
<span data-ttu-id="ec642-124">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="ec642-124">The resource group name.</span></span>

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

### <span data-ttu-id="ec642-125">Etiketli</span><span class="sxs-lookup"><span data-stu-id="ec642-125">-Tag</span></span>
<span data-ttu-id="ec642-126">Veri Fabrikası 'nin etiketleri.</span><span class="sxs-lookup"><span data-stu-id="ec642-126">The tags of the data factory.</span></span>

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

### <span data-ttu-id="ec642-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="ec642-127">-Confirm</span></span>
<span data-ttu-id="ec642-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ec642-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec642-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec642-129">-WhatIf</span></span>
<span data-ttu-id="ec642-130">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="ec642-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="ec642-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec642-131">CommonParameters</span></span>
<span data-ttu-id="ec642-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ec642-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec642-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec642-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec642-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ec642-134">INPUTS</span></span>

### <span data-ttu-id="ec642-135">System. String</span><span class="sxs-lookup"><span data-stu-id="ec642-135">System.String</span></span>

### <span data-ttu-id="ec642-136">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ec642-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ec642-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ec642-137">OUTPUTS</span></span>

### <span data-ttu-id="ec642-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="ec642-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="ec642-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ec642-139">NOTES</span></span>
<span data-ttu-id="ec642-140">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="ec642-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="ec642-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ec642-141">RELATED LINKS</span></span>

[<span data-ttu-id="ec642-142">Get-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ec642-142">Get-AzureRmDataFactoryV2</span></span>]()

[<span data-ttu-id="ec642-143">Remove-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ec642-143">Remove-AzureRmDataFactoryV2</span></span>]()
