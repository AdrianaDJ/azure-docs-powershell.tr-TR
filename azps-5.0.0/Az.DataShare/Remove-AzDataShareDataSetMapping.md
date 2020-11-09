---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSetMapping.md
ms.openlocfilehash: 16b212a0c5549f74b56e8c80be8d949a025ecb24
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320270"
---
# <span data-ttu-id="6e304-101">Remove-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="6e304-101">Remove-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="6e304-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e304-102">SYNOPSIS</span></span>
<span data-ttu-id="6e304-103">Veri kümesi eşlemesini kaldırır</span><span class="sxs-lookup"><span data-stu-id="6e304-103">Removes a dataset mapping</span></span>

## <span data-ttu-id="6e304-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6e304-104">SYNTAX</span></span>

### <span data-ttu-id="6e304-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6e304-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e304-106">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="6e304-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareDataSetMapping -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e304-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6e304-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareDataSetMapping -InputObject <PSDataShareDataSetMapping> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e304-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="6e304-108">DESCRIPTION</span></span>
<span data-ttu-id="6e304-109">**Remove-AzDataShareDataSetMapping** cmdlet 'i, veri kümesi eşlemelerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6e304-109">The **Remove-AzDataShareDataSetMapping** cmdlet removes a dataset mappings.</span></span>

## <span data-ttu-id="6e304-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6e304-110">EXAMPLES</span></span>

### <span data-ttu-id="6e304-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6e304-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "DSM"
Are you sure you want to remove dataset mapping "DSM"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="6e304-112">Bu komutlar, sharesubscription WikiAds 'daki DSM adlı veri kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6e304-112">This commands removes the dataset named DSM from sharesubscription WikiAds.</span></span> 

## <span data-ttu-id="6e304-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6e304-113">PARAMETERS</span></span>

### <span data-ttu-id="6e304-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6e304-114">-AccountName</span></span>
<span data-ttu-id="6e304-115">Azure veri paylaşımı hesap adı</span><span class="sxs-lookup"><span data-stu-id="6e304-115">Azure data share account name</span></span>

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

### <span data-ttu-id="6e304-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e304-116">-DefaultProfile</span></span>
<span data-ttu-id="6e304-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6e304-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e304-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6e304-118">-InputObject</span></span>
<span data-ttu-id="6e304-119">Azure veri kümesi eşleme nesnesi</span><span class="sxs-lookup"><span data-stu-id="6e304-119">The azure data set mapping object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6e304-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="6e304-120">-Name</span></span>
<span data-ttu-id="6e304-121">Azure veri kümesi eşleme adı</span><span class="sxs-lookup"><span data-stu-id="6e304-121">Azure data set mapping name</span></span>

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

### <span data-ttu-id="6e304-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="6e304-122">-PassThru</span></span>
<span data-ttu-id="6e304-123">Return Object (belirtilmişse).</span><span class="sxs-lookup"><span data-stu-id="6e304-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="6e304-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e304-124">-ResourceGroupName</span></span>
<span data-ttu-id="6e304-125">Azure veri paylaşımı hesabının kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="6e304-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="6e304-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="6e304-126">-ResourceId</span></span>
<span data-ttu-id="6e304-127">Azure veri kümesi eşlemesinin kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="6e304-127">The resource id of the azure data set mapping</span></span>

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

### <span data-ttu-id="6e304-128">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="6e304-128">-ShareSubscriptionName</span></span>
<span data-ttu-id="6e304-129">Azure veri paylaşımı abonelik adı</span><span class="sxs-lookup"><span data-stu-id="6e304-129">Azure data share subscription name</span></span>

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

### <span data-ttu-id="6e304-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="6e304-130">-Confirm</span></span>
<span data-ttu-id="6e304-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6e304-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e304-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e304-132">-WhatIf</span></span>
<span data-ttu-id="6e304-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6e304-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e304-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6e304-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e304-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e304-135">CommonParameters</span></span>
<span data-ttu-id="6e304-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6e304-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e304-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6e304-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e304-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6e304-138">INPUTS</span></span>

### <span data-ttu-id="6e304-139">System. String</span><span class="sxs-lookup"><span data-stu-id="6e304-139">System.String</span></span>

### <span data-ttu-id="6e304-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="6e304-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="6e304-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6e304-141">OUTPUTS</span></span>

### <span data-ttu-id="6e304-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6e304-142">System.Boolean</span></span>

## <span data-ttu-id="6e304-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6e304-143">NOTES</span></span>

## <span data-ttu-id="6e304-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6e304-144">RELATED LINKS</span></span>
