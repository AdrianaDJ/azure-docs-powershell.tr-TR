---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubKey.md
ms.openlocfilehash: 8be39cb4b4b173d3b87efbf0b7ecea72ae233061
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763056"
---
# <span data-ttu-id="8fd8e-101">New-AzureRmEventHubKey</span><span class="sxs-lookup"><span data-stu-id="8fd8e-101">New-AzureRmEventHubKey</span></span>

## <span data-ttu-id="8fd8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8fd8e-102">SYNOPSIS</span></span>
<span data-ttu-id="8fd8e-103">Belirtilen olay hub yetkilendirme kuralı için yeni bir birincil veya ikincil anahtar oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8fd8e-103">Creates a new primary or secondary key for the specified Event Hubs authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8fd8e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8fd8e-104">SYNTAX</span></span>

### <span data-ttu-id="8fd8e-105">NamespaceAuthorizationRuleSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8fd8e-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-RegenerateKey] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8fd8e-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="8fd8e-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-RegenerateKey] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8fd8e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="8fd8e-107">DESCRIPTION</span></span>
<span data-ttu-id="8fd8e-108">New-AzureRmEventHubKey cmdlet 'i belirtilen olay hub 'Ları yetkilendirme kuralı için birincil veya ikincil SAS anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8fd8e-108">The New-AzureRmEventHubKey cmdlet regenerates the primary or secondary SAS key for the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="8fd8e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8fd8e-109">EXAMPLES</span></span>

### <span data-ttu-id="8fd8e-110">Örnek 1,1</span><span class="sxs-lookup"><span data-stu-id="8fd8e-110">Example 1.1</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="8fd8e-111">Cyauthrulename yetkilendirme kuralı için birincil anahtarı yeniden oluşturur \` \` .</span><span class="sxs-lookup"><span data-stu-id="8fd8e-111">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="8fd8e-112">Örnek 1,2</span><span class="sxs-lookup"><span data-stu-id="8fd8e-112">Example 1.2</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="8fd8e-113">Cyauthrulename yetkilendirme kuralı için birincil anahtarı yeniden oluşturur \` \` .</span><span class="sxs-lookup"><span data-stu-id="8fd8e-113">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="8fd8e-114">Örnek 2,1</span><span class="sxs-lookup"><span data-stu-id="8fd8e-114">Example 2.1</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

### <span data-ttu-id="8fd8e-115">Örnek 2,2</span><span class="sxs-lookup"><span data-stu-id="8fd8e-115">Example 2.2</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

<span data-ttu-id="8fd8e-116">Cyauthrulename yetkilendirme kuralı için ikincil anahtarı yeniden oluşturur \` \` .</span><span class="sxs-lookup"><span data-stu-id="8fd8e-116">Regenerates the secondary key for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="8fd8e-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8fd8e-117">PARAMETERS</span></span>

### <span data-ttu-id="8fd8e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fd8e-118">-DefaultProfile</span></span>
<span data-ttu-id="8fd8e-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8fd8e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fd8e-120">-EventHub</span><span class="sxs-lookup"><span data-stu-id="8fd8e-120">-EventHub</span></span>
<span data-ttu-id="8fd8e-121">EventHub adı</span><span class="sxs-lookup"><span data-stu-id="8fd8e-121">EventHub Name</span></span>

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fd8e-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="8fd8e-122">-Name</span></span>
<span data-ttu-id="8fd8e-123">AuthorizationRule adı</span><span class="sxs-lookup"><span data-stu-id="8fd8e-123">AuthorizationRule Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fd8e-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8fd8e-124">-Namespace</span></span>
<span data-ttu-id="8fd8e-125">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="8fd8e-125">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fd8e-126">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="8fd8e-126">-RegenerateKey</span></span>
<span data-ttu-id="8fd8e-127">Anahtarları yeniden üret-' PrimaryKey '/' SecondaryKey '</span><span class="sxs-lookup"><span data-stu-id="8fd8e-127">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fd8e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fd8e-128">-ResourceGroupName</span></span>
<span data-ttu-id="8fd8e-129">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="8fd8e-129">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fd8e-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="8fd8e-130">-Confirm</span></span>
<span data-ttu-id="8fd8e-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8fd8e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8fd8e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8fd8e-132">-WhatIf</span></span>
<span data-ttu-id="8fd8e-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8fd8e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8fd8e-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8fd8e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8fd8e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fd8e-135">CommonParameters</span></span>
<span data-ttu-id="8fd8e-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8fd8e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="8fd8e-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fd8e-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fd8e-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8fd8e-138">INPUTS</span></span>

### <span data-ttu-id="8fd8e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="8fd8e-139">System.String</span></span>


## <span data-ttu-id="8fd8e-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8fd8e-140">OUTPUTS</span></span>

### <span data-ttu-id="8fd8e-141">Microsoft. Azure. Commands. EventHub. modeller. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="8fd8e-141">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span></span>


## <span data-ttu-id="8fd8e-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8fd8e-142">NOTES</span></span>

## <span data-ttu-id="8fd8e-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8fd8e-143">RELATED LINKS</span></span>
