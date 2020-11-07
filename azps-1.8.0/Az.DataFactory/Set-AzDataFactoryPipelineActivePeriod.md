---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: D853A91F-95E7-4C36-AC0F-2C10DFCF68F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactorypipelineactiveperiod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryPipelineActivePeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryPipelineActivePeriod.md
ms.openlocfilehash: edb2e94900d383675bd183c09df16e295828aae1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917039"
---
# <span data-ttu-id="ce0f1-101">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="ce0f1-101">Set-AzDataFactoryPipelineActivePeriod</span></span>

## <span data-ttu-id="ce0f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce0f1-102">SYNOPSIS</span></span>
<span data-ttu-id="ce0f1-103">Veri dilimleri için etkin dönemi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="ce0f1-103">Configures the active period for data slices.</span></span>

## <span data-ttu-id="ce0f1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ce0f1-104">SYNTAX</span></span>

### <span data-ttu-id="ce0f1-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ce0f1-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryPipelineActivePeriod [-PipelineName] <String> [-DataFactoryName] <String>
 [-StartDateTime] <DateTime> [[-EndDateTime] <DateTime>] [-AutoResolve] [-ForceRecalculate]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ce0f1-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="ce0f1-106">ByFactoryObject</span></span>
```
Set-AzDataFactoryPipelineActivePeriod [-PipelineName] <String> [-DataFactory] <PSDataFactory>
 [-StartDateTime] <DateTime> [[-EndDateTime] <DateTime>] [-AutoResolve] [-ForceRecalculate]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce0f1-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ce0f1-107">DESCRIPTION</span></span>
<span data-ttu-id="ce0f1-108">**Set-Azdatafactorypipelineactivedönem** cmdlet 'ı, Azure Veri Fabrikası 'nde ardışık düzen tarafından işlenen veri dilimleri için etkin dönemi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="ce0f1-108">The **Set-AzDataFactoryPipelineActivePeriod** cmdlet configures the active period for the data slices that are processed by a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="ce0f1-109">Bir veri kümesindeki dilimlerin durumunu değiştirmek için Set-AzDataFactorySliceStatus cmdlet 'ini kullanıyorsanız, bir dilimin başlangıç saati ve bitiş saatinin ardışık düzenin etkin döneminde olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="ce0f1-109">If you use the Set-AzDataFactorySliceStatus cmdlet to modify the status of slices for a dataset, make sure that the start time and end time for a slice are in the active period of the pipeline.</span></span>
<span data-ttu-id="ce0f1-110">Bir ardışık düzen oluşturduktan sonra, veri işlemenin gerçekleştiği dönemi belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ce0f1-110">After you create a pipeline, you can specify the period in which data processing occurs.</span></span>
<span data-ttu-id="ce0f1-111">Potansiyel satış için etkin dönem belirtmek, veri dilimlerinin her veri fabrikası veri kümesi için tanımlanmış **kullanılabilirlik** özelliklerine bağlı olarak işlenme süresini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="ce0f1-111">Specifying the active period for a pipeline defines the time duration in which the data slices are processed based on the **Availability** properties that were defined for each Data Factory dataset.</span></span>

## <span data-ttu-id="ce0f1-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ce0f1-112">EXAMPLES</span></span>

### <span data-ttu-id="ce0f1-113">Örnek 1: etkin dönemi yapılandırma</span><span class="sxs-lookup"><span data-stu-id="ce0f1-113">Example 1: Configure the active period</span></span>
```
PS C:\>Set-AzDataFactoryPipelineActivePeriod -ResourceGroupName "ADF" -PipelineName "DPWikisample" -DataFactoryName "WikiADF" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-22T16:00:00Z
Confirm
Are you sure you want to set pipeline 'DPWikisample' active period from '05/21/2014 16:00:00' to
'05/22/2014 16:00:00'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="ce0f1-114">Bu komut, Dpıda örnek işlemler adlı ardışık düzenin etkin dönemini yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="ce0f1-114">This command configures the active period for the data slices that the pipeline named DPWikisample processes.</span></span>
<span data-ttu-id="ce0f1-115">Komut, veri dilimlerinin başlangıç ve bitiş noktalarını değer olarak sağlar.</span><span class="sxs-lookup"><span data-stu-id="ce0f1-115">The command provides beginning and end points for the data slices as values.</span></span>
<span data-ttu-id="ce0f1-116">Komut bir $True değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="ce0f1-116">The command returns a value of $True.</span></span>

## <span data-ttu-id="ce0f1-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ce0f1-117">PARAMETERS</span></span>

### <span data-ttu-id="ce0f1-118">-AutoResolve</span><span class="sxs-lookup"><span data-stu-id="ce0f1-118">-AutoResolve</span></span>
<span data-ttu-id="ce0f1-119">Bu cmdlet 'in Otomatik Çözümle kullandığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ce0f1-119">Indicates that this cmdlet uses auto resolve.</span></span>

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

