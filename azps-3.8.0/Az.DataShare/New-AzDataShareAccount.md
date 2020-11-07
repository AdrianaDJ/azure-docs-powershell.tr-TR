---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatashareaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareAccount.md
ms.openlocfilehash: 2b3eda3aadca93415d93154a9a70361c789c94ce
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937444"
---
# <span data-ttu-id="f4091-101">New-AzDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="f4091-101">New-AzDataShareAccount</span></span>

## <span data-ttu-id="f4091-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4091-102">SYNOPSIS</span></span>
<span data-ttu-id="f4091-103">Yeni veri paylaşımı hesabı oluşturur</span><span class="sxs-lookup"><span data-stu-id="f4091-103">Creates new data share account</span></span>

## <span data-ttu-id="f4091-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f4091-104">SYNTAX</span></span>

```
New-AzDataShareAccount -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4091-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f4091-105">DESCRIPTION</span></span>
<span data-ttu-id="f4091-106">**New-AzDataShareAccount** cmdlet 'ı belirtilen Azure Resource grubunda bir datashare hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f4091-106">**New-AzDataShareAccount** cmdlet creates a datashare account in the specified Azure resource group.</span></span>

## <span data-ttu-id="f4091-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f4091-107">EXAMPLES</span></span>

### <span data-ttu-id="f4091-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f4091-108">Example 1</span></span>
```
PS C:\> New-AzDataShareAccount -ResourceGroupName "ADS" -Name "WikiADS" -Location "WestUS"
DataShareAccountName   : WikiADS
ResourceGroupName : ADS
Location          : WestUS
ProvisioningState : Succeeded
Tags              : {}
Identity          : Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSIdentity
Type              : Microsoft.DataShare/accounts
Id                : /subscriptions/4834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiADS
```

<span data-ttu-id="f4091-109">"ADS" kaynak grubunda "WikiADS" adlı bir hesap oluşturur</span><span class="sxs-lookup"><span data-stu-id="f4091-109">Creates an account named "WikiADS" in resource group "ADS"</span></span>

## <span data-ttu-id="f4091-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f4091-110">PARAMETERS</span></span>

### <span data-ttu-id="f4091-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="f4091-111">-AsJob</span></span>
<span data-ttu-id="f4091-112">{{Fill Iş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="f4091-112">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="f4091-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4091-113">-DefaultProfile</span></span>
<span data-ttu-id="f4091-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f4091-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4091-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="f4091-115">-Location</span></span>
<span data-ttu-id="f4091-116">Veri paylaşımı hesabının oluşturulacağı konum.</span><span class="sxs-lookup"><span data-stu-id="f4091-116">The location in which to create the data share account.</span></span>

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

### <span data-ttu-id="f4091-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="f4091-117">-Name</span></span>
<span data-ttu-id="f4091-118">Azure veri paylaşımı hesap adı.</span><span class="sxs-lookup"><span data-stu-id="f4091-118">Azure data share account name.</span></span>

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

### <span data-ttu-id="f4091-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4091-119">-ResourceGroupName</span></span>
<span data-ttu-id="f4091-120">Azure veri paylaşımı hesabının kaynak grubu adı uygulamasında oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="f4091-120">The resource group name of the azure data share account will be created in.</span></span>

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

### <span data-ttu-id="f4091-121">Etiketli</span><span class="sxs-lookup"><span data-stu-id="f4091-121">-Tag</span></span>
<span data-ttu-id="f4091-122">Azure veri paylaşımı hesabıyla ilişkilendirilecek Etiketler.</span><span class="sxs-lookup"><span data-stu-id="f4091-122">The tags to associate with the azure data share account.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4091-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="f4091-123">-Confirm</span></span>
<span data-ttu-id="f4091-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f4091-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4091-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4091-125">-WhatIf</span></span>
<span data-ttu-id="f4091-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f4091-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4091-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f4091-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4091-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4091-128">CommonParameters</span></span>
<span data-ttu-id="f4091-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f4091-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4091-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4091-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4091-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f4091-131">INPUTS</span></span>

### <span data-ttu-id="f4091-132">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="f4091-132">None</span></span>

## <span data-ttu-id="f4091-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f4091-133">OUTPUTS</span></span>

### <span data-ttu-id="f4091-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="f4091-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span></span>

## <span data-ttu-id="f4091-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f4091-135">NOTES</span></span>

## <span data-ttu-id="f4091-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f4091-136">RELATED LINKS</span></span>
