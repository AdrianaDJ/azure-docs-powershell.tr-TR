---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntimeNode.md
ms.openlocfilehash: 4c46ebfb5031d64e685a77768ef6d4c7353d8462
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591773"
---
# <span data-ttu-id="d69cc-101">Remove-AzureRmDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="d69cc-101">Remove-AzureRmDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="d69cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d69cc-102">SYNOPSIS</span></span>
<span data-ttu-id="d69cc-103">Tümleştirme çalışma zamanında verilen ada sahip düğümü kaldırma.</span><span class="sxs-lookup"><span data-stu-id="d69cc-103">Remove a node with the given name on an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d69cc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d69cc-104">SYNTAX</span></span>

### <span data-ttu-id="d69cc-105">Byıntegrationruntimename (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d69cc-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force]
 [-IntegrationRuntimeName] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d69cc-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="d69cc-106">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d69cc-107">Byıntegrationruntimeobject</span><span class="sxs-lookup"><span data-stu-id="d69cc-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force]
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d69cc-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d69cc-108">DESCRIPTION</span></span>
<span data-ttu-id="d69cc-109">Remove-AzureRmDataFactoryV2IntegrationRuntimeNode cmdlet 'i Integration Runtime 'de bir düğümü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d69cc-109">The Remove-AzureRmDataFactoryV2IntegrationRuntimeNode cmdlet removes a node in an integration runtime.</span></span>

## <span data-ttu-id="d69cc-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d69cc-110">EXAMPLES</span></span>

### <span data-ttu-id="d69cc-111">Örnek 1: Tümleştirme çalışma zamanından düğümü kaldırma</span><span class="sxs-lookup"><span data-stu-id="d69cc-111">Example 1: Remove a node from an integration runtime</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' -NodeName 'Node_1'
```

<span data-ttu-id="d69cc-112">Bu komut, ' RG-test-dfv2 ' adlı kaynak grubu ve ' test-df-EU2 ' adlı veri fabrikası için abonelikteki ' Node_1 ' adlı bir düğümü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d69cc-112">This command removes an node named 'Node_1' in the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="d69cc-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d69cc-113">PARAMETERS</span></span>

### <span data-ttu-id="d69cc-114">-Onay</span><span class="sxs-lookup"><span data-stu-id="d69cc-114">-Confirm</span></span>
<span data-ttu-id="d69cc-115">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d69cc-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d69cc-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d69cc-116">-DataFactoryName</span></span>
<span data-ttu-id="d69cc-117">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="d69cc-117">The data factory name.</span></span>

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

### <span data-ttu-id="d69cc-118">-Force</span><span class="sxs-lookup"><span data-stu-id="d69cc-118">-Force</span></span>
<span data-ttu-id="d69cc-119">Onay istemeden cmdlet 'i çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="d69cc-119">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="d69cc-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d69cc-120">-InputObject</span></span>
<span data-ttu-id="d69cc-121">Integration Runtime nesnesi.</span><span class="sxs-lookup"><span data-stu-id="d69cc-121">The integration runtime object.</span></span>

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

### <span data-ttu-id="d69cc-122">-Integrationruntimename</span><span class="sxs-lookup"><span data-stu-id="d69cc-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="d69cc-123">Tümleştirme çalışma zamanı adı.</span><span class="sxs-lookup"><span data-stu-id="d69cc-123">The integration runtime name.</span></span>

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

### <span data-ttu-id="d69cc-124">-DüğümAdı</span><span class="sxs-lookup"><span data-stu-id="d69cc-124">-NodeName</span></span>
<span data-ttu-id="d69cc-125">Integration Runtime düğüm adı.</span><span class="sxs-lookup"><span data-stu-id="d69cc-125">The integration runtime node name.</span></span>

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

### <span data-ttu-id="d69cc-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d69cc-126">-ResourceGroupName</span></span>
<span data-ttu-id="d69cc-127">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="d69cc-127">The resource group name.</span></span>

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

### <span data-ttu-id="d69cc-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d69cc-128">-ResourceId</span></span>
<span data-ttu-id="d69cc-129">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="d69cc-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="d69cc-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d69cc-130">-WhatIf</span></span>
<span data-ttu-id="d69cc-131">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="d69cc-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="d69cc-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d69cc-132">-DefaultProfile</span></span>
<span data-ttu-id="d69cc-133">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d69cc-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d69cc-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d69cc-134">CommonParameters</span></span>
<span data-ttu-id="d69cc-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d69cc-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d69cc-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d69cc-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d69cc-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d69cc-137">INPUTS</span></span>

### <span data-ttu-id="d69cc-138">System. String</span><span class="sxs-lookup"><span data-stu-id="d69cc-138">System.String</span></span>
<span data-ttu-id="d69cc-139">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="d69cc-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="d69cc-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d69cc-140">OUTPUTS</span></span>

### <span data-ttu-id="d69cc-141">System. Object</span><span class="sxs-lookup"><span data-stu-id="d69cc-141">System.Object</span></span>

## <span data-ttu-id="d69cc-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d69cc-142">NOTES</span></span>

## <span data-ttu-id="d69cc-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d69cc-143">RELATED LINKS</span></span>

