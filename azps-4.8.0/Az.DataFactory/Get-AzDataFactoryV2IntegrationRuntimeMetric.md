---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntimemetric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeMetric.md
ms.openlocfilehash: 9b82d302bba1c2f51de3748fb9c335dd0db2699d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268006"
---
# <span data-ttu-id="17155-101">Get-AzDataFactoryV2IntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="17155-101">Get-AzDataFactoryV2IntegrationRuntimeMetric</span></span>

## <span data-ttu-id="17155-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17155-102">SYNOPSIS</span></span>
<span data-ttu-id="17155-103">Tümleştirme çalışma zamanı için ölçüm verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="17155-103">Gets metric data for an integration runtime.</span></span> 

## <span data-ttu-id="17155-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="17155-104">SYNTAX</span></span>

### <span data-ttu-id="17155-105">Byıntegrationruntimename (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="17155-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeMetric [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17155-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="17155-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeMetric [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="17155-107">Byıntegrationruntimeobject</span><span class="sxs-lookup"><span data-stu-id="17155-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeMetric [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17155-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="17155-108">DESCRIPTION</span></span>
<span data-ttu-id="17155-109">Get-AzDataFactoryV2IntegrationRuntimeMetric cmdlet 'i, veri fabrikasında Integration Runtime hakkında ölçüm verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="17155-109">The Get-AzDataFactoryV2IntegrationRuntimeMetric cmdlet gets metric data about integration runtime in a data factory.</span></span>

## <span data-ttu-id="17155-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="17155-110">EXAMPLES</span></span>

### <span data-ttu-id="17155-111">Örnek 1: Tümleştirme çalışma zamanı ölçüsünü alma</span><span class="sxs-lookup"><span data-stu-id="17155-111">Example 1: Get integration runtime metric</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntimeMetric -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

IntegrationRuntimeName ResourceGroupName DataFactoryName   Nodes   
---------------------- ----------------- ---------------   -----   
test-selfhost-ir       rg-test-dfv2      test-df-eu2       {Node_1}
```

<span data-ttu-id="17155-112">Bu komut, ' RG-test-dfv2 ' ve ' test-df-EU2 ' adlı veri fabrikası için abonelikteki ' test-Selfhost-IR ' adlı tümleştirme çalışma zamanı hakkında ölçüm verilerini görüntüler.</span><span class="sxs-lookup"><span data-stu-id="17155-112">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="17155-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="17155-113">PARAMETERS</span></span>

### <span data-ttu-id="17155-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="17155-114">-DataFactoryName</span></span>
<span data-ttu-id="17155-115">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="17155-115">The data factory name.</span></span>

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

### <span data-ttu-id="17155-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17155-116">-DefaultProfile</span></span>
<span data-ttu-id="17155-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="17155-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17155-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="17155-118">-InputObject</span></span>
<span data-ttu-id="17155-119">Integration Runtime nesnesi.</span><span class="sxs-lookup"><span data-stu-id="17155-119">The integration runtime object.</span></span>

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

### <span data-ttu-id="17155-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="17155-120">-Name</span></span>
<span data-ttu-id="17155-121">Tümleştirme çalışma zamanı adı.</span><span class="sxs-lookup"><span data-stu-id="17155-121">The integration runtime name.</span></span>

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

### <span data-ttu-id="17155-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17155-122">-ResourceGroupName</span></span>
<span data-ttu-id="17155-123">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="17155-123">The resource group name.</span></span>

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

### <span data-ttu-id="17155-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="17155-124">-ResourceId</span></span>
<span data-ttu-id="17155-125">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="17155-125">The Azure resource ID.</span></span>

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

### <span data-ttu-id="17155-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17155-126">CommonParameters</span></span>
<span data-ttu-id="17155-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="17155-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17155-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17155-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17155-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="17155-129">INPUTS</span></span>

### <span data-ttu-id="17155-130">System. String</span><span class="sxs-lookup"><span data-stu-id="17155-130">System.String</span></span>

### <span data-ttu-id="17155-131">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="17155-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="17155-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="17155-132">OUTPUTS</span></span>

### <span data-ttu-id="17155-133">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psıntegrationruntimeölçüler</span><span class="sxs-lookup"><span data-stu-id="17155-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeMetrics</span></span>

## <span data-ttu-id="17155-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="17155-134">NOTES</span></span>

## <span data-ttu-id="17155-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="17155-135">RELATED LINKS</span></span>

[<span data-ttu-id="17155-136">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="17155-136">Get-AzDataFactoryV2IntegrationRuntime</span></span>]()

