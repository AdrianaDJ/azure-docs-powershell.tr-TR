---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: E1E0919A-062B-4794-ADE7-E17133A40604
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryPipeline.md
ms.openlocfilehash: 48638f53f58fd420e9a7b3dfe2e50a3e61d2314f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587972"
---
# <span data-ttu-id="8e794-101">Remove-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="8e794-101">Remove-AzureRmDataFactoryPipeline</span></span>

## <span data-ttu-id="8e794-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e794-102">SYNOPSIS</span></span>
<span data-ttu-id="8e794-103">Bir ardışık düzeni Azure Veri Fabrikası 'nden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8e794-103">Removes a pipeline from Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e794-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8e794-104">SYNTAX</span></span>

### <span data-ttu-id="8e794-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8e794-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryPipeline [-Force] [-Name] <String> [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8e794-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="8e794-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryPipeline [-Force] [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e794-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="8e794-107">DESCRIPTION</span></span>
<span data-ttu-id="8e794-108">**Remove-AzureRmDataFactoryPipeline** cmdlet 'ı Azure Veri Fabrikası 'ndan ardışık düzeni kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8e794-108">The **Remove-AzureRmDataFactoryPipeline** cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="8e794-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8e794-109">EXAMPLES</span></span>

### <span data-ttu-id="8e794-110">Örnek 1: ardışık düzeni kaldırma</span><span class="sxs-lookup"><span data-stu-id="8e794-110">Example 1: Remove a pipeline</span></span>
```
PS C:\>Remove-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="8e794-111">Bu cmdlet, WikiADF adlı veri fabrikası</span><span class="sxs-lookup"><span data-stu-id="8e794-111">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="8e794-112">Komut bir $True değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="8e794-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="8e794-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8e794-113">PARAMETERS</span></span>

### <span data-ttu-id="8e794-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="8e794-114">-DataFactory</span></span>
<span data-ttu-id="8e794-115">**Psdatafactory** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8e794-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="8e794-116">Bu cmdlet, bu parametrenin belirttiği veri fabrikası için bir ardışık düzeni kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8e794-116">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="8e794-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="8e794-117">-DataFactoryName</span></span>
<span data-ttu-id="8e794-118">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8e794-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="8e794-119">Bu cmdlet, bu parametrenin belirttiği veri fabrikası için bir ardışık düzeni kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8e794-119">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="8e794-120">-Force</span><span class="sxs-lookup"><span data-stu-id="8e794-120">-Force</span></span>
<span data-ttu-id="8e794-121">Bu cmdlet 'in bir ardışık düzeni sizden onay istemeden kaldırmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8e794-121">Indicates that this cmdlet removes a pipeline without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="8e794-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="8e794-122">-Name</span></span>
<span data-ttu-id="8e794-123">Kaldırılacak ardışık düzenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8e794-123">Specifies the name of the pipeline to remove.</span></span>

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

### <span data-ttu-id="8e794-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e794-124">-ResourceGroupName</span></span>
<span data-ttu-id="8e794-125">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8e794-125">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="8e794-126">Bu cmdlet, bu parametrenin belirttiği gruptan bir ardışık düzeni kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8e794-126">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="8e794-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="8e794-127">-Confirm</span></span>
<span data-ttu-id="8e794-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8e794-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e794-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e794-129">-WhatIf</span></span>
<span data-ttu-id="8e794-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8e794-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e794-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8e794-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e794-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e794-132">-DefaultProfile</span></span>
<span data-ttu-id="8e794-133">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8e794-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e794-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e794-134">CommonParameters</span></span>
<span data-ttu-id="8e794-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8e794-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e794-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e794-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e794-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8e794-137">INPUTS</span></span>

## <span data-ttu-id="8e794-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8e794-138">OUTPUTS</span></span>

### <span data-ttu-id="8e794-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8e794-139">System.Boolean</span></span>

## <span data-ttu-id="8e794-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8e794-140">NOTES</span></span>
* <span data-ttu-id="8e794-141">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="8e794-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="8e794-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8e794-142">RELATED LINKS</span></span>

[<span data-ttu-id="8e794-143">Get-Azurermdatafactorypda</span><span class="sxs-lookup"><span data-stu-id="8e794-143">Get-AzureRmDataFactoryPipeline</span></span>](./Get-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="8e794-144">Yeni-Azurermdatafactorypeline</span><span class="sxs-lookup"><span data-stu-id="8e794-144">New-AzureRmDataFactoryPipeline</span></span>](./New-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="8e794-145">Özgeçmiş-Azurermdatafactorypda</span><span class="sxs-lookup"><span data-stu-id="8e794-145">Resume-AzureRmDataFactoryPipeline</span></span>](./Resume-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="8e794-146">Set-Azurermdatafactoryptam</span><span class="sxs-lookup"><span data-stu-id="8e794-146">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="8e794-147">Askıya al-Azurermdatafactorypla</span><span class="sxs-lookup"><span data-stu-id="8e794-147">Suspend-AzureRmDataFactoryPipeline</span></span>](./Suspend-AzureRmDataFactoryPipeline.md)


