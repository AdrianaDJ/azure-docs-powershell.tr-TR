---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubKey.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: f4f28ee3f07127803e6187f00565ee8d4caf3084
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594715"
---
# <span data-ttu-id="2316f-101">Get-AzureRmEventHubKey</span><span class="sxs-lookup"><span data-stu-id="2316f-101">Get-AzureRmEventHubKey</span></span>

## <span data-ttu-id="2316f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2316f-102">SYNOPSIS</span></span>
<span data-ttu-id="2316f-103">Belirtilen olay hub yetkilendirme kuralının birincil anahtar ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="2316f-103">Gets the primary key details of the specified Event Hubs authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2316f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2316f-104">SYNTAX</span></span>

### <span data-ttu-id="2316f-105">NamespaceAuthorizationRuleSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2316f-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmEventHubKey [-ResourceGroupName] <String> -Namespace <String> -Name <String>
```

### <span data-ttu-id="2316f-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="2316f-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace <String>] -EventHub <String> -Name <String>
```

## <span data-ttu-id="2316f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="2316f-107">DESCRIPTION</span></span>
<span data-ttu-id="2316f-108">Get-AzureRmEventHubKey cmdlet 'i, belirtilen olay hub yetkilendirme kuralının birincil ve Ikincil ConnectionString ve anahtar ayrıntılarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="2316f-108">The Get-AzureRmEventHubKey cmdlet returns Primary and Secondary connectionstrings and keys details of the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="2316f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2316f-109">EXAMPLES</span></span>

### <span data-ttu-id="2316f-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2316f-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="2316f-111">Birincil ve Ikincil ConnectionString 'in ayrıntılarını ve \` myauthrulename yetkilendirme kuralı için anahtarları alır \` .</span><span class="sxs-lookup"><span data-stu-id="2316f-111">Gets details of Primary and Secondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="2316f-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2316f-112">PARAMETERS</span></span>

### <span data-ttu-id="2316f-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2316f-113">-ResourceGroupName</span></span>
<span data-ttu-id="2316f-114">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="2316f-114">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2316f-115">-EventHub</span><span class="sxs-lookup"><span data-stu-id="2316f-115">-EventHub</span></span>
<span data-ttu-id="2316f-116">EventHub adı.</span><span class="sxs-lookup"><span data-stu-id="2316f-116">EventHub Name.</span></span>

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2316f-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="2316f-117">-Name</span></span>
<span data-ttu-id="2316f-118">AuthorizationRule adı.</span><span class="sxs-lookup"><span data-stu-id="2316f-118">AuthorizationRule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2316f-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2316f-119">-Namespace</span></span>
<span data-ttu-id="2316f-120">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="2316f-120">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: NamespaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="2316f-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2316f-121">INPUTS</span></span>

### <span data-ttu-id="2316f-122">System. String</span><span class="sxs-lookup"><span data-stu-id="2316f-122">System.String</span></span>

## <span data-ttu-id="2316f-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2316f-123">OUTPUTS</span></span>

### <span data-ttu-id="2316f-124">Microsoft. Azure. Commands. EventHub. modeller. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="2316f-124">Microsoft.Azure.Commands.EventHub.Models.ListKeysAttributes</span></span>

## <span data-ttu-id="2316f-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2316f-125">NOTES</span></span>

## <span data-ttu-id="2316f-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2316f-126">RELATED LINKS</span></span>

