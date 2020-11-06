---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeMetric.md
ms.openlocfilehash: aba54b47a5d335bb4f6ef1fbbf7bef66fa694aaf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587982"
---
# <span data-ttu-id="c2297-101">Get-AzureRmDataFactoryV2IntegrationRuntimeMetric</span><span class="sxs-lookup"><span data-stu-id="c2297-101">Get-AzureRmDataFactoryV2IntegrationRuntimeMetric</span></span>

## <span data-ttu-id="c2297-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2297-102">SYNOPSIS</span></span>
<span data-ttu-id="c2297-103">Tümleştirme çalışma zamanı için ölçüm verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="c2297-103">Gets metric data for an integration runtime.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2297-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c2297-104">SYNTAX</span></span>

### <span data-ttu-id="c2297-105">Byıntegrationruntimename (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c2297-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2297-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="c2297-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2297-107">Byıntegrationruntimeobject</span><span class="sxs-lookup"><span data-stu-id="c2297-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeMetric [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2297-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c2297-108">DESCRIPTION</span></span>
<span data-ttu-id="c2297-109">Get-AzureRmDataFactoryV2IntegrationRuntimeMetric cmdlet 'i, veri fabrikasında Integration Runtime hakkında ölçüm verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="c2297-109">The Get-AzureRmDataFactoryV2IntegrationRuntimeMetric cmdlet gets metric data about integration runtime in a data factory.</span></span>

## <span data-ttu-id="c2297-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c2297-110">EXAMPLES</span></span>

### <span data-ttu-id="c2297-111">Örnek 1: Tümleştirme çalışma zamanı ölçüsünü alma</span><span class="sxs-lookup"><span data-stu-id="c2297-111">Example 1: Get integration runtime metric</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntimeMetric -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

IntegrationRuntimeName ResourceGroupName DataFactoryName   Nodes   
---------------------- ----------------- ---------------   -----   
test-selfhost-ir       rg-test-dfv2      test-df-eu2       {Node_1}
```

<span data-ttu-id="c2297-112">Bu komut, ' RG-test-dfv2 ' ve ' test-df-EU2 ' adlı veri fabrikası için abonelikteki ' test-Selfhost-IR ' adlı tümleştirme çalışma zamanı hakkında ölçüm verilerini görüntüler.</span><span class="sxs-lookup"><span data-stu-id="c2297-112">This command displays metric data about the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="c2297-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c2297-113">PARAMETERS</span></span>

### <span data-ttu-id="c2297-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="c2297-114">-DataFactoryName</span></span>
<span data-ttu-id="c2297-115">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="c2297-115">The data factory name.</span></span>

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

### <span data-ttu-id="c2297-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c2297-116">-InputObject</span></span>
<span data-ttu-id="c2297-117">Integration Runtime nesnesi.</span><span class="sxs-lookup"><span data-stu-id="c2297-117">The integration runtime object.</span></span>

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

### <span data-ttu-id="c2297-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="c2297-118">-Name</span></span>
<span data-ttu-id="c2297-119">Tümleştirme çalışma zamanı adı.</span><span class="sxs-lookup"><span data-stu-id="c2297-119">The integration runtime name.</span></span>

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

### <span data-ttu-id="c2297-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2297-120">-ResourceGroupName</span></span>
<span data-ttu-id="c2297-121">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="c2297-121">The resource group name.</span></span>

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

### <span data-ttu-id="c2297-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="c2297-122">-ResourceId</span></span>
<span data-ttu-id="c2297-123">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="c2297-123">The Azure resource ID.</span></span>

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

### <span data-ttu-id="c2297-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2297-124">-DefaultProfile</span></span>
<span data-ttu-id="c2297-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c2297-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2297-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2297-126">CommonParameters</span></span>
<span data-ttu-id="c2297-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c2297-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2297-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2297-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2297-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c2297-129">INPUTS</span></span>

### <span data-ttu-id="c2297-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c2297-130">System.String</span></span>
<span data-ttu-id="c2297-131">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="c2297-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="c2297-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c2297-132">OUTPUTS</span></span>

### <span data-ttu-id="c2297-133">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psıntegrationruntimeölçüler</span><span class="sxs-lookup"><span data-stu-id="c2297-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeMetrics</span></span>

## <span data-ttu-id="c2297-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c2297-134">NOTES</span></span>

## <span data-ttu-id="c2297-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c2297-135">RELATED LINKS</span></span>

[<span data-ttu-id="c2297-136">Get-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="c2297-136">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

