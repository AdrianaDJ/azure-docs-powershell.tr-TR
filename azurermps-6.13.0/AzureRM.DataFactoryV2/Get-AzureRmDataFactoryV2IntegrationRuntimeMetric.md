---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2integrationruntimemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeMetric.md
ms.openlocfilehash: 07c5b03b3d5717115238e3cd66b9f80925b51537
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592015"
---
# <span data-ttu-id="b7d07-101">Get-AzureRmDataFactoryV2IntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="b7d07-101">Get-AzureRmDataFactoryV2IntegrationRuntimeMetric</span></span>

## <span data-ttu-id="b7d07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7d07-102">SYNOPSIS</span></span>
<span data-ttu-id="b7d07-103">Tümleştirme çalışma zamanı için ölçüm verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="b7d07-103">Gets metric data for an integration runtime.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7d07-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b7d07-104">SYNTAX</span></span>

### <span data-ttu-id="b7d07-105">Byıntegrationruntimename (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b7d07-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7d07-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="b7d07-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7d07-107">Byıntegrationruntimeobject</span><span class="sxs-lookup"><span data-stu-id="b7d07-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7d07-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="b7d07-108">DESCRIPTION</span></span>
<span data-ttu-id="b7d07-109">Get-AzureRmDataFactoryV2IntegrationRuntimeMetric cmdlet 'i, veri fabrikasında Integration Runtime hakkında ölçüm verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="b7d07-109">The Get-AzureRmDataFactoryV2IntegrationRuntimeMetric cmdlet gets metric data about integration runtime in a data factory.</span></span>

## <span data-ttu-id="b7d07-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b7d07-110">EXAMPLES</span></span>

### <span data-ttu-id="b7d07-111">Örnek 1: Tümleştirme çalışma zamanı ölçüsünü alma</span><span class="sxs-lookup"><span data-stu-id="b7d07-111">Example 1: Get integration runtime metric</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntimeMetric -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

IntegrationRuntimeName ResourceGroupName DataFactoryName   Nodes   
---------------------- ----------------- ---------------   -----   
test-selfhost-ir       rg-test-dfv2      test-df-eu2       {Node_1}
```

<span data-ttu-id="b7d07-112">Bu komut, ' RG-test-dfv2 ' ve ' test-df-EU2 ' adlı veri fabrikası için abonelikteki ' test-Selfhost-IR ' adlı tümleştirme çalışma zamanı hakkında ölçüm verilerini görüntüler.</span><span class="sxs-lookup"><span data-stu-id="b7d07-112">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="b7d07-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b7d07-113">PARAMETERS</span></span>

### <span data-ttu-id="b7d07-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="b7d07-114">-DataFactoryName</span></span>
<span data-ttu-id="b7d07-115">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="b7d07-115">The data factory name.</span></span>

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

### <span data-ttu-id="b7d07-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7d07-116">-DefaultProfile</span></span>
<span data-ttu-id="b7d07-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b7d07-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7d07-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b7d07-118">-InputObject</span></span>
<span data-ttu-id="b7d07-119">Integration Runtime nesnesi.</span><span class="sxs-lookup"><span data-stu-id="b7d07-119">The integration runtime object.</span></span>

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

### <span data-ttu-id="b7d07-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="b7d07-120">-Name</span></span>
<span data-ttu-id="b7d07-121">Tümleştirme çalışma zamanı adı.</span><span class="sxs-lookup"><span data-stu-id="b7d07-121">The integration runtime name.</span></span>

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

### <span data-ttu-id="b7d07-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7d07-122">-ResourceGroupName</span></span>
<span data-ttu-id="b7d07-123">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="b7d07-123">The resource group name.</span></span>

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

### <span data-ttu-id="b7d07-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b7d07-124">-ResourceId</span></span>
<span data-ttu-id="b7d07-125">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="b7d07-125">The Azure resource ID.</span></span>

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

### <span data-ttu-id="b7d07-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7d07-126">CommonParameters</span></span>
<span data-ttu-id="b7d07-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b7d07-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7d07-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7d07-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7d07-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b7d07-129">INPUTS</span></span>

### <span data-ttu-id="b7d07-130">System. String</span><span class="sxs-lookup"><span data-stu-id="b7d07-130">System.String</span></span>

### <span data-ttu-id="b7d07-131">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="b7d07-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>
<span data-ttu-id="b7d07-132">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b7d07-132">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="b7d07-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b7d07-133">OUTPUTS</span></span>

### <span data-ttu-id="b7d07-134">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psıntegrationruntimeölçüler</span><span class="sxs-lookup"><span data-stu-id="b7d07-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeMetrics</span></span>

## <span data-ttu-id="b7d07-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b7d07-135">NOTES</span></span>

## <span data-ttu-id="b7d07-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b7d07-136">RELATED LINKS</span></span>

[<span data-ttu-id="b7d07-137">Get-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="b7d07-137">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

