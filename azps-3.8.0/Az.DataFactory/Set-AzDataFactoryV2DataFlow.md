---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: 42d9de3f23f1aca904aa0f42722217d0b9bf8a3a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938305"
---
# <span data-ttu-id="a8e77-101">Set-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="a8e77-101">Set-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="a8e77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8e77-102">SYNOPSIS</span></span>
<span data-ttu-id="a8e77-103">Veri Fabrikası içinde veri akışı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a8e77-103">Creates a data flow in Data Factory.</span></span>

## <span data-ttu-id="a8e77-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a8e77-104">SYNTAX</span></span>

### <span data-ttu-id="a8e77-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a8e77-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2DataFlow [-Name] <String> [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a8e77-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="a8e77-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2DataFlow [-DefinitionFile] <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8e77-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a8e77-107">DESCRIPTION</span></span>
<span data-ttu-id="a8e77-108">Set-AzDataFactoryV2DataFlow cmdlet 'i bir veri akışı oluşturur veya Azure Veri Fabrikası 'nda varolan bir veri akışını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="a8e77-108">The Set-AzDataFactoryV2DataFlow cmdlet creates a data flow or updates an existing data flow in Azure Data Factory.</span></span>

## <span data-ttu-id="a8e77-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a8e77-109">EXAMPLES</span></span>

### <span data-ttu-id="a8e77-110">Örnek 1: veri akışı oluşturma</span><span class="sxs-lookup"><span data-stu-id="a8e77-110">Example 1: Create a data flow</span></span>
```powershell
PS C:\> Set-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "TaxiDemo1" -DefinitionFile "C:\\samples\\WikiSample\\TaxiDemo1.json"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="a8e77-111">Bu komut WikiADF adındaki TaxiDemo1 adlı bir veri akışı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a8e77-111">This command creates a data flow named TaxiDemo1 in the data factory named WikiADF.</span></span>
<span data-ttu-id="a8e77-112">Komut, veri akışını TaxiDemo1.jsdosyadaki bilgilerde temel alır.</span><span class="sxs-lookup"><span data-stu-id="a8e77-112">The command bases the data flow on information in the TaxiDemo1.json file.</span></span>

## <span data-ttu-id="a8e77-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a8e77-113">PARAMETERS</span></span>

### <span data-ttu-id="a8e77-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="a8e77-114">-DataFactoryName</span></span>
<span data-ttu-id="a8e77-115">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="a8e77-115">The data factory name.</span></span>

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

### <span data-ttu-id="a8e77-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8e77-116">-DefaultProfile</span></span>
<span data-ttu-id="a8e77-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a8e77-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8e77-118">-Definitionfıle</span><span class="sxs-lookup"><span data-stu-id="a8e77-118">-DefinitionFile</span></span>
<span data-ttu-id="a8e77-119">JSON dosyası yolu.</span><span class="sxs-lookup"><span data-stu-id="a8e77-119">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8e77-120">-Force</span><span class="sxs-lookup"><span data-stu-id="a8e77-120">-Force</span></span>
<span data-ttu-id="a8e77-121">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="a8e77-121">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="a8e77-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="a8e77-122">-Name</span></span>
<span data-ttu-id="a8e77-123">Veri akışı adı.</span><span class="sxs-lookup"><span data-stu-id="a8e77-123">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFlowName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8e77-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8e77-124">-ResourceGroupName</span></span>
<span data-ttu-id="a8e77-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="a8e77-125">The resource group name.</span></span>

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

### <span data-ttu-id="a8e77-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a8e77-126">-ResourceId</span></span>
<span data-ttu-id="a8e77-127">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="a8e77-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="a8e77-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="a8e77-128">-Confirm</span></span>
<span data-ttu-id="a8e77-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a8e77-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8e77-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8e77-130">-WhatIf</span></span>
<span data-ttu-id="a8e77-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a8e77-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8e77-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a8e77-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8e77-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8e77-133">CommonParameters</span></span>
<span data-ttu-id="a8e77-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a8e77-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8e77-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a8e77-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8e77-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a8e77-136">INPUTS</span></span>

### <span data-ttu-id="a8e77-137">System. String</span><span class="sxs-lookup"><span data-stu-id="a8e77-137">System.String</span></span>

## <span data-ttu-id="a8e77-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a8e77-138">OUTPUTS</span></span>

### <span data-ttu-id="a8e77-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDAtaakışı</span><span class="sxs-lookup"><span data-stu-id="a8e77-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span></span>

## <span data-ttu-id="a8e77-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a8e77-140">NOTES</span></span>
<span data-ttu-id="a8e77-141">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="a8e77-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="a8e77-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a8e77-142">RELATED LINKS</span></span>

[<span data-ttu-id="a8e77-143">Get-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="a8e77-143">Get-AzDataFactoryDataFlow</span></span>](./Get-AzDataFactoryDataFlow.md)

[<span data-ttu-id="a8e77-144">Remove-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="a8e77-144">Remove-AzDataFactoryDataFlow</span></span>](./Remove-AzDataFactoryDataFlow.md)
