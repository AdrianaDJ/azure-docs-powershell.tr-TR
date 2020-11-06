---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: A03F32C3-BB01-46A5-86C5-B7A4DDC42351
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/new-azurermnotificationhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubKey.md
ms.openlocfilehash: 66d947cc9d5765fdbfeb815019bbd739f7c3d819
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594452"
---
# <span data-ttu-id="5c724-101">New-AzureRmNotificationHubKey</span><span class="sxs-lookup"><span data-stu-id="5c724-101">New-AzureRmNotificationHubKey</span></span>

## <span data-ttu-id="5c724-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c724-102">SYNOPSIS</span></span>
<span data-ttu-id="5c724-103">Bir NotificationHub için yetkilendirme kuralı anahtarını yeniden üretin.</span><span class="sxs-lookup"><span data-stu-id="5c724-103">Regenerate the Authorization Rule Key for a NotificationHub .</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5c724-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5c724-104">SYNTAX</span></span>

```
New-AzureRmNotificationHubKey [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [[-AuthorizationRule] <String>] [-PolicyKey] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c724-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5c724-105">DESCRIPTION</span></span>
<span data-ttu-id="5c724-106">New-AzureRmNotificationHubKey cmdlet, NotificationHub yetkilendirme kuralı için birincil anahtar/Ikincil anahtarı yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5c724-106">New-AzureRmNotificationHubKey cmdlet regenerates the Primary Key/Secondary Key for the NotificationHub Authorization Rule.</span></span>

## <span data-ttu-id="5c724-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5c724-107">EXAMPLES</span></span>

### <span data-ttu-id="5c724-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5c724-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="5c724-109">{{Buraya örnek açıklama ekleyin}}</span><span class="sxs-lookup"><span data-stu-id="5c724-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="5c724-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5c724-110">PARAMETERS</span></span>

### <span data-ttu-id="5c724-111">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="5c724-111">-AuthorizationRule</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c724-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c724-112">-DefaultProfile</span></span>
<span data-ttu-id="5c724-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="5c724-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5c724-114">-Force</span><span class="sxs-lookup"><span data-stu-id="5c724-114">-Force</span></span>
<span data-ttu-id="5c724-115">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="5c724-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="5c724-116">-Namespace</span><span class="sxs-lookup"><span data-stu-id="5c724-116">-Namespace</span></span>
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

### <span data-ttu-id="5c724-117">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="5c724-117">-NotificationHub</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c724-118">-PolicyKey</span><span class="sxs-lookup"><span data-stu-id="5c724-118">-PolicyKey</span></span>
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

### <span data-ttu-id="5c724-119">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5c724-119">-ResourceGroup</span></span>
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

### <span data-ttu-id="5c724-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="5c724-120">-Confirm</span></span>
<span data-ttu-id="5c724-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5c724-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c724-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c724-122">-WhatIf</span></span>
<span data-ttu-id="5c724-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5c724-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c724-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5c724-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c724-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c724-125">CommonParameters</span></span>
<span data-ttu-id="5c724-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5c724-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c724-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c724-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c724-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5c724-128">INPUTS</span></span>

### <span data-ttu-id="5c724-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="5c724-129">None</span></span>
<span data-ttu-id="5c724-130">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="5c724-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5c724-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5c724-131">OUTPUTS</span></span>

### <span data-ttu-id="5c724-132">Microsoft. Azure. Management. Notificationhub. model. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="5c724-132">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="5c724-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5c724-133">NOTES</span></span>

## <span data-ttu-id="5c724-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5c724-134">RELATED LINKS</span></span>

