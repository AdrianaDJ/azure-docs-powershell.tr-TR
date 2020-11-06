---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: E1E0919A-062B-4794-ADE7-E17133A40604
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryPipeline.md
ms.openlocfilehash: aede985cfac5b8ab25c4056eb44e54ea7c6b1c2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592021"
---
# <span data-ttu-id="84bc2-101">Remove-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="84bc2-101">Remove-AzureRmDataFactoryPipeline</span></span>

## <span data-ttu-id="84bc2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84bc2-102">SYNOPSIS</span></span>
<span data-ttu-id="84bc2-103">Bir ardışık düzeni Azure Veri Fabrikası 'nden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="84bc2-103">Removes a pipeline from Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84bc2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="84bc2-104">SYNTAX</span></span>

### <span data-ttu-id="84bc2-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="84bc2-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryPipeline [-Force] [-Name] <String> [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="84bc2-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="84bc2-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryPipeline [-Force] [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84bc2-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="84bc2-107">DESCRIPTION</span></span>
<span data-ttu-id="84bc2-108">**Remove-AzureRmDataFactoryPipeline** cmdlet 'ı Azure Veri Fabrikası 'ndan ardışık düzeni kaldırır.</span><span class="sxs-lookup"><span data-stu-id="84bc2-108">The **Remove-AzureRmDataFactoryPipeline** cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="84bc2-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="84bc2-109">EXAMPLES</span></span>

### <span data-ttu-id="84bc2-110">Örnek 1: ardışık düzeni kaldırma</span><span class="sxs-lookup"><span data-stu-id="84bc2-110">Example 1: Remove a pipeline</span></span>
```
PS C:\>Remove-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="84bc2-111">Bu cmdlet, WikiADF adlı veri fabrikası</span><span class="sxs-lookup"><span data-stu-id="84bc2-111">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="84bc2-112">Komut bir $True değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="84bc2-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="84bc2-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="84bc2-113">PARAMETERS</span></span>

### <span data-ttu-id="84bc2-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="84bc2-114">-DataFactory</span></span>
<span data-ttu-id="84bc2-115">**Psdatafactory** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="84bc2-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="84bc2-116">Bu cmdlet, bu parametrenin belirttiği veri fabrikası için bir ardışık düzeni kaldırır.</span><span class="sxs-lookup"><span data-stu-id="84bc2-116">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="84bc2-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="84bc2-117">-DataFactoryName</span></span>
<span data-ttu-id="84bc2-118">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="84bc2-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="84bc2-119">Bu cmdlet, bu parametrenin belirttiği veri fabrikası için bir ardışık düzeni kaldırır.</span><span class="sxs-lookup"><span data-stu-id="84bc2-119">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="84bc2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84bc2-120">-DefaultProfile</span></span>
<span data-ttu-id="84bc2-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="84bc2-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="84bc2-122">-Force</span><span class="sxs-lookup"><span data-stu-id="84bc2-122">-Force</span></span>
<span data-ttu-id="84bc2-123">Bu cmdlet 'in bir ardışık düzeni sizden onay istemeden kaldırmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="84bc2-123">Indicates that this cmdlet removes a pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="84bc2-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="84bc2-124">-Name</span></span>
<span data-ttu-id="84bc2-125">Kaldırılacak ardışık düzenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="84bc2-125">Specifies the name of the pipeline to remove.</span></span>

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

### <span data-ttu-id="84bc2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84bc2-126">-ResourceGroupName</span></span>
<span data-ttu-id="84bc2-127">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="84bc2-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="84bc2-128">Bu cmdlet, bu parametrenin belirttiği gruptan bir ardışık düzeni kaldırır.</span><span class="sxs-lookup"><span data-stu-id="84bc2-128">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="84bc2-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="84bc2-129">-Confirm</span></span>
<span data-ttu-id="84bc2-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="84bc2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84bc2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84bc2-131">-WhatIf</span></span>
<span data-ttu-id="84bc2-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="84bc2-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84bc2-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="84bc2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84bc2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84bc2-134">CommonParameters</span></span>
<span data-ttu-id="84bc2-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="84bc2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84bc2-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84bc2-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84bc2-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="84bc2-137">INPUTS</span></span>

### <span data-ttu-id="84bc2-138">System. String</span><span class="sxs-lookup"><span data-stu-id="84bc2-138">System.String</span></span>

### <span data-ttu-id="84bc2-139">Microsoft.Azure.Commands.DataFactories.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="84bc2-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="84bc2-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="84bc2-140">OUTPUTS</span></span>

### <span data-ttu-id="84bc2-141">System. void</span><span class="sxs-lookup"><span data-stu-id="84bc2-141">System.Void</span></span>

## <span data-ttu-id="84bc2-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="84bc2-142">NOTES</span></span>
* <span data-ttu-id="84bc2-143">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="84bc2-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="84bc2-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="84bc2-144">RELATED LINKS</span></span>

[<span data-ttu-id="84bc2-145">Get-Azurermdatafactorypda</span><span class="sxs-lookup"><span data-stu-id="84bc2-145">Get-AzureRmDataFactoryPipeline</span></span>](./Get-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="84bc2-146">Yeni-Azurermdatafactorypeline</span><span class="sxs-lookup"><span data-stu-id="84bc2-146">New-AzureRmDataFactoryPipeline</span></span>](./New-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="84bc2-147">Özgeçmiş-Azurermdatafactorypda</span><span class="sxs-lookup"><span data-stu-id="84bc2-147">Resume-AzureRmDataFactoryPipeline</span></span>](./Resume-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="84bc2-148">Set-Azurermdatafactoryptam</span><span class="sxs-lookup"><span data-stu-id="84bc2-148">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="84bc2-149">Askıya al-Azurermdatafactorypla</span><span class="sxs-lookup"><span data-stu-id="84bc2-149">Suspend-AzureRmDataFactoryPipeline</span></span>](./Suspend-AzureRmDataFactoryPipeline.md)


