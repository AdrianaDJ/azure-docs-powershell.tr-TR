---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/new-azspatialanchorsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccount.md
ms.openlocfilehash: 2e4379007b296467bf86adff7c46f654eee671e1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104515"
---
# <span data-ttu-id="3af01-101">New-AzSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="3af01-101">New-AzSpatialAnchorsAccount</span></span>

## <span data-ttu-id="3af01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3af01-102">SYNOPSIS</span></span>
<span data-ttu-id="3af01-103">Uzamsal bağlayıcı hesabı oluşturma</span><span class="sxs-lookup"><span data-stu-id="3af01-103">Create Spatial Anchors Account</span></span>

## <span data-ttu-id="3af01-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3af01-104">SYNTAX</span></span>

```
New-AzSpatialAnchorsAccount -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3af01-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3af01-105">DESCRIPTION</span></span>
<span data-ttu-id="3af01-106">Belirli bir abonelikte, kaynak grubunda ve bölgede yeni bir uzamsal yönetim bilgileri hesabı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="3af01-106">Create a new Spatial Intelligence Account in certain Subscription, Resource Group and Region.</span></span>

## <span data-ttu-id="3af01-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3af01-107">EXAMPLES</span></span>

### <span data-ttu-id="3af01-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3af01-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmSpatialAnchorsAccount -ResourceGroup rg1 -Name example -Location centralus

ResourceGroupName   : rg1
AccountId           : 5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef/
AccountDomain       : mixedreality.azure.com
Tags                : {}
Location            : centralus
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/SpatialAnchorsAccounts/example
Name                : example
Type                : Microsoft.MixedReality/SpatialAnchorsAccounts
```

<span data-ttu-id="3af01-109">Geçerli abonelikte "örnek" yeni bir uzamsal bağlayıcı hesabı oluştur, kaynak grubu "RG1" ve Merkezi ABD.</span><span class="sxs-lookup"><span data-stu-id="3af01-109">Create a new Spatial Anchors Account "example" in current Subscription, Resource Group "rg1" and Central US.</span></span>

## <span data-ttu-id="3af01-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3af01-110">PARAMETERS</span></span>

### <span data-ttu-id="3af01-111">-Onay</span><span class="sxs-lookup"><span data-stu-id="3af01-111">-Confirm</span></span>
<span data-ttu-id="3af01-112">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3af01-112">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3af01-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3af01-113">-DefaultProfile</span></span>
<span data-ttu-id="3af01-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3af01-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3af01-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="3af01-115">-Location</span></span>
<span data-ttu-id="3af01-116">Uzamsal bağlayıcı hesap konumu.</span><span class="sxs-lookup"><span data-stu-id="3af01-116">Spatial Anchors Account Location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3af01-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="3af01-117">-Name</span></span>
<span data-ttu-id="3af01-118">Uzamsal bağlayıcı hesap adı.</span><span class="sxs-lookup"><span data-stu-id="3af01-118">Spatial Anchors Account Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SpatialAnchorsAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3af01-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3af01-119">-ResourceGroupName</span></span>
<span data-ttu-id="3af01-120">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="3af01-120">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3af01-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3af01-121">-WhatIf</span></span>
<span data-ttu-id="3af01-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3af01-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3af01-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3af01-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3af01-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3af01-124">CommonParameters</span></span>
<span data-ttu-id="3af01-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3af01-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="3af01-126">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3af01-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3af01-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3af01-127">INPUTS</span></span>

### <span data-ttu-id="3af01-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="3af01-128">None</span></span>

## <span data-ttu-id="3af01-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3af01-129">OUTPUTS</span></span>

### <span data-ttu-id="3af01-130">Microsoft. Azure. Commands. MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="3af01-130">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="3af01-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3af01-131">NOTES</span></span>

## <span data-ttu-id="3af01-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3af01-132">RELATED LINKS</span></span>
