---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2dataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2DataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2DataFlow.md
ms.openlocfilehash: a563d6b0e72c60632d99df2668552b649ffb1662
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752448"
---
# <span data-ttu-id="b16a4-101">Set-AzDataFactoryV2DataFlow</span><span class="sxs-lookup"><span data-stu-id="b16a4-101">Set-AzDataFactoryV2DataFlow</span></span>

## <span data-ttu-id="b16a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b16a4-102">SYNOPSIS</span></span>
<span data-ttu-id="b16a4-103">Veri Fabrikası içinde veri akışı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b16a4-103">Creates a data flow in Data Factory.</span></span>

## <span data-ttu-id="b16a4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b16a4-104">SYNTAX</span></span>

### <span data-ttu-id="b16a4-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b16a4-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2DataFlow [-Name] <String> [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b16a4-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="b16a4-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2DataFlow [-DefinitionFile] <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b16a4-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b16a4-107">DESCRIPTION</span></span>
<span data-ttu-id="b16a4-108">Set-AzDataFactoryV2DataFlow cmdlet 'i bir veri akışı oluşturur veya Azure Veri Fabrikası 'nda varolan bir veri akışını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="b16a4-108">The Set-AzDataFactoryV2DataFlow cmdlet creates a data flow or updates an existing data flow in Azure Data Factory.</span></span>

## <span data-ttu-id="b16a4-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b16a4-109">EXAMPLES</span></span>

### <span data-ttu-id="b16a4-110">Örnek 1: veri akışı oluşturma</span><span class="sxs-lookup"><span data-stu-id="b16a4-110">Example 1: Create a data flow</span></span>
```powershell
PS C:\> Set-AzDataFactoryV2DataFlow -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "TaxiDemo1" -DefinitionFile "C:\\samples\\WikiSample\\TaxiDemo1.json"

DataFlowName           DataFactoryName ResourceGroupName                                                    Properties
------------           --------------- -----------------                                                    ----------
TaxiDemo1                      WikiADF               adf Microsoft.Azure.Management.DataFactory.Models.MappingDataFlow
```

<span data-ttu-id="b16a4-111">Bu komut WikiADF adındaki TaxiDemo1 adlı bir veri akışı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b16a4-111">This command creates a data flow named TaxiDemo1 in the data factory named WikiADF.</span></span>
<span data-ttu-id="b16a4-112">Komut, veri akışını TaxiDemo1.jsdosyadaki bilgilerde temel alır.</span><span class="sxs-lookup"><span data-stu-id="b16a4-112">The command bases the data flow on information in the TaxiDemo1.json file.</span></span>

## <span data-ttu-id="b16a4-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b16a4-113">PARAMETERS</span></span>

### <span data-ttu-id="b16a4-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="b16a4-114">-DataFactoryName</span></span>
<span data-ttu-id="b16a4-115">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="b16a4-115">The data factory name.</span></span>

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

### <span data-ttu-id="b16a4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b16a4-116">-DefaultProfile</span></span>
<span data-ttu-id="b16a4-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b16a4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b16a4-118">-Definitionfıle</span><span class="sxs-lookup"><span data-stu-id="b16a4-118">-DefinitionFile</span></span>
<span data-ttu-id="b16a4-119">JSON dosyası yolu.</span><span class="sxs-lookup"><span data-stu-id="b16a4-119">The JSON file path.</span></span>

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

### <span data-ttu-id="b16a4-120">-Force</span><span class="sxs-lookup"><span data-stu-id="b16a4-120">-Force</span></span>
<span data-ttu-id="b16a4-121">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="b16a4-121">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="b16a4-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="b16a4-122">-Name</span></span>
<span data-ttu-id="b16a4-123">Veri akışı adı.</span><span class="sxs-lookup"><span data-stu-id="b16a4-123">The data flow name.</span></span>

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

### <span data-ttu-id="b16a4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b16a4-124">-ResourceGroupName</span></span>
<span data-ttu-id="b16a4-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="b16a4-125">The resource group name.</span></span>

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

### <span data-ttu-id="b16a4-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b16a4-126">-ResourceId</span></span>
<span data-ttu-id="b16a4-127">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="b16a4-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="b16a4-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="b16a4-128">-Confirm</span></span>
<span data-ttu-id="b16a4-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b16a4-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b16a4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b16a4-130">-WhatIf</span></span>
<span data-ttu-id="b16a4-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b16a4-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b16a4-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b16a4-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b16a4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b16a4-133">CommonParameters</span></span>
<span data-ttu-id="b16a4-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b16a4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b16a4-135">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b16a4-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b16a4-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b16a4-136">INPUTS</span></span>

### <span data-ttu-id="b16a4-137">System. String</span><span class="sxs-lookup"><span data-stu-id="b16a4-137">System.String</span></span>

## <span data-ttu-id="b16a4-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b16a4-138">OUTPUTS</span></span>

### <span data-ttu-id="b16a4-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDAtaakışı</span><span class="sxs-lookup"><span data-stu-id="b16a4-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlow</span></span>

## <span data-ttu-id="b16a4-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b16a4-140">NOTES</span></span>
<span data-ttu-id="b16a4-141">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="b16a4-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="b16a4-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b16a4-142">RELATED LINKS</span></span>

[<span data-ttu-id="b16a4-143">Get-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="b16a4-143">Get-AzDataFactoryDataFlow</span></span>](./Get-AzDataFactoryDataFlow.md)

[<span data-ttu-id="b16a4-144">Remove-AzDataFactoryDataFlow</span><span class="sxs-lookup"><span data-stu-id="b16a4-144">Remove-AzDataFactoryDataFlow</span></span>](./Remove-AzDataFactoryDataFlow.md)
