---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2integrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2IntegrationRuntimeNode.md
ms.openlocfilehash: b1f68a334485522aae5f634162941ff20dd59fd9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098282"
---
# <span data-ttu-id="ebb33-101">Remove-AzDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="ebb33-101">Remove-AzDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="ebb33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ebb33-102">SYNOPSIS</span></span>
<span data-ttu-id="ebb33-103">Tümleştirme çalışma zamanında verilen ada sahip düğümü kaldırma.</span><span class="sxs-lookup"><span data-stu-id="ebb33-103">Remove a node with the given name on an integration runtime.</span></span>

## <span data-ttu-id="ebb33-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ebb33-104">SYNTAX</span></span>

### <span data-ttu-id="ebb33-105">Byıntegrationruntimename (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ebb33-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force] [-IntegrationRuntimeName] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebb33-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="ebb33-106">ByResourceId</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebb33-107">Byıntegrationruntimeobject</span><span class="sxs-lookup"><span data-stu-id="ebb33-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ebb33-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="ebb33-108">DESCRIPTION</span></span>
<span data-ttu-id="ebb33-109">Remove-AzDataFactoryV2IntegrationRuntimeNode cmdlet 'i Integration Runtime 'de bir düğümü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ebb33-109">The Remove-AzDataFactoryV2IntegrationRuntimeNode cmdlet removes a node in an integration runtime.</span></span>

## <span data-ttu-id="ebb33-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ebb33-110">EXAMPLES</span></span>

### <span data-ttu-id="ebb33-111">Örnek 1: Tümleştirme çalışma zamanından düğümü kaldırma</span><span class="sxs-lookup"><span data-stu-id="ebb33-111">Example 1: Remove a node from an integration runtime</span></span>
```
PS C:\> Remove-AzDataFactoryV2IntegrationRuntimeNode -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' -NodeName 'Node_1'
```

<span data-ttu-id="ebb33-112">Bu komut, ' RG-test-dfv2 ' adlı kaynak grubu ve ' test-df-EU2 ' adlı veri fabrikası için abonelikteki ' Node_1 ' adlı bir düğümü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ebb33-112">This command removes an node named 'Node_1' in the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="ebb33-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ebb33-113">PARAMETERS</span></span>

### <span data-ttu-id="ebb33-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ebb33-114">-DataFactoryName</span></span>
<span data-ttu-id="ebb33-115">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="ebb33-115">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebb33-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebb33-116">-DefaultProfile</span></span>
<span data-ttu-id="ebb33-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ebb33-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ebb33-118">-Force</span><span class="sxs-lookup"><span data-stu-id="ebb33-118">-Force</span></span>
<span data-ttu-id="ebb33-119">Onay istemeden cmdlet 'i çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="ebb33-119">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="ebb33-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ebb33-120">-InputObject</span></span>
<span data-ttu-id="ebb33-121">Integration Runtime nesnesi.</span><span class="sxs-lookup"><span data-stu-id="ebb33-121">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ebb33-122">-Integrationruntimename</span><span class="sxs-lookup"><span data-stu-id="ebb33-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="ebb33-123">Tümleştirme çalışma zamanı adı.</span><span class="sxs-lookup"><span data-stu-id="ebb33-123">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebb33-124">-DüğümAdı</span><span class="sxs-lookup"><span data-stu-id="ebb33-124">-NodeName</span></span>
<span data-ttu-id="ebb33-125">Integration Runtime düğüm adı.</span><span class="sxs-lookup"><span data-stu-id="ebb33-125">The integration runtime node name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebb33-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebb33-126">-ResourceGroupName</span></span>
<span data-ttu-id="ebb33-127">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="ebb33-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebb33-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="ebb33-128">-ResourceId</span></span>
<span data-ttu-id="ebb33-129">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="ebb33-129">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebb33-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="ebb33-130">-Confirm</span></span>
<span data-ttu-id="ebb33-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ebb33-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ebb33-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebb33-132">-WhatIf</span></span>
<span data-ttu-id="ebb33-133">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="ebb33-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="ebb33-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebb33-134">CommonParameters</span></span>
<span data-ttu-id="ebb33-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ebb33-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebb33-136">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebb33-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebb33-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ebb33-137">INPUTS</span></span>

### <span data-ttu-id="ebb33-138">System. String</span><span class="sxs-lookup"><span data-stu-id="ebb33-138">System.String</span></span>

### <span data-ttu-id="ebb33-139">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="ebb33-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="ebb33-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ebb33-140">OUTPUTS</span></span>

### <span data-ttu-id="ebb33-141">System. void</span><span class="sxs-lookup"><span data-stu-id="ebb33-141">System.Void</span></span>

## <span data-ttu-id="ebb33-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ebb33-142">NOTES</span></span>

## <span data-ttu-id="ebb33-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ebb33-143">RELATED LINKS</span></span>
