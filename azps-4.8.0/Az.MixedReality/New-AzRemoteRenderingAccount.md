---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/new-azremoterenderingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzRemoteRenderingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzRemoteRenderingAccount.md
ms.openlocfilehash: 94692e40f53026e7f554dd124e112399c949205d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109940"
---
# <span data-ttu-id="fab33-101">New-AzRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="fab33-101">New-AzRemoteRenderingAccount</span></span>

## <span data-ttu-id="fab33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fab33-102">SYNOPSIS</span></span>
<span data-ttu-id="fab33-103">Uzaktan Işleme hesabı oluşturma</span><span class="sxs-lookup"><span data-stu-id="fab33-103">Create Remote Rendering Account</span></span>

## <span data-ttu-id="fab33-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fab33-104">SYNTAX</span></span>

```
New-AzRemoteRenderingAccount -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fab33-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fab33-105">DESCRIPTION</span></span>
<span data-ttu-id="fab33-106">Belirli bir abonelikte, kaynak grubunda ve bölgede yeni bir uzaktan Işleme hesabı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="fab33-106">Create a new Remote Rendering Account in certain Subscription, Resource Group and Region.</span></span>

## <span data-ttu-id="fab33-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fab33-107">EXAMPLES</span></span>

### <span data-ttu-id="fab33-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="fab33-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmRemoteRenderingAccount -ResourceGroup rg1 -Name example -Location centralus

ResourceGroupName   : rg1
AccountId           : 5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef/
AccountDomain       : mixedreality.azure.com
Tags                : {}
Location            : centralus
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/RemoteRenderingAccounts/example
Name                : example
Type                : Microsoft.MixedReality/RemoteRenderingAccounts
```

<span data-ttu-id="fab33-109">Geçerli abonelikte "örnek" yeni bir uzaktan Işleme hesabı oluştur, kaynak grubu "RG1" ve Merkezi ABD.</span><span class="sxs-lookup"><span data-stu-id="fab33-109">Create a new Remote Rendering Account "example" in current Subscription, Resource Group "rg1" and Central US.</span></span>

## <span data-ttu-id="fab33-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fab33-110">PARAMETERS</span></span>

### <span data-ttu-id="fab33-111">-Onay</span><span class="sxs-lookup"><span data-stu-id="fab33-111">-Confirm</span></span>
<span data-ttu-id="fab33-112">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fab33-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fab33-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fab33-113">-DefaultProfile</span></span>
<span data-ttu-id="fab33-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fab33-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fab33-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="fab33-115">-Location</span></span>
<span data-ttu-id="fab33-116">Uzaktan Işleme hesabı konumu.</span><span class="sxs-lookup"><span data-stu-id="fab33-116">Remote Rendering Account Location.</span></span>

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

### <span data-ttu-id="fab33-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="fab33-117">-Name</span></span>
<span data-ttu-id="fab33-118">Uzaktan Işleme hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="fab33-118">Remote Rendering Account Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RemoteRenderingAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fab33-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fab33-119">-ResourceGroupName</span></span>
<span data-ttu-id="fab33-120">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="fab33-120">Resource Group Name.</span></span>

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

### <span data-ttu-id="fab33-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fab33-121">-WhatIf</span></span>
<span data-ttu-id="fab33-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fab33-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fab33-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fab33-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fab33-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fab33-124">CommonParameters</span></span>
<span data-ttu-id="fab33-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fab33-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="fab33-126">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fab33-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fab33-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fab33-127">INPUTS</span></span>

### <span data-ttu-id="fab33-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="fab33-128">None</span></span>

## <span data-ttu-id="fab33-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fab33-129">OUTPUTS</span></span>

### <span data-ttu-id="fab33-130">Microsoft. Azure. Commands. MixedReality. RemoteRenderingAccount. PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="fab33-130">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

## <span data-ttu-id="fab33-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fab33-131">NOTES</span></span>

## <span data-ttu-id="fab33-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fab33-132">RELATED LINKS</span></span>
