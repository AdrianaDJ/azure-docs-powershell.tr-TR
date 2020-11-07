---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactoryv2integrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: 8571e210a39bc1d617b391eb4cf71aa45a34d69c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752497"
---
# <span data-ttu-id="13212-101">New-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="13212-101">New-AzDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="13212-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13212-102">SYNOPSIS</span></span>
<span data-ttu-id="13212-103">Self-hosted Integration Runtime anahtarını yeniden oluşturun.</span><span class="sxs-lookup"><span data-stu-id="13212-103">Regenerate self-hosted integration runtime key.</span></span>

## <span data-ttu-id="13212-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="13212-104">SYNTAX</span></span>

### <span data-ttu-id="13212-105">Byıntegrationruntimename (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="13212-105">ByIntegrationRuntimeName (Default)</span></span>
```
New-AzDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-Name] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13212-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="13212-106">ByResourceId</span></span>
```
New-AzDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13212-107">Byıntegrationruntimeobject</span><span class="sxs-lookup"><span data-stu-id="13212-107">ByIntegrationRuntimeObject</span></span>
```
New-AzDataFactoryV2IntegrationRuntimeKey -KeyName <String> [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13212-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="13212-108">DESCRIPTION</span></span>
<span data-ttu-id="13212-109">**New-AzDataFactoryV2IntegrationRuntimeKey** cmdlet 'ı ' KeyName ' parametresiyle belirtilen anahtar adıyla tümleştirme çalışma zamanı anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="13212-109">The cmdlet **New-AzDataFactoryV2IntegrationRuntimeKey** regenerates the integration runtime key with the key name specified by 'KeyName' parameter.</span></span> <span data-ttu-id="13212-110">Önceki anahtar geçersiz olur.</span><span class="sxs-lookup"><span data-stu-id="13212-110">The previous key will is invalid.</span></span>

## <span data-ttu-id="13212-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="13212-111">EXAMPLES</span></span>

### <span data-ttu-id="13212-112">Örnek 1: Tümleştirme çalışma zamanı için yeni anahtar oluşturma</span><span class="sxs-lookup"><span data-stu-id="13212-112">Example 1: Generate a new key for an integration runtime</span></span>
```
PS C:\> New-AzDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' -KeyName authKey2

AuthKey1 AuthKey2
-------- --------
         IR@89895504-f647-48fd-8dd3-42fa556d67e3@***
```

<span data-ttu-id="13212-113">' Test-Selfhost-IR ' adlı tümleştirme çalışma zamanı için cmdlet ' authKey2 ' anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="13212-113">The cmdlet regenerates key 'authKey2' for integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="13212-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="13212-114">PARAMETERS</span></span>

### <span data-ttu-id="13212-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="13212-115">-DataFactoryName</span></span>
<span data-ttu-id="13212-116">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="13212-116">The data factory name.</span></span>

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

### <span data-ttu-id="13212-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13212-117">-DefaultProfile</span></span>
<span data-ttu-id="13212-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="13212-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13212-119">-Force</span><span class="sxs-lookup"><span data-stu-id="13212-119">-Force</span></span>
<span data-ttu-id="13212-120">Onay istemeden cmdlet 'i çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="13212-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="13212-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="13212-121">-InputObject</span></span>
<span data-ttu-id="13212-122">Integration Runtime nesnesi.</span><span class="sxs-lookup"><span data-stu-id="13212-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="13212-123">-AnahtarAdı</span><span class="sxs-lookup"><span data-stu-id="13212-123">-KeyName</span></span>
<span data-ttu-id="13212-124">Self-hosted Integration Runtime 'ın kimlik doğrulama anahtarı adı.</span><span class="sxs-lookup"><span data-stu-id="13212-124">The authentication key name of the self-hosted integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AuthKey1, AuthKey2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13212-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="13212-125">-Name</span></span>
<span data-ttu-id="13212-126">Tümleştirme çalışma zamanı adı.</span><span class="sxs-lookup"><span data-stu-id="13212-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="13212-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13212-127">-ResourceGroupName</span></span>
<span data-ttu-id="13212-128">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="13212-128">The resource group name.</span></span>

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

### <span data-ttu-id="13212-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="13212-129">-ResourceId</span></span>
<span data-ttu-id="13212-130">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="13212-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="13212-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="13212-131">-Confirm</span></span>
<span data-ttu-id="13212-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="13212-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13212-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13212-133">-WhatIf</span></span>
<span data-ttu-id="13212-134">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="13212-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13212-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13212-135">CommonParameters</span></span>
<span data-ttu-id="13212-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="13212-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13212-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13212-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13212-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="13212-138">INPUTS</span></span>

### <span data-ttu-id="13212-139">System. String</span><span class="sxs-lookup"><span data-stu-id="13212-139">System.String</span></span>

### <span data-ttu-id="13212-140">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="13212-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="13212-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="13212-141">OUTPUTS</span></span>

### <span data-ttu-id="13212-142">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psıntegrationruntimekeys</span><span class="sxs-lookup"><span data-stu-id="13212-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="13212-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="13212-143">NOTES</span></span>

## <span data-ttu-id="13212-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="13212-144">RELATED LINKS</span></span>

[<span data-ttu-id="13212-145">Get-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="13212-145">Get-AzDataFactoryV2IntegrationRuntimeKey</span></span>]()
