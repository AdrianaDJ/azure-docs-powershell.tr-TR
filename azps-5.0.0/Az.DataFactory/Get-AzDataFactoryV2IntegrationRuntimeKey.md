---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: 6cfda34b1718cfd73108362ee81fbe9c638310c7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321014"
---
# <span data-ttu-id="54a7c-101">Get-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="54a7c-101">Get-AzDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="54a7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54a7c-102">SYNOPSIS</span></span>
<span data-ttu-id="54a7c-103">Self-hosted Integration Runtime için anahtarları alır.</span><span class="sxs-lookup"><span data-stu-id="54a7c-103">Gets keys for a self-hosted integration runtime.</span></span>

## <span data-ttu-id="54a7c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="54a7c-104">SYNTAX</span></span>

### <span data-ttu-id="54a7c-105">Byıntegrationruntimename (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="54a7c-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeKey [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54a7c-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="54a7c-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="54a7c-107">Byıntegrationruntimeobject</span><span class="sxs-lookup"><span data-stu-id="54a7c-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeKey [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54a7c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="54a7c-108">DESCRIPTION</span></span>
<span data-ttu-id="54a7c-109">Tümleştirme çalışma zamanı için anahtarları alma.</span><span class="sxs-lookup"><span data-stu-id="54a7c-109">Get keys for an integration runtime.</span></span> <span data-ttu-id="54a7c-110">Anahtarlar, tümleştirme çalışma zamanı düğümünü kaydettirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="54a7c-110">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="54a7c-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="54a7c-111">EXAMPLES</span></span>

### <span data-ttu-id="54a7c-112">Örnek 1: Tümleştirme çalışma zamanı anahtarlarını alma</span><span class="sxs-lookup"><span data-stu-id="54a7c-112">Example 1: Get integration runtime keys</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

AuthKey1                                                 AuthKey2
--------                                                 --------
IR@89895504-f647-48fd-8dd3-42fa556d67e3******            IR@89895504-f647-48fd-8dd3-42fa556d67e3****
```

<span data-ttu-id="54a7c-113">Cmdlet ' test-Selfhost-IR ' adlı bir tümleştirme çalışma zamanı için anahtarları alır.</span><span class="sxs-lookup"><span data-stu-id="54a7c-113">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="54a7c-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="54a7c-114">PARAMETERS</span></span>

### <span data-ttu-id="54a7c-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="54a7c-115">-DataFactoryName</span></span>
<span data-ttu-id="54a7c-116">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="54a7c-116">The data factory name.</span></span>

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

### <span data-ttu-id="54a7c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54a7c-117">-DefaultProfile</span></span>
<span data-ttu-id="54a7c-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="54a7c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54a7c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="54a7c-119">-InputObject</span></span>
<span data-ttu-id="54a7c-120">Integration Runtime nesnesi.</span><span class="sxs-lookup"><span data-stu-id="54a7c-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="54a7c-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="54a7c-121">-Name</span></span>
<span data-ttu-id="54a7c-122">Tümleştirme çalışma zamanı adı.</span><span class="sxs-lookup"><span data-stu-id="54a7c-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="54a7c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54a7c-123">-ResourceGroupName</span></span>
<span data-ttu-id="54a7c-124">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="54a7c-124">The resource group name.</span></span>

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

### <span data-ttu-id="54a7c-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="54a7c-125">-ResourceId</span></span>
<span data-ttu-id="54a7c-126">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="54a7c-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="54a7c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54a7c-127">CommonParameters</span></span>
<span data-ttu-id="54a7c-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="54a7c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54a7c-129">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54a7c-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54a7c-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="54a7c-130">INPUTS</span></span>

### <span data-ttu-id="54a7c-131">System. String</span><span class="sxs-lookup"><span data-stu-id="54a7c-131">System.String</span></span>

### <span data-ttu-id="54a7c-132">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="54a7c-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="54a7c-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="54a7c-133">OUTPUTS</span></span>

### <span data-ttu-id="54a7c-134">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psıntegrationruntimekeys</span><span class="sxs-lookup"><span data-stu-id="54a7c-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="54a7c-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="54a7c-135">NOTES</span></span>

## <span data-ttu-id="54a7c-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="54a7c-136">RELATED LINKS</span></span>

[<span data-ttu-id="54a7c-137">New-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="54a7c-137">New-AzDataFactoryV2IntegrationRuntimeKey</span></span>]()
