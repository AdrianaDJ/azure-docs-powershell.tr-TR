---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: b4af5eae61e47d8617eb270451f406f349162f50
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938376"
---
# <span data-ttu-id="407f7-101">Get-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="407f7-101">Get-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="407f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="407f7-102">SYNOPSIS</span></span>
<span data-ttu-id="407f7-103">Veri Fabrikası içindeki veri akışları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="407f7-103">Gets information about data flows in Data Factory.</span></span>

## <span data-ttu-id="407f7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="407f7-104">SYNTAX</span></span>

### <span data-ttu-id="407f7-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="407f7-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2DataFlow [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="407f7-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="407f7-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2DataFlow [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="407f7-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="407f7-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2DataFlow [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="407f7-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="407f7-108">DESCRIPTION</span></span>
<span data-ttu-id="407f7-109">Get-AzDataFactoryV2DataFlow cmdlet 'i Azure Veri Fabrikası 'ndaki veri akışları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="407f7-109">The Get-AzDataFactoryV2DataFlow cmdlet gets information about data flows in Azure Data Factory.</span></span>
<span data-ttu-id="407f7-110">Veri akışının adını belirtirseniz, bu cmdlet bu veri akışı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="407f7-110">If you specify the name of a data flow, this cmdlet gets information about that data flow.</span></span>
<span data-ttu-id="407f7-111">Bir ad belirtmezseniz, bu cmdlet Veri Fabrikası içindeki tüm veri akışları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="407f7-111">If you do not specify a name, this cmdlet gets information about all the data flows in the data factory.</span></span>

## <span data-ttu-id="407f7-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="407f7-112">EXAMPLES</span></span>
### <span data-ttu-id="407f7-113">Örnek 1: tüm veri akışları hakkında bilgi alın</span><span class="sxs-lookup"><span data-stu-id="407f7-113">Example 1: Get information about all data flows</span></span>
```powershell
PS C:\> Get-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
dataflow1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
dataflow3                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="407f7-114">Bu komut, WikiADF adlı veri fabrikası 'ndaki tüm veri akışları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="407f7-114">This command gets information about all data flows in the data factory named WikiADF.</span></span>

### <span data-ttu-id="407f7-115">Örnek 2: belirli bir veri akışı hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="407f7-115">Example 2: Get information about a specific data flow</span></span>
```powershell
PS C:\> Get-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "dataflow1"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="407f7-116">Bu komut WikiADF adındaki dataflow1 adlı veri akışı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="407f7-116">This command gets information about the data flow named dataflow1 in the data factory named WikiADF.</span></span>

## <span data-ttu-id="407f7-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="407f7-117">PARAMETERS</span></span>

### <span data-ttu-id="407f7-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="407f7-118">-DataFactory</span></span>
<span data-ttu-id="407f7-119">Veri fabrikası nesnesi.</span><span class="sxs-lookup"><span data-stu-id="407f7-119">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="407f7-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="407f7-120">-DataFactoryName</span></span>
<span data-ttu-id="407f7-121">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="407f7-121">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="407f7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="407f7-122">-DefaultProfile</span></span>
<span data-ttu-id="407f7-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="407f7-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="407f7-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="407f7-124">-Name</span></span>
<span data-ttu-id="407f7-125">Veri akışı adı.</span><span class="sxs-lookup"><span data-stu-id="407f7-125">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: DataFlowName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="407f7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="407f7-126">-ResourceGroupName</span></span>
<span data-ttu-id="407f7-127">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="407f7-127">The resource group name.</span></span>

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

### <span data-ttu-id="407f7-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="407f7-128">-ResourceId</span></span>
<span data-ttu-id="407f7-129">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="407f7-129">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="407f7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="407f7-130">CommonParameters</span></span>
<span data-ttu-id="407f7-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="407f7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="407f7-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="407f7-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="407f7-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="407f7-133">INPUTS</span></span>

### <span data-ttu-id="407f7-134">System. String</span><span class="sxs-lookup"><span data-stu-id="407f7-134">System.String</span></span>

### <span data-ttu-id="407f7-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="407f7-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="407f7-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="407f7-136">OUTPUTS</span></span>

### <span data-ttu-id="407f7-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDAtaakışı</span><span class="sxs-lookup"><span data-stu-id="407f7-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span></span>

## <span data-ttu-id="407f7-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="407f7-138">NOTES</span></span>
<span data-ttu-id="407f7-139">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="407f7-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="407f7-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="407f7-140">RELATED LINKS</span></span>

[<span data-ttu-id="407f7-141">Set-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="407f7-141">Set-AzDataFactoryDataFlow</span></span>](./Set-AzDataFactoryDataFlow.md)

[<span data-ttu-id="407f7-142">Remove-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="407f7-142">Remove-AzDataFactoryDataFlow</span></span>](./Remove-AzDataFactoryDataFlow.md)