---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 83e6de07f7796e49732a35cfea4573002e6208df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592016"
---
# <span data-ttu-id="0524d-101">Get-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="0524d-101">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="0524d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0524d-102">SYNOPSIS</span></span>
<span data-ttu-id="0524d-103">Tümleştirme çalışma zamanı kaynakları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="0524d-103">Gets information about integration runtime resources.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0524d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0524d-104">SYNTAX</span></span>

### <span data-ttu-id="0524d-105">Byıntegrationruntimename (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0524d-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntime [[-Name] <String>] [-Status] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0524d-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="0524d-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntime [-Status] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0524d-107">Byıntegrationruntimeobject</span><span class="sxs-lookup"><span data-stu-id="0524d-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntime [-Status] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0524d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0524d-108">DESCRIPTION</span></span>
<span data-ttu-id="0524d-109">Get-AzureRmDataFactoryV2IntegrationRuntime cmdlet 'i Veri Fabrikası içindeki tümleştirme çalışma zamanları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="0524d-109">The Get-AzureRmDataFactoryV2IntegrationRuntime cmdlet gets information about integration runtimes in a data factory.</span></span>
<span data-ttu-id="0524d-110">Bir tümleştirme çalışma zamanının adını belirtirseniz, bu cmdlet Bu tümleştirme çalışma zamanı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="0524d-110">If you specify the name of an integration runtime, this cmdlet gets information about that integration runtime.</span></span>
<span data-ttu-id="0524d-111">Bir ad belirtmezseniz, bu cmdlet Veri Fabrikası içindeki tüm tümleştirme çalışma zamanları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="0524d-111">If you do not specify a name, this cmdlet gets information about all of the integration runtimes in a data factory.</span></span>

## <span data-ttu-id="0524d-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0524d-112">EXAMPLES</span></span>

### <span data-ttu-id="0524d-113">Örnek 1: veri fabrikasında tüm tümleştirme çalışma zamanlarını listeleme</span><span class="sxs-lookup"><span data-stu-id="0524d-113">Example 1: List all integration runtimes in a data factory</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2

    ResourceGroupName DataFactoryName Name                   Description
    ----------------- --------------- ----                   -----------
    rg-test-dfv2      test-df-eu2     test-reserved-ir       Reserved IR
    rg-test-dfv2      test-df-eu2     test-dedicated-ir      Reserved IR
    rg-test-dfv2      test-df-eu2     test-selfhost-ir       selfhost IR
```

<span data-ttu-id="0524d-114">' Test-df-EU2 ' adındaki Veri Fabrikası 'ndaki tüm tümleştirme çalışma zamanlarını listeleyin.</span><span class="sxs-lookup"><span data-stu-id="0524d-114">List all integration runtimes in the data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="0524d-115">Örnek 2: Yönetilen adanmış tümleştirme çalışma zamanını alma</span><span class="sxs-lookup"><span data-stu-id="0524d-115">Example 2: Get managed dedicated integration runtime</span></span>
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

<span data-ttu-id="0524d-116">Bu komut, ' RG-test-dfv2 ' adlı kaynak grubunun aboneliğindeki ' test-adanmış-IR ' adlı tümleştirme çalışma zamanı hakkında bilgi görüntüler ve ' test-df-EU2 '.</span><span class="sxs-lookup"><span data-stu-id="0524d-116">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="0524d-117">Örnek 3: ayrıntı durumuyla yönetilen adanmış tümleştirme çalışma zamanını alma</span><span class="sxs-lookup"><span data-stu-id="0524d-117">Example 3: Get managed dedicated integration runtime with detail status</span></span>
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

<span data-ttu-id="0524d-118">Bu komut, ' RG-test-dfv2 ' adlı kaynak grubunun aboneliğindeki ' test-adanmış-IR ' adlı tümleştirme çalışma zamanı hakkında bilgi görüntüler ve ' test-df-EU2 '.</span><span class="sxs-lookup"><span data-stu-id="0524d-118">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="0524d-119">Örnek 4: kendi kendine barındırılan tümleştirme çalışma zamanını alın</span><span class="sxs-lookup"><span data-stu-id="0524d-119">Example 4: Get self-hosted integration runtime</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-selfhost-ir

    ResourceGroupName DataFactoryName Name                 Description
    ----------------- --------------- ----                 -----------
    rg-test-dfv2      test-df-eu2     test-selfhost-ir     selfhost IR
```

