---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatashareinvitation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareInvitation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareInvitation.md
ms.openlocfilehash: 9aee75f06ca1c97b691ae607e4c9eaa3accd74e4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752167"
---
# <span data-ttu-id="dff65-101">Remove-AzDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="dff65-101">Remove-AzDataShareInvitation</span></span>

## <span data-ttu-id="dff65-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dff65-102">SYNOPSIS</span></span>
<span data-ttu-id="dff65-103">daveti kaldırır</span><span class="sxs-lookup"><span data-stu-id="dff65-103">removes an invitation</span></span>

## <span data-ttu-id="dff65-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dff65-104">SYNTAX</span></span>

### <span data-ttu-id="dff65-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="dff65-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareInvitation -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dff65-106">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="dff65-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareInvitation -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dff65-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dff65-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareInvitation -InputObject <PSDataShareInvitation> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dff65-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="dff65-108">DESCRIPTION</span></span>
<span data-ttu-id="dff65-109">**Remove-Azdatasharedavetiyesi** cmdlet 'i bir datashare davetini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="dff65-109">The **Remove-AzDataShareInvitation** cmdlet removes a datashare invitation.</span></span>

## <span data-ttu-id="dff65-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dff65-110">EXAMPLES</span></span>

### <span data-ttu-id="dff65-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="dff65-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "ADSInvite"
Are you sure you want to remove dataset mapping "ADSInvite"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="dff65-112">Bu komut, Share AdsShare ile ADSInvite adındaki daveti kaldırır.</span><span class="sxs-lookup"><span data-stu-id="dff65-112">This commands removes an invitation named ADSInvite from share AdsShare.</span></span> 

## <span data-ttu-id="dff65-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dff65-113">PARAMETERS</span></span>

### <span data-ttu-id="dff65-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="dff65-114">-AccountName</span></span>
<span data-ttu-id="dff65-115">Azure veri paylaşımı hesap adı</span><span class="sxs-lookup"><span data-stu-id="dff65-115">Azure data share account name</span></span>

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

### <span data-ttu-id="dff65-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dff65-116">-DefaultProfile</span></span>
<span data-ttu-id="dff65-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dff65-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dff65-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dff65-118">-InputObject</span></span>
<span data-ttu-id="dff65-119">Azure veri paylaşımı davet nesnesi</span><span class="sxs-lookup"><span data-stu-id="dff65-119">Azure data share invitation object</span></span>


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

### <span data-ttu-id="dff65-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="dff65-120">-Name</span></span>
<span data-ttu-id="dff65-121">Azure veri paylaşımı davet adı</span><span class="sxs-lookup"><span data-stu-id="dff65-121">Azure data share invitation name</span></span>

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

### <span data-ttu-id="dff65-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="dff65-122">-PassThru</span></span>
<span data-ttu-id="dff65-123">Return Object (belirtilmişse).</span><span class="sxs-lookup"><span data-stu-id="dff65-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="dff65-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dff65-124">-ResourceGroupName</span></span>
<span data-ttu-id="dff65-125">Azure veri paylaşımı hesabının kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="dff65-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="dff65-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="dff65-126">-ResourceId</span></span>
<span data-ttu-id="dff65-127">Azure veri paylaşımı davetinin kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="dff65-127">The resource id of the azure data share invitation</span></span>

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

### <span data-ttu-id="dff65-128">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="dff65-128">-ShareName</span></span>
<span data-ttu-id="dff65-129">Azure veri paylaşımı adı.</span><span class="sxs-lookup"><span data-stu-id="dff65-129">Azure data share name.</span></span>

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

### <span data-ttu-id="dff65-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="dff65-130">-Confirm</span></span>
<span data-ttu-id="dff65-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="dff65-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dff65-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dff65-132">-WhatIf</span></span>
<span data-ttu-id="dff65-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dff65-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dff65-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="dff65-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dff65-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dff65-135">CommonParameters</span></span>
<span data-ttu-id="dff65-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dff65-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dff65-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dff65-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dff65-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dff65-138">INPUTS</span></span>

### <span data-ttu-id="dff65-139">System. String</span><span class="sxs-lookup"><span data-stu-id="dff65-139">System.String</span></span>

### <span data-ttu-id="dff65-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDAtapaylaşıdavetiyesi</span><span class="sxs-lookup"><span data-stu-id="dff65-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span></span>

## <span data-ttu-id="dff65-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dff65-141">OUTPUTS</span></span>

### <span data-ttu-id="dff65-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dff65-142">System.Boolean</span></span>

## <span data-ttu-id="dff65-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dff65-143">NOTES</span></span>

## <span data-ttu-id="dff65-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dff65-144">RELATED LINKS</span></span>
