---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 1EC19069-B64C-4F0F-99A3-07C16E46C0A0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/new-azurermnotificationhubsnamespacekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespaceKey.md
ms.openlocfilehash: 070befe362c6730b3592eac18cf8db70cd688716
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590118"
---
# <span data-ttu-id="bde05-101">New-AzureRmNotificationHubsNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="bde05-101">New-AzureRmNotificationHubsNamespaceKey</span></span>

## <span data-ttu-id="bde05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bde05-102">SYNOPSIS</span></span>
<span data-ttu-id="bde05-103">Ad alanı için yetkilendirme kuralı anahtarını yeniden üretin.</span><span class="sxs-lookup"><span data-stu-id="bde05-103">Regenerate the Authorization Rule Key for a Namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bde05-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bde05-104">SYNTAX</span></span>

```
New-AzureRmNotificationHubsNamespaceKey [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-PolicyKey] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bde05-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bde05-105">DESCRIPTION</span></span>
<span data-ttu-id="bde05-106">New-AzureRmNotificationHubNamespaceKey cmdlet, ad alanı yetkilendirme kuralı için birincil anahtar/Ikincil anahtarı yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bde05-106">New-AzureRmNotificationHubNamespaceKey cmdlet regenerates the Primary Key/Secondary Key for the Namespace Authorization Rule.</span></span>

## <span data-ttu-id="bde05-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bde05-107">EXAMPLES</span></span>

### <span data-ttu-id="bde05-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="bde05-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="bde05-109">{{Buraya örnek açıklama ekleyin}}</span><span class="sxs-lookup"><span data-stu-id="bde05-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="bde05-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bde05-110">PARAMETERS</span></span>

### <span data-ttu-id="bde05-111">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="bde05-111">-AuthorizationRule</span></span>
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

### <span data-ttu-id="bde05-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bde05-112">-DefaultProfile</span></span>
<span data-ttu-id="bde05-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="bde05-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bde05-114">-Force</span><span class="sxs-lookup"><span data-stu-id="bde05-114">-Force</span></span>
<span data-ttu-id="bde05-115">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="bde05-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="bde05-116">-Namespace</span><span class="sxs-lookup"><span data-stu-id="bde05-116">-Namespace</span></span>
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

### <span data-ttu-id="bde05-117">-PolicyKey</span><span class="sxs-lookup"><span data-stu-id="bde05-117">-PolicyKey</span></span>
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

### <span data-ttu-id="bde05-118">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="bde05-118">-ResourceGroup</span></span>
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

### <span data-ttu-id="bde05-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="bde05-119">-Confirm</span></span>
<span data-ttu-id="bde05-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bde05-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bde05-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bde05-121">-WhatIf</span></span>
<span data-ttu-id="bde05-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bde05-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bde05-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bde05-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bde05-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bde05-124">CommonParameters</span></span>
<span data-ttu-id="bde05-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bde05-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bde05-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bde05-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bde05-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bde05-127">INPUTS</span></span>

### <span data-ttu-id="bde05-128">System. String</span><span class="sxs-lookup"><span data-stu-id="bde05-128">System.String</span></span>

## <span data-ttu-id="bde05-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bde05-129">OUTPUTS</span></span>

### <span data-ttu-id="bde05-130">Microsoft. Azure. Management. Notificationhub. model. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="bde05-130">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="bde05-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bde05-131">NOTES</span></span>

## <span data-ttu-id="bde05-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bde05-132">RELATED LINKS</span></span>
