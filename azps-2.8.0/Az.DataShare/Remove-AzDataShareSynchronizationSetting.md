---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharesynchronizationsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSynchronizationSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSynchronizationSetting.md
ms.openlocfilehash: 0ff167f14c9a831cb2afe2ce335a0c8bcd18acc4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752163"
---
# <span data-ttu-id="48eb2-101">Remove-AzDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="48eb2-101">Remove-AzDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="48eb2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48eb2-102">SYNOPSIS</span></span>
<span data-ttu-id="48eb2-103">Eşitleme ayarını kaldırır</span><span class="sxs-lookup"><span data-stu-id="48eb2-103">removes a synchronization setting</span></span>

## <span data-ttu-id="48eb2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="48eb2-104">SYNTAX</span></span>

### <span data-ttu-id="48eb2-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="48eb2-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareSynchronizationSetting -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="48eb2-106">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="48eb2-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareSynchronizationSetting -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48eb2-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="48eb2-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareSynchronizationSetting -InputObject <PSDataShareSynchronizationSetting> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48eb2-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="48eb2-108">DESCRIPTION</span></span>
<span data-ttu-id="48eb2-109">**Remove-Azdatasharesynmadizationsetting** cmdlet 'i, datashare eşitleme ayarını kaldırır</span><span class="sxs-lookup"><span data-stu-id="48eb2-109">The **Remove-AzDataShareSynchronizationSetting** cmdlet removes a datashare synchronization setting</span></span>

## <span data-ttu-id="48eb2-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="48eb2-110">EXAMPLES</span></span>

### <span data-ttu-id="48eb2-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="48eb2-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareSynchronizationSetting -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsShareSynchronizationSetting"

Are you sure you want to remove synchronization-setting "AdsShareSynchronizationSetting"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="48eb2-112">Bu komut, paylaşımapaylaşımı ayarı adlı bir eşitleme ayarını Share AdsShare dizininden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="48eb2-112">This commands removes a synchronization setting named AdsShareSynchronizationSetting from share AdsShare.</span></span> 

## <span data-ttu-id="48eb2-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="48eb2-113">PARAMETERS</span></span>

### <span data-ttu-id="48eb2-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="48eb2-114">-AccountName</span></span>
<span data-ttu-id="48eb2-115">Azure veri paylaşımı hesap adı</span><span class="sxs-lookup"><span data-stu-id="48eb2-115">Azure Data Share Account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48eb2-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="48eb2-116">-AsJob</span></span>
<span data-ttu-id="48eb2-117">{{Fill Iş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="48eb2-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="48eb2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48eb2-118">-DefaultProfile</span></span>
<span data-ttu-id="48eb2-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="48eb2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48eb2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="48eb2-120">-InputObject</span></span>
<span data-ttu-id="48eb2-121">Azure veri paylaşımı eşitleme ayarı.</span><span class="sxs-lookup"><span data-stu-id="48eb2-121">The Azure Data Share Synchronization setting.</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="48eb2-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="48eb2-122">-Name</span></span>
<span data-ttu-id="48eb2-123">Eşitleme ayarı adı</span><span class="sxs-lookup"><span data-stu-id="48eb2-123">Synchronization setting name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48eb2-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="48eb2-124">-PassThru</span></span>
<span data-ttu-id="48eb2-125">Return Object (belirtilmişse).</span><span class="sxs-lookup"><span data-stu-id="48eb2-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="48eb2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48eb2-126">-ResourceGroupName</span></span>
<span data-ttu-id="48eb2-127">Azure veri paylaşımı hesabının kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="48eb2-127">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48eb2-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="48eb2-128">-ResourceId</span></span>
<span data-ttu-id="48eb2-129">Eşitleme ayarının kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="48eb2-129">The resource id of the synchronization setting</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48eb2-130">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="48eb2-130">-ShareName</span></span>
<span data-ttu-id="48eb2-131">Azure veri paylaşımı adı</span><span class="sxs-lookup"><span data-stu-id="48eb2-131">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48eb2-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="48eb2-132">-Confirm</span></span>
<span data-ttu-id="48eb2-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="48eb2-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48eb2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48eb2-134">-WhatIf</span></span>
<span data-ttu-id="48eb2-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="48eb2-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48eb2-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="48eb2-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48eb2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48eb2-137">CommonParameters</span></span>
<span data-ttu-id="48eb2-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="48eb2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48eb2-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48eb2-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48eb2-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="48eb2-140">INPUTS</span></span>

### <span data-ttu-id="48eb2-141">System. String</span><span class="sxs-lookup"><span data-stu-id="48eb2-141">System.String</span></span>

### <span data-ttu-id="48eb2-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSData</span><span class="sxs-lookup"><span data-stu-id="48eb2-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="48eb2-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="48eb2-143">OUTPUTS</span></span>

### <span data-ttu-id="48eb2-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="48eb2-144">System.Boolean</span></span>

## <span data-ttu-id="48eb2-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="48eb2-145">NOTES</span></span>

## <span data-ttu-id="48eb2-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="48eb2-146">RELATED LINKS</span></span>
