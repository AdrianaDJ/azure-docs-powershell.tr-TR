---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactoryv2integrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntimeNode.md
ms.openlocfilehash: bc16145569fd46b80e6d7a5afc1755f36346fa9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586729"
---
# <span data-ttu-id="31c34-101">Remove-AzureRmDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="31c34-101">Remove-AzureRmDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="31c34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31c34-102">SYNOPSIS</span></span>
<span data-ttu-id="31c34-103">Tümleştirme çalışma zamanında verilen ada sahip düğümü kaldırma.</span><span class="sxs-lookup"><span data-stu-id="31c34-103">Remove a node with the given name on an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31c34-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="31c34-104">SYNTAX</span></span>

### <span data-ttu-id="31c34-105">Byıntegrationruntimename (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="31c34-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force]
 [-IntegrationRuntimeName] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31c34-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="31c34-106">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31c34-107">Byıntegrationruntimeobject</span><span class="sxs-lookup"><span data-stu-id="31c34-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force]
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="31c34-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="31c34-108">DESCRIPTION</span></span>
<span data-ttu-id="31c34-109">Remove-AzureRmDataFactoryV2IntegrationRuntimeNode cmdlet 'i Integration Runtime 'de bir düğümü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="31c34-109">The Remove-AzureRmDataFactoryV2IntegrationRuntimeNode cmdlet removes a node in an integration runtime.</span></span>

## <span data-ttu-id="31c34-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="31c34-110">EXAMPLES</span></span>

### <span data-ttu-id="31c34-111">Örnek 1: Tümleştirme çalışma zamanından düğümü kaldırma</span><span class="sxs-lookup"><span data-stu-id="31c34-111">Example 1: Remove a node from an integration runtime</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' -NodeName 'Node_1'
```

<span data-ttu-id="31c34-112">Bu komut, ' RG-test-dfv2 ' adlı kaynak grubu ve ' test-df-EU2 ' adlı veri fabrikası için abonelikteki ' Node_1 ' adlı bir düğümü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="31c34-112">This command removes an node named 'Node_1' in the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="31c34-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="31c34-113">PARAMETERS</span></span>

### <span data-ttu-id="31c34-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="31c34-114">-DataFactoryName</span></span>
<span data-ttu-id="31c34-115">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="31c34-115">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31c34-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31c34-116">-DefaultProfile</span></span>
<span data-ttu-id="31c34-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="31c34-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31c34-118">-Force</span><span class="sxs-lookup"><span data-stu-id="31c34-118">-Force</span></span>
<span data-ttu-id="31c34-119">Onay istemeden cmdlet 'i çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="31c34-119">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31c34-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="31c34-120">-InputObject</span></span>
<span data-ttu-id="31c34-121">Integration Runtime nesnesi.</span><span class="sxs-lookup"><span data-stu-id="31c34-121">The integration runtime object.</span></span>

```yaml
Type: PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31c34-122">-Integrationruntimename</span><span class="sxs-lookup"><span data-stu-id="31c34-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="31c34-123">Tümleştirme çalışma zamanı adı.</span><span class="sxs-lookup"><span data-stu-id="31c34-123">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31c34-124">-DüğümAdı</span><span class="sxs-lookup"><span data-stu-id="31c34-124">-NodeName</span></span>
<span data-ttu-id="31c34-125">Integration Runtime düğüm adı.</span><span class="sxs-lookup"><span data-stu-id="31c34-125">The integration runtime node name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31c34-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31c34-126">-ResourceGroupName</span></span>
<span data-ttu-id="31c34-127">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="31c34-127">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31c34-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="31c34-128">-ResourceId</span></span>
<span data-ttu-id="31c34-129">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="31c34-129">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31c34-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="31c34-130">-Confirm</span></span>
<span data-ttu-id="31c34-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="31c34-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31c34-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31c34-132">-WhatIf</span></span>
<span data-ttu-id="31c34-133">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="31c34-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31c34-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31c34-134">CommonParameters</span></span>
<span data-ttu-id="31c34-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="31c34-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31c34-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31c34-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31c34-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="31c34-137">INPUTS</span></span>

### <span data-ttu-id="31c34-138">System. String</span><span class="sxs-lookup"><span data-stu-id="31c34-138">System.String</span></span>
<span data-ttu-id="31c34-139">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="31c34-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="31c34-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="31c34-140">OUTPUTS</span></span>

### <span data-ttu-id="31c34-141">System. Object</span><span class="sxs-lookup"><span data-stu-id="31c34-141">System.Object</span></span>

## <span data-ttu-id="31c34-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="31c34-142">NOTES</span></span>

## <span data-ttu-id="31c34-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="31c34-143">RELATED LINKS</span></span>

