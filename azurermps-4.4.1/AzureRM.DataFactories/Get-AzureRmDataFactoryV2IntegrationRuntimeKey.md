---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: 7bab6fb42e5d50cc0ede06a42540cf628a5ee4a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593821"
---
# <span data-ttu-id="3b53a-101">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="3b53a-101">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="3b53a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b53a-102">SYNOPSIS</span></span>
<span data-ttu-id="3b53a-103">Self-hosted Integration Runtime için anahtarları alır.</span><span class="sxs-lookup"><span data-stu-id="3b53a-103">Gets keys for a self-hosted integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b53a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3b53a-104">SYNTAX</span></span>

### <span data-ttu-id="3b53a-105">Byıntegrationruntimename (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3b53a-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3b53a-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="3b53a-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3b53a-107">Byıntegrationruntimeobject</span><span class="sxs-lookup"><span data-stu-id="3b53a-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b53a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="3b53a-108">DESCRIPTION</span></span>
<span data-ttu-id="3b53a-109">Tümleştirme çalışma zamanı için anahtarları alma.</span><span class="sxs-lookup"><span data-stu-id="3b53a-109">Get keys for an integration runtime.</span></span> <span data-ttu-id="3b53a-110">Anahtarlar, tümleştirme çalışma zamanı düğümünü kaydettirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="3b53a-110">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="3b53a-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3b53a-111">EXAMPLES</span></span>

### <span data-ttu-id="3b53a-112">Örnek 1: Tümleştirme çalışma zamanı anahtarlarını alma</span><span class="sxs-lookup"><span data-stu-id="3b53a-112">Example 1: Get integration runtime keys</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

AuthKey1                                                 AuthKey2
--------                                                 --------
IR@89895504-f647-48fd-8dd3-42fa556d67e3******            IR@89895504-f647-48fd-8dd3-42fa556d67e3****
```

<span data-ttu-id="3b53a-113">Cmdlet ' test-Selfhost-IR ' adlı bir tümleştirme çalışma zamanı için anahtarları alır.</span><span class="sxs-lookup"><span data-stu-id="3b53a-113">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="3b53a-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3b53a-114">PARAMETERS</span></span>

### <span data-ttu-id="3b53a-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="3b53a-115">-DataFactoryName</span></span>
<span data-ttu-id="3b53a-116">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="3b53a-116">The data factory name.</span></span>

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

### <span data-ttu-id="3b53a-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3b53a-117">-InputObject</span></span>
<span data-ttu-id="3b53a-118">Integration Runtime nesnesi.</span><span class="sxs-lookup"><span data-stu-id="3b53a-118">The integration runtime object.</span></span>

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

### <span data-ttu-id="3b53a-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="3b53a-119">-Name</span></span>
<span data-ttu-id="3b53a-120">Tümleştirme çalışma zamanı adı.</span><span class="sxs-lookup"><span data-stu-id="3b53a-120">The integration runtime name.</span></span>

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

### <span data-ttu-id="3b53a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b53a-121">-ResourceGroupName</span></span>
<span data-ttu-id="3b53a-122">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="3b53a-122">The resource group name.</span></span>

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

### <span data-ttu-id="3b53a-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="3b53a-123">-ResourceId</span></span>
<span data-ttu-id="3b53a-124">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="3b53a-124">The Azure resource ID.</span></span>

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

### <span data-ttu-id="3b53a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b53a-125">-DefaultProfile</span></span>
<span data-ttu-id="3b53a-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3b53a-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b53a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b53a-127">CommonParameters</span></span>
<span data-ttu-id="3b53a-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3b53a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b53a-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b53a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b53a-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3b53a-130">INPUTS</span></span>

### <span data-ttu-id="3b53a-131">System. String</span><span class="sxs-lookup"><span data-stu-id="3b53a-131">System.String</span></span>
<span data-ttu-id="3b53a-132">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="3b53a-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span> 

## <span data-ttu-id="3b53a-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3b53a-133">OUTPUTS</span></span>

### <span data-ttu-id="3b53a-134">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psıntegrationruntimekeys</span><span class="sxs-lookup"><span data-stu-id="3b53a-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="3b53a-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3b53a-135">NOTES</span></span>

## <span data-ttu-id="3b53a-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3b53a-136">RELATED LINKS</span></span>

[<span data-ttu-id="3b53a-137">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="3b53a-137">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>]()
