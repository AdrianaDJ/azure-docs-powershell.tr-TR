---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D7B2CDFF-D9A2-48C7-B331-132A6A6843CA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 10fdb8920164857b42ac57a3c989417c2a967ab9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105614"
---
# <span data-ttu-id="b5f33-101">Get-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b5f33-101">Get-AzureSBAuthorizationRule</span></span>

## <span data-ttu-id="b5f33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5f33-102">SYNOPSIS</span></span>
<span data-ttu-id="b5f33-103">Hizmet veri yolu yetkilendirme kurallarını alır.</span><span class="sxs-lookup"><span data-stu-id="b5f33-103">Gets Service bus authorization rules.</span></span>


## <span data-ttu-id="b5f33-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b5f33-104">SYNTAX</span></span>

### <span data-ttu-id="b5f33-105">EntitySAS</span><span class="sxs-lookup"><span data-stu-id="b5f33-105">EntitySAS</span></span>
```
Get-AzureSBAuthorizationRule [-Name <String>] [-Permission <AccessRights[]>] -Namespace <String>
 -EntityName <String> -EntityType <ServiceBusEntityType> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b5f33-106">NamespaceSAS</span><span class="sxs-lookup"><span data-stu-id="b5f33-106">NamespaceSAS</span></span>
```
Get-AzureSBAuthorizationRule [-Name <String>] [-Permission <AccessRights[]>] -Namespace <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b5f33-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b5f33-107">DESCRIPTION</span></span>
<span data-ttu-id="b5f33-108">Hizmet veri yolu yetkilendirme kurallarını alır.</span><span class="sxs-lookup"><span data-stu-id="b5f33-108">Gets Service bus authorization rules.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="b5f33-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b5f33-109">EXAMPLES</span></span>

### <span data-ttu-id="b5f33-110">Örnek 1: ad alanı düzeyinde yetkilendirme kuralı alma</span><span class="sxs-lookup"><span data-stu-id="b5f33-110">Example 1: Get authorization rule at namespace level</span></span>
```
PS C:\> Get-AzureSBAuthorizationRule -Namespace MyNamespace
```

<span data-ttu-id="b5f33-111">MyNamespace adresindeki kullanılabilir tüm yetkilendirme kurallarını alır.</span><span class="sxs-lookup"><span data-stu-id="b5f33-111">Gets all available authorization rules at MyNamespace.</span></span>

### <span data-ttu-id="b5f33-112">Örnek 2: bir sıranın yetkilendirme kuralını alma</span><span class="sxs-lookup"><span data-stu-id="b5f33-112">Example 2: Get authorization rule for a Queue</span></span>
```
PS C:\> Get-AzureSBAuthorizationRule -Namespace MyNamespace -EntityName MyEntity -EntityType Queue
```

<span data-ttu-id="b5f33-113">Kullanılabilir tüm yetkilendirme kurallarını MyNamespace üzerinde bir MyEntity sırası alır.</span><span class="sxs-lookup"><span data-stu-id="b5f33-113">Gets all available authorization rules a MyEntity Queue on MyNamespace.</span></span>

### <span data-ttu-id="b5f33-114">Örnek 3: ada göre yetkilendirme kuralını alma</span><span class="sxs-lookup"><span data-stu-id="b5f33-114">Example 3: Get authorization rule by name</span></span>
```
PS C:\> Get-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace
```

<span data-ttu-id="b5f33-115">MyRule on MyNamespace Level adlı bir yetkilendirme kuralı alır.</span><span class="sxs-lookup"><span data-stu-id="b5f33-115">Gets an authorization rule called MyRule on MyNamespace level.</span></span>

### <span data-ttu-id="b5f33-116">Örnek 4: izin ile yetkilendirme kuralını alma</span><span class="sxs-lookup"><span data-stu-id="b5f33-116">Example 4: Get authorization rule by permission</span></span>
```
PS C:\> Get-AzureSBAuthorizationRule -Namespace MyNamespace -Permission $("Send")
```

