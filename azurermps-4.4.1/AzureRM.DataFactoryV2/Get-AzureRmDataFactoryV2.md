---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2.md
gitcommit: https://github.com/Azure/azure-powershell/blob/7fe7039e96038b4a91513dfda26026ad8e0a352b
ms.openlocfilehash: 8742babd73e28e28797db75952d7eb9e9c8dc4a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591766"
---
# <span data-ttu-id="90111-101">Get-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="90111-101">Get-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="90111-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90111-102">SYNOPSIS</span></span>
<span data-ttu-id="90111-103">Veri Fabrikası hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="90111-103">Gets information about Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90111-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="90111-104">SYNTAX</span></span>

```
Get-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [[-Name] <String>]
```

## <span data-ttu-id="90111-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="90111-105">DESCRIPTION</span></span>
<span data-ttu-id="90111-106">Get-AzureRmDataFactoryV2 cmdlet 'i bir Azure Kaynak grubundaki veri fabrikası hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="90111-106">The Get-AzureRmDataFactoryV2 cmdlet gets information about data factories in an Azure resource group.</span></span>
<span data-ttu-id="90111-107">Veri Fabrikası adı belirtirseniz, bu cmdlet bu veri fabrikası hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="90111-107">If you specify the name of a data factory, this cmdlet gets information about that data factory.</span></span>
<span data-ttu-id="90111-108">Bir ad belirtmezseniz, bu cmdlet bir Azure Kaynak grubundaki tüm veri fabrikaları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="90111-108">If you do not specify a name, this cmdlet gets information about all of the data factories in an Azure resource group.</span></span>


## <span data-ttu-id="90111-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="90111-109">EXAMPLES</span></span>

### <span data-ttu-id="90111-110">Örnek 1: tüm veri fabrikaları</span><span class="sxs-lookup"><span data-stu-id="90111-110">Example 1: Get all data factories</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2 -ResourceGroupName "ADF"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded

    DataFactoryName   : WikiADF2
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf2
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          :
    ProvisioningState : Succeeded

```

<span data-ttu-id="90111-111">Azure aboneliğindeki tüm veri fabrikaları hakkında bilgi görüntüler.</span><span class="sxs-lookup"><span data-stu-id="90111-111">Displays information about all data factories in the Azure subscription.</span></span>

### <span data-ttu-id="90111-112">Örnek 2: belirli bir veri fabrikası edinin</span><span class="sxs-lookup"><span data-stu-id="90111-112">Example 2: Get a specific data factory</span></span>
```
PS C:\> $DataFactory = Get-AzureRmDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataF
                        actory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded

```

<span data-ttu-id="90111-113">Bu komut, ADF adlı kaynak grubu için aboneliğindeki WikiADF adlı veri fabrikası hakkında bilgi görüntüler ve $DataFactory değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="90111-113">This command displays information about the data factory named WikiADF in the subscription for the resource group named ADF, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="90111-114">$DataFactory 'da depolanan veri fabrikasını kullanmak için sonraki cmdlet lerde DataFactory parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="90111-114">Specify the DataFactory parameter in subsequent cmdlets to use the data factory stored in $DataFactory.</span></span>

## <span data-ttu-id="90111-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="90111-115">PARAMETERS</span></span>

### <span data-ttu-id="90111-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="90111-116">-Name</span></span>
<span data-ttu-id="90111-117">Bilgi alınacak veri fabrikasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="90111-117">Specifies the name of the data factory about which to get information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DataFactoryName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90111-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90111-118">-ResourceGroupName</span></span>
<span data-ttu-id="90111-119">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="90111-119">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="90111-120">Bu cmdlet, bu parametrenin belirttiği gruba ait veri fabrikası hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="90111-120">This cmdlet gets information about data factories that belong to the group this parameter specifies.</span></span>

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

## <span data-ttu-id="90111-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="90111-121">INPUTS</span></span>

### <span data-ttu-id="90111-122">System. String</span><span class="sxs-lookup"><span data-stu-id="90111-122">System.String</span></span>


## <span data-ttu-id="90111-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="90111-123">OUTPUTS</span></span>

### <span data-ttu-id="90111-124">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft.Azure.Commands.DataFactoryV2.Models.PSDAtafabrikası, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="90111-124">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="90111-125">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="90111-125">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>


## <span data-ttu-id="90111-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="90111-126">NOTES</span></span>
<span data-ttu-id="90111-127">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="90111-127">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="90111-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="90111-128">RELATED LINKS</span></span>
[<span data-ttu-id="90111-129">Set-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="90111-129">Set-AzureRmDataFactoryV2</span></span>]()

[<span data-ttu-id="90111-130">Remove-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="90111-130">Remove-AzureRmDataFactoryV2</span></span>]()
