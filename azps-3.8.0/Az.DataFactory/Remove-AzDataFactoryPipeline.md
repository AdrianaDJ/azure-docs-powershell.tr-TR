---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: E1E0919A-062B-4794-ADE7-E17133A40604
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryPipeline.md
ms.openlocfilehash: 2bae0bd597cbd97a81efeaecb07e052457b88438
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94095959"
---
# <span data-ttu-id="8ecec-101">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="8ecec-101">Remove-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="8ecec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ecec-102">SYNOPSIS</span></span>
<span data-ttu-id="8ecec-103">Bir ardışık düzeni Azure Veri Fabrikası 'nden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8ecec-103">Removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="8ecec-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8ecec-104">SYNTAX</span></span>

### <span data-ttu-id="8ecec-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8ecec-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryPipeline [-Force] [-Name] <String> [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8ecec-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="8ecec-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryPipeline [-Force] [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ecec-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="8ecec-107">DESCRIPTION</span></span>
<span data-ttu-id="8ecec-108">**Remove-AzDataFactoryPipeline** cmdlet 'ı Azure Veri Fabrikası 'ndan ardışık düzeni kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8ecec-108">The **Remove-AzDataFactoryPipeline** cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="8ecec-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8ecec-109">EXAMPLES</span></span>

### <span data-ttu-id="8ecec-110">Örnek 1: ardışık düzeni kaldırma</span><span class="sxs-lookup"><span data-stu-id="8ecec-110">Example 1: Remove a pipeline</span></span>
```
PS C:\>Remove-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="8ecec-111">Bu cmdlet, WikiADF adlı veri fabrikası</span><span class="sxs-lookup"><span data-stu-id="8ecec-111">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="8ecec-112">Komut bir $True değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="8ecec-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="8ecec-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8ecec-113">PARAMETERS</span></span>

### <span data-ttu-id="8ecec-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="8ecec-114">-DataFactory</span></span>
<span data-ttu-id="8ecec-115">**Psdatafactory** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ecec-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="8ecec-116">Bu cmdlet, bu parametrenin belirttiği veri fabrikası için bir ardışık düzeni kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8ecec-116">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ecec-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="8ecec-117">-DataFactoryName</span></span>
<span data-ttu-id="8ecec-118">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ecec-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="8ecec-119">Bu cmdlet, bu parametrenin belirttiği veri fabrikası için bir ardışık düzeni kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8ecec-119">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="8ecec-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ecec-120">-DefaultProfile</span></span>
<span data-ttu-id="8ecec-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="8ecec-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8ecec-122">-Force</span><span class="sxs-lookup"><span data-stu-id="8ecec-122">-Force</span></span>
<span data-ttu-id="8ecec-123">Bu cmdlet 'in bir ardışık düzeni sizden onay istemeden kaldırmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8ecec-123">Indicates that this cmdlet removes a pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="8ecec-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="8ecec-124">-Name</span></span>
<span data-ttu-id="8ecec-125">Kaldırılacak ardışık düzenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ecec-125">Specifies the name of the pipeline to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PipelineName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ecec-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ecec-126">-ResourceGroupName</span></span>
<span data-ttu-id="8ecec-127">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ecec-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="8ecec-128">Bu cmdlet, bu parametrenin belirttiği gruptan bir ardışık düzeni kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8ecec-128">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="8ecec-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="8ecec-129">-Confirm</span></span>
<span data-ttu-id="8ecec-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8ecec-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ecec-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ecec-131">-WhatIf</span></span>
<span data-ttu-id="8ecec-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8ecec-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ecec-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8ecec-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ecec-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ecec-134">CommonParameters</span></span>
<span data-ttu-id="8ecec-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8ecec-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ecec-136">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ecec-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ecec-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8ecec-137">INPUTS</span></span>

### <span data-ttu-id="8ecec-138">System. String</span><span class="sxs-lookup"><span data-stu-id="8ecec-138">System.String</span></span>

### <span data-ttu-id="8ecec-139">Microsoft.Azure.Commands.DataFactories.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="8ecec-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="8ecec-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8ecec-140">OUTPUTS</span></span>

### <span data-ttu-id="8ecec-141">System. void</span><span class="sxs-lookup"><span data-stu-id="8ecec-141">System.Void</span></span>

## <span data-ttu-id="8ecec-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8ecec-142">NOTES</span></span>
* <span data-ttu-id="8ecec-143">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="8ecec-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="8ecec-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8ecec-144">RELATED LINKS</span></span>

[<span data-ttu-id="8ecec-145">Get-Azverfactorypya</span><span class="sxs-lookup"><span data-stu-id="8ecec-145">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="8ecec-146">Yeni-Azveri Factorypya</span><span class="sxs-lookup"><span data-stu-id="8ecec-146">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="8ecec-147">Özgeçmiş-Azverfactorypya</span><span class="sxs-lookup"><span data-stu-id="8ecec-147">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="8ecec-148">Set-Azdatafactorypipelineactivedönem</span><span class="sxs-lookup"><span data-stu-id="8ecec-148">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="8ecec-149">Askıya al-Azverfactorypya</span><span class="sxs-lookup"><span data-stu-id="8ecec-149">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


