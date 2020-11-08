---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2dataflowdebugsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlowDebugSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlowDebugSession.md
ms.openlocfilehash: 951f1b6a03c621e0dd8bc5d559eaf317cfd43a2c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109713"
---
# <span data-ttu-id="56570-101">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="56570-101">Get-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="56570-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56570-102">SYNOPSIS</span></span>
<span data-ttu-id="56570-103">Azure Veri Fabrikası tarafından tüm etkin veri akışı hata ayıklama oturumlarını alma</span><span class="sxs-lookup"><span data-stu-id="56570-103">Get all active data flow debug sessions by Azure Data Factory</span></span>

## <span data-ttu-id="56570-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="56570-104">SYNTAX</span></span>

### <span data-ttu-id="56570-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="56570-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2DataFlowDebugSession [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56570-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="56570-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2DataFlowDebugSession [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="56570-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="56570-107">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2DataFlowDebugSession [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56570-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="56570-108">DESCRIPTION</span></span>
<span data-ttu-id="56570-109">Azure Veri Fabrikası ile tüm etkin veri akışı hata ayıklama oturumlarını ayrıntılarıyla listeleyin.</span><span class="sxs-lookup"><span data-stu-id="56570-109">List all active data flow debug sessions by Azure Data Factory with details.</span></span>

## <span data-ttu-id="56570-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="56570-110">EXAMPLES</span></span>

### <span data-ttu-id="56570-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="56570-111">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Get-AzDataFactoryV2DataFlowDebugSession -ResourceGroupName adf -DataFactoryName WikiADF

SessionId                            ComputeType CoreCount                         StartTime                  LastActivityTime TimeToLiveInMinutes IntegrationRuntimeName                                      DataFlowName
---------                            ----------- ---------                         ---------                  ---------------- ------------------- ----------------------                                      ------------
3c68dbd6-f9c3-4b5f-a200-2310258016a7     General         8 2019-10-04T18:19:58.5550364+00:00 2019-10-04T18:24:51.3680548+00:00                  60                        DebugSession-0a7e0d6e-f2b7-48cc-8cd8-618326f5662f
```

<span data-ttu-id="56570-112">Azure Veri Fabrikası 'ndaki tüm etkin veri akışı hata ayıklama oturumlarını "WikiADF" alın.</span><span class="sxs-lookup"><span data-stu-id="56570-112">Get all active data flow debug sessions in Azure Data Factory "WikiADF".</span></span>

## <span data-ttu-id="56570-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="56570-113">PARAMETERS</span></span>

### <span data-ttu-id="56570-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="56570-114">-DataFactory</span></span>
<span data-ttu-id="56570-115">Veri fabrikası nesnesi.</span><span class="sxs-lookup"><span data-stu-id="56570-115">The data factory object.</span></span>

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

### <span data-ttu-id="56570-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="56570-116">-DataFactoryName</span></span>
<span data-ttu-id="56570-117">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="56570-117">The data factory name.</span></span>

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

### <span data-ttu-id="56570-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56570-118">-DefaultProfile</span></span>
<span data-ttu-id="56570-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="56570-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56570-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56570-120">-ResourceGroupName</span></span>
<span data-ttu-id="56570-121">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="56570-121">The resource group name.</span></span>

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

### <span data-ttu-id="56570-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="56570-122">-ResourceId</span></span>
<span data-ttu-id="56570-123">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="56570-123">The Azure resource ID.</span></span>

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

### <span data-ttu-id="56570-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56570-124">CommonParameters</span></span>
<span data-ttu-id="56570-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="56570-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56570-126">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="56570-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56570-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="56570-127">INPUTS</span></span>

### <span data-ttu-id="56570-128">System. String</span><span class="sxs-lookup"><span data-stu-id="56570-128">System.String</span></span>

### <span data-ttu-id="56570-129">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="56570-129">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="56570-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="56570-130">OUTPUTS</span></span>

### <span data-ttu-id="56570-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDAtaflowdebugsessionınfo</span><span class="sxs-lookup"><span data-stu-id="56570-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionInfo</span></span>

## <span data-ttu-id="56570-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="56570-132">NOTES</span></span>
<span data-ttu-id="56570-133">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="56570-133">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="56570-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="56570-134">RELATED LINKS</span></span>

[<span data-ttu-id="56570-135">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="56570-135">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="56570-136">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="56570-136">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="56570-137">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="56570-137">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)

[<span data-ttu-id="56570-138">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="56570-138">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)