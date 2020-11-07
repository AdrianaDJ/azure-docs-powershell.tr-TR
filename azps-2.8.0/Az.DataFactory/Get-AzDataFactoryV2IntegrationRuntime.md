---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 96c635caef26a1dc90ae2646cb4899012105f526
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752540"
---
# <span data-ttu-id="e09c4-101">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e09c4-101">Get-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="e09c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e09c4-102">SYNOPSIS</span></span>
<span data-ttu-id="e09c4-103">Tümleştirme çalışma zamanı kaynakları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="e09c4-103">Gets information about integration runtime resources.</span></span>

## <span data-ttu-id="e09c4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e09c4-104">SYNTAX</span></span>

### <span data-ttu-id="e09c4-105">Byıntegrationruntimename (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e09c4-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntime [[-Name] <String>] [-Status] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e09c4-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="e09c4-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntime [-Status] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e09c4-107">Byıntegrationruntimeobject</span><span class="sxs-lookup"><span data-stu-id="e09c4-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntime [-Status] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e09c4-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e09c4-108">DESCRIPTION</span></span>
<span data-ttu-id="e09c4-109">Get-AzDataFactoryV2IntegrationRuntime cmdlet 'i Veri Fabrikası içindeki tümleştirme çalışma zamanları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="e09c4-109">The Get-AzDataFactoryV2IntegrationRuntime cmdlet gets information about integration runtimes in a data factory.</span></span>
<span data-ttu-id="e09c4-110">Bir tümleştirme çalışma zamanının adını belirtirseniz, bu cmdlet Bu tümleştirme çalışma zamanı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="e09c4-110">If you specify the name of an integration runtime, this cmdlet gets information about that integration runtime.</span></span>
<span data-ttu-id="e09c4-111">Bir ad belirtmezseniz, bu cmdlet Veri Fabrikası içindeki tüm tümleştirme çalışma zamanları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="e09c4-111">If you do not specify a name, this cmdlet gets information about all of the integration runtimes in a data factory.</span></span>

## <span data-ttu-id="e09c4-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e09c4-112">EXAMPLES</span></span>

### <span data-ttu-id="e09c4-113">Örnek 1: veri fabrikasında tüm tümleştirme çalışma zamanlarını listeleme</span><span class="sxs-lookup"><span data-stu-id="e09c4-113">Example 1: List all integration runtimes in a data factory</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2

    ResourceGroupName DataFactoryName Name                   Description
    ----------------- --------------- ----                   -----------
    rg-test-dfv2      test-df-eu2     test-reserved-ir       Reserved IR
    rg-test-dfv2      test-df-eu2     test-dedicated-ir      Reserved IR
    rg-test-dfv2      test-df-eu2     test-selfhost-ir       selfhost IR
```

<span data-ttu-id="e09c4-114">' Test-df-EU2 ' adındaki Veri Fabrikası 'ndaki tüm tümleştirme çalışma zamanlarını listeleyin.</span><span class="sxs-lookup"><span data-stu-id="e09c4-114">List all integration runtimes in the data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="e09c4-115">Örnek 2: Yönetilen adanmış tümleştirme çalışma zamanını alma</span><span class="sxs-lookup"><span data-stu-id="e09c4-115">Example 2: Get managed dedicated integration runtime</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-dedicated-ir

    Location                     : West US
    NodeSize                     : Standard_D1_v2
    NodeCount                    : 1
    MaxParallelExecutionsPerNode : 1
    CatalogServerEndpoint        : test.database.windows.net
    CatalogAdminUserName         : test
    CatalogAdminPassword         : **********
    CatalogPricingTier           : S1
    VNetId                       : 
    Subnet                       : 
    State                        : Starting
    ResourceGroupName            : rg-test-dfv2
    DataFactoryName              : test-df-eu2
    Name                         : test-dedicated-ir
    Description                  : Reserved IR
```

<span data-ttu-id="e09c4-116">Bu komut, ' RG-test-dfv2 ' adlı kaynak grubunun aboneliğindeki ' test-adanmış-IR ' adlı tümleştirme çalışma zamanı hakkında bilgi görüntüler ve ' test-df-EU2 '.</span><span class="sxs-lookup"><span data-stu-id="e09c4-116">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="e09c4-117">Örnek 3: ayrıntı durumuyla yönetilen adanmış tümleştirme çalışma zamanını alma</span><span class="sxs-lookup"><span data-stu-id="e09c4-117">Example 3: Get managed dedicated integration runtime with detail status</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-dedicated-ir -Status

    CreateTime                   : 
    Nodes                        : 
    OtherErrors                  : 
    LastOperation                : 
    State                        : Initial
    Location                     : West US
    NodeSize                     : Standard_D1_v2
    NodeCount                    : 1
    MaxParallelExecutionsPerNode : 1
    CatalogServerEndpoint        : test.database.windows.net
    CatalogAdminUserName         : test
    CatalogAdminPassword         : **********
    CatalogPricingTier           : S1
    VNetId                       : 
    Subnet                       : 
    ResourceGroupName            : rg-test-dfv2
    DataFactoryName              : test-df-eu2
    Name                         : test-dedicated-ir
    Description                  : Reserved IR
