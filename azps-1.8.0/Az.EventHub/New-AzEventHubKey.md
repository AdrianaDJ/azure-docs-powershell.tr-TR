---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubKey.md
ms.openlocfilehash: bb66aacb406871731cb2f356c19a91e8bb27429c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760833"
---
# <span data-ttu-id="4406b-101">New-AzEventHubKey</span><span class="sxs-lookup"><span data-stu-id="4406b-101">New-AzEventHubKey</span></span>

## <span data-ttu-id="4406b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4406b-102">SYNOPSIS</span></span>
<span data-ttu-id="4406b-103">Belirtilen olay hub yetkilendirme kuralı için yeni bir birincil veya ikincil anahtar oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4406b-103">Creates a new primary or secondary key for the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="4406b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4406b-104">SYNTAX</span></span>

### <span data-ttu-id="4406b-105">NamespaceAuthorizationRuleSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4406b-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-RegenerateKey] <String> [[-KeyValue] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4406b-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="4406b-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String> [-Name] <String>
 [-RegenerateKey] <String> [[-KeyValue] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4406b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4406b-107">DESCRIPTION</span></span>
<span data-ttu-id="4406b-108">New-AzEventHubKey cmdlet 'i belirtilen olay hub 'Ları yetkilendirme kuralı için birincil veya ikincil SAS anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4406b-108">The New-AzEventHubKey cmdlet regenerates the primary or secondary SAS key for the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="4406b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4406b-109">EXAMPLES</span></span>

### <span data-ttu-id="4406b-110">Örnek 1,1-adalanı-AuthorizationRule PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="4406b-110">Example 1.1 - Namespace - AuthorizationRule PrimaryKey</span></span>
```
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="4406b-111">Cyauthrulename yetkilendirme kuralı için birincil anahtarı yeniden oluşturur \` \` .</span><span class="sxs-lookup"><span data-stu-id="4406b-111">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="4406b-112">Örnek 1,2-EventHub-AuthorizationRule PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="4406b-112">Example 1.2 - EventHub - AuthorizationRule PrimaryKey</span></span>
```
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="4406b-113">Cyauthrulename yetkilendirme kuralı için birincil anahtarı yeniden oluşturur \` \` .</span><span class="sxs-lookup"><span data-stu-id="4406b-113">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="4406b-114">Örnek 2,1-adalanı-AuthorizationRule SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="4406b-114">Example 2.1  - Namespace - AuthorizationRule SecondaryKey</span></span>
```
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

### <span data-ttu-id="4406b-115">Örnek 2,2-EventHub-AuthorizationRule SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="4406b-115">Example 2.2 - EventHub - AuthorizationRule SecondaryKey</span></span>
```
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

<span data-ttu-id="4406b-116">Cyauthrulename yetkilendirme kuralı için ikincil anahtarı yeniden oluşturur \` \` .</span><span class="sxs-lookup"><span data-stu-id="4406b-116">Regenerates the secondary key for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="4406b-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4406b-117">PARAMETERS</span></span>

### <span data-ttu-id="4406b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4406b-118">-DefaultProfile</span></span>
<span data-ttu-id="4406b-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4406b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4406b-120">-EventHub</span><span class="sxs-lookup"><span data-stu-id="4406b-120">-EventHub</span></span>
<span data-ttu-id="4406b-121">EventHub adı</span><span class="sxs-lookup"><span data-stu-id="4406b-121">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4406b-122">-KeyValue</span><span class="sxs-lookup"><span data-stu-id="4406b-122">-KeyValue</span></span>
<span data-ttu-id="4406b-123">SAS belirtecini imzalamak ve doğrulamak için Base64 ile kodlanmış 256 bit anahtar.</span><span class="sxs-lookup"><span data-stu-id="4406b-123">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4406b-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="4406b-124">-Name</span></span>
<span data-ttu-id="4406b-125">AuthorizationRule adı</span><span class="sxs-lookup"><span data-stu-id="4406b-125">AuthorizationRule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4406b-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4406b-126">-Namespace</span></span>
<span data-ttu-id="4406b-127">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="4406b-127">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4406b-128">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="4406b-128">-RegenerateKey</span></span>
<span data-ttu-id="4406b-129">Anahtarları yeniden üret-' PrimaryKey '/' SecondaryKey '</span><span class="sxs-lookup"><span data-stu-id="4406b-129">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4406b-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4406b-130">-ResourceGroupName</span></span>
<span data-ttu-id="4406b-131">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="4406b-131">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4406b-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="4406b-132">-Confirm</span></span>
<span data-ttu-id="4406b-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4406b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4406b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4406b-134">-WhatIf</span></span>
<span data-ttu-id="4406b-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4406b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4406b-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4406b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4406b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4406b-137">CommonParameters</span></span>
<span data-ttu-id="4406b-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4406b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4406b-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4406b-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4406b-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4406b-140">INPUTS</span></span>

### <span data-ttu-id="4406b-141">System. String</span><span class="sxs-lookup"><span data-stu-id="4406b-141">System.String</span></span>

## <span data-ttu-id="4406b-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4406b-142">OUTPUTS</span></span>

### <span data-ttu-id="4406b-143">Microsoft. Azure. Commands. EventHub. modeller. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="4406b-143">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="4406b-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4406b-144">NOTES</span></span>

## <span data-ttu-id="4406b-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4406b-145">RELATED LINKS</span></span>
