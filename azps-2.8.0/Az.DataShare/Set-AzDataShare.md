---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/set-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Set-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Set-AzDataShare.md
ms.openlocfilehash: f10aaca629519d40334aabdac604531b726edd69
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752158"
---
# <span data-ttu-id="6fbd6-101">Set-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="6fbd6-101">Set-AzDataShare</span></span>

## <span data-ttu-id="6fbd6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fbd6-102">SYNOPSIS</span></span>
<span data-ttu-id="6fbd6-103">Var olan veri paylaşımını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="6fbd6-103">Updates an existing data share</span></span>

## <span data-ttu-id="6fbd6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6fbd6-104">SYNTAX</span></span>

### <span data-ttu-id="6fbd6-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6fbd6-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-Description <String>]
 [-TermsOfUse <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fbd6-106">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="6fbd6-106">ByResourceIdParameterSet</span></span>
```
Set-AzDataShare -ResourceId <String> [-Description <String>] [-TermsOfUse <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fbd6-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6fbd6-107">ByObjectParameterSet</span></span>
```
Set-AzDataShare -InputObject <PSDataShare> [-Description <String>] [-TermsOfUse <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6fbd6-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="6fbd6-108">DESCRIPTION</span></span>
<span data-ttu-id="6fbd6-109">**Set-AzDataShare** cmdlet 'i, belirli bir Azure veri paylaşımı hesabında bulunan bir veri paylaşımını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="6fbd6-109">The **Set-AzDataShare** cmdlet updates a data share that exists within a specified azure data share account.</span></span>

## <span data-ttu-id="6fbd6-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6fbd6-110">EXAMPLES</span></span>

### <span data-ttu-id="6fbd6-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6fbd6-111">Example 1</span></span>
```
PS C:\> Set-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -Name "AdsShare" -Description "Updated description" -TermsOfUse "Updated terms"
Name                : AdsShare
Id                  : /subscriptions/f3ead1ff-d0ab-4cf4-9a5a-86f1661d4685/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shares/AdsShare
Type                : Microsoft.DataShare/shares
CreatedAt           : 6/11/2019 12:00:00 AM
CreatedBy           : Contoso ADS
ShareKind           : CopyBased
Description         : Updated description
ProvisioningState   : Succeeded
Terms               : Updated terms
```

<span data-ttu-id="6fbd6-112">Bu komut, AdsShare adlı bir veri paylaşımını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="6fbd6-112">This command updates an existing data share named AdsShare</span></span>

## <span data-ttu-id="6fbd6-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6fbd6-113">PARAMETERS</span></span>

### <span data-ttu-id="6fbd6-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6fbd6-114">-AccountName</span></span>
<span data-ttu-id="6fbd6-115">Azure veri paylaşımı hesap adı</span><span class="sxs-lookup"><span data-stu-id="6fbd6-115">Azure data share account name</span></span>

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

### <span data-ttu-id="6fbd6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fbd6-116">-DefaultProfile</span></span>
<span data-ttu-id="6fbd6-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6fbd6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fbd6-118">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="6fbd6-118">-Description</span></span>
<span data-ttu-id="6fbd6-119">Veri paylaşımının açıklaması</span><span class="sxs-lookup"><span data-stu-id="6fbd6-119">Description of Data Share</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fbd6-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6fbd6-120">-InputObject</span></span>
<span data-ttu-id="6fbd6-121">Azure veri paylaşımı nesnesi</span><span class="sxs-lookup"><span data-stu-id="6fbd6-121">Azure data share object</span></span>


```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6fbd6-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="6fbd6-122">-Name</span></span>
<span data-ttu-id="6fbd6-123">Azure veri paylaşımı adı</span><span class="sxs-lookup"><span data-stu-id="6fbd6-123">Azure data share name</span></span>

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

### <span data-ttu-id="6fbd6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fbd6-124">-ResourceGroupName</span></span>
<span data-ttu-id="6fbd6-125">Azure veri paylaşımı hesabının kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="6fbd6-125">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="6fbd6-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="6fbd6-126">-ResourceId</span></span>
<span data-ttu-id="6fbd6-127">Azure veri paylaşımı 'nın kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="6fbd6-127">The resource id of the azure data share</span></span>

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

### <span data-ttu-id="6fbd6-128">-TermsOfUse</span><span class="sxs-lookup"><span data-stu-id="6fbd6-128">-TermsOfUse</span></span>
<span data-ttu-id="6fbd6-129">Veri paylaşımı için kullanım koşulları</span><span class="sxs-lookup"><span data-stu-id="6fbd6-129">Terms of Use for Data Share</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fbd6-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="6fbd6-130">-Confirm</span></span>
<span data-ttu-id="6fbd6-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6fbd6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fbd6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fbd6-132">-WhatIf</span></span>
<span data-ttu-id="6fbd6-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6fbd6-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6fbd6-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6fbd6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fbd6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fbd6-135">CommonParameters</span></span>
<span data-ttu-id="6fbd6-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6fbd6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fbd6-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fbd6-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fbd6-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6fbd6-138">INPUTS</span></span>

### <span data-ttu-id="6fbd6-139">System. String</span><span class="sxs-lookup"><span data-stu-id="6fbd6-139">System.String</span></span>

### <span data-ttu-id="6fbd6-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDAtapaylaşımı</span><span class="sxs-lookup"><span data-stu-id="6fbd6-140">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="6fbd6-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6fbd6-141">OUTPUTS</span></span>

### <span data-ttu-id="6fbd6-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDAtapaylaşımı</span><span class="sxs-lookup"><span data-stu-id="6fbd6-142">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="6fbd6-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6fbd6-143">NOTES</span></span>

## <span data-ttu-id="6fbd6-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6fbd6-144">RELATED LINKS</span></span>