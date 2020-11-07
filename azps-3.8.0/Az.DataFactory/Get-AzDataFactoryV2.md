---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2.md
ms.openlocfilehash: d52ddd20253e2d6969a19b92f7bd973584a7f630
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938381"
---
# <span data-ttu-id="666d2-101">Get-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="666d2-101">Get-AzDataFactoryV2</span></span>

## <span data-ttu-id="666d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="666d2-102">SYNOPSIS</span></span>
<span data-ttu-id="666d2-103">Veri Fabrikası hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="666d2-103">Gets information about Data Factory.</span></span>

## <span data-ttu-id="666d2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="666d2-104">SYNTAX</span></span>

### <span data-ttu-id="666d2-105">Bysubscriptionıd (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="666d2-105">BySubscriptionId (Default)</span></span>
```
Get-AzDataFactoryV2 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="666d2-106">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="666d2-106">ByFactoryName</span></span>
```
Get-AzDataFactoryV2 [-ResourceGroupName] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="666d2-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="666d2-107">DESCRIPTION</span></span>
<span data-ttu-id="666d2-108">Get-AzDataFactoryV2 cmdlet 'i bir Azure Kaynak grubundaki veri fabrikası hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="666d2-108">The Get-AzDataFactoryV2 cmdlet gets information about data factories in an Azure resource group.</span></span>
<span data-ttu-id="666d2-109">Veri Fabrikası adı belirtirseniz, bu cmdlet bu veri fabrikası hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="666d2-109">If you specify the name of a data factory, this cmdlet gets information about that data factory.</span></span>
<span data-ttu-id="666d2-110">Bir ad belirtmezseniz, bu cmdlet bir Azure Kaynak grubundaki tüm veri fabrikaları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="666d2-110">If you do not specify a name, this cmdlet gets information about all of the data factories in an Azure resource group.</span></span>

## <span data-ttu-id="666d2-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="666d2-111">EXAMPLES</span></span>

### <span data-ttu-id="666d2-112">Örnek 1: tüm veri fabrikaları</span><span class="sxs-lookup"><span data-stu-id="666d2-112">Example 1: Get all data factories</span></span>
```
PS C:\> Get-AzDataFactoryV2 -ResourceGroupName "ADF"

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

<span data-ttu-id="666d2-113">Azure aboneliğindeki tüm veri fabrikaları hakkında bilgi görüntüler.</span><span class="sxs-lookup"><span data-stu-id="666d2-113">Displays information about all data factories in the Azure subscription.</span></span>

### <span data-ttu-id="666d2-114">Örnek 2: belirli bir veri fabrikası edinin</span><span class="sxs-lookup"><span data-stu-id="666d2-114">Example 2: Get a specific data factory</span></span>
```
PS C:\> $DataFactory = Get-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataF
                        actory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded
```

<span data-ttu-id="666d2-115">Bu komut, ADF adlı kaynak grubu için aboneliğindeki WikiADF adlı veri fabrikası hakkında bilgi görüntüler ve $DataFactory değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="666d2-115">This command displays information about the data factory named WikiADF in the subscription for the resource group named ADF, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="666d2-116">$DataFactory 'da depolanan veri fabrikasını kullanmak için sonraki cmdlet lerde DataFactory parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="666d2-116">Specify the DataFactory parameter in subsequent cmdlets to use the data factory stored in $DataFactory.</span></span>

## <span data-ttu-id="666d2-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="666d2-117">PARAMETERS</span></span>

### <span data-ttu-id="666d2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="666d2-118">-DefaultProfile</span></span>
<span data-ttu-id="666d2-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="666d2-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="666d2-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="666d2-120">-Name</span></span>
<span data-ttu-id="666d2-121">Bilgi alınacak veri fabrikasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="666d2-121">Specifies the name of the data factory about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="666d2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="666d2-122">-ResourceGroupName</span></span>
<span data-ttu-id="666d2-123">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="666d2-123">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="666d2-124">Bu cmdlet, bu parametrenin belirttiği gruba ait veri fabrikası hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="666d2-124">This cmdlet gets information about data factories that belong to the group this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="666d2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="666d2-125">CommonParameters</span></span>
<span data-ttu-id="666d2-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="666d2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="666d2-127">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="666d2-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="666d2-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="666d2-128">INPUTS</span></span>

### <span data-ttu-id="666d2-129">System. String</span><span class="sxs-lookup"><span data-stu-id="666d2-129">System.String</span></span>

## <span data-ttu-id="666d2-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="666d2-130">OUTPUTS</span></span>

### <span data-ttu-id="666d2-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="666d2-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="666d2-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="666d2-132">NOTES</span></span>
<span data-ttu-id="666d2-133">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="666d2-133">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="666d2-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="666d2-134">RELATED LINKS</span></span>

[<span data-ttu-id="666d2-135">Set-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="666d2-135">Set-AzDataFactoryV2</span></span>]()

[<span data-ttu-id="666d2-136">Remove-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="666d2-136">Remove-AzDataFactoryV2</span></span>]()

