---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 63889ce74af1051211a579d1af7cc54be14822f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762225"
---
# <span data-ttu-id="0ca9d-101">Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential</span><span class="sxs-lookup"><span data-stu-id="0ca9d-101">Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential</span></span>

## <span data-ttu-id="0ca9d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ca9d-102">SYNOPSIS</span></span>
<span data-ttu-id="0ca9d-103">Tümleştirme çalışma zamanı düğümleri arasında kimlik bilgilerini eşitler.</span><span class="sxs-lookup"><span data-stu-id="0ca9d-103">Synchronizes credentials among integration runtime nodes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ca9d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0ca9d-104">SYNTAX</span></span>

### <span data-ttu-id="0ca9d-105">Byıntegrationruntimename (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0ca9d-105">ByIntegrationRuntimeName (Default)</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-IntegrationRuntimeName] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="0ca9d-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="0ca9d-106">ByResourceId</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-ResourceId] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="0ca9d-107">Byıntegrationruntimeobject</span><span class="sxs-lookup"><span data-stu-id="0ca9d-107">ByIntegrationRuntimeObject</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-InputObject] <PSIntegrationRuntime>
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="0ca9d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0ca9d-108">DESCRIPTION</span></span>
<span data-ttu-id="0ca9d-109">**Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential** cmdlet 'i tümleştirme çalışma zamanı düğümleri arasında Şirket içi kimlik bilgilerini eşitler ve bu da tüm düğümlerde aynı kimlik bilgilerini özdeş hale getirir.</span><span class="sxs-lookup"><span data-stu-id="0ca9d-109">The **Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential** cmdlet synchronizes on-premises credentials among integration runtime nodes, which forces the credentials to be identical in all nodes.</span></span>

## <span data-ttu-id="0ca9d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0ca9d-110">EXAMPLES</span></span>

### <span data-ttu-id="0ca9d-111">Örnek 1: Tümleştirme çalışma zamanı kimlik bilgisini eşitleme</span><span class="sxs-lookup"><span data-stu-id="0ca9d-111">Example 1: Sync an integration runtime credential</span></span>
```
PS C:\> Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'
```

<span data-ttu-id="0ca9d-112">Cmdlet, tümleştirme çalışma zamanı düğümleri arasında kimlik bilgilerini eşitler.</span><span class="sxs-lookup"><span data-stu-id="0ca9d-112">The cmdlet synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="0ca9d-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0ca9d-113">PARAMETERS</span></span>

### <span data-ttu-id="0ca9d-114">-Onay</span><span class="sxs-lookup"><span data-stu-id="0ca9d-114">-Confirm</span></span>
<span data-ttu-id="0ca9d-115">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0ca9d-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ca9d-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="0ca9d-116">-DataFactoryName</span></span>
<span data-ttu-id="0ca9d-117">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="0ca9d-117">The data factory name.</span></span>

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

### <span data-ttu-id="0ca9d-118">-Force</span><span class="sxs-lookup"><span data-stu-id="0ca9d-118">-Force</span></span>
<span data-ttu-id="0ca9d-119">Onay istemeden cmdlet 'i çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="0ca9d-119">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="0ca9d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0ca9d-120">-InputObject</span></span>
<span data-ttu-id="0ca9d-121">Integration Runtime nesnesi.</span><span class="sxs-lookup"><span data-stu-id="0ca9d-121">The integration runtime object.</span></span>

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

### <span data-ttu-id="0ca9d-122">-Integrationruntimename</span><span class="sxs-lookup"><span data-stu-id="0ca9d-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="0ca9d-123">Tümleştirme çalışma zamanı adı.</span><span class="sxs-lookup"><span data-stu-id="0ca9d-123">The integration runtime name.</span></span>

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

### <span data-ttu-id="0ca9d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ca9d-124">-ResourceGroupName</span></span>
<span data-ttu-id="0ca9d-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="0ca9d-125">The resource group name.</span></span>

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

### <span data-ttu-id="0ca9d-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="0ca9d-126">-ResourceId</span></span>
<span data-ttu-id="0ca9d-127">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="0ca9d-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="0ca9d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ca9d-128">-WhatIf</span></span>
<span data-ttu-id="0ca9d-129">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="0ca9d-129">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="0ca9d-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0ca9d-130">INPUTS</span></span>

### <span data-ttu-id="0ca9d-131">System. String</span><span class="sxs-lookup"><span data-stu-id="0ca9d-131">System.String</span></span>
<span data-ttu-id="0ca9d-132">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="0ca9d-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>


## <span data-ttu-id="0ca9d-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0ca9d-133">OUTPUTS</span></span>

### <span data-ttu-id="0ca9d-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="0ca9d-134">System.Object</span></span>

## <span data-ttu-id="0ca9d-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0ca9d-135">NOTES</span></span>

## <span data-ttu-id="0ca9d-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0ca9d-136">RELATED LINKS</span></span>
