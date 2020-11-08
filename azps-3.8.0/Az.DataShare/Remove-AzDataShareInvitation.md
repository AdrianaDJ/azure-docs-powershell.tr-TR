---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatashareinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareInvitation.md
ms.openlocfilehash: 19347de88b1b43c41f8ce774630e92dfc3ad592c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098347"
---
# <span data-ttu-id="f90b0-101">Remove-AzDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="f90b0-101">Remove-AzDataShareInvitation</span></span>

## <span data-ttu-id="f90b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f90b0-102">SYNOPSIS</span></span>
<span data-ttu-id="f90b0-103">daveti kaldırır</span><span class="sxs-lookup"><span data-stu-id="f90b0-103">removes an invitation</span></span>

## <span data-ttu-id="f90b0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f90b0-104">SYNTAX</span></span>

### <span data-ttu-id="f90b0-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f90b0-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f90b0-106">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="f90b0-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareInvitation -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f90b0-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f90b0-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareInvitation -InputObject <PSDataShareInvitation> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f90b0-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f90b0-108">DESCRIPTION</span></span>
<span data-ttu-id="f90b0-109">**Remove-Azdatasharedavetiyesi** cmdlet 'i bir datashare davetini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f90b0-109">The **Remove-AzDataShareInvitation** cmdlet removes a datashare invitation.</span></span>

## <span data-ttu-id="f90b0-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f90b0-110">EXAMPLES</span></span>

### <span data-ttu-id="f90b0-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f90b0-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "ADSInvite"
Are you sure you want to remove dataset mapping "ADSInvite"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="f90b0-112">Bu komut, Share AdsShare ile ADSInvite adındaki daveti kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f90b0-112">This commands removes an invitation named ADSInvite from share AdsShare.</span></span> 

## <span data-ttu-id="f90b0-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f90b0-113">PARAMETERS</span></span>

### <span data-ttu-id="f90b0-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f90b0-114">-AccountName</span></span>
<span data-ttu-id="f90b0-115">Azure veri paylaşımı hesap adı</span><span class="sxs-lookup"><span data-stu-id="f90b0-115">Azure data share account name</span></span>

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

### <span data-ttu-id="f90b0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f90b0-116">-DefaultProfile</span></span>
<span data-ttu-id="f90b0-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f90b0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f90b0-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f90b0-118">-InputObject</span></span>
<span data-ttu-id="f90b0-119">Azure veri paylaşımı davet nesnesi</span><span class="sxs-lookup"><span data-stu-id="f90b0-119">Azure data share invitation object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f90b0-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="f90b0-120">-Name</span></span>
<span data-ttu-id="f90b0-121">Azure veri paylaşımı davet adı</span><span class="sxs-lookup"><span data-stu-id="f90b0-121">Azure data share invitation name</span></span>

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

### <span data-ttu-id="f90b0-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="f90b0-122">-PassThru</span></span>
<span data-ttu-id="f90b0-123">Return Object (belirtilmişse).</span><span class="sxs-lookup"><span data-stu-id="f90b0-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="f90b0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f90b0-124">-ResourceGroupName</span></span>
<span data-ttu-id="f90b0-125">Azure veri paylaşımı hesabının kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="f90b0-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="f90b0-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="f90b0-126">-ResourceId</span></span>
<span data-ttu-id="f90b0-127">Azure veri paylaşımı davetinin kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="f90b0-127">The resource id of the azure data share invitation</span></span>

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

### <span data-ttu-id="f90b0-128">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="f90b0-128">-ShareName</span></span>
<span data-ttu-id="f90b0-129">Azure veri paylaşımı adı.</span><span class="sxs-lookup"><span data-stu-id="f90b0-129">Azure data share name.</span></span>

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

### <span data-ttu-id="f90b0-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="f90b0-130">-Confirm</span></span>
<span data-ttu-id="f90b0-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f90b0-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f90b0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f90b0-132">-WhatIf</span></span>
<span data-ttu-id="f90b0-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f90b0-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f90b0-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f90b0-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f90b0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f90b0-135">CommonParameters</span></span>
<span data-ttu-id="f90b0-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f90b0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f90b0-137">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f90b0-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f90b0-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f90b0-138">INPUTS</span></span>

### <span data-ttu-id="f90b0-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f90b0-139">System.String</span></span>

### <span data-ttu-id="f90b0-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDAtapaylaşıdavetiyesi</span><span class="sxs-lookup"><span data-stu-id="f90b0-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span></span>

## <span data-ttu-id="f90b0-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f90b0-141">OUTPUTS</span></span>

### <span data-ttu-id="f90b0-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f90b0-142">System.Boolean</span></span>

## <span data-ttu-id="f90b0-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f90b0-143">NOTES</span></span>

## <span data-ttu-id="f90b0-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f90b0-144">RELATED LINKS</span></span>
