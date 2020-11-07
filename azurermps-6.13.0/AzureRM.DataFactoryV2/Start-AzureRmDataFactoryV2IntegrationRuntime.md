---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/start-azurermdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Start-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Start-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: a9254fbac7e0c98413f4367d9b5e62581f6cb64c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762618"
---
# <span data-ttu-id="4b34c-101">Start-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="4b34c-101">Start-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="4b34c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b34c-102">SYNOPSIS</span></span>
<span data-ttu-id="4b34c-103">Yönetilen adanmış tümleştirme çalışma zamanını başlatır.</span><span class="sxs-lookup"><span data-stu-id="4b34c-103">Starts a managed dedicated integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b34c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4b34c-104">SYNTAX</span></span>

### <span data-ttu-id="4b34c-105">Byıntegrationruntimename (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4b34c-105">ByIntegrationRuntimeName (Default)</span></span>
```
Start-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4b34c-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="4b34c-106">ByResourceId</span></span>
```
Start-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b34c-107">Byıntegrationruntimeobject</span><span class="sxs-lookup"><span data-stu-id="4b34c-107">ByIntegrationRuntimeObject</span></span>
```
Start-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b34c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="4b34c-108">DESCRIPTION</span></span>
<span data-ttu-id="4b34c-109">**Start-AzureRmDataFactoryV2IntegrationRuntime** cmdlet 'i yönetilen adanmış tümleştirme çalışma zamanını başlatır.</span><span class="sxs-lookup"><span data-stu-id="4b34c-109">The **Start-AzureRmDataFactoryV2IntegrationRuntime** cmdlet starts a managed dedicated integration runtime.</span></span> <span data-ttu-id="4b34c-110">Kaynak sağlandı ve işlemden sonra durum ' Started '.</span><span class="sxs-lookup"><span data-stu-id="4b34c-110">The resource is provisioned and after the operation the state is 'Started'.</span></span>

## <span data-ttu-id="4b34c-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4b34c-111">EXAMPLES</span></span>

### <span data-ttu-id="4b34c-112">Örnek 1: Tümleştirme çalışma zamanı başlatma</span><span class="sxs-lookup"><span data-stu-id="4b34c-112">Example 1: Start an integration runtime</span></span>
```
PS C:\> Start-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name test-dedicated-ir' -Force

    CreateTime                   : 9/11/2017 2:16:12 PM
    Nodes                        : {tvm-1650185656_1-20170911t141751z}
    OtherErrors                  : {}
    LastOperation                : 
    State                        : Started
    Location                     : West US
    NodeSize                     : Standard_D1_v2
    NodeCount                    : 1
    MaxParallelExecutionsPerNode : 1
    CatalogServerEndpoint        : testsvr.database.windows.net
    CatalogAdminUserName         : admin
    CatalogAdminPassword         : **********
    CatalogPricingTier           : S1
    VNetId                       : 
    Subnet                       : 
    Id                           : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-dedicated-ir
    ResourceGroupName            : rg-test-dfv2
    DataFactoryName              : test-df-eu2
    Name                         : test-dedicated-ir
    Description                  : Reserved IR
```

<span data-ttu-id="4b34c-113">Bu cmdlet ' test-adanmış-IR ' adlı Yönetilen adanmış tümleştirme çalışma zamanını başlatır.</span><span class="sxs-lookup"><span data-stu-id="4b34c-113">This cmdlet starts a managed dedicated integration runtime named 'test-dedicated-ir'.</span></span>

## <span data-ttu-id="4b34c-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4b34c-114">PARAMETERS</span></span>

### <span data-ttu-id="4b34c-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="4b34c-115">-DataFactoryName</span></span>
<span data-ttu-id="4b34c-116">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="4b34c-116">The data factory name.</span></span>

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

### <span data-ttu-id="4b34c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b34c-117">-DefaultProfile</span></span>
<span data-ttu-id="4b34c-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4b34c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b34c-119">-Force</span><span class="sxs-lookup"><span data-stu-id="4b34c-119">-Force</span></span>
<span data-ttu-id="4b34c-120">Onay istemeden cmdlet 'i çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="4b34c-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="4b34c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4b34c-121">-InputObject</span></span>
<span data-ttu-id="4b34c-122">Integration Runtime nesnesi.</span><span class="sxs-lookup"><span data-stu-id="4b34c-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="4b34c-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="4b34c-123">-Name</span></span>
<span data-ttu-id="4b34c-124">Tümleştirme çalışma zamanı adı.</span><span class="sxs-lookup"><span data-stu-id="4b34c-124">The integration runtime name.</span></span>

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

### <span data-ttu-id="4b34c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b34c-125">-ResourceGroupName</span></span>
<span data-ttu-id="4b34c-126">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="4b34c-126">The resource group name.</span></span>

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

### <span data-ttu-id="4b34c-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="4b34c-127">-ResourceId</span></span>
<span data-ttu-id="4b34c-128">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="4b34c-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="4b34c-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="4b34c-129">-Confirm</span></span>
<span data-ttu-id="4b34c-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4b34c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b34c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b34c-131">-WhatIf</span></span>
<span data-ttu-id="4b34c-132">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="4b34c-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="4b34c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b34c-133">CommonParameters</span></span>
<span data-ttu-id="4b34c-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4b34c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b34c-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b34c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b34c-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4b34c-136">INPUTS</span></span>

### <span data-ttu-id="4b34c-137">System. String</span><span class="sxs-lookup"><span data-stu-id="4b34c-137">System.String</span></span>

### <span data-ttu-id="4b34c-138">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="4b34c-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>
<span data-ttu-id="4b34c-139">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4b34c-139">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="4b34c-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4b34c-140">OUTPUTS</span></span>

### <span data-ttu-id="4b34c-141">Microsoft. Azure. Commands. DataFactoryV2. modeller. PSManagedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="4b34c-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="4b34c-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4b34c-142">NOTES</span></span>

## <span data-ttu-id="4b34c-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4b34c-143">RELATED LINKS</span></span>

[<span data-ttu-id="4b34c-144">Stop-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="4b34c-144">Stop-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
