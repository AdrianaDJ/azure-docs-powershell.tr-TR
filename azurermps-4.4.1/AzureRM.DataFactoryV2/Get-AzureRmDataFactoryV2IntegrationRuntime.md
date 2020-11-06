---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntime.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: ef5b99a27c547ec1e71c2339de8f4c9536549981
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594751"
---
# <span data-ttu-id="2de30-101">Get-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="2de30-101">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="2de30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2de30-102">SYNOPSIS</span></span>
<span data-ttu-id="2de30-103">Tümleştirme çalışma zamanı kaynakları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="2de30-103">Gets information about integration runtime resources.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2de30-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2de30-104">SYNTAX</span></span>

### <span data-ttu-id="2de30-105">Byıntegrationruntimename (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2de30-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntime [[-Name] <String>] [-Status] [-ResourceGroupName] <String>
 [-DataFactoryName] <String>
```

### <span data-ttu-id="2de30-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="2de30-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntime [-Status] [-ResourceId] <String>
```

### <span data-ttu-id="2de30-107">Byıntegrationruntimeobject</span><span class="sxs-lookup"><span data-stu-id="2de30-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntime [-Status] [-InputObject] <PSIntegrationRuntime>
```

## <span data-ttu-id="2de30-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="2de30-108">DESCRIPTION</span></span>
<span data-ttu-id="2de30-109">Get-AzureRmDataFactoryV2IntegrationRuntime cmdlet 'i Veri Fabrikası içindeki tümleştirme çalışma zamanları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="2de30-109">The Get-AzureRmDataFactoryV2IntegrationRuntime cmdlet gets information about integration runtimes in a data factory.</span></span>
<span data-ttu-id="2de30-110">Bir tümleştirme çalışma zamanının adını belirtirseniz, bu cmdlet Bu tümleştirme çalışma zamanı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="2de30-110">If you specify the name of an integration runtime, this cmdlet gets information about that integration runtime.</span></span>
<span data-ttu-id="2de30-111">Bir ad belirtmezseniz, bu cmdlet Veri Fabrikası içindeki tüm tümleştirme çalışma zamanları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="2de30-111">If you do not specify a name, this cmdlet gets information about all of the integration runtimes in a data factory.</span></span>

## <span data-ttu-id="2de30-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2de30-112">EXAMPLES</span></span>

### <span data-ttu-id="2de30-113">Örnek 1: veri fabrikasında tüm tümleştirme çalışma zamanlarını listeleme</span><span class="sxs-lookup"><span data-stu-id="2de30-113">Example 1: List all integration runtimes in a data factory</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2

    ResourceGroupName DataFactoryName Name                   Description
    ----------------- --------------- ----                   -----------
    rg-test-dfv2      test-df-eu2     test-reserved-ir       Reserved IR
    rg-test-dfv2      test-df-eu2     test-dedicated-ir      Reserved IR
    rg-test-dfv2      test-df-eu2     test-selfhost-ir       selfhost IR
```

<span data-ttu-id="2de30-114">' Test-df-EU2 ' adındaki Veri Fabrikası 'ndaki tüm tümleştirme çalışma zamanlarını listeleyin.</span><span class="sxs-lookup"><span data-stu-id="2de30-114">List all integration runtimes in the data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="2de30-115">Örnek 2: Yönetilen adanmış tümleştirme çalışma zamanını alma</span><span class="sxs-lookup"><span data-stu-id="2de30-115">Example 2: Get managed dedicated integration runtime</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-dedicated-ir

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

<span data-ttu-id="2de30-116">Bu komut, ' RG-test-dfv2 ' adlı kaynak grubunun aboneliğindeki ' test-adanmış-IR ' adlı tümleştirme çalışma zamanı hakkında bilgi görüntüler ve ' test-df-EU2 '.</span><span class="sxs-lookup"><span data-stu-id="2de30-116">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="2de30-117">Örnek 3: ayrıntı durumuyla yönetilen adanmış tümleştirme çalışma zamanını alma</span><span class="sxs-lookup"><span data-stu-id="2de30-117">Example 3: Get managed dedicated integration runtime with detail status</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-dedicated-ir -Status

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

