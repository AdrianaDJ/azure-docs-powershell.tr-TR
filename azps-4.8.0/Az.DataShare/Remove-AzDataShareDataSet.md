---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareDataSet.md
ms.openlocfilehash: c3d5105fc3b43a3f6b7ff8b45c5ba8236fed656b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108338"
---
# <span data-ttu-id="8984e-101">Remove-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="8984e-101">Remove-AzDataShareDataSet</span></span>

## <span data-ttu-id="8984e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8984e-102">SYNOPSIS</span></span>
<span data-ttu-id="8984e-103">Veri kümesi eşlemesini kaldırır</span><span class="sxs-lookup"><span data-stu-id="8984e-103">Removes a dataset mapping</span></span>

## <span data-ttu-id="8984e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8984e-104">SYNTAX</span></span>

### <span data-ttu-id="8984e-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8984e-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8984e-106">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="8984e-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareDataSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8984e-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8984e-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareDataSet -InputObject <PSDataShareDataSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8984e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="8984e-108">DESCRIPTION</span></span>
<span data-ttu-id="8984e-109">**Remove-AzDataShareDataSet** cmdlet 'i bir veri kümesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8984e-109">The **Remove-AzDataShareDataSet** cmdlet removes a dataset.</span></span>

## <span data-ttu-id="8984e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8984e-110">EXAMPLES</span></span>

### <span data-ttu-id="8984e-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8984e-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSet -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "DS"
Are you sure you want to remove dataset mapping "DS"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="8984e-112">Bu komut, DS adındaki veri kümesini Paylaş.</span><span class="sxs-lookup"><span data-stu-id="8984e-112">This commands removes the dataset named DS from share WikiAds.</span></span> 

## <span data-ttu-id="8984e-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8984e-113">PARAMETERS</span></span>

### <span data-ttu-id="8984e-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8984e-114">-AccountName</span></span>
<span data-ttu-id="8984e-115">Azure veri paylaşımı hesap adı.</span><span class="sxs-lookup"><span data-stu-id="8984e-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="8984e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8984e-116">-DefaultProfile</span></span>
<span data-ttu-id="8984e-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8984e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8984e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8984e-118">-InputObject</span></span>
<span data-ttu-id="8984e-119">Azure veri kümesi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="8984e-119">The azure data set object.</span></span>


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

### <span data-ttu-id="8984e-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="8984e-120">-Name</span></span>
<span data-ttu-id="8984e-121">Azure veri kümesi adı.</span><span class="sxs-lookup"><span data-stu-id="8984e-121">Azure data set name.</span></span>

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

### <span data-ttu-id="8984e-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="8984e-122">-PassThru</span></span>
<span data-ttu-id="8984e-123">Return Object (belirtilmişse).</span><span class="sxs-lookup"><span data-stu-id="8984e-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="8984e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8984e-124">-ResourceGroupName</span></span>
<span data-ttu-id="8984e-125">Azure veri paylaşımı hesabının kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="8984e-125">The resource group name of the azure data share account.</span></span>

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

### <span data-ttu-id="8984e-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="8984e-126">-ResourceId</span></span>
<span data-ttu-id="8984e-127">Azure veri kümesinin kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="8984e-127">The resource id of the azure data set.</span></span>

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

### <span data-ttu-id="8984e-128">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="8984e-128">-ShareName</span></span>
<span data-ttu-id="8984e-129">Azure veri paylaşımı adı.</span><span class="sxs-lookup"><span data-stu-id="8984e-129">Azure data share name.</span></span>

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

### <span data-ttu-id="8984e-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="8984e-130">-Confirm</span></span>
<span data-ttu-id="8984e-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8984e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8984e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8984e-132">-WhatIf</span></span>
<span data-ttu-id="8984e-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8984e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8984e-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8984e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8984e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8984e-135">CommonParameters</span></span>
<span data-ttu-id="8984e-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8984e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8984e-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="8984e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8984e-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8984e-138">INPUTS</span></span>

### <span data-ttu-id="8984e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="8984e-139">System.String</span></span>

### <span data-ttu-id="8984e-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="8984e-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="8984e-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8984e-141">OUTPUTS</span></span>

### <span data-ttu-id="8984e-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8984e-142">System.Boolean</span></span>

## <span data-ttu-id="8984e-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8984e-143">NOTES</span></span>

## <span data-ttu-id="8984e-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8984e-144">RELATED LINKS</span></span>
