---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential.md
ms.openlocfilehash: e89f4c69996f5527c49db72f3185e5a126b348c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588242"
---
# <span data-ttu-id="30812-101">Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential</span><span class="sxs-lookup"><span data-stu-id="30812-101">Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential</span></span>

## <span data-ttu-id="30812-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30812-102">SYNOPSIS</span></span>
<span data-ttu-id="30812-103">Tümleştirme çalışma zamanı düğümleri arasında kimlik bilgilerini eşitler.</span><span class="sxs-lookup"><span data-stu-id="30812-103">Synchronizes credentials among integration runtime nodes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30812-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="30812-104">SYNTAX</span></span>

### <span data-ttu-id="30812-105">Byıntegrationruntimename (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="30812-105">ByIntegrationRuntimeName (Default)</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-IntegrationRuntimeName] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30812-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="30812-106">ByResourceId</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30812-107">Byıntegrationruntimeobject</span><span class="sxs-lookup"><span data-stu-id="30812-107">ByIntegrationRuntimeObject</span></span>
```
Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30812-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="30812-108">DESCRIPTION</span></span>
<span data-ttu-id="30812-109">**Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential** cmdlet 'i tümleştirme çalışma zamanı düğümleri arasında Şirket içi kimlik bilgilerini eşitler ve bu da tüm düğümlerde aynı kimlik bilgilerini özdeş hale getirir.</span><span class="sxs-lookup"><span data-stu-id="30812-109">The **Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential** cmdlet synchronizes on-premises credentials among integration runtime nodes, which forces the credentials to be identical in all nodes.</span></span>

## <span data-ttu-id="30812-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="30812-110">EXAMPLES</span></span>

### <span data-ttu-id="30812-111">Örnek 1: Tümleştirme çalışma zamanı kimlik bilgisini eşitleme</span><span class="sxs-lookup"><span data-stu-id="30812-111">Example 1: Sync an integration runtime credential</span></span>
```
PS C:\> Sync-AzureRmDataFactoryV2IntegrationRuntimeCredential -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'
```

<span data-ttu-id="30812-112">Cmdlet, tümleştirme çalışma zamanı düğümleri arasında kimlik bilgilerini eşitler.</span><span class="sxs-lookup"><span data-stu-id="30812-112">The cmdlet synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="30812-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="30812-113">PARAMETERS</span></span>

### <span data-ttu-id="30812-114">-Onay</span><span class="sxs-lookup"><span data-stu-id="30812-114">-Confirm</span></span>
<span data-ttu-id="30812-115">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="30812-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30812-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="30812-116">-DataFactoryName</span></span>
<span data-ttu-id="30812-117">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="30812-117">The data factory name.</span></span>

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

### <span data-ttu-id="30812-118">-Force</span><span class="sxs-lookup"><span data-stu-id="30812-118">-Force</span></span>
<span data-ttu-id="30812-119">Onay istemeden cmdlet 'i çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="30812-119">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="30812-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="30812-120">-InputObject</span></span>
<span data-ttu-id="30812-121">Integration Runtime nesnesi.</span><span class="sxs-lookup"><span data-stu-id="30812-121">The integration runtime object.</span></span>

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

### <span data-ttu-id="30812-122">-Integrationruntimename</span><span class="sxs-lookup"><span data-stu-id="30812-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="30812-123">Tümleştirme çalışma zamanı adı.</span><span class="sxs-lookup"><span data-stu-id="30812-123">The integration runtime name.</span></span>

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

### <span data-ttu-id="30812-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30812-124">-ResourceGroupName</span></span>
<span data-ttu-id="30812-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="30812-125">The resource group name.</span></span>

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

### <span data-ttu-id="30812-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="30812-126">-ResourceId</span></span>
<span data-ttu-id="30812-127">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="30812-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="30812-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30812-128">-WhatIf</span></span>
<span data-ttu-id="30812-129">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="30812-129">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="30812-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30812-130">-DefaultProfile</span></span>
<span data-ttu-id="30812-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="30812-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30812-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30812-132">CommonParameters</span></span>
<span data-ttu-id="30812-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="30812-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30812-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30812-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30812-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="30812-135">INPUTS</span></span>

### <span data-ttu-id="30812-136">System. String</span><span class="sxs-lookup"><span data-stu-id="30812-136">System.String</span></span>
<span data-ttu-id="30812-137">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="30812-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="30812-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="30812-138">OUTPUTS</span></span>

### <span data-ttu-id="30812-139">System. Object</span><span class="sxs-lookup"><span data-stu-id="30812-139">System.Object</span></span>

## <span data-ttu-id="30812-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="30812-140">NOTES</span></span>

## <span data-ttu-id="30812-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="30812-141">RELATED LINKS</span></span>

