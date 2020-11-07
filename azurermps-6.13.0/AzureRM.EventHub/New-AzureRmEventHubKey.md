---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubKey.md
ms.openlocfilehash: 891e72945e3557ad1047b007504572a981449cd9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764130"
---
# <span data-ttu-id="ea8c8-101">New-AzureRmEventHubKey</span><span class="sxs-lookup"><span data-stu-id="ea8c8-101">New-AzureRmEventHubKey</span></span>

## <span data-ttu-id="ea8c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea8c8-102">SYNOPSIS</span></span>
<span data-ttu-id="ea8c8-103">Belirtilen olay hub yetkilendirme kuralı için yeni bir birincil veya ikincil anahtar oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ea8c8-103">Creates a new primary or secondary key for the specified Event Hubs authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea8c8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ea8c8-104">SYNTAX</span></span>

### <span data-ttu-id="ea8c8-105">NamespaceAuthorizationRuleSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ea8c8-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-RegenerateKey] <String> [[-KeyValue] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea8c8-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="ea8c8-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-RegenerateKey] <String> [[-KeyValue] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea8c8-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ea8c8-107">DESCRIPTION</span></span>
<span data-ttu-id="ea8c8-108">New-AzureRmEventHubKey cmdlet 'i belirtilen olay hub 'Ları yetkilendirme kuralı için birincil veya ikincil SAS anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ea8c8-108">The New-AzureRmEventHubKey cmdlet regenerates the primary or secondary SAS key for the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="ea8c8-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ea8c8-109">EXAMPLES</span></span>

### <span data-ttu-id="ea8c8-110">Örnek 1,1-adalanı-AuthorizationRule PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="ea8c8-110">Example 1.1 - Namespace - AuthorizationRule PrimaryKey</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="ea8c8-111">Cyauthrulename yetkilendirme kuralı için birincil anahtarı yeniden oluşturur \` \` .</span><span class="sxs-lookup"><span data-stu-id="ea8c8-111">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="ea8c8-112">Örnek 1,2-EventHub-AuthorizationRule PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="ea8c8-112">Example 1.2 - EventHub - AuthorizationRule PrimaryKey</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="ea8c8-113">Cyauthrulename yetkilendirme kuralı için birincil anahtarı yeniden oluşturur \` \` .</span><span class="sxs-lookup"><span data-stu-id="ea8c8-113">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="ea8c8-114">Örnek 2,1-adalanı-AuthorizationRule SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="ea8c8-114">Example 2.1  - Namespace - AuthorizationRule SecondaryKey</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

### <span data-ttu-id="ea8c8-115">Örnek 2,2-EventHub-AuthorizationRule SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="ea8c8-115">Example 2.2 - EventHub - AuthorizationRule SecondaryKey</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

<span data-ttu-id="ea8c8-116">Cyauthrulename yetkilendirme kuralı için ikincil anahtarı yeniden oluşturur \` \` .</span><span class="sxs-lookup"><span data-stu-id="ea8c8-116">Regenerates the secondary key for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="ea8c8-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ea8c8-117">PARAMETERS</span></span>

### <span data-ttu-id="ea8c8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea8c8-118">-DefaultProfile</span></span>
<span data-ttu-id="ea8c8-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ea8c8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea8c8-120">-EventHub</span><span class="sxs-lookup"><span data-stu-id="ea8c8-120">-EventHub</span></span>
<span data-ttu-id="ea8c8-121">EventHub adı</span><span class="sxs-lookup"><span data-stu-id="ea8c8-121">EventHub Name</span></span>

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

### <span data-ttu-id="ea8c8-122">-KeyValue</span><span class="sxs-lookup"><span data-stu-id="ea8c8-122">-KeyValue</span></span>
<span data-ttu-id="ea8c8-123">SAS belirtecini imzalamak ve doğrulamak için Base64 ile kodlanmış 256 bit anahtar.</span><span class="sxs-lookup"><span data-stu-id="ea8c8-123">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

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

### <span data-ttu-id="ea8c8-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="ea8c8-124">-Name</span></span>
<span data-ttu-id="ea8c8-125">AuthorizationRule adı</span><span class="sxs-lookup"><span data-stu-id="ea8c8-125">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="ea8c8-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ea8c8-126">-Namespace</span></span>
<span data-ttu-id="ea8c8-127">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="ea8c8-127">Namespace Name</span></span>

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

### <span data-ttu-id="ea8c8-128">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="ea8c8-128">-RegenerateKey</span></span>
<span data-ttu-id="ea8c8-129">Anahtarları yeniden üret-' PrimaryKey '/' SecondaryKey '</span><span class="sxs-lookup"><span data-stu-id="ea8c8-129">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'</span></span>

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

### <span data-ttu-id="ea8c8-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea8c8-130">-ResourceGroupName</span></span>
<span data-ttu-id="ea8c8-131">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="ea8c8-131">Resource Group Name</span></span>

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

### <span data-ttu-id="ea8c8-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="ea8c8-132">-Confirm</span></span>
<span data-ttu-id="ea8c8-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ea8c8-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea8c8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea8c8-134">-WhatIf</span></span>
<span data-ttu-id="ea8c8-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ea8c8-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea8c8-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ea8c8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea8c8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea8c8-137">CommonParameters</span></span>
<span data-ttu-id="ea8c8-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ea8c8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea8c8-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea8c8-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea8c8-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ea8c8-140">INPUTS</span></span>

### <span data-ttu-id="ea8c8-141">System. String</span><span class="sxs-lookup"><span data-stu-id="ea8c8-141">System.String</span></span>

## <span data-ttu-id="ea8c8-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ea8c8-142">OUTPUTS</span></span>

### <span data-ttu-id="ea8c8-143">Microsoft. Azure. Commands. EventHub. modeller. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="ea8c8-143">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="ea8c8-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ea8c8-144">NOTES</span></span>

## <span data-ttu-id="ea8c8-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ea8c8-145">RELATED LINKS</span></span>
