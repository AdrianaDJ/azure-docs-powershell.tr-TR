---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/new-azsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/New-AzSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/New-AzSubscription.md
ms.openlocfilehash: 167678bfe84117cdc53e9e90b520abe24fed4b92
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266724"
---
# <span data-ttu-id="a9296-101">New-AzSubscription</span><span class="sxs-lookup"><span data-stu-id="a9296-101">New-AzSubscription</span></span>

## <span data-ttu-id="a9296-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9296-102">SYNOPSIS</span></span>
<span data-ttu-id="a9296-103">Azure aboneliği oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a9296-103">Creates an Azure subscription.</span></span>

## <span data-ttu-id="a9296-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a9296-104">SYNTAX</span></span>

```
New-AzSubscription -EnrollmentAccountObjectId <String> [[-Name] <String>] -OfferType <String>
 [-OwnerObjectId <String[]>] [-OwnerSignInName <String[]>] [-OwnerApplicationId <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9296-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a9296-105">DESCRIPTION</span></span>
<span data-ttu-id="a9296-106">**New-AzSubscription** cmdlet 'ı bir Azure aboneliği oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a9296-106">The **New-AzSubscription** cmdlet creates an Azure subscription.</span></span>

## <span data-ttu-id="a9296-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a9296-107">EXAMPLES</span></span>

### <span data-ttu-id="a9296-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a9296-108">Example 1</span></span>
```
PS C:\> New-AzSubscription -Name "My Subscription" -EnrollmentAccountObjectId ((Get-AzEnrollmentAccount)[0].ObjectId) -OfferType MS-AZR-0017P

Name        : My Subscription
Id          : 86869d42-1782-4337-98b0-c905fb937d46
TenantId    : a5dcb057-fd83-4384-9d49-5198004d33a5
State       : Enabled
```

<span data-ttu-id="a9296-109">Belirtilen kayıt hesabı altında belirtilen teklif türüyle bir Azure aboneliği oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a9296-109">Creates an Azure subscription under the specified enrollment account with the specified offer type.</span></span>

## <span data-ttu-id="a9296-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a9296-110">PARAMETERS</span></span>

### <span data-ttu-id="a9296-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="a9296-111">-AsJob</span></span>
<span data-ttu-id="a9296-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="a9296-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a9296-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9296-113">-DefaultProfile</span></span>
<span data-ttu-id="a9296-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a9296-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9296-115">-, Mentaccountobjectid</span><span class="sxs-lookup"><span data-stu-id="a9296-115">-EnrollmentAccountObjectId</span></span>
<span data-ttu-id="a9296-116">Aboneliği oluştururken kullanılacak kayıt hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="a9296-116">Name of the enrollment account to use when creating the subscription.</span></span>

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

### <span data-ttu-id="a9296-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="a9296-117">-Name</span></span>
<span data-ttu-id="a9296-118">Oluşturulacak aboneliğin adı.</span><span class="sxs-lookup"><span data-stu-id="a9296-118">The name of the subscription to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9296-119">-OfferType</span><span class="sxs-lookup"><span data-stu-id="a9296-119">-OfferType</span></span>
<span data-ttu-id="a9296-120">Aboneliği oluştururken kullanılacak teklifin türü.</span><span class="sxs-lookup"><span data-stu-id="a9296-120">The type of offer to use when creating the subscription.</span></span>

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

### <span data-ttu-id="a9296-121">-Ownerapplicationıd</span><span class="sxs-lookup"><span data-stu-id="a9296-121">-OwnerApplicationId</span></span>
<span data-ttu-id="a9296-122">Aboneliğe sahip erişimine izin verileceği uygulama SPN 'si.</span><span class="sxs-lookup"><span data-stu-id="a9296-122">The app SPN(s) to be granted Owner access to the subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: OwnerSPN, OwnerServicePrincipalName

Required: False
Position: Named
Default value: Name
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9296-123">-OwnerObjectId</span><span class="sxs-lookup"><span data-stu-id="a9296-123">-OwnerObjectId</span></span>
<span data-ttu-id="a9296-124">Kullanıcı veya Grup nesneleri veya Grup nesneleri, aboneliğe erişim izni verecek.</span><span class="sxs-lookup"><span data-stu-id="a9296-124">The user(s) or group object(s) id(s) to be granted Owner access to the subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: OwnerId, OwnerPrincipalId

Required: False
Position: Named
Default value: Name
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9296-125">-Ownersignınname</span><span class="sxs-lookup"><span data-stu-id="a9296-125">-OwnerSignInName</span></span>
<span data-ttu-id="a9296-126">Aboneliğe kullanıcıya sahip erişimi verilecek Kullanıcı.</span><span class="sxs-lookup"><span data-stu-id="a9296-126">The user(s) to be granted Owner access to the subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: OwnerEmail, OwnerUserPrincipalName

Required: False
Position: Named
Default value: Name
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9296-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="a9296-127">-Confirm</span></span>
<span data-ttu-id="a9296-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a9296-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9296-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9296-129">-WhatIf</span></span>
<span data-ttu-id="a9296-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a9296-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a9296-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a9296-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9296-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9296-132">CommonParameters</span></span>
<span data-ttu-id="a9296-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a9296-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9296-134">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9296-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9296-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a9296-135">INPUTS</span></span>

### <span data-ttu-id="a9296-136">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="a9296-136">None</span></span>

## <span data-ttu-id="a9296-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a9296-137">OUTPUTS</span></span>

### <span data-ttu-id="a9296-138">Microsoft. Azure. Commands. Subscription. modeller. psazuyeniden gönderme komutları</span><span class="sxs-lookup"><span data-stu-id="a9296-138">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="a9296-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a9296-139">NOTES</span></span>

## <span data-ttu-id="a9296-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a9296-140">RELATED LINKS</span></span>