### <span data-ttu-id="ce0f1-120">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="ce0f1-120">-DataFactory</span></span>
<span data-ttu-id="ce0f1-121">**Psdatafactory** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ce0f1-121">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="ce0f1-122">Bu cmdlet, bu parametrenin belirttiği veri fabrikasına ait etkin dönemi değiştirir.</span><span class="sxs-lookup"><span data-stu-id="ce0f1-122">This cmdlet modifies the active period for a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ce0f1-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ce0f1-123">-DataFactoryName</span></span>
<span data-ttu-id="ce0f1-124">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ce0f1-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="ce0f1-125">Bu cmdlet, bu parametrenin belirttiği veri fabrikasına ait etkin dönemi değiştirir.</span><span class="sxs-lookup"><span data-stu-id="ce0f1-125">This cmdlet modifies the active period for a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ce0f1-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce0f1-126">-DefaultProfile</span></span>
<span data-ttu-id="ce0f1-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="ce0f1-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ce0f1-128">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="ce0f1-128">-EndDateTime</span></span>
<span data-ttu-id="ce0f1-129">Bir dönemin sonunu **DateTime** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="ce0f1-129">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="ce0f1-130">Bu dönemde veri işleme veya veri dilimleri işlenir.</span><span class="sxs-lookup"><span data-stu-id="ce0f1-130">Data processing occurs or data slices are processed within this period.</span></span>
<span data-ttu-id="ce0f1-131">**TarihSaat** nesneleri hakkında daha fazla bilgi için, yazın `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="ce0f1-131">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="ce0f1-132">*EndDateTime* aşağıdaki örneklerde olduğu gibi ISO8601 biçiminde belirtilmelidir: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000 z (UTC) 2015-01-01T00</span><span class="sxs-lookup"><span data-stu-id="ce0f1-132">*EndDateTime* must be specified in the ISO8601 format as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce0f1-133">-Forcerecalbir</span><span class="sxs-lookup"><span data-stu-id="ce0f1-133">-ForceRecalculate</span></span>
<span data-ttu-id="ce0f1-134">Bu cmdlet 'in zorla yeniden hesaplamayı kullandığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ce0f1-134">Indicates that this cmdlet uses force recalculate.</span></span>

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

### <span data-ttu-id="ce0f1-135">-Ardışık Düzen adı</span><span class="sxs-lookup"><span data-stu-id="ce0f1-135">-PipelineName</span></span>
<span data-ttu-id="ce0f1-136">Ardışık düzenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ce0f1-136">Specifies the name of the pipeline.</span></span>
<span data-ttu-id="ce0f1-137">Bu cmdlet, bu parametrenin belirttiği ardışık düzenin etkin dönemini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="ce0f1-137">This cmdlet sets the active period for the pipeline that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce0f1-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce0f1-138">-ResourceGroupName</span></span>
<span data-ttu-id="ce0f1-139">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ce0f1-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="ce0f1-140">Bu cmdlet, bu parametrenin belirttiği gruba ait bir ardışık düzenin etkin dönemini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="ce0f1-140">This cmdlet modifies the active period for a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ce0f1-141">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="ce0f1-141">-StartDateTime</span></span>
<span data-ttu-id="ce0f1-142">Bir dönemin başlangıcını **DateTime** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="ce0f1-142">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="ce0f1-143">Bu dönemde veri işleme veya veri dilimleri işlenir.</span><span class="sxs-lookup"><span data-stu-id="ce0f1-143">Data processing occurs or data slices are processed within this period.</span></span>
<span data-ttu-id="ce0f1-144">*Startdatetıme* , ISO8601 biçiminde belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="ce0f1-144">*StartDateTime* must be specified in the ISO8601 format.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce0f1-145">-Onay</span><span class="sxs-lookup"><span data-stu-id="ce0f1-145">-Confirm</span></span>
<span data-ttu-id="ce0f1-146">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ce0f1-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce0f1-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce0f1-147">-WhatIf</span></span>
<span data-ttu-id="ce0f1-148">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ce0f1-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce0f1-149">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ce0f1-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce0f1-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce0f1-150">CommonParameters</span></span>
<span data-ttu-id="ce0f1-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ce0f1-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce0f1-152">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce0f1-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce0f1-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ce0f1-153">INPUTS</span></span>

### <span data-ttu-id="ce0f1-154">System. String</span><span class="sxs-lookup"><span data-stu-id="ce0f1-154">System.String</span></span>

### <span data-ttu-id="ce0f1-155">Microsoft.Azure.Commands.DataFactories.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="ce0f1-155">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="ce0f1-156">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ce0f1-156">OUTPUTS</span></span>

### <span data-ttu-id="ce0f1-157">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ce0f1-157">System.Boolean</span></span>

## <span data-ttu-id="ce0f1-158">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ce0f1-158">NOTES</span></span>
* <span data-ttu-id="ce0f1-159">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="ce0f1-159">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="ce0f1-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ce0f1-160">RELATED LINKS</span></span>

[<span data-ttu-id="ce0f1-161">Yeni-Azveri Factorypya</span><span class="sxs-lookup"><span data-stu-id="ce0f1-161">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="ce0f1-162">Set-AzDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="ce0f1-162">Set-AzDataFactorySliceStatus</span></span>](./Set-AzDataFactorySliceStatus.md)