<span data-ttu-id="b5f33-117">Ad alanı düzeyine gönderme izni olan tüm yetkilendirme kurallarını alır.</span><span class="sxs-lookup"><span data-stu-id="b5f33-117">Gets all authorization rules that have send permission on namespace level.</span></span>

## <span data-ttu-id="b5f33-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b5f33-118">PARAMETERS</span></span>

### <span data-ttu-id="b5f33-119">-VarlıkAdı</span><span class="sxs-lookup"><span data-stu-id="b5f33-119">-EntityName</span></span>
<span data-ttu-id="b5f33-120">Kuralın uygulanacağı varlık adı.</span><span class="sxs-lookup"><span data-stu-id="b5f33-120">The entity name to apply rule at.</span></span>

```yaml
Type: String
Parameter Sets: EntitySAS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5f33-121">-EntityType</span><span class="sxs-lookup"><span data-stu-id="b5f33-121">-EntityType</span></span>
<span data-ttu-id="b5f33-122">Varlık türü (kuyruk, konu, geçiş, NotificationHub).</span><span class="sxs-lookup"><span data-stu-id="b5f33-122">The entity type (Queue, Topic, Relay, NotificationHub).</span></span>

```yaml
Type: ServiceBusEntityType
Parameter Sets: EntitySAS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5f33-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="b5f33-123">-Name</span></span>
<span data-ttu-id="b5f33-124">Benzersiz yetkilendirme kuralı adı.</span><span class="sxs-lookup"><span data-stu-id="b5f33-124">The unique authorization rule name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5f33-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b5f33-125">-Namespace</span></span>
<span data-ttu-id="b5f33-126">Yetkilendirme kuralını uygulamak için ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="b5f33-126">The namespace name to apply the authorization rule.</span></span>
<span data-ttu-id="b5f33-127">Hiçbir EntityName sağlanmadı kural ad alanı düzeyinde olacaktır.</span><span class="sxs-lookup"><span data-stu-id="b5f33-127">If no EntityName provided the rule will be on the namespace level.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5f33-128">-İzin</span><span class="sxs-lookup"><span data-stu-id="b5f33-128">-Permission</span></span>
<span data-ttu-id="b5f33-129">Filtrelemek için yetkilendirme izinleri (gönder, Yönet, dinle).</span><span class="sxs-lookup"><span data-stu-id="b5f33-129">The authorization permissions to filter (Send, Manage, Listen).</span></span>
<span data-ttu-id="b5f33-130">Bu, tam eşleşme kullanır.</span><span class="sxs-lookup"><span data-stu-id="b5f33-130">This uses exact match.</span></span>

```yaml
Type: AccessRights[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5f33-131">-Profil</span><span class="sxs-lookup"><span data-stu-id="b5f33-131">-Profile</span></span>
<span data-ttu-id="b5f33-132">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5f33-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b5f33-133">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="b5f33-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5f33-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5f33-134">CommonParameters</span></span>
<span data-ttu-id="b5f33-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b5f33-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5f33-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5f33-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5f33-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b5f33-137">INPUTS</span></span>

## <span data-ttu-id="b5f33-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b5f33-138">OUTPUTS</span></span>

## <span data-ttu-id="b5f33-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b5f33-139">NOTES</span></span>

## <span data-ttu-id="b5f33-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b5f33-140">RELATED LINKS</span></span>

[<span data-ttu-id="b5f33-141">New-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b5f33-141">New-AzureSBAuthorizationRule</span></span>](./New-AzureSBAuthorizationRule.md)

[<span data-ttu-id="b5f33-142">Remove-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b5f33-142">Remove-AzureSBAuthorizationRule</span></span>](./Remove-AzureSBAuthorizationRule.md)

[<span data-ttu-id="b5f33-143">Set-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b5f33-143">Set-AzureSBAuthorizationRule</span></span>](./Set-AzureSBAuthorizationRule.md)


