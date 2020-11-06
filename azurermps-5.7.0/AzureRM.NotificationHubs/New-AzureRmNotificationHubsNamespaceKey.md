---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 1EC19069-B64C-4F0F-99A3-07C16E46C0A0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/new-azurermnotificationhubsnamespacekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespaceKey.md
ms.openlocfilehash: 4756402ab46deb0260db19474a26e2c568055187
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594048"
---
# <span data-ttu-id="5ddce-101">New-AzureRmNotificationHubsNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="5ddce-101">New-AzureRmNotificationHubsNamespaceKey</span></span>

## <span data-ttu-id="5ddce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ddce-102">SYNOPSIS</span></span>
<span data-ttu-id="5ddce-103">Ad alanı için yetkilendirme kuralı anahtarını yeniden üretin.</span><span class="sxs-lookup"><span data-stu-id="5ddce-103">Regenerate the Authorization Rule Key for a Namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ddce-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5ddce-104">SYNTAX</span></span>

```
New-AzureRmNotificationHubsNamespaceKey [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-PolicyKey] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ddce-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5ddce-105">DESCRIPTION</span></span>
<span data-ttu-id="5ddce-106">New-AzureRmNotificationHubNamespaceKey cmdlet, ad alanı yetkilendirme kuralı için birincil anahtar/Ikincil anahtarı yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5ddce-106">New-AzureRmNotificationHubNamespaceKey cmdlet regenerates the Primary Key/Secondary Key for the Namespace Authorization Rule.</span></span>

## <span data-ttu-id="5ddce-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5ddce-107">EXAMPLES</span></span>

### <span data-ttu-id="5ddce-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5ddce-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="5ddce-109">{{Buraya örnek açıklama ekleyin}}</span><span class="sxs-lookup"><span data-stu-id="5ddce-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="5ddce-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5ddce-110">PARAMETERS</span></span>

### <span data-ttu-id="5ddce-111">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="5ddce-111">-AuthorizationRule</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ddce-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ddce-112">-DefaultProfile</span></span>
<span data-ttu-id="5ddce-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="5ddce-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5ddce-114">-Force</span><span class="sxs-lookup"><span data-stu-id="5ddce-114">-Force</span></span>
<span data-ttu-id="5ddce-115">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="5ddce-115">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ddce-116">-Namespace</span><span class="sxs-lookup"><span data-stu-id="5ddce-116">-Namespace</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ddce-117">-PolicyKey</span><span class="sxs-lookup"><span data-stu-id="5ddce-117">-PolicyKey</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ddce-118">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5ddce-118">-ResourceGroup</span></span>
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

### <span data-ttu-id="5ddce-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="5ddce-119">-Confirm</span></span>
<span data-ttu-id="5ddce-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5ddce-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ddce-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ddce-121">-WhatIf</span></span>
<span data-ttu-id="5ddce-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5ddce-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ddce-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5ddce-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ddce-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ddce-124">CommonParameters</span></span>
<span data-ttu-id="5ddce-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5ddce-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ddce-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ddce-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ddce-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5ddce-127">INPUTS</span></span>

### <span data-ttu-id="5ddce-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="5ddce-128">None</span></span>
<span data-ttu-id="5ddce-129">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="5ddce-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5ddce-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5ddce-130">OUTPUTS</span></span>

### <span data-ttu-id="5ddce-131">Microsoft. Azure. Management. Notificationhub. model. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="5ddce-131">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="5ddce-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5ddce-132">NOTES</span></span>

## <span data-ttu-id="5ddce-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5ddce-133">RELATED LINKS</span></span>

