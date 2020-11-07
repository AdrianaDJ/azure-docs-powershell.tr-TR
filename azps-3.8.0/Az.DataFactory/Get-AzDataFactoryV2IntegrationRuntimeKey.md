---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: 6cfda34b1718cfd73108362ee81fbe9c638310c7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938373"
---
# <span data-ttu-id="f291f-101">Get-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="f291f-101">Get-AzDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="f291f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f291f-102">SYNOPSIS</span></span>
<span data-ttu-id="f291f-103">Self-hosted Integration Runtime için anahtarları alır.</span><span class="sxs-lookup"><span data-stu-id="f291f-103">Gets keys for a self-hosted integration runtime.</span></span>

## <span data-ttu-id="f291f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f291f-104">SYNTAX</span></span>

### <span data-ttu-id="f291f-105">Byıntegrationruntimename (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f291f-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeKey [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f291f-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="f291f-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f291f-107">Byıntegrationruntimeobject</span><span class="sxs-lookup"><span data-stu-id="f291f-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeKey [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f291f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f291f-108">DESCRIPTION</span></span>
<span data-ttu-id="f291f-109">Tümleştirme çalışma zamanı için anahtarları alma.</span><span class="sxs-lookup"><span data-stu-id="f291f-109">Get keys for an integration runtime.</span></span> <span data-ttu-id="f291f-110">Anahtarlar, tümleştirme çalışma zamanı düğümünü kaydettirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f291f-110">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="f291f-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f291f-111">EXAMPLES</span></span>

### <span data-ttu-id="f291f-112">Örnek 1: Tümleştirme çalışma zamanı anahtarlarını alma</span><span class="sxs-lookup"><span data-stu-id="f291f-112">Example 1: Get integration runtime keys</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

AuthKey1                                                 AuthKey2
--------                                                 --------
IR@89895504-f647-48fd-8dd3-42fa556d67e3******            IR@89895504-f647-48fd-8dd3-42fa556d67e3****
```

<span data-ttu-id="f291f-113">Cmdlet ' test-Selfhost-IR ' adlı bir tümleştirme çalışma zamanı için anahtarları alır.</span><span class="sxs-lookup"><span data-stu-id="f291f-113">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="f291f-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f291f-114">PARAMETERS</span></span>

### <span data-ttu-id="f291f-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f291f-115">-DataFactoryName</span></span>
<span data-ttu-id="f291f-116">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="f291f-116">The data factory name.</span></span>

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

### <span data-ttu-id="f291f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f291f-117">-DefaultProfile</span></span>
<span data-ttu-id="f291f-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f291f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f291f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f291f-119">-InputObject</span></span>
<span data-ttu-id="f291f-120">Integration Runtime nesnesi.</span><span class="sxs-lookup"><span data-stu-id="f291f-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="f291f-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="f291f-121">-Name</span></span>
<span data-ttu-id="f291f-122">Tümleştirme çalışma zamanı adı.</span><span class="sxs-lookup"><span data-stu-id="f291f-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="f291f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f291f-123">-ResourceGroupName</span></span>
<span data-ttu-id="f291f-124">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="f291f-124">The resource group name.</span></span>

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

### <span data-ttu-id="f291f-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="f291f-125">-ResourceId</span></span>
<span data-ttu-id="f291f-126">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="f291f-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="f291f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f291f-127">CommonParameters</span></span>
<span data-ttu-id="f291f-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f291f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f291f-129">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f291f-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f291f-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f291f-130">INPUTS</span></span>

### <span data-ttu-id="f291f-131">System. String</span><span class="sxs-lookup"><span data-stu-id="f291f-131">System.String</span></span>

### <span data-ttu-id="f291f-132">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="f291f-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="f291f-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f291f-133">OUTPUTS</span></span>

### <span data-ttu-id="f291f-134">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psıntegrationruntimekeys</span><span class="sxs-lookup"><span data-stu-id="f291f-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="f291f-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f291f-135">NOTES</span></span>

## <span data-ttu-id="f291f-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f291f-136">RELATED LINKS</span></span>

[<span data-ttu-id="f291f-137">New-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="f291f-137">New-AzDataFactoryV2IntegrationRuntimeKey</span></span>]()
