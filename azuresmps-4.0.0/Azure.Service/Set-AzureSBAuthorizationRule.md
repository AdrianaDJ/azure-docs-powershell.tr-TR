---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 17065902-97EA-4F5F-926B-B7CBEE3EAF84
online version: ''
schema: 2.0.0
ms.openlocfilehash: ab76cf3052f28b0ff89e3e41aaa08127cc33411e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105820"
---
# <span data-ttu-id="34778-101">Set-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="34778-101">Set-AzureSBAuthorizationRule</span></span>

## <span data-ttu-id="34778-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34778-102">SYNOPSIS</span></span>
<span data-ttu-id="34778-103">Var olan hizmet veri yolu yetkilendirme kuralını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="34778-103">Updates existing Service Bus authorization rule.</span></span>

## <span data-ttu-id="34778-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="34778-104">SYNTAX</span></span>

### <span data-ttu-id="34778-105">EntitySAS</span><span class="sxs-lookup"><span data-stu-id="34778-105">EntitySAS</span></span>
```
Set-AzureSBAuthorizationRule -Name <String> [-Permission <AccessRights[]>] -Namespace <String>
 -EntityName <String> -EntityType <ServiceBusEntityType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="34778-106">NamespaceSAS</span><span class="sxs-lookup"><span data-stu-id="34778-106">NamespaceSAS</span></span>
```
Set-AzureSBAuthorizationRule -Name <String> [-Permission <AccessRights[]>] -Namespace <String>
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="34778-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="34778-107">DESCRIPTION</span></span>
<span data-ttu-id="34778-108">Var olan hizmet veri yolu yetkilendirme kuralını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="34778-108">Updates existing Service Bus authorization rule.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="34778-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="34778-109">EXAMPLES</span></span>

### <span data-ttu-id="34778-110">Örnek 1: ad alanı düzeyindeki yetkilendirme kuralının birincil anahtarını yenileme</span><span class="sxs-lookup"><span data-stu-id="34778-110">Example 1: Renew primary key for authorization rule at namespace level</span></span>
```
PS C:\> Set-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace -Permission $("Send")
```

<span data-ttu-id="34778-111">Birincil anahtar yenilenir.</span><span class="sxs-lookup"><span data-stu-id="34778-111">The primary key is renewed.</span></span>

### <span data-ttu-id="34778-112">Örnek 2: yetkilendirme kuralını güncelleştirme izni</span><span class="sxs-lookup"><span data-stu-id="34778-112">Example 2: Update authorization rule permission</span></span>
```
PS C:\> Set-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace -Permission $("Listen", "Send") -EntityName MyEntity -EntityType Queue
```

<span data-ttu-id="34778-113">İzinleri güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="34778-113">Updates the permissions.</span></span>

## <span data-ttu-id="34778-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="34778-114">PARAMETERS</span></span>

### <span data-ttu-id="34778-115">-VarlıkAdı</span><span class="sxs-lookup"><span data-stu-id="34778-115">-EntityName</span></span>
<span data-ttu-id="34778-116">Kuralın uygulanacağı varlık adı.</span><span class="sxs-lookup"><span data-stu-id="34778-116">The entity name to apply rule at.</span></span>

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

### <span data-ttu-id="34778-117">-EntityType</span><span class="sxs-lookup"><span data-stu-id="34778-117">-EntityType</span></span>
<span data-ttu-id="34778-118">Varlık türü (kuyruk, konu, geçiş, NotificationHub).</span><span class="sxs-lookup"><span data-stu-id="34778-118">The entity type (Queue, Topic, Relay, NotificationHub).</span></span>

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

### <span data-ttu-id="34778-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="34778-119">-Name</span></span>
<span data-ttu-id="34778-120">Benzersiz yetkilendirme kuralı adı.</span><span class="sxs-lookup"><span data-stu-id="34778-120">The unique authorization rule name.</span></span>

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

### <span data-ttu-id="34778-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="34778-121">-Namespace</span></span>
<span data-ttu-id="34778-122">Yetkilendirme kuralını uygulamak için ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="34778-122">The namespace name to apply the authorization rule.</span></span>
<span data-ttu-id="34778-123">Hiçbir EntityName sağlanmadı kural ad alanı düzeyinde olacaktır.</span><span class="sxs-lookup"><span data-stu-id="34778-123">If no EntityName provided the rule will be on the namespace level.</span></span>

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

### <span data-ttu-id="34778-124">-İzin</span><span class="sxs-lookup"><span data-stu-id="34778-124">-Permission</span></span>
<span data-ttu-id="34778-125">Yetkilendirme izinleri (gönder, Yönet, dinle).</span><span class="sxs-lookup"><span data-stu-id="34778-125">The authorization permissions (Send, Manage, Listen).</span></span>

```yaml
Type: AccessRights[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34778-126">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="34778-126">-PrimaryKey</span></span>
<span data-ttu-id="34778-127">Paylaşılan erişim Imzası birincil anahtarı.</span><span class="sxs-lookup"><span data-stu-id="34778-127">The Shared Access Signature primary key.</span></span>
<span data-ttu-id="34778-128">Sağlanmadıysa oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="34778-128">Will be generated if not provided.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34778-129">-Profil</span><span class="sxs-lookup"><span data-stu-id="34778-129">-Profile</span></span>
<span data-ttu-id="34778-130">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="34778-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="34778-131">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="34778-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="34778-132">-Secondaryanahtarı</span><span class="sxs-lookup"><span data-stu-id="34778-132">-SecondaryKey</span></span>
<span data-ttu-id="34778-133">Paylaşılan erişim Imzası ikincil anahtarı.</span><span class="sxs-lookup"><span data-stu-id="34778-133">The Shared Access Signature secondary key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34778-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34778-134">CommonParameters</span></span>
<span data-ttu-id="34778-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="34778-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34778-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34778-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34778-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="34778-137">INPUTS</span></span>

## <span data-ttu-id="34778-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="34778-138">OUTPUTS</span></span>

## <span data-ttu-id="34778-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="34778-139">NOTES</span></span>

## <span data-ttu-id="34778-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="34778-140">RELATED LINKS</span></span>

[<span data-ttu-id="34778-141">Get-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="34778-141">Get-AzureSBAuthorizationRule</span></span>](./Get-AzureSBAuthorizationRule.md)

[<span data-ttu-id="34778-142">New-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="34778-142">New-AzureSBAuthorizationRule</span></span>](./New-AzureSBAuthorizationRule.md)

[<span data-ttu-id="34778-143">Remove-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="34778-143">Remove-AzureSBAuthorizationRule</span></span>](./Remove-AzureSBAuthorizationRule.md)


