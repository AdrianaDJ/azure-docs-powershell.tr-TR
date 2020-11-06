---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2integrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: 0f57e0ac27e47272c2b6e72a3c847d9f06a568a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592014"
---
# <span data-ttu-id="3a73b-101">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="3a73b-101">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="3a73b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a73b-102">SYNOPSIS</span></span>
<span data-ttu-id="3a73b-103">Self-hosted Integration Runtime için anahtarları alır.</span><span class="sxs-lookup"><span data-stu-id="3a73b-103">Gets keys for a self-hosted integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a73b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3a73b-104">SYNTAX</span></span>

### <span data-ttu-id="3a73b-105">Byıntegrationruntimename (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3a73b-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a73b-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="3a73b-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3a73b-107">Byıntegrationruntimeobject</span><span class="sxs-lookup"><span data-stu-id="3a73b-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a73b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="3a73b-108">DESCRIPTION</span></span>
<span data-ttu-id="3a73b-109">Tümleştirme çalışma zamanı için anahtarları alma.</span><span class="sxs-lookup"><span data-stu-id="3a73b-109">Get keys for an integration runtime.</span></span> <span data-ttu-id="3a73b-110">Anahtarlar, tümleştirme çalışma zamanı düğümünü kaydettirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="3a73b-110">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="3a73b-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3a73b-111">EXAMPLES</span></span>

### <span data-ttu-id="3a73b-112">Örnek 1: Tümleştirme çalışma zamanı anahtarlarını alma</span><span class="sxs-lookup"><span data-stu-id="3a73b-112">Example 1: Get integration runtime keys</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

AuthKey1                                                 AuthKey2
--------                                                 --------
IR@89895504-f647-48fd-8dd3-42fa556d67e3******            IR@89895504-f647-48fd-8dd3-42fa556d67e3****
```

<span data-ttu-id="3a73b-113">Cmdlet ' test-Selfhost-IR ' adlı bir tümleştirme çalışma zamanı için anahtarları alır.</span><span class="sxs-lookup"><span data-stu-id="3a73b-113">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="3a73b-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3a73b-114">PARAMETERS</span></span>

### <span data-ttu-id="3a73b-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="3a73b-115">-DataFactoryName</span></span>
<span data-ttu-id="3a73b-116">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="3a73b-116">The data factory name.</span></span>

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

### <span data-ttu-id="3a73b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a73b-117">-DefaultProfile</span></span>
<span data-ttu-id="3a73b-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3a73b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a73b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3a73b-119">-InputObject</span></span>
<span data-ttu-id="3a73b-120">Integration Runtime nesnesi.</span><span class="sxs-lookup"><span data-stu-id="3a73b-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="3a73b-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="3a73b-121">-Name</span></span>
<span data-ttu-id="3a73b-122">Tümleştirme çalışma zamanı adı.</span><span class="sxs-lookup"><span data-stu-id="3a73b-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="3a73b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a73b-123">-ResourceGroupName</span></span>
<span data-ttu-id="3a73b-124">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="3a73b-124">The resource group name.</span></span>

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

### <span data-ttu-id="3a73b-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="3a73b-125">-ResourceId</span></span>
<span data-ttu-id="3a73b-126">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="3a73b-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="3a73b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a73b-127">CommonParameters</span></span>
<span data-ttu-id="3a73b-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3a73b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a73b-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a73b-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a73b-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3a73b-130">INPUTS</span></span>

### <span data-ttu-id="3a73b-131">System. String</span><span class="sxs-lookup"><span data-stu-id="3a73b-131">System.String</span></span>

### <span data-ttu-id="3a73b-132">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="3a73b-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>
<span data-ttu-id="3a73b-133">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3a73b-133">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="3a73b-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3a73b-134">OUTPUTS</span></span>

### <span data-ttu-id="3a73b-135">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psıntegrationruntimekeys</span><span class="sxs-lookup"><span data-stu-id="3a73b-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="3a73b-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3a73b-136">NOTES</span></span>

## <span data-ttu-id="3a73b-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3a73b-137">RELATED LINKS</span></span>

[<span data-ttu-id="3a73b-138">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="3a73b-138">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>]()
