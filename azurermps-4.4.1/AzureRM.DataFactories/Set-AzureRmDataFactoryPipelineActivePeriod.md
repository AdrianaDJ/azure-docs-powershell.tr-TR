---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: D853A91F-95E7-4C36-AC0F-2C10DFCF68F8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactoryPipelineActivePeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactoryPipelineActivePeriod.md
ms.openlocfilehash: 033b787d444d8a4f97650b93f7621399648b1343
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586908"
---
# <span data-ttu-id="9959e-101">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="9959e-101">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>

## <span data-ttu-id="9959e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9959e-102">SYNOPSIS</span></span>
<span data-ttu-id="9959e-103">Veri dilimleri için etkin dönemi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="9959e-103">Configures the active period for data slices.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9959e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9959e-104">SYNTAX</span></span>

### <span data-ttu-id="9959e-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9959e-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryPipelineActivePeriod [-PipelineName] <String> [-DataFactoryName] <String>
 [-StartDateTime] <DateTime> [[-EndDateTime] <DateTime>] [-AutoResolve] [-ForceRecalculate]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9959e-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="9959e-106">ByFactoryObject</span></span>
```
Set-AzureRmDataFactoryPipelineActivePeriod [-PipelineName] <String> [-DataFactory] <PSDataFactory>
 [-StartDateTime] <DateTime> [[-EndDateTime] <DateTime>] [-AutoResolve] [-ForceRecalculate]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9959e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="9959e-107">DESCRIPTION</span></span>
<span data-ttu-id="9959e-108">**Set-Azurermdatafactorypelıneactivedönem** cmdlet 'ı Azure Veri Fabrikası 'nde ardışık düzen tarafından işlenen veri dilimleri için etkin dönemi yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="9959e-108">The **Set-AzureRmDataFactoryPipelineActivePeriod** cmdlet configures the active period for the data slices that are processed by a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="9959e-109">Bir veri kümesindeki dilimlerin durumunu değiştirmek için Set-AzureRmDataFactorySliceStatus cmdlet 'ini kullanıyorsanız, bir dilimin başlangıç saati ve bitiş saatinin ardışık düzenin etkin döneminde olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="9959e-109">If you use the Set-AzureRmDataFactorySliceStatus cmdlet to modify the status of slices for a dataset, make sure that the start time and end time for a slice are in the active period of the pipeline.</span></span>

<span data-ttu-id="9959e-110">Bir ardışık düzen oluşturduktan sonra, veri işlemenin gerçekleştiği dönemi belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9959e-110">After you create a pipeline, you can specify the period in which data processing occurs.</span></span>
<span data-ttu-id="9959e-111">Potansiyel satış için etkin dönem belirtmek, veri dilimlerinin her veri fabrikası veri kümesi için tanımlanmış **kullanılabilirlik** özelliklerine bağlı olarak işlenme süresini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="9959e-111">Specifying the active period for a pipeline defines the time duration in which the data slices are processed based on the **Availability** properties that were defined for each Data Factory dataset.</span></span>

## <span data-ttu-id="9959e-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9959e-112">EXAMPLES</span></span>

### <span data-ttu-id="9959e-113">Örnek 1: etkin dönemi yapılandırma</span><span class="sxs-lookup"><span data-stu-id="9959e-113">Example 1: Configure the active period</span></span>
```
PS C:\>Set-AzureRmDataFactoryPipelineActivePeriod -ResourceGroupName "ADF" -PipelineName "DPWikisample" -DataFactoryName "WikiADF" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-22T16:00:00Z
Confirm
Are you sure you want to set pipeline 'DPWikisample' active period from '05/21/2014 16:00:00' to
'05/22/2014 16:00:00'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="9959e-114">Bu komut, Dpıda örnek işlemler adlı ardışık düzenin etkin dönemini yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="9959e-114">This command configures the active period for the data slices that the pipeline named DPWikisample processes.</span></span>
<span data-ttu-id="9959e-115">Komut, veri dilimlerinin başlangıç ve bitiş noktalarını değer olarak sağlar.</span><span class="sxs-lookup"><span data-stu-id="9959e-115">The command provides beginning and end points for the data slices as values.</span></span>
<span data-ttu-id="9959e-116">Komut bir $True değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="9959e-116">The command returns a value of $True.</span></span>

## <span data-ttu-id="9959e-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9959e-117">PARAMETERS</span></span>

### <span data-ttu-id="9959e-118">-AutoResolve</span><span class="sxs-lookup"><span data-stu-id="9959e-118">-AutoResolve</span></span>
<span data-ttu-id="9959e-119">Bu cmdlet 'in Otomatik Çözümle kullandığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9959e-119">Indicates that this cmdlet uses auto resolve.</span></span>

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