```

<span data-ttu-id="e09c4-118">Bu komut, ' RG-test-dfv2 ' adlı kaynak grubunun aboneliğindeki ' test-adanmış-IR ' adlı tümleştirme çalışma zamanı hakkında bilgi görüntüler ve ' test-df-EU2 '.</span><span class="sxs-lookup"><span data-stu-id="e09c4-118">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="e09c4-119">Örnek 4: kendi kendine barındırılan tümleştirme çalışma zamanını alın</span><span class="sxs-lookup"><span data-stu-id="e09c4-119">Example 4: Get self-hosted integration runtime</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-selfhost-ir

    ResourceGroupName DataFactoryName Name                 Description
    ----------------- --------------- ----                 -----------
    rg-test-dfv2      test-df-eu2     test-selfhost-ir     selfhost IR
```

<span data-ttu-id="e09c4-120">Bu komut, ' RG-test-dfv2 ' adlı kaynak grubunun aboneliğindeki ' test-adanmış-IR ' adlı tümleştirme çalışma zamanı hakkında bilgi görüntüler ve ' test-df-EU2 '.</span><span class="sxs-lookup"><span data-stu-id="e09c4-120">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="e09c4-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e09c4-121">PARAMETERS</span></span>

### <span data-ttu-id="e09c4-122">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="e09c4-122">-DataFactoryName</span></span>
<span data-ttu-id="e09c4-123">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="e09c4-123">The data factory name.</span></span>

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

### <span data-ttu-id="e09c4-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e09c4-124">-DefaultProfile</span></span>
<span data-ttu-id="e09c4-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e09c4-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e09c4-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e09c4-126">-InputObject</span></span>
<span data-ttu-id="e09c4-127">Integration Runtime nesnesi.</span><span class="sxs-lookup"><span data-stu-id="e09c4-127">The integration runtime object.</span></span>

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

### <span data-ttu-id="e09c4-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="e09c4-128">-Name</span></span>
<span data-ttu-id="e09c4-129">Tümleştirme çalışma zamanı adı.</span><span class="sxs-lookup"><span data-stu-id="e09c4-129">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e09c4-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e09c4-130">-ResourceGroupName</span></span>
<span data-ttu-id="e09c4-131">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="e09c4-131">The resource group name.</span></span>

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

### <span data-ttu-id="e09c4-132">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e09c4-132">-ResourceId</span></span>
<span data-ttu-id="e09c4-133">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="e09c4-133">The Azure resource ID.</span></span>

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

### <span data-ttu-id="e09c4-134">-Durum</span><span class="sxs-lookup"><span data-stu-id="e09c4-134">-Status</span></span>
<span data-ttu-id="e09c4-135">Tümleştirme çalışma zamanı ayrıntı durumu.</span><span class="sxs-lookup"><span data-stu-id="e09c4-135">The integration runtime detail status.</span></span>

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

### <span data-ttu-id="e09c4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e09c4-136">CommonParameters</span></span>
<span data-ttu-id="e09c4-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e09c4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e09c4-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e09c4-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e09c4-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e09c4-139">INPUTS</span></span>

### <span data-ttu-id="e09c4-140">System. String</span><span class="sxs-lookup"><span data-stu-id="e09c4-140">System.String</span></span>

### <span data-ttu-id="e09c4-141">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="e09c4-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="e09c4-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e09c4-142">OUTPUTS</span></span>

### <span data-ttu-id="e09c4-143">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="e09c4-143">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

### <span data-ttu-id="e09c4-144">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psmanagedıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="e09c4-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntime</span></span>

### <span data-ttu-id="e09c4-145">Microsoft. Azure. Commands. DataFactoryV2. modeller. PSSelfHostedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e09c4-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntime</span></span>

### <span data-ttu-id="e09c4-146">Microsoft. Azure. Commands. DataFactoryV2. modeller. PSLinkedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e09c4-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedIntegrationRuntime</span></span>

## <span data-ttu-id="e09c4-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e09c4-147">NOTES</span></span>
<span data-ttu-id="e09c4-148">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrika, kopyalama, Etkinlikler, tümleştirme çalışma zamanı</span><span class="sxs-lookup"><span data-stu-id="e09c4-148">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="e09c4-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e09c4-149">RELATED LINKS</span></span>

[<span data-ttu-id="e09c4-150">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e09c4-150">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="e09c4-151">Remove-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e09c4-151">Remove-AzDataFactoryV2IntegrationRuntime</span></span>]()
