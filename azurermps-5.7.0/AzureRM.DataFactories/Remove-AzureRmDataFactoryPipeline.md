---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: E1E0919A-062B-4794-ADE7-E17133A40604
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryPipeline.md
ms.openlocfilehash: dec686838bd7826b57e7b158f4ed741608eaf782
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587587"
---
# <span data-ttu-id="6939a-101">Remove-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="6939a-101">Remove-AzureRmDataFactoryPipeline</span></span>

## <span data-ttu-id="6939a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6939a-102">SYNOPSIS</span></span>
<span data-ttu-id="6939a-103">Bir ardışık düzeni Azure Veri Fabrikası 'nden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6939a-103">Removes a pipeline from Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6939a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6939a-104">SYNTAX</span></span>

### <span data-ttu-id="6939a-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6939a-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryPipeline [-Force] [-Name] <String> [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6939a-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="6939a-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryPipeline [-Force] [-Name] <String> [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6939a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6939a-107">DESCRIPTION</span></span>
<span data-ttu-id="6939a-108">**Remove-AzureRmDataFactoryPipeline** cmdlet 'ı Azure Veri Fabrikası 'ndan ardışık düzeni kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6939a-108">The **Remove-AzureRmDataFactoryPipeline** cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="6939a-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6939a-109">EXAMPLES</span></span>

### <span data-ttu-id="6939a-110">Örnek 1: ardışık düzeni kaldırma</span><span class="sxs-lookup"><span data-stu-id="6939a-110">Example 1: Remove a pipeline</span></span>
```
PS C:\>Remove-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
Confirm
Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="6939a-111">Bu cmdlet, WikiADF adlı veri fabrikası</span><span class="sxs-lookup"><span data-stu-id="6939a-111">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="6939a-112">Komut bir $True değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="6939a-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="6939a-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6939a-113">PARAMETERS</span></span>

### <span data-ttu-id="6939a-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="6939a-114">-DataFactory</span></span>
<span data-ttu-id="6939a-115">**Psdatafactory** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6939a-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="6939a-116">Bu cmdlet, bu parametrenin belirttiği veri fabrikası için bir ardışık düzeni kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6939a-116">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6939a-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="6939a-117">-DataFactoryName</span></span>
<span data-ttu-id="6939a-118">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6939a-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="6939a-119">Bu cmdlet, bu parametrenin belirttiği veri fabrikası için bir ardışık düzeni kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6939a-119">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6939a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6939a-120">-DefaultProfile</span></span>
<span data-ttu-id="6939a-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="6939a-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6939a-122">-Force</span><span class="sxs-lookup"><span data-stu-id="6939a-122">-Force</span></span>
<span data-ttu-id="6939a-123">Bu cmdlet 'in bir ardışık düzeni sizden onay istemeden kaldırmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6939a-123">Indicates that this cmdlet removes a pipeline without prompting you for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6939a-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="6939a-124">-Name</span></span>
<span data-ttu-id="6939a-125">Kaldırılacak ardışık düzenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6939a-125">Specifies the name of the pipeline to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: PipelineName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6939a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6939a-126">-ResourceGroupName</span></span>
<span data-ttu-id="6939a-127">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6939a-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="6939a-128">Bu cmdlet, bu parametrenin belirttiği gruptan bir ardışık düzeni kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6939a-128">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6939a-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="6939a-129">-Confirm</span></span>
<span data-ttu-id="6939a-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6939a-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6939a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6939a-131">-WhatIf</span></span>
<span data-ttu-id="6939a-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6939a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6939a-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6939a-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6939a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6939a-134">CommonParameters</span></span>
<span data-ttu-id="6939a-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6939a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6939a-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6939a-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6939a-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6939a-137">INPUTS</span></span>

### <span data-ttu-id="6939a-138">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="6939a-138">None</span></span>
<span data-ttu-id="6939a-139">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="6939a-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6939a-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6939a-140">OUTPUTS</span></span>

### <span data-ttu-id="6939a-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6939a-141">System.Boolean</span></span>

## <span data-ttu-id="6939a-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6939a-142">NOTES</span></span>
* <span data-ttu-id="6939a-143">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="6939a-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="6939a-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6939a-144">RELATED LINKS</span></span>

[<span data-ttu-id="6939a-145">Get-Azurermdatafactorypda</span><span class="sxs-lookup"><span data-stu-id="6939a-145">Get-AzureRmDataFactoryPipeline</span></span>](./Get-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="6939a-146">Yeni-Azurermdatafactorypeline</span><span class="sxs-lookup"><span data-stu-id="6939a-146">New-AzureRmDataFactoryPipeline</span></span>](./New-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="6939a-147">Özgeçmiş-Azurermdatafactorypda</span><span class="sxs-lookup"><span data-stu-id="6939a-147">Resume-AzureRmDataFactoryPipeline</span></span>](./Resume-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="6939a-148">Set-Azurermdatafactoryptam</span><span class="sxs-lookup"><span data-stu-id="6939a-148">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="6939a-149">Askıya al-Azurermdatafactorypla</span><span class="sxs-lookup"><span data-stu-id="6939a-149">Suspend-AzureRmDataFactoryPipeline</span></span>](./Suspend-AzureRmDataFactoryPipeline.md)


