---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShare.md
ms.openlocfilehash: f2a9f5f5689d4e0d7907df481e22c2d8864266ae
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097641"
---
# <span data-ttu-id="8c74b-101">New-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="8c74b-101">New-AzDataShare</span></span>

## <span data-ttu-id="8c74b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c74b-102">SYNOPSIS</span></span>
<span data-ttu-id="8c74b-103">Azure veri paylaşımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8c74b-103">Creates a azure data share.</span></span>

## <span data-ttu-id="8c74b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8c74b-104">SYNTAX</span></span>

```
New-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-Description <String>]
 [-TermsOfUse <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c74b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8c74b-105">DESCRIPTION</span></span>
<span data-ttu-id="8c74b-106">**New-AzDataShare** cmdlet 'i, kaynak grubu adı, hesap adı, paylaşım adı ve paylaşım türü gibi belirli bir Azure veri paylaşımı hesabında veri paylaşımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8c74b-106">The **New-AzDataShare** cmdlet creates a data share within a specified azure data share account by providing the resource group name, account name, share name and share kind.</span></span> <span data-ttu-id="8c74b-107">Açıklama ve kullanım şartları, veri paylaşımı oluşturulurken ayarlanabilir isteğe bağlı parametrelerdir.</span><span class="sxs-lookup"><span data-stu-id="8c74b-107">Description and terms of use are optional parameters that can be set while creating the data share.</span></span>

## <span data-ttu-id="8c74b-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8c74b-108">EXAMPLES</span></span>

### <span data-ttu-id="8c74b-109">Örnek 1: veri paylaşımı oluşturma</span><span class="sxs-lookup"><span data-stu-id="8c74b-109">Example 1 : Create a data share</span></span>
```
PS C:\>New-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -Name "AdsShare" -ShareKind "CopyBased" -Description "Example of description" -TermsOfUse "This should not be shared"
Name                : AdsShare
Id                  : /subscriptions/f3ead1ff-d0ab-4cf4-9a5a-86f1661d4685/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shares/AdsShare
Type                : Microsoft.DataShare/shares
CreatedAt           : 6/11/2019 12:00:00 AM
CreatedBy           : Contoso ADS
ShareKind           : CopyBased
Description         : Example of description  
ProvisioningState   : Succeeded
Terms               : This should not be shared
```

<span data-ttu-id="8c74b-110">Bu komut, kaynak grup REKLAMLARı ile ilgili açıklama ve kullanım şartları altındaki veri paylaşımı hesap WikiAdsAccount altında, tür Copyshare adlı bir veri paylaşımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8c74b-110">This command creates a data share named AdsShare of kind CopyBased in data share account WikiAdsAccount under resource group ADS with description and terms of use.</span></span>

## <span data-ttu-id="8c74b-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8c74b-111">PARAMETERS</span></span>

### <span data-ttu-id="8c74b-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8c74b-112">-AccountName</span></span>
<span data-ttu-id="8c74b-113">Azure veri paylaşımı hesap adı</span><span class="sxs-lookup"><span data-stu-id="8c74b-113">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c74b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c74b-114">-DefaultProfile</span></span>
<span data-ttu-id="8c74b-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8c74b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c74b-116">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="8c74b-116">-Description</span></span>
<span data-ttu-id="8c74b-117">Azure veri paylaşımı 'nın açıklaması</span><span class="sxs-lookup"><span data-stu-id="8c74b-117">Description of azure data share</span></span>

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

### <span data-ttu-id="8c74b-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="8c74b-118">-Name</span></span>
<span data-ttu-id="8c74b-119">Azure veri paylaşımı adı</span><span class="sxs-lookup"><span data-stu-id="8c74b-119">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c74b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c74b-120">-ResourceGroupName</span></span>
<span data-ttu-id="8c74b-121">Azure veri paylaşımı hesabının kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="8c74b-121">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c74b-122">-TermsOfUse</span><span class="sxs-lookup"><span data-stu-id="8c74b-122">-TermsOfUse</span></span>
<span data-ttu-id="8c74b-123">Azure veri paylaşımı için kullanım şartları</span><span class="sxs-lookup"><span data-stu-id="8c74b-123">Terms of use for azure data share</span></span>

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

### <span data-ttu-id="8c74b-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="8c74b-124">-Confirm</span></span>
<span data-ttu-id="8c74b-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8c74b-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c74b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c74b-126">-WhatIf</span></span>
<span data-ttu-id="8c74b-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8c74b-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c74b-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8c74b-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c74b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c74b-129">CommonParameters</span></span>
<span data-ttu-id="8c74b-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8c74b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c74b-131">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c74b-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c74b-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8c74b-132">INPUTS</span></span>

### <span data-ttu-id="8c74b-133">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="8c74b-133">None</span></span>

## <span data-ttu-id="8c74b-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8c74b-134">OUTPUTS</span></span>

### <span data-ttu-id="8c74b-135">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDAtapaylaşımı</span><span class="sxs-lookup"><span data-stu-id="8c74b-135">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="8c74b-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8c74b-136">NOTES</span></span>

## <span data-ttu-id="8c74b-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8c74b-137">RELATED LINKS</span></span>
