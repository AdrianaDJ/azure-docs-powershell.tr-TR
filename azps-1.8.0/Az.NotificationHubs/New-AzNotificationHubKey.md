---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: A03F32C3-BB01-46A5-86C5-B7A4DDC42351
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubKey.md
ms.openlocfilehash: f426dc06d08e10d0811382b00e2072f65ebf1b0b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759902"
---
# <span data-ttu-id="9aec3-101">New-AzNotificationHubKey</span><span class="sxs-lookup"><span data-stu-id="9aec3-101">New-AzNotificationHubKey</span></span>

## <span data-ttu-id="9aec3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9aec3-102">SYNOPSIS</span></span>
<span data-ttu-id="9aec3-103">Bir NotificationHub için yetkilendirme kuralı anahtarını yeniden üretin.</span><span class="sxs-lookup"><span data-stu-id="9aec3-103">Regenerate the Authorization Rule Key for a NotificationHub .</span></span>

## <span data-ttu-id="9aec3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9aec3-104">SYNTAX</span></span>

```
New-AzNotificationHubKey [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [[-AuthorizationRule] <String>] [-PolicyKey] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9aec3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9aec3-105">DESCRIPTION</span></span>
<span data-ttu-id="9aec3-106">New-AzNotificationHubKey cmdlet, NotificationHub yetkilendirme kuralı için birincil anahtar/Ikincil anahtarı yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9aec3-106">New-AzNotificationHubKey cmdlet regenerates the Primary Key/Secondary Key for the NotificationHub Authorization Rule.</span></span>

## <span data-ttu-id="9aec3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9aec3-107">EXAMPLES</span></span>

### <span data-ttu-id="9aec3-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9aec3-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="9aec3-109">{{Buraya örnek açıklama ekleyin}}</span><span class="sxs-lookup"><span data-stu-id="9aec3-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="9aec3-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9aec3-110">PARAMETERS</span></span>

### <span data-ttu-id="9aec3-111">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="9aec3-111">-AuthorizationRule</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9aec3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9aec3-112">-DefaultProfile</span></span>
<span data-ttu-id="9aec3-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="9aec3-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9aec3-114">-Force</span><span class="sxs-lookup"><span data-stu-id="9aec3-114">-Force</span></span>
<span data-ttu-id="9aec3-115">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="9aec3-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="9aec3-116">-Namespace</span><span class="sxs-lookup"><span data-stu-id="9aec3-116">-Namespace</span></span>
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

### <span data-ttu-id="9aec3-117">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="9aec3-117">-NotificationHub</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9aec3-118">-PolicyKey</span><span class="sxs-lookup"><span data-stu-id="9aec3-118">-PolicyKey</span></span>
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

### <span data-ttu-id="9aec3-119">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9aec3-119">-ResourceGroup</span></span>
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

### <span data-ttu-id="9aec3-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="9aec3-120">-Confirm</span></span>
<span data-ttu-id="9aec3-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9aec3-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9aec3-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9aec3-122">-WhatIf</span></span>
<span data-ttu-id="9aec3-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9aec3-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9aec3-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9aec3-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9aec3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9aec3-125">CommonParameters</span></span>
<span data-ttu-id="9aec3-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9aec3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9aec3-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9aec3-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9aec3-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9aec3-128">INPUTS</span></span>

### <span data-ttu-id="9aec3-129">System. String</span><span class="sxs-lookup"><span data-stu-id="9aec3-129">System.String</span></span>

## <span data-ttu-id="9aec3-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9aec3-130">OUTPUTS</span></span>

### <span data-ttu-id="9aec3-131">Microsoft. Azure. Management. Notificationhub. model. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="9aec3-131">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="9aec3-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9aec3-132">NOTES</span></span>

## <span data-ttu-id="9aec3-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9aec3-133">RELATED LINKS</span></span>
