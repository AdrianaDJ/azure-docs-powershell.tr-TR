---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/sync-azurermdatafactoryv2integrationruntimecredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential.md
ms.openlocfilehash: 05b9c5bce3158413f562c38eb116523609696523
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590320"
---
# <span data-ttu-id="b4d74-101">Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential</span><span class="sxs-lookup"><span data-stu-id="b4d74-101">Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential</span></span>

## <span data-ttu-id="b4d74-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4d74-102">SYNOPSIS</span></span>
<span data-ttu-id="b4d74-103">Tümleştirme çalışma zamanı düğümleri arasında kimlik bilgilerini eşitler.</span><span class="sxs-lookup"><span data-stu-id="b4d74-103">Synchronizes credentials among integration runtime nodes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4d74-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b4d74-104">SYNTAX</span></span>

### <span data-ttu-id="b4d74-105">Byıntegrationruntimename (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b4d74-105">ByIntegrationRuntimeName (Default)</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-IntegrationRuntimeName] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4d74-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="b4d74-106">ByResourceId</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4d74-107">Byıntegrationruntimeobject</span><span class="sxs-lookup"><span data-stu-id="b4d74-107">ByIntegrationRuntimeObject</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4d74-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="b4d74-108">DESCRIPTION</span></span>
<span data-ttu-id="b4d74-109">**Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential** cmdlet 'i tümleştirme çalışma zamanı düğümleri arasında Şirket içi kimlik bilgilerini eşitler ve bu da tüm düğümlerde aynı kimlik bilgilerini özdeş hale getirir.</span><span class="sxs-lookup"><span data-stu-id="b4d74-109">The **Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential** cmdlet synchronizes on-premises credentials among integration runtime nodes, which forces the credentials to be identical in all nodes.</span></span>

## <span data-ttu-id="b4d74-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b4d74-110">EXAMPLES</span></span>

### <span data-ttu-id="b4d74-111">Örnek 1: Tümleştirme çalışma zamanı kimlik bilgisini eşitleme</span><span class="sxs-lookup"><span data-stu-id="b4d74-111">Example 1: Sync an integration runtime credential</span></span>
```
PS C:\> Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'
```

<span data-ttu-id="b4d74-112">Cmdlet, tümleştirme çalışma zamanı düğümleri arasında kimlik bilgilerini eşitler.</span><span class="sxs-lookup"><span data-stu-id="b4d74-112">The cmdlet synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="b4d74-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b4d74-113">PARAMETERS</span></span>

### <span data-ttu-id="b4d74-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="b4d74-114">-DataFactoryName</span></span>
<span data-ttu-id="b4d74-115">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="b4d74-115">The data factory name.</span></span>

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

### <span data-ttu-id="b4d74-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4d74-116">-DefaultProfile</span></span>
<span data-ttu-id="b4d74-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b4d74-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4d74-118">-Force</span><span class="sxs-lookup"><span data-stu-id="b4d74-118">-Force</span></span>
<span data-ttu-id="b4d74-119">Onay istemeden cmdlet 'i çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="b4d74-119">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="b4d74-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4d74-120">-InputObject</span></span>
<span data-ttu-id="b4d74-121">Integration Runtime nesnesi.</span><span class="sxs-lookup"><span data-stu-id="b4d74-121">The integration runtime object.</span></span>

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

### <span data-ttu-id="b4d74-122">-Integrationruntimename</span><span class="sxs-lookup"><span data-stu-id="b4d74-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="b4d74-123">Tümleştirme çalışma zamanı adı.</span><span class="sxs-lookup"><span data-stu-id="b4d74-123">The integration runtime name.</span></span>

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

### <span data-ttu-id="b4d74-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4d74-124">-ResourceGroupName</span></span>
<span data-ttu-id="b4d74-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="b4d74-125">The resource group name.</span></span>

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

### <span data-ttu-id="b4d74-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b4d74-126">-ResourceId</span></span>
<span data-ttu-id="b4d74-127">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="b4d74-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="b4d74-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="b4d74-128">-Confirm</span></span>
<span data-ttu-id="b4d74-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b4d74-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4d74-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4d74-130">-WhatIf</span></span>
<span data-ttu-id="b4d74-131">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="b4d74-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="b4d74-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4d74-132">CommonParameters</span></span>
<span data-ttu-id="b4d74-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b4d74-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4d74-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4d74-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4d74-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b4d74-135">INPUTS</span></span>

### <span data-ttu-id="b4d74-136">System. String</span><span class="sxs-lookup"><span data-stu-id="b4d74-136">System.String</span></span>

### <span data-ttu-id="b4d74-137">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="b4d74-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>
<span data-ttu-id="b4d74-138">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b4d74-138">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="b4d74-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b4d74-139">OUTPUTS</span></span>

### <span data-ttu-id="b4d74-140">System. void</span><span class="sxs-lookup"><span data-stu-id="b4d74-140">System.Void</span></span>

## <span data-ttu-id="b4d74-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b4d74-141">NOTES</span></span>

## <span data-ttu-id="b4d74-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b4d74-142">RELATED LINKS</span></span>