<span data-ttu-id="0524d-120">Bu komut, ' RG-test-dfv2 ' adlı kaynak grubunun aboneliğindeki ' test-adanmış-IR ' adlı tümleştirme çalışma zamanı hakkında bilgi görüntüler ve ' test-df-EU2 '.</span><span class="sxs-lookup"><span data-stu-id="0524d-120">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="0524d-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0524d-121">PARAMETERS</span></span>

### <span data-ttu-id="0524d-122">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="0524d-122">-DataFactoryName</span></span>
<span data-ttu-id="0524d-123">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="0524d-123">The data factory name.</span></span>

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

### <span data-ttu-id="0524d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0524d-124">-DefaultProfile</span></span>
<span data-ttu-id="0524d-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0524d-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0524d-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0524d-126">-InputObject</span></span>
<span data-ttu-id="0524d-127">Integration Runtime nesnesi.</span><span class="sxs-lookup"><span data-stu-id="0524d-127">The integration runtime object.</span></span>

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

### <span data-ttu-id="0524d-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="0524d-128">-Name</span></span>
<span data-ttu-id="0524d-129">Tümleştirme çalışma zamanı adı.</span><span class="sxs-lookup"><span data-stu-id="0524d-129">The integration runtime name.</span></span>

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

### <span data-ttu-id="0524d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0524d-130">-ResourceGroupName</span></span>
<span data-ttu-id="0524d-131">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="0524d-131">The resource group name.</span></span>

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

### <span data-ttu-id="0524d-132">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="0524d-132">-ResourceId</span></span>
<span data-ttu-id="0524d-133">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="0524d-133">The Azure resource ID.</span></span>

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

### <span data-ttu-id="0524d-134">-Durum</span><span class="sxs-lookup"><span data-stu-id="0524d-134">-Status</span></span>
<span data-ttu-id="0524d-135">Tümleştirme çalışma zamanı ayrıntı durumu.</span><span class="sxs-lookup"><span data-stu-id="0524d-135">The integration runtime detail status.</span></span>

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

### <span data-ttu-id="0524d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0524d-136">CommonParameters</span></span>
<span data-ttu-id="0524d-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0524d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0524d-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0524d-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0524d-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0524d-139">INPUTS</span></span>

### <span data-ttu-id="0524d-140">System. String</span><span class="sxs-lookup"><span data-stu-id="0524d-140">System.String</span></span>

### <span data-ttu-id="0524d-141">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="0524d-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>
<span data-ttu-id="0524d-142">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0524d-142">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="0524d-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0524d-143">OUTPUTS</span></span>

### <span data-ttu-id="0524d-144">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="0524d-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

### <span data-ttu-id="0524d-145">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psmanagedıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="0524d-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntime</span></span>

### <span data-ttu-id="0524d-146">Microsoft. Azure. Commands. DataFactoryV2. modeller. PSSelfHostedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="0524d-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntime</span></span>

### <span data-ttu-id="0524d-147">Microsoft. Azure. Commands. DataFactoryV2. modeller. PSLinkedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="0524d-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedIntegrationRuntime</span></span>

## <span data-ttu-id="0524d-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0524d-148">NOTES</span></span>
<span data-ttu-id="0524d-149">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrika, kopyalama, Etkinlikler, tümleştirme çalışma zamanı</span><span class="sxs-lookup"><span data-stu-id="0524d-149">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="0524d-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0524d-150">RELATED LINKS</span></span>

[<span data-ttu-id="0524d-151">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="0524d-151">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="0524d-152">Remove-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="0524d-152">Remove-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
