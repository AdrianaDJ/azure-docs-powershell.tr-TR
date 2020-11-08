---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: aa838b24cc2410d9d699bac4dc8d4c00e3153174
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938268"
---
# <span data-ttu-id="12d93-101">Stop-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="12d93-101">Stop-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="12d93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12d93-102">SYNOPSIS</span></span>
<span data-ttu-id="12d93-103">Yönetilen adanmış tümleştirme çalışma zamanını durdurur.</span><span class="sxs-lookup"><span data-stu-id="12d93-103">Stops a managed dedicated integration runtime.</span></span>

## <span data-ttu-id="12d93-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="12d93-104">SYNTAX</span></span>

### <span data-ttu-id="12d93-105">Byıntegrationruntimename (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="12d93-105">ByIntegrationRuntimeName (Default)</span></span>
```
Stop-AzDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="12d93-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="12d93-106">ByResourceId</span></span>
```
Stop-AzDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12d93-107">Byıntegrationruntimeobject</span><span class="sxs-lookup"><span data-stu-id="12d93-107">ByIntegrationRuntimeObject</span></span>
```
Stop-AzDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12d93-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="12d93-108">DESCRIPTION</span></span>
<span data-ttu-id="12d93-109">**Stop-AzDataFactoryV2IntegrationRuntime** cmdlet 'i, Start-AzDataFactoryV2IntegrationRuntime cmdlet 'i tarafından başlatılan ' Started ' durumundaki yönetilen adanmış tümleştirme çalışma zamanını durdurur.</span><span class="sxs-lookup"><span data-stu-id="12d93-109">The **Stop-AzDataFactoryV2IntegrationRuntime** cmdlet stops a managed dedicated integration runtime in 'Started' state, which was started by the Start-AzDataFactoryV2IntegrationRuntime cmdlet.</span></span> <span data-ttu-id="12d93-110">Kaynaklar serbest bırakıldı ve durum aktarımları ' durduruldu '.</span><span class="sxs-lookup"><span data-stu-id="12d93-110">The resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="12d93-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="12d93-111">EXAMPLES</span></span>

### <span data-ttu-id="12d93-112">Örnek 1: ' Başlangıç ' durumundaki bir yönetilen tümleştirme çalışma zamanını durdurun.</span><span class="sxs-lookup"><span data-stu-id="12d93-112">Example 1: Stop a managed integration runtime that is in 'Started' state.</span></span>
```
PS C:\> Stop-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserlved-ir'
```

<span data-ttu-id="12d93-113">Yönetilen tümleştirme çalışma zamanı ' testi-reserl,-IR ', ' Started ' durumunda.</span><span class="sxs-lookup"><span data-stu-id="12d93-113">The managed integration runtime 'test-reserlved-ir' is in 'Started' state.</span></span> <span data-ttu-id="12d93-114">Stop-AzDataFactoryV2IntegrationRuntime cmdlet 'i çalıştırdıktan sonra, kaynaklar serbest bırakılarak, durum aktarımları ' durduruldu '.</span><span class="sxs-lookup"><span data-stu-id="12d93-114">After running Stop-AzDataFactoryV2IntegrationRuntime cmdlet, the resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="12d93-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="12d93-115">PARAMETERS</span></span>

### <span data-ttu-id="12d93-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="12d93-116">-DataFactoryName</span></span>
<span data-ttu-id="12d93-117">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="12d93-117">The data factory name.</span></span>

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

### <span data-ttu-id="12d93-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12d93-118">-DefaultProfile</span></span>
<span data-ttu-id="12d93-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="12d93-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12d93-120">-Force</span><span class="sxs-lookup"><span data-stu-id="12d93-120">-Force</span></span>
<span data-ttu-id="12d93-121">Onay istemeden cmdlet 'i çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="12d93-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="12d93-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="12d93-122">-InputObject</span></span>
<span data-ttu-id="12d93-123">Integration Runtime nesnesi.</span><span class="sxs-lookup"><span data-stu-id="12d93-123">The integration runtime object.</span></span>

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

### <span data-ttu-id="12d93-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="12d93-124">-Name</span></span>
<span data-ttu-id="12d93-125">Tümleştirme çalışma zamanı adı.</span><span class="sxs-lookup"><span data-stu-id="12d93-125">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12d93-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12d93-126">-ResourceGroupName</span></span>
<span data-ttu-id="12d93-127">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="12d93-127">The resource group name.</span></span>

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

### <span data-ttu-id="12d93-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="12d93-128">-ResourceId</span></span>
<span data-ttu-id="12d93-129">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="12d93-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="12d93-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="12d93-130">-Confirm</span></span>
<span data-ttu-id="12d93-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="12d93-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12d93-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12d93-132">-WhatIf</span></span>
<span data-ttu-id="12d93-133">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="12d93-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="12d93-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12d93-134">CommonParameters</span></span>
<span data-ttu-id="12d93-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="12d93-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12d93-136">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12d93-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12d93-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="12d93-137">INPUTS</span></span>

### <span data-ttu-id="12d93-138">System. String</span><span class="sxs-lookup"><span data-stu-id="12d93-138">System.String</span></span>

### <span data-ttu-id="12d93-139">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="12d93-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="12d93-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="12d93-140">OUTPUTS</span></span>

### <span data-ttu-id="12d93-141">System. void</span><span class="sxs-lookup"><span data-stu-id="12d93-141">System.Void</span></span>

## <span data-ttu-id="12d93-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="12d93-142">NOTES</span></span>
<span data-ttu-id="12d93-143">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrika, kopyalama, Etkinlikler, tümleştirme çalışma zamanı</span><span class="sxs-lookup"><span data-stu-id="12d93-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="12d93-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="12d93-144">RELATED LINKS</span></span>

[<span data-ttu-id="12d93-145">Start-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="12d93-145">Start-AzDataFactoryV2IntegrationRuntime</span></span>]()