---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 0c24f77b51bcfc50ec11e211fc7f11b60e348221
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938317"
---
# <span data-ttu-id="d4712-101">Remove-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="d4712-101">Remove-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="d4712-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4712-102">SYNOPSIS</span></span>
<span data-ttu-id="d4712-103">Tümleştirme çalışma zamanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d4712-103">Removes an integration runtime.</span></span>

## <span data-ttu-id="d4712-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d4712-104">SYNTAX</span></span>

### <span data-ttu-id="d4712-105">Byıntegrationruntimename (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d4712-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force] [-Name] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4712-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="d4712-106">ByResourceId</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4712-107">Byıntegrationruntimeobject</span><span class="sxs-lookup"><span data-stu-id="d4712-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force]
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d4712-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d4712-108">DESCRIPTION</span></span>
<span data-ttu-id="d4712-109">Remove-AzDataFactoryV2IntegrationRuntime cmdlet 'i Integration Runtime 'yi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d4712-109">The Remove-AzDataFactoryV2IntegrationRuntime cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="d4712-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d4712-110">EXAMPLES</span></span>

### <span data-ttu-id="d4712-111">Örnek 1: Tümleştirme çalışma zamanını kaldırma</span><span class="sxs-lookup"><span data-stu-id="d4712-111">Example 1: Remove a integration runtime</span></span>
```
PS C:\> Remove-AzDataFactoryV2IntegrationRuntime  -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="d4712-112">Bu komut, ' test-ayrılmış-IR ' adlı tümleştirme çalışma zamanını ' test-df ' adındaki Veri Fabrikası 'ndan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d4712-112">This command removes the integration runtime named 'test-reserved-ir' from the data factory named 'test-df'.</span></span>
<span data-ttu-id="d4712-113">Bu komut $True değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="d4712-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="d4712-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d4712-114">PARAMETERS</span></span>

### <span data-ttu-id="d4712-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d4712-115">-DataFactoryName</span></span>
<span data-ttu-id="d4712-116">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="d4712-116">The data factory name.</span></span>

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

### <span data-ttu-id="d4712-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4712-117">-DefaultProfile</span></span>
<span data-ttu-id="d4712-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d4712-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4712-119">-Force</span><span class="sxs-lookup"><span data-stu-id="d4712-119">-Force</span></span>
<span data-ttu-id="d4712-120">Onay istemeden cmdlet 'i çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="d4712-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="d4712-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d4712-121">-InputObject</span></span>
<span data-ttu-id="d4712-122">Integration Runtime nesnesi.</span><span class="sxs-lookup"><span data-stu-id="d4712-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="d4712-123">-LinkedDataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d4712-123">-LinkedDataFactoryName</span></span>
<span data-ttu-id="d4712-124">Bağlı veri fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="d4712-124">The linked data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4712-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="d4712-125">-Name</span></span>
<span data-ttu-id="d4712-126">Tümleştirme çalışma zamanı adı.</span><span class="sxs-lookup"><span data-stu-id="d4712-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="d4712-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4712-127">-ResourceGroupName</span></span>
<span data-ttu-id="d4712-128">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="d4712-128">The resource group name.</span></span>

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

### <span data-ttu-id="d4712-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d4712-129">-ResourceId</span></span>
<span data-ttu-id="d4712-130">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="d4712-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="d4712-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="d4712-131">-Confirm</span></span>
<span data-ttu-id="d4712-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d4712-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4712-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4712-133">-WhatIf</span></span>
<span data-ttu-id="d4712-134">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="d4712-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="d4712-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4712-135">CommonParameters</span></span>
<span data-ttu-id="d4712-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d4712-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4712-137">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4712-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4712-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d4712-138">INPUTS</span></span>

### <span data-ttu-id="d4712-139">System. String</span><span class="sxs-lookup"><span data-stu-id="d4712-139">System.String</span></span>

### <span data-ttu-id="d4712-140">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="d4712-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="d4712-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d4712-141">OUTPUTS</span></span>

### <span data-ttu-id="d4712-142">System. void</span><span class="sxs-lookup"><span data-stu-id="d4712-142">System.Void</span></span>

## <span data-ttu-id="d4712-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d4712-143">NOTES</span></span>
<span data-ttu-id="d4712-144">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrika, kopyalama, Etkinlikler, tümleştirme çalışma zamanı</span><span class="sxs-lookup"><span data-stu-id="d4712-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="d4712-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d4712-145">RELATED LINKS</span></span>

[<span data-ttu-id="d4712-146">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="d4712-146">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="d4712-147">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="d4712-147">Get-AzDataFactoryV2IntegrationRuntime</span></span>]()
