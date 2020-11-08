---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatashareaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareAccount.md
ms.openlocfilehash: b24fe9e6587fe50a41d601c70c2687891bea2f16
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267756"
---
# <span data-ttu-id="70e26-101">New-AzDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="70e26-101">New-AzDataShareAccount</span></span>

## <span data-ttu-id="70e26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70e26-102">SYNOPSIS</span></span>
<span data-ttu-id="70e26-103">Yeni veri paylaşımı hesabı oluşturur</span><span class="sxs-lookup"><span data-stu-id="70e26-103">Creates new data share account</span></span>

## <span data-ttu-id="70e26-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="70e26-104">SYNTAX</span></span>

```
New-AzDataShareAccount -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70e26-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="70e26-105">DESCRIPTION</span></span>
<span data-ttu-id="70e26-106">**New-AzDataShareAccount** cmdlet 'ı belirtilen Azure Resource grubunda bir datashare hesabı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="70e26-106">**New-AzDataShareAccount** cmdlet creates a datashare account in the specified Azure resource group.</span></span>

## <span data-ttu-id="70e26-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="70e26-107">EXAMPLES</span></span>

### <span data-ttu-id="70e26-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="70e26-108">Example 1</span></span>
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

<span data-ttu-id="70e26-109">"ADS" kaynak grubunda "WikiADS" adlı bir hesap oluşturur</span><span class="sxs-lookup"><span data-stu-id="70e26-109">Creates an account named "WikiADS" in resource group "ADS"</span></span>

## <span data-ttu-id="70e26-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="70e26-110">PARAMETERS</span></span>

### <span data-ttu-id="70e26-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="70e26-111">-AsJob</span></span>
<span data-ttu-id="70e26-112">{{Fill Iş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="70e26-112">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="70e26-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70e26-113">-DefaultProfile</span></span>
<span data-ttu-id="70e26-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="70e26-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70e26-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="70e26-115">-Location</span></span>
<span data-ttu-id="70e26-116">Veri paylaşımı hesabının oluşturulacağı konum.</span><span class="sxs-lookup"><span data-stu-id="70e26-116">The location in which to create the data share account.</span></span>

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

### <span data-ttu-id="70e26-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="70e26-117">-Name</span></span>
<span data-ttu-id="70e26-118">Azure veri paylaşımı hesap adı.</span><span class="sxs-lookup"><span data-stu-id="70e26-118">Azure data share account name.</span></span>

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

### <span data-ttu-id="70e26-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70e26-119">-ResourceGroupName</span></span>
<span data-ttu-id="70e26-120">Azure veri paylaşımı hesabının kaynak grubu adı uygulamasında oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="70e26-120">The resource group name of the azure data share account will be created in.</span></span>

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

### <span data-ttu-id="70e26-121">Etiketli</span><span class="sxs-lookup"><span data-stu-id="70e26-121">-Tag</span></span>
<span data-ttu-id="70e26-122">Azure veri paylaşımı hesabıyla ilişkilendirilecek Etiketler.</span><span class="sxs-lookup"><span data-stu-id="70e26-122">The tags to associate with the azure data share account.</span></span>

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

### <span data-ttu-id="70e26-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="70e26-123">-Confirm</span></span>
<span data-ttu-id="70e26-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="70e26-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70e26-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70e26-125">-WhatIf</span></span>
<span data-ttu-id="70e26-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="70e26-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70e26-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="70e26-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70e26-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70e26-128">CommonParameters</span></span>
<span data-ttu-id="70e26-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="70e26-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70e26-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="70e26-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70e26-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="70e26-131">INPUTS</span></span>

### <span data-ttu-id="70e26-132">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="70e26-132">None</span></span>

## <span data-ttu-id="70e26-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="70e26-133">OUTPUTS</span></span>

### <span data-ttu-id="70e26-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="70e26-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span></span>

## <span data-ttu-id="70e26-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="70e26-135">NOTES</span></span>

## <span data-ttu-id="70e26-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="70e26-136">RELATED LINKS</span></span>
