---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: 636ba1466eb0c5c0e8fda0433c74ec2291d2db9b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752465"
---
# <span data-ttu-id="7faaf-101">Remove-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="7faaf-101">Remove-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="7faaf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7faaf-102">SYNOPSIS</span></span>
<span data-ttu-id="7faaf-103">Veri Fabrikası 'nden bir ardışık düzeni kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7faaf-103">Removes a pipeline from Data Factory.</span></span>

## <span data-ttu-id="7faaf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7faaf-104">SYNTAX</span></span>

### <span data-ttu-id="7faaf-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7faaf-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2Pipeline [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7faaf-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7faaf-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2Pipeline [-InputObject] <PSPipeline> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7faaf-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="7faaf-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2Pipeline [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7faaf-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="7faaf-108">DESCRIPTION</span></span>
<span data-ttu-id="7faaf-109">Remove-AzDataFactoryV2Pipeline cmdlet 'i Azure Veri Fabrikası 'ndan ardışık düzeni kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7faaf-109">The Remove-AzDataFactoryV2Pipeline cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="7faaf-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7faaf-110">EXAMPLES</span></span>

### <span data-ttu-id="7faaf-111">Örnek 1: ardışık düzeni kaldırma</span><span class="sxs-lookup"><span data-stu-id="7faaf-111">Example 1: Remove a pipeline</span></span>
```
PS C:\> Remove-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
          Confirm
          Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="7faaf-112">Bu cmdlet, WikiADF adlı veri fabrikası</span><span class="sxs-lookup"><span data-stu-id="7faaf-112">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="7faaf-113">Komut bir $True değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="7faaf-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="7faaf-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7faaf-114">PARAMETERS</span></span>

### <span data-ttu-id="7faaf-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="7faaf-115">-DataFactoryName</span></span>
<span data-ttu-id="7faaf-116">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7faaf-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="7faaf-117">Bu cmdlet, bu parametrenin belirttiği veri fabrikası için bir ardışık düzeni kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7faaf-117">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7faaf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7faaf-118">-DefaultProfile</span></span>
<span data-ttu-id="7faaf-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7faaf-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7faaf-120">-Force</span><span class="sxs-lookup"><span data-stu-id="7faaf-120">-Force</span></span>
<span data-ttu-id="7faaf-121">Onay istemeden cmdlet 'i çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="7faaf-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="7faaf-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7faaf-122">-InputObject</span></span>
<span data-ttu-id="7faaf-123">Potansiyel satış nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7faaf-123">Specifies a Pipeline object.</span></span>
<span data-ttu-id="7faaf-124">Bu cmdlet, bu parametrenin belirttiği ardışık düzeni kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7faaf-124">This cmdlet removes the pipeline that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7faaf-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="7faaf-125">-Name</span></span>
<span data-ttu-id="7faaf-126">Kaldırılacak ardışık düzenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7faaf-126">Specifies the name of the pipeline to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: PipelineName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7faaf-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7faaf-127">-ResourceGroupName</span></span>
<span data-ttu-id="7faaf-128">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7faaf-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="7faaf-129">Bu cmdlet, bu parametrenin belirttiği gruptan bir ardışık düzeni kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7faaf-129">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7faaf-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="7faaf-130">-ResourceId</span></span>
<span data-ttu-id="7faaf-131">Kaldırılacak ardışık düzenin Azure Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="7faaf-131">The Azure resource ID of the pipeline to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7faaf-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="7faaf-132">-Confirm</span></span>
<span data-ttu-id="7faaf-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7faaf-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7faaf-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7faaf-134">-WhatIf</span></span>
<span data-ttu-id="7faaf-135">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="7faaf-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="7faaf-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7faaf-136">CommonParameters</span></span>
<span data-ttu-id="7faaf-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7faaf-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7faaf-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7faaf-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7faaf-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7faaf-139">INPUTS</span></span>

### <span data-ttu-id="7faaf-140">Microsoft. Azure. Commands. DataFactoryV2. modeller. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="7faaf-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

### <span data-ttu-id="7faaf-141">System. String</span><span class="sxs-lookup"><span data-stu-id="7faaf-141">System.String</span></span>

## <span data-ttu-id="7faaf-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7faaf-142">OUTPUTS</span></span>

### <span data-ttu-id="7faaf-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7faaf-143">System.Boolean</span></span>

## <span data-ttu-id="7faaf-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7faaf-144">NOTES</span></span>
<span data-ttu-id="7faaf-145">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="7faaf-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="7faaf-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7faaf-146">RELATED LINKS</span></span>

[<span data-ttu-id="7faaf-147">Get-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="7faaf-147">Get-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="7faaf-148">Set-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="7faaf-148">Set-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="7faaf-149">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="7faaf-149">Invoke-AzDataFactoryV2Pipeline</span></span>]()