<span data-ttu-id="2de30-118">Bu komut, ' RG-test-dfv2 ' adlı kaynak grubunun aboneliğindeki ' test-adanmış-IR ' adlı tümleştirme çalışma zamanı hakkında bilgi görüntüler ve ' test-df-EU2 '.</span><span class="sxs-lookup"><span data-stu-id="2de30-118">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="2de30-119">Örnek 4: kendi kendine barındırılan tümleştirme çalışma zamanını alın</span><span class="sxs-lookup"><span data-stu-id="2de30-119">Example 4: Get self-hosted integration runtime</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-selfhost-ir

    ResourceGroupName DataFactoryName Name                 Description
    ----------------- --------------- ----                 -----------
    rg-test-dfv2      test-df-eu2     test-selfhost-ir     selfhost IR
```

<span data-ttu-id="2de30-120">Bu komut, ' RG-test-dfv2 ' adlı kaynak grubunun aboneliğindeki ' test-adanmış-IR ' adlı tümleştirme çalışma zamanı hakkında bilgi görüntüler ve ' test-df-EU2 '.</span><span class="sxs-lookup"><span data-stu-id="2de30-120">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="2de30-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2de30-121">PARAMETERS</span></span>

### <span data-ttu-id="2de30-122">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="2de30-122">-DataFactoryName</span></span>
<span data-ttu-id="2de30-123">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="2de30-123">The data factory name.</span></span>

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

### <span data-ttu-id="2de30-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2de30-124">-InputObject</span></span>
<span data-ttu-id="2de30-125">Integration Runtime nesnesi.</span><span class="sxs-lookup"><span data-stu-id="2de30-125">The integration runtime object.</span></span>

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

### <span data-ttu-id="2de30-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="2de30-126">-Name</span></span>
<span data-ttu-id="2de30-127">Tümleştirme çalışma zamanı adı.</span><span class="sxs-lookup"><span data-stu-id="2de30-127">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2de30-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2de30-128">-ResourceGroupName</span></span>
<span data-ttu-id="2de30-129">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="2de30-129">The resource group name.</span></span>

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

### <span data-ttu-id="2de30-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="2de30-130">-ResourceId</span></span>
<span data-ttu-id="2de30-131">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="2de30-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="2de30-132">-Durum</span><span class="sxs-lookup"><span data-stu-id="2de30-132">-Status</span></span>
<span data-ttu-id="2de30-133">Tümleştirme çalışma zamanı ayrıntı durumu.</span><span class="sxs-lookup"><span data-stu-id="2de30-133">The integration runtime detail status.</span></span>

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

## <span data-ttu-id="2de30-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2de30-134">INPUTS</span></span>

### <span data-ttu-id="2de30-135">System. String</span><span class="sxs-lookup"><span data-stu-id="2de30-135">System.String</span></span>
<span data-ttu-id="2de30-136">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="2de30-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>


## <span data-ttu-id="2de30-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2de30-137">OUTPUTS</span></span>

### <span data-ttu-id="2de30-138">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. DataFactoryV2. modeller. Psıntegrationruntime, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="2de30-138">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="2de30-139">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psmanageınvotegrationruntime Microsoft. Azure. Commands. DataFactoryV2. modeller. PSSelfHostedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="2de30-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntime Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntime</span></span>


## <span data-ttu-id="2de30-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2de30-140">NOTES</span></span>
<span data-ttu-id="2de30-141">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrika, kopyalama, Etkinlikler, tümleştirme çalışma zamanı</span><span class="sxs-lookup"><span data-stu-id="2de30-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="2de30-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2de30-142">RELATED LINKS</span></span>
[<span data-ttu-id="2de30-143">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="2de30-143">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="2de30-144">Remove-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="2de30-144">Remove-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
