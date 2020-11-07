---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSet.md
ms.openlocfilehash: 122d5118761e3a4b7a400b4bc73daa29d218c4ea
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752174"
---
# <span data-ttu-id="89ad2-101">Remove-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="89ad2-101">Remove-AzDataShareDataSet</span></span>

## <span data-ttu-id="89ad2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89ad2-102">SYNOPSIS</span></span>
<span data-ttu-id="89ad2-103">Veri kümesi eşlemesini kaldırır</span><span class="sxs-lookup"><span data-stu-id="89ad2-103">Removes a dataset mapping</span></span>

## <span data-ttu-id="89ad2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="89ad2-104">SYNTAX</span></span>

### <span data-ttu-id="89ad2-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="89ad2-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89ad2-106">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="89ad2-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareDataSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89ad2-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="89ad2-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareDataSet -InputObject <PSDataShareDataSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89ad2-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="89ad2-108">DESCRIPTION</span></span>
<span data-ttu-id="89ad2-109">**Remove-AzDataShareDataSet** cmdlet 'i bir veri kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="89ad2-109">The **Remove-AzDataShareDataSet** cmdlet removes a dataset.</span></span>

## <span data-ttu-id="89ad2-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="89ad2-110">EXAMPLES</span></span>

### <span data-ttu-id="89ad2-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="89ad2-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSet -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "DS"
Are you sure you want to remove dataset mapping "DS"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="89ad2-112">Bu komut, DS adındaki veri kümesini Paylaş.</span><span class="sxs-lookup"><span data-stu-id="89ad2-112">This commands removes the dataset named DS from share WikiAds.</span></span> 

## <span data-ttu-id="89ad2-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="89ad2-113">PARAMETERS</span></span>

### <span data-ttu-id="89ad2-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="89ad2-114">-AccountName</span></span>
<span data-ttu-id="89ad2-115">Azure veri paylaşımı hesap adı.</span><span class="sxs-lookup"><span data-stu-id="89ad2-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="89ad2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89ad2-116">-DefaultProfile</span></span>
<span data-ttu-id="89ad2-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="89ad2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89ad2-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="89ad2-118">-InputObject</span></span>
<span data-ttu-id="89ad2-119">Azure veri kümesi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="89ad2-119">The azure data set object.</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89ad2-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="89ad2-120">-Name</span></span>
<span data-ttu-id="89ad2-121">Azure veri kümesi adı.</span><span class="sxs-lookup"><span data-stu-id="89ad2-121">Azure data set name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89ad2-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="89ad2-122">-PassThru</span></span>
<span data-ttu-id="89ad2-123">Return Object (belirtilmişse).</span><span class="sxs-lookup"><span data-stu-id="89ad2-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="89ad2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89ad2-124">-ResourceGroupName</span></span>
<span data-ttu-id="89ad2-125">Azure veri paylaşımı hesabının kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="89ad2-125">The resource group name of the azure data share account.</span></span>

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

### <span data-ttu-id="89ad2-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="89ad2-126">-ResourceId</span></span>
<span data-ttu-id="89ad2-127">Azure veri kümesinin kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="89ad2-127">The resource id of the azure data set.</span></span>

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

### <span data-ttu-id="89ad2-128">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="89ad2-128">-ShareName</span></span>
<span data-ttu-id="89ad2-129">Azure veri paylaşımı adı.</span><span class="sxs-lookup"><span data-stu-id="89ad2-129">Azure data share name.</span></span>

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

### <span data-ttu-id="89ad2-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="89ad2-130">-Confirm</span></span>
<span data-ttu-id="89ad2-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="89ad2-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89ad2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89ad2-132">-WhatIf</span></span>
<span data-ttu-id="89ad2-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="89ad2-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89ad2-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="89ad2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89ad2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89ad2-135">CommonParameters</span></span>
<span data-ttu-id="89ad2-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="89ad2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89ad2-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89ad2-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89ad2-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="89ad2-138">INPUTS</span></span>

### <span data-ttu-id="89ad2-139">System. String</span><span class="sxs-lookup"><span data-stu-id="89ad2-139">System.String</span></span>

### <span data-ttu-id="89ad2-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="89ad2-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="89ad2-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="89ad2-141">OUTPUTS</span></span>

### <span data-ttu-id="89ad2-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="89ad2-142">System.Boolean</span></span>

## <span data-ttu-id="89ad2-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="89ad2-143">NOTES</span></span>

## <span data-ttu-id="89ad2-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="89ad2-144">RELATED LINKS</span></span>
