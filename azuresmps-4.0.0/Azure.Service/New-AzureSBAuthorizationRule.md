---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 75320133-E7B1-40D4-B16D-567686D5AE99
online version: ''
schema: 2.0.0
ms.openlocfilehash: 40d3bdc73ce6bcbb199cf99bb0586de52f05e132
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105987"
---
# <span data-ttu-id="2d393-101">New-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="2d393-101">New-AzureSBAuthorizationRule</span></span>

## <span data-ttu-id="2d393-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d393-102">SYNOPSIS</span></span>
<span data-ttu-id="2d393-103">Yeni hizmet veri yolu yetkilendirme kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2d393-103">Creates new Service Bus authorization rule.</span></span>

## <span data-ttu-id="2d393-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2d393-104">SYNTAX</span></span>

### <span data-ttu-id="2d393-105">EntitySAS</span><span class="sxs-lookup"><span data-stu-id="2d393-105">EntitySAS</span></span>
```
New-AzureSBAuthorizationRule -Name <String> [-Permission <AccessRights[]>] -Namespace <String>
 -EntityName <String> -EntityType <ServiceBusEntityType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="2d393-106">NamespaceSAS</span><span class="sxs-lookup"><span data-stu-id="2d393-106">NamespaceSAS</span></span>
```
New-AzureSBAuthorizationRule -Name <String> [-Permission <AccessRights[]>] -Namespace <String>
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2d393-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="2d393-107">DESCRIPTION</span></span>
<span data-ttu-id="2d393-108">**New-AzureSBAuthorizationRule** cmdlet 'ı bir hizmet veri yolu yetkilendirme kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2d393-108">The **New-AzureSBAuthorizationRule** cmdlet creates a Service Bus authorization rule.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="2d393-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2d393-109">EXAMPLES</span></span>

### <span data-ttu-id="2d393-110">Örnek 1: oluşturulan birincil anahtarla yetkilendirme kuralı oluşturma</span><span class="sxs-lookup"><span data-stu-id="2d393-110">Example 1: Create an authorization rule with generated primary key</span></span>
```
PS C:\> New-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace -Permission $("Send")
```

<span data-ttu-id="2d393-111">Ad alanı düzeyinde gönder izniyle yeni yetkilendirme kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2d393-111">Creates new authorization rule on namespace level with Send permission.</span></span>

### <span data-ttu-id="2d393-112">Örnek 2: birincil anahtar sağlayarak yetkilendirme kuralı oluşturur</span><span class="sxs-lookup"><span data-stu-id="2d393-112">Example 2: Creates an authorization rule by providing the primary key</span></span>
```
PS C:\> New-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace -Permission $("Manage", "Listen", "Send") -EntityName MyEntity -EntityType Queue -PrimaryKey P+lL/Mnd2Z9sj5hwMrRyAxQDdX8RHfbdqU2eIAqs1rc=
```

<span data-ttu-id="2d393-113">Myentilik sıra düzeyinde tüm izinlerle yeni yetkilendirme kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2d393-113">Creates new authorization rule on MyEntity Queue level with all permissions.</span></span>

## <span data-ttu-id="2d393-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2d393-114">PARAMETERS</span></span>

### <span data-ttu-id="2d393-115">-VarlıkAdı</span><span class="sxs-lookup"><span data-stu-id="2d393-115">-EntityName</span></span>
<span data-ttu-id="2d393-116">Kural uygulanacak varlık adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d393-116">Specifies the entity name to apply rule at.</span></span>

```yaml
Type: String
Parameter Sets: EntitySAS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d393-117">-EntityType</span><span class="sxs-lookup"><span data-stu-id="2d393-117">-EntityType</span></span>
<span data-ttu-id="2d393-118">Varlık türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d393-118">Specifies the entity type.</span></span>
<span data-ttu-id="2d393-119">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="2d393-119">Valid values are:</span></span>
  
- <span data-ttu-id="2d393-120">Kuyruğ</span><span class="sxs-lookup"><span data-stu-id="2d393-120">Queue</span></span>
- <span data-ttu-id="2d393-121">Başlıkta</span><span class="sxs-lookup"><span data-stu-id="2d393-121">Topic</span></span>
- <span data-ttu-id="2d393-122">Geçir</span><span class="sxs-lookup"><span data-stu-id="2d393-122">Relay</span></span>
- <span data-ttu-id="2d393-123">NotificationHub</span><span class="sxs-lookup"><span data-stu-id="2d393-123">NotificationHub</span></span>

```yaml
Type: ServiceBusEntityType
Parameter Sets: EntitySAS
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d393-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="2d393-124">-Name</span></span>
<span data-ttu-id="2d393-125">Benzersiz yetkilendirme kuralı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d393-125">Specifies the unique authorization rule name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d393-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2d393-126">-Namespace</span></span>
<span data-ttu-id="2d393-127">Yetkilendirme kuralını uygulamak için ad alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d393-127">Specifies the namespace name to apply the authorization rule.</span></span>
<span data-ttu-id="2d393-128">Hiçbir *EntityName* sağlanmadı kural ad alanı düzeyinde olacaktır.</span><span class="sxs-lookup"><span data-stu-id="2d393-128">If no *EntityName* provided the rule will be on the namespace level.</span></span>

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

### <span data-ttu-id="2d393-129">-İzin</span><span class="sxs-lookup"><span data-stu-id="2d393-129">-Permission</span></span>
<span data-ttu-id="2d393-130">Yetkilendirme izinleri (gönder, Yönet, dinle).</span><span class="sxs-lookup"><span data-stu-id="2d393-130">The authorization permissions (Send, Manage, Listen).</span></span>

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

### <span data-ttu-id="2d393-131">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="2d393-131">-PrimaryKey</span></span>
<span data-ttu-id="2d393-132">Paylaşılan erişim Imzası birincil anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d393-132">Specifies the Shared Access Signature primary key.</span></span>
<span data-ttu-id="2d393-133">Sağlanmadıysa oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="2d393-133">Will be generated if not provided.</span></span>

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

### <span data-ttu-id="2d393-134">-Profil</span><span class="sxs-lookup"><span data-stu-id="2d393-134">-Profile</span></span>
<span data-ttu-id="2d393-135">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d393-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2d393-136">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="2d393-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2d393-137">-Secondaryanahtarı</span><span class="sxs-lookup"><span data-stu-id="2d393-137">-SecondaryKey</span></span>
<span data-ttu-id="2d393-138">Paylaşılan erişim Imzası ikincil anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d393-138">Specifies the Shared Access Signature secondary key.</span></span>

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

### <span data-ttu-id="2d393-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d393-139">CommonParameters</span></span>
<span data-ttu-id="2d393-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2d393-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d393-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d393-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d393-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2d393-142">INPUTS</span></span>

## <span data-ttu-id="2d393-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2d393-143">OUTPUTS</span></span>

## <span data-ttu-id="2d393-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2d393-144">NOTES</span></span>

## <span data-ttu-id="2d393-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2d393-145">RELATED LINKS</span></span>

[<span data-ttu-id="2d393-146">Get-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="2d393-146">Get-AzureSBAuthorizationRule</span></span>](./Get-AzureSBAuthorizationRule.md)

[<span data-ttu-id="2d393-147">Remove-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="2d393-147">Remove-AzureSBAuthorizationRule</span></span>](./Remove-AzureSBAuthorizationRule.md)

[<span data-ttu-id="2d393-148">Set-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="2d393-148">Set-AzureSBAuthorizationRule</span></span>](./Set-AzureSBAuthorizationRule.md)