### <span data-ttu-id="9959e-120">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="9959e-120">-DataFactory</span></span>
<span data-ttu-id="9959e-121">**Psdatafactory** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9959e-121">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="9959e-122">Bu cmdlet, bu parametrenin belirttiği veri fabrikasına ait etkin dönemi değiştirir.</span><span class="sxs-lookup"><span data-stu-id="9959e-122">This cmdlet modifies the active period for a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="9959e-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="9959e-123">-DataFactoryName</span></span>
<span data-ttu-id="9959e-124">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9959e-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="9959e-125">Bu cmdlet, bu parametrenin belirttiği veri fabrikasına ait etkin dönemi değiştirir.</span><span class="sxs-lookup"><span data-stu-id="9959e-125">This cmdlet modifies the active period for a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="9959e-126">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="9959e-126">-EndDateTime</span></span>
<span data-ttu-id="9959e-127">Bir dönemin sonunu **DateTime** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="9959e-127">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="9959e-128">Bu dönemde veri işleme veya veri dilimleri işlenir.</span><span class="sxs-lookup"><span data-stu-id="9959e-128">Data processing occurs or data slices are processed within this period.</span></span>
<span data-ttu-id="9959e-129">**TarihSaat** nesneleri hakkında daha fazla bilgi için, yazın `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="9959e-129">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="9959e-130">*EndDateTime* aşağıdaki örneklerde olduğu gibi ISO8601 biçiminde belirtilmelidir:</span><span class="sxs-lookup"><span data-stu-id="9959e-130">*EndDateTime* must be specified in the ISO8601 format as in the following examples:</span></span> 

<span data-ttu-id="9959e-131">2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000 Z (UTC) 2015-01-01T00:00:00-08:00 (Pasifik standart saati)</span><span class="sxs-lookup"><span data-stu-id="9959e-131">2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time)</span></span>

<span data-ttu-id="9959e-132">Varsayılan saat dilimi göstergesi UTC.</span><span class="sxs-lookup"><span data-stu-id="9959e-132">The default time zone designator is UTC.</span></span>

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

### <span data-ttu-id="9959e-133">-Forcerecalbir</span><span class="sxs-lookup"><span data-stu-id="9959e-133">-ForceRecalculate</span></span>
<span data-ttu-id="9959e-134">Bu cmdlet 'in zorla yeniden hesaplamayı kullandığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9959e-134">Indicates that this cmdlet uses force recalculate.</span></span>

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

### <span data-ttu-id="9959e-135">-Ardışık Düzen adı</span><span class="sxs-lookup"><span data-stu-id="9959e-135">-PipelineName</span></span>
<span data-ttu-id="9959e-136">Ardışık düzenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9959e-136">Specifies the name of the pipeline.</span></span>
<span data-ttu-id="9959e-137">Bu cmdlet, bu parametrenin belirttiği ardışık düzenin etkin dönemini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="9959e-137">This cmdlet sets the active period for the pipeline that this parameter specifies.</span></span>

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

### <span data-ttu-id="9959e-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9959e-138">-ResourceGroupName</span></span>
<span data-ttu-id="9959e-139">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9959e-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="9959e-140">Bu cmdlet, bu parametrenin belirttiği gruba ait bir ardışık düzenin etkin dönemini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="9959e-140">This cmdlet modifies the active period for a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="9959e-141">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="9959e-141">-StartDateTime</span></span>
<span data-ttu-id="9959e-142">Bir dönemin başlangıcını **DateTime** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="9959e-142">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="9959e-143">Bu dönemde veri işleme veya veri dilimleri işlenir.</span><span class="sxs-lookup"><span data-stu-id="9959e-143">Data processing occurs or data slices are processed within this period.</span></span>

<span data-ttu-id="9959e-144">*Startdatetıme* , ISO8601 biçiminde belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="9959e-144">*StartDateTime* must be specified in the ISO8601 format.</span></span>

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

### <span data-ttu-id="9959e-145">-Onay</span><span class="sxs-lookup"><span data-stu-id="9959e-145">-Confirm</span></span>
<span data-ttu-id="9959e-146">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9959e-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9959e-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9959e-147">-WhatIf</span></span>
<span data-ttu-id="9959e-148">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9959e-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9959e-149">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9959e-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9959e-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9959e-150">-DefaultProfile</span></span>
<span data-ttu-id="9959e-151">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9959e-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9959e-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9959e-152">CommonParameters</span></span>
<span data-ttu-id="9959e-153">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9959e-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9959e-154">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9959e-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9959e-155">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9959e-155">INPUTS</span></span>

## <span data-ttu-id="9959e-156">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9959e-156">OUTPUTS</span></span>

### <span data-ttu-id="9959e-157">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9959e-157">System.Boolean</span></span>

## <span data-ttu-id="9959e-158">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9959e-158">NOTES</span></span>
* <span data-ttu-id="9959e-159">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="9959e-159">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="9959e-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9959e-160">RELATED LINKS</span></span>

[<span data-ttu-id="9959e-161">Yeni-Azurermdatafactorypeline</span><span class="sxs-lookup"><span data-stu-id="9959e-161">New-AzureRmDataFactoryPipeline</span></span>](./New-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="9959e-162">Set-AzureRmDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="9959e-162">Set-AzureRmDataFactorySliceStatus</span></span>](./Set-AzureRmDataFactorySliceStatus.md)


