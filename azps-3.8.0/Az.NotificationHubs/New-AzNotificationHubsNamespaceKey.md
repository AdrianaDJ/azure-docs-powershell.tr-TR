---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 1EC19069-B64C-4F0F-99A3-07C16E46C0A0
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubsnamespacekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceKey.md
ms.openlocfilehash: a575ae0151cd28a9bcc3580a77ad3a0c79a2984b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098259"
---
# <span data-ttu-id="5cfac-101">New-AzNotificationHubsNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="5cfac-101">New-AzNotificationHubsNamespaceKey</span></span>

## <span data-ttu-id="5cfac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5cfac-102">SYNOPSIS</span></span>
<span data-ttu-id="5cfac-103">Ad alanı için yetkilendirme kuralı anahtarını yeniden üretin.</span><span class="sxs-lookup"><span data-stu-id="5cfac-103">Regenerate the Authorization Rule Key for a Namespace.</span></span>

## <span data-ttu-id="5cfac-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5cfac-104">SYNTAX</span></span>

```
New-AzNotificationHubsNamespaceKey [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-PolicyKey] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5cfac-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5cfac-105">DESCRIPTION</span></span>
<span data-ttu-id="5cfac-106">New-AzNotificationHubNamespaceKey cmdlet, ad alanı yetkilendirme kuralı için birincil anahtar/Ikincil anahtarı yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5cfac-106">New-AzNotificationHubNamespaceKey cmdlet regenerates the Primary Key/Secondary Key for the Namespace Authorization Rule.</span></span>

## <span data-ttu-id="5cfac-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5cfac-107">EXAMPLES</span></span>

### <span data-ttu-id="5cfac-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5cfac-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="5cfac-109">{{Buraya örnek açıklama ekleyin}}</span><span class="sxs-lookup"><span data-stu-id="5cfac-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="5cfac-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5cfac-110">PARAMETERS</span></span>

### <span data-ttu-id="5cfac-111">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="5cfac-111">-AuthorizationRule</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cfac-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cfac-112">-DefaultProfile</span></span>
<span data-ttu-id="5cfac-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="5cfac-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5cfac-114">-Force</span><span class="sxs-lookup"><span data-stu-id="5cfac-114">-Force</span></span>
<span data-ttu-id="5cfac-115">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="5cfac-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="5cfac-116">-Namespace</span><span class="sxs-lookup"><span data-stu-id="5cfac-116">-Namespace</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cfac-117">-PolicyKey</span><span class="sxs-lookup"><span data-stu-id="5cfac-117">-PolicyKey</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cfac-118">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5cfac-118">-ResourceGroup</span></span>
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

### <span data-ttu-id="5cfac-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="5cfac-119">-Confirm</span></span>
<span data-ttu-id="5cfac-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5cfac-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cfac-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cfac-121">-WhatIf</span></span>
<span data-ttu-id="5cfac-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5cfac-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5cfac-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5cfac-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cfac-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cfac-124">CommonParameters</span></span>
<span data-ttu-id="5cfac-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5cfac-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cfac-126">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cfac-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cfac-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5cfac-127">INPUTS</span></span>

### <span data-ttu-id="5cfac-128">System. String</span><span class="sxs-lookup"><span data-stu-id="5cfac-128">System.String</span></span>

## <span data-ttu-id="5cfac-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5cfac-129">OUTPUTS</span></span>

### <span data-ttu-id="5cfac-130">Microsoft. Azure. Management. Notificationhub. model. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="5cfac-130">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="5cfac-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5cfac-131">NOTES</span></span>

## <span data-ttu-id="5cfac-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5cfac-132">RELATED LINKS</span></span>