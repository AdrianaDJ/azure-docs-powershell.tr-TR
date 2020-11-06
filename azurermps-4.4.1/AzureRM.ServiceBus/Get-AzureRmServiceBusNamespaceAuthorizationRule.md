---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespaceAuthorizationRule.md
ms.openlocfilehash: 70b58b53b8e1ef88c59983b9da134a0fb935bcd2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590630"
---
# <span data-ttu-id="b3302-101">Get-AzureRmServiceBusNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b3302-101">Get-AzureRmServiceBusNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="b3302-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3302-102">SYNOPSIS</span></span>
<span data-ttu-id="b3302-103">Belirli bir ad alanı için belirtilen yetkilendirme kuralının açıklamasını alır.</span><span class="sxs-lookup"><span data-stu-id="b3302-103">Gets a description of the specified authorization rule for a given namespace.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3302-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b3302-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusNamespaceAuthorizationRule [-ResourceGroup] <String> -Namespace <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3302-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b3302-105">DESCRIPTION</span></span>
<span data-ttu-id="b3302-106">**Get-AzureRmServiceBusNamespaceAuthorizationRule** cmdlet 'i, verilen ad alanında belirtilen yetkilendirme kuralının açıklamasını alır.</span><span class="sxs-lookup"><span data-stu-id="b3302-106">The **Get-AzureRmServiceBusNamespaceAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given namespace.</span></span>

## <span data-ttu-id="b3302-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b3302-107">EXAMPLES</span></span>

### <span data-ttu-id="b3302-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b3302-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthorizationRuleName AuthoRule1
```

<span data-ttu-id="b3302-109">Belirtilen ad alanı için belirtilen yetkilendirme kuralı açıklamasını döndürür.</span><span class="sxs-lookup"><span data-stu-id="b3302-109">Returns the specified authorization rule description for a specified namespace.</span></span>

## <span data-ttu-id="b3302-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b3302-110">PARAMETERS</span></span>

### <span data-ttu-id="b3302-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b3302-111">-ResourceGroup</span></span>
<span data-ttu-id="b3302-112">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="b3302-112">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3302-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3302-113">-DefaultProfile</span></span>
<span data-ttu-id="b3302-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b3302-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3302-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="b3302-115">-Name</span></span>
<span data-ttu-id="b3302-116">ServiceBus ad alanı Authorizationkural adı.</span><span class="sxs-lookup"><span data-stu-id="b3302-116">ServiceBus Namespace AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3302-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b3302-117">-Namespace</span></span>
<span data-ttu-id="b3302-118">ServiceBus ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="b3302-118">ServiceBus Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3302-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3302-119">CommonParameters</span></span>
<span data-ttu-id="b3302-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b3302-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3302-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3302-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3302-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b3302-122">INPUTS</span></span>

### <span data-ttu-id="b3302-123">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b3302-123">-ResourceGroup</span></span>
 <span data-ttu-id="b3302-124">System. String</span><span class="sxs-lookup"><span data-stu-id="b3302-124">System.String</span></span>
 

### <span data-ttu-id="b3302-125">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="b3302-125">-NamespaceName</span></span>
 <span data-ttu-id="b3302-126">System. String</span><span class="sxs-lookup"><span data-stu-id="b3302-126">System.String</span></span>
 

### <span data-ttu-id="b3302-127">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="b3302-127">-AuthorizationRuleName</span></span>
 <span data-ttu-id="b3302-128">System. String</span><span class="sxs-lookup"><span data-stu-id="b3302-128">System.String</span></span>

## <span data-ttu-id="b3302-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b3302-129">OUTPUTS</span></span>

### <span data-ttu-id="b3302-130">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. ServiceBus. modeller. SharedAccessAuthorizationRuleAttributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="b3302-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="b3302-131">ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/AuthorizationRules/AuthoRule1 tür: Microsoft. ServiceBus/AuthorizationRules Name: AuthoRule1 location: Etiketler: haklar: {Listen, gönder}</span><span class="sxs-lookup"><span data-stu-id="b3302-131">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/AuthorizationRules/AuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : AuthoRule1 Location : Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="b3302-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b3302-132">NOTES</span></span>

## <span data-ttu-id="b3302-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b3302-133">RELATED LINKS</span></span>

