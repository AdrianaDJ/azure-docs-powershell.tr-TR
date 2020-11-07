---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareSubscription.md
ms.openlocfilehash: a2bcfa4232c7e69bdb17a5d56ff7b79373593b06
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752164"
---
# <span data-ttu-id="0c3a8-101">Remove-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="0c3a8-101">Remove-AzDataShareSubscription</span></span>

## <span data-ttu-id="0c3a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c3a8-102">SYNOPSIS</span></span>
<span data-ttu-id="0c3a8-103">paylaşım aboneliğini kaldırır</span><span class="sxs-lookup"><span data-stu-id="0c3a8-103">removes a share subscription</span></span>

## <span data-ttu-id="0c3a8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0c3a8-104">SYNTAX</span></span>

### <span data-ttu-id="0c3a8-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0c3a8-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c3a8-106">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="0c3a8-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareSubscription -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c3a8-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0c3a8-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareSubscription -InputObject <PSDataShareSubscription> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c3a8-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0c3a8-108">DESCRIPTION</span></span>
<span data-ttu-id="0c3a8-109">**Remove-AzDataShareSubscription** cmdlet 'i bir paylaşım aboneliğini kaldırır</span><span class="sxs-lookup"><span data-stu-id="0c3a8-109">The **Remove-AzDataShareSubscription** cmdlet removes a share subscription</span></span>

## <span data-ttu-id="0c3a8-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0c3a8-110">EXAMPLES</span></span>

### <span data-ttu-id="0c3a8-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0c3a8-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareSubscription -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShareSubscription"
Are you sure you want to remove sharesubscription "AdsShareSubscription"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="0c3a8-112">Bu komut, hesap WikiAds 'den bir sharesubscripın adlı bir paylaşım listesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0c3a8-112">This commands removes a sharesubscription named AdsShareSubscription from account WikiAds.</span></span> 

## <span data-ttu-id="0c3a8-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0c3a8-113">PARAMETERS</span></span>

### <span data-ttu-id="0c3a8-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0c3a8-114">-AccountName</span></span>
<span data-ttu-id="0c3a8-115">Azure veri paylaşımı hesap adı.</span><span class="sxs-lookup"><span data-stu-id="0c3a8-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="0c3a8-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="0c3a8-116">-AsJob</span></span>
<span data-ttu-id="0c3a8-117">{{Fill Iş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="0c3a8-117">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="0c3a8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c3a8-118">-DefaultProfile</span></span>
<span data-ttu-id="0c3a8-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0c3a8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c3a8-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0c3a8-120">-InputObject</span></span>
<span data-ttu-id="0c3a8-121">Azure veri paylaşımı abonelik nesnesi</span><span class="sxs-lookup"><span data-stu-id="0c3a8-121">Azure data share subscription object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0c3a8-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="0c3a8-122">-Name</span></span>
<span data-ttu-id="0c3a8-123">Azure veri paylaşımı abonelik adı</span><span class="sxs-lookup"><span data-stu-id="0c3a8-123">Azure data share subscription name</span></span>

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

### <span data-ttu-id="0c3a8-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="0c3a8-124">-PassThru</span></span>
<span data-ttu-id="0c3a8-125">Return Object (belirtilmişse).</span><span class="sxs-lookup"><span data-stu-id="0c3a8-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="0c3a8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c3a8-126">-ResourceGroupName</span></span>
<span data-ttu-id="0c3a8-127">Azure veri paylaşımı hesabının kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="0c3a8-127">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="0c3a8-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="0c3a8-128">-ResourceId</span></span>
<span data-ttu-id="0c3a8-129">Azure veri paylaşımı aboneliğinin kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="0c3a8-129">The resource id of the azure data share subscription</span></span>

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

### <span data-ttu-id="0c3a8-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="0c3a8-130">-Confirm</span></span>
<span data-ttu-id="0c3a8-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0c3a8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c3a8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c3a8-132">-WhatIf</span></span>
<span data-ttu-id="0c3a8-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0c3a8-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c3a8-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0c3a8-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c3a8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c3a8-135">CommonParameters</span></span>
<span data-ttu-id="0c3a8-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0c3a8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c3a8-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c3a8-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c3a8-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0c3a8-138">INPUTS</span></span>

### <span data-ttu-id="0c3a8-139">System. String</span><span class="sxs-lookup"><span data-stu-id="0c3a8-139">System.String</span></span>

### <span data-ttu-id="0c3a8-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="0c3a8-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="0c3a8-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0c3a8-141">OUTPUTS</span></span>

### <span data-ttu-id="0c3a8-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0c3a8-142">System.Boolean</span></span>

## <span data-ttu-id="0c3a8-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0c3a8-143">NOTES</span></span>

## <span data-ttu-id="0c3a8-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0c3a8-144">RELATED LINKS</span></span>
