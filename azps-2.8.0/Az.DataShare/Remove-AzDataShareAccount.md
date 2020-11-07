---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatashareaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShareAccount.md
ms.openlocfilehash: 4888cacfbc92a38402bab089555ac6d6e7174038
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752177"
---
# <span data-ttu-id="c2613-101">Remove-AzDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="c2613-101">Remove-AzDataShareAccount</span></span>

## <span data-ttu-id="c2613-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2613-102">SYNOPSIS</span></span>
<span data-ttu-id="c2613-103">Datashare hesabını kaldırır</span><span class="sxs-lookup"><span data-stu-id="c2613-103">Removes a datashare account</span></span>

## <span data-ttu-id="c2613-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c2613-104">SYNTAX</span></span>

### <span data-ttu-id="c2613-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c2613-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzDataShareAccount -ResourceGroupName <String> -Name <String> [-PassThru] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2613-106">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="c2613-106">ByResourceIdParameterSet</span></span>
```
Remove-AzDataShareAccount -ResourceId <String> [-PassThru] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2613-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2613-107">ByObjectParameterSet</span></span>
```
Remove-AzDataShareAccount -InputObject <PSDataShareAccount> [-PassThru] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2613-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c2613-108">DESCRIPTION</span></span>
<span data-ttu-id="c2613-109">**Remove-AzDataShareAccount** cmdlet 'i, datashare hesabını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c2613-109">The **Remove-AzDataShareAccount** cmdlet removes a datashare account.</span></span>

## <span data-ttu-id="c2613-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c2613-110">EXAMPLES</span></span>

### <span data-ttu-id="c2613-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c2613-111">Example 1</span></span>
```
PS C:\> Remove-AzDataShareAccount -Name "WikiADS" -ResourceGroupName "ADS"
Confirm
Are you sure you want to remove datashare account 'WikiADS' in resource group 'ADS'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="c2613-112">Bu komut, ADS adlı kaynak grubundaki WikiADS adlı datashare hesabını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c2613-112">This command removes the datashare account named WikiADS from the resource group named ADS.</span></span>
<span data-ttu-id="c2613-113">Bu komut $True değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="c2613-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="c2613-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c2613-114">PARAMETERS</span></span>

### <span data-ttu-id="c2613-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="c2613-115">-AsJob</span></span>
<span data-ttu-id="c2613-116">{{Fill Iş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="c2613-116">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="c2613-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2613-117">-DefaultProfile</span></span>
<span data-ttu-id="c2613-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c2613-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2613-119">-Force</span><span class="sxs-lookup"><span data-stu-id="c2613-119">-Force</span></span>
<span data-ttu-id="c2613-120">{{Fill Force açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="c2613-120">{{Fill Force Description}}</span></span>

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

### <span data-ttu-id="c2613-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c2613-121">-InputObject</span></span>
<span data-ttu-id="c2613-122">Azure veri paylaşımı hesap nesnesi.</span><span class="sxs-lookup"><span data-stu-id="c2613-122">The azure data share account object.</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2613-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="c2613-123">-Name</span></span>
<span data-ttu-id="c2613-124">Azure veri paylaşımı hesap adı.</span><span class="sxs-lookup"><span data-stu-id="c2613-124">Azure data share account name.</span></span>

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

### <span data-ttu-id="c2613-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="c2613-125">-PassThru</span></span>
<span data-ttu-id="c2613-126">Return Object (belirtilmişse).</span><span class="sxs-lookup"><span data-stu-id="c2613-126">Return object (if specified).</span></span>

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

### <span data-ttu-id="c2613-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2613-127">-ResourceGroupName</span></span>
<span data-ttu-id="c2613-128">Azure veri paylaşımı hesabının kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="c2613-128">The resource group name of azure data share account.</span></span>

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

### <span data-ttu-id="c2613-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="c2613-129">-ResourceId</span></span>
<span data-ttu-id="c2613-130">Azure veri paylaşımı hesabının kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="c2613-130">The resource id of the azure data share account.</span></span>

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

### <span data-ttu-id="c2613-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="c2613-131">-Confirm</span></span>
<span data-ttu-id="c2613-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c2613-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2613-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2613-133">-WhatIf</span></span>
<span data-ttu-id="c2613-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c2613-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2613-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c2613-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2613-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2613-136">CommonParameters</span></span>
<span data-ttu-id="c2613-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c2613-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2613-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2613-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2613-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c2613-139">INPUTS</span></span>

### <span data-ttu-id="c2613-140">System. String</span><span class="sxs-lookup"><span data-stu-id="c2613-140">System.String</span></span>

### <span data-ttu-id="c2613-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="c2613-141">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span></span>

## <span data-ttu-id="c2613-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c2613-142">OUTPUTS</span></span>

### <span data-ttu-id="c2613-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c2613-143">System.Boolean</span></span>

## <span data-ttu-id="c2613-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c2613-144">NOTES</span></span>

## <span data-ttu-id="c2613-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c2613-145">RELATED LINKS</span></span>