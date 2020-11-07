---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/sync-azdatafactoryv2integrationruntimecredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Sync-AzDataFactoryV2IntegrationRuntimeCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Sync-AzDataFactoryV2IntegrationRuntimeCredential.md
ms.openlocfilehash: 40f6a6c5f446b23a92a2ca5c5c8c872297b2a81a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752422"
---
# <span data-ttu-id="37ece-101">Sync-AzDataFactoryV2IntegrationRuntimeCredential</span><span class="sxs-lookup"><span data-stu-id="37ece-101">Sync-AzDataFactoryV2IntegrationRuntimeCredential</span></span>

## <span data-ttu-id="37ece-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37ece-102">SYNOPSIS</span></span>
<span data-ttu-id="37ece-103">Tümleştirme çalışma zamanı düğümleri arasında kimlik bilgilerini eşitler.</span><span class="sxs-lookup"><span data-stu-id="37ece-103">Synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="37ece-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="37ece-104">SYNTAX</span></span>

### <span data-ttu-id="37ece-105">Byıntegrationruntimename (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="37ece-105">ByIntegrationRuntimeName (Default)</span></span>
```
Sync-AzDataFactoryV2IntegrationRuntimeCredential [-Force] [-IntegrationRuntimeName] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37ece-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="37ece-106">ByResourceId</span></span>
```
Sync-AzDataFactoryV2IntegrationRuntimeCredential [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37ece-107">Byıntegrationruntimeobject</span><span class="sxs-lookup"><span data-stu-id="37ece-107">ByIntegrationRuntimeObject</span></span>
```
Sync-AzDataFactoryV2IntegrationRuntimeCredential [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37ece-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="37ece-108">DESCRIPTION</span></span>
<span data-ttu-id="37ece-109">**Sync-AzDataFactoryV2IntegrationRuntimeCredential** cmdlet 'i tümleştirme çalışma zamanı düğümleri arasında Şirket içi kimlik bilgilerini eşitler ve bu da tüm düğümlerde aynı kimlik bilgilerini özdeş hale getirir.</span><span class="sxs-lookup"><span data-stu-id="37ece-109">The **Sync-AzDataFactoryV2IntegrationRuntimeCredential** cmdlet synchronizes on-premises credentials among integration runtime nodes, which forces the credentials to be identical in all nodes.</span></span>

## <span data-ttu-id="37ece-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="37ece-110">EXAMPLES</span></span>

### <span data-ttu-id="37ece-111">Örnek 1: Tümleştirme çalışma zamanı kimlik bilgisini eşitleme</span><span class="sxs-lookup"><span data-stu-id="37ece-111">Example 1: Sync an integration runtime credential</span></span>
```
PS C:\> Sync-AzDataFactoryV2IntegrationRuntimeCredential -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'
```

<span data-ttu-id="37ece-112">Cmdlet, tümleştirme çalışma zamanı düğümleri arasında kimlik bilgilerini eşitler.</span><span class="sxs-lookup"><span data-stu-id="37ece-112">The cmdlet synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="37ece-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="37ece-113">PARAMETERS</span></span>

### <span data-ttu-id="37ece-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="37ece-114">-DataFactoryName</span></span>
<span data-ttu-id="37ece-115">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="37ece-115">The data factory name.</span></span>

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

### <span data-ttu-id="37ece-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37ece-116">-DefaultProfile</span></span>
<span data-ttu-id="37ece-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="37ece-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37ece-118">-Force</span><span class="sxs-lookup"><span data-stu-id="37ece-118">-Force</span></span>
<span data-ttu-id="37ece-119">Onay istemeden cmdlet 'i çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="37ece-119">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="37ece-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="37ece-120">-InputObject</span></span>
<span data-ttu-id="37ece-121">Integration Runtime nesnesi.</span><span class="sxs-lookup"><span data-stu-id="37ece-121">The integration runtime object.</span></span>

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

### <span data-ttu-id="37ece-122">-Integrationruntimename</span><span class="sxs-lookup"><span data-stu-id="37ece-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="37ece-123">Tümleştirme çalışma zamanı adı.</span><span class="sxs-lookup"><span data-stu-id="37ece-123">The integration runtime name.</span></span>

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

### <span data-ttu-id="37ece-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37ece-124">-ResourceGroupName</span></span>
<span data-ttu-id="37ece-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="37ece-125">The resource group name.</span></span>

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

### <span data-ttu-id="37ece-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="37ece-126">-ResourceId</span></span>
<span data-ttu-id="37ece-127">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="37ece-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="37ece-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="37ece-128">-Confirm</span></span>
<span data-ttu-id="37ece-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="37ece-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37ece-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37ece-130">-WhatIf</span></span>
<span data-ttu-id="37ece-131">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="37ece-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="37ece-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37ece-132">CommonParameters</span></span>
<span data-ttu-id="37ece-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="37ece-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37ece-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37ece-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37ece-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="37ece-135">INPUTS</span></span>

### <span data-ttu-id="37ece-136">System. String</span><span class="sxs-lookup"><span data-stu-id="37ece-136">System.String</span></span>

### <span data-ttu-id="37ece-137">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="37ece-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="37ece-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="37ece-138">OUTPUTS</span></span>

### <span data-ttu-id="37ece-139">System. void</span><span class="sxs-lookup"><span data-stu-id="37ece-139">System.Void</span></span>

## <span data-ttu-id="37ece-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="37ece-140">NOTES</span></span>

## <span data-ttu-id="37ece-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="37ece-141">RELATED LINKS</span></span>
