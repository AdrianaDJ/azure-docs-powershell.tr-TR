---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E246C177-EAEE-4D7A-A544-664F47862FC7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 92d450a10628ea7e85a49962ac262d4dece8e4c8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106131"
---
# <span data-ttu-id="5aec5-101">Remove-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="5aec5-101">Remove-AzureSBAuthorizationRule</span></span>

## <span data-ttu-id="5aec5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5aec5-102">SYNOPSIS</span></span>
<span data-ttu-id="5aec5-103">Var olan hizmet veri yolu yetkilendirme kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5aec5-103">Removes existing Service Bus authorization rule.</span></span>

## <span data-ttu-id="5aec5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5aec5-104">SYNTAX</span></span>

### <span data-ttu-id="5aec5-105">EntitySAS</span><span class="sxs-lookup"><span data-stu-id="5aec5-105">EntitySAS</span></span>
```
Remove-AzureSBAuthorizationRule -Name <String> -Namespace <String> -EntityName <String>
 -EntityType <ServiceBusEntityType> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="5aec5-106">NamespaceSAS</span><span class="sxs-lookup"><span data-stu-id="5aec5-106">NamespaceSAS</span></span>
```
Remove-AzureSBAuthorizationRule -Name <String> -Namespace <String> [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="5aec5-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="5aec5-107">DESCRIPTION</span></span>
<span data-ttu-id="5aec5-108">Var olan hizmet veri yolu yetkilendirme kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5aec5-108">Removes existing Service Bus authorization rule.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="5aec5-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5aec5-109">EXAMPLES</span></span>

### <span data-ttu-id="5aec5-110">Örnek 1: ad alanı düzeyindeki yetkilendirme kuralını kaldırma</span><span class="sxs-lookup"><span data-stu-id="5aec5-110">Example 1: Remove authorization rule at namespace level</span></span>
```
PS C:\> Remove-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace
```

<span data-ttu-id="5aec5-111">MyRule MyRule MyNamespace 'dan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5aec5-111">Removes authorization rule MyRule from MyNamespace.</span></span>

### <span data-ttu-id="5aec5-112">Örnek 2: bir sıranın yetkilendirme kuralını kaldırma</span><span class="sxs-lookup"><span data-stu-id="5aec5-112">Example 2: Remove authorization rule for a Queue</span></span>
```
PS C:\> Remove-AzureSBAuthorizationRule -Name MyRule -Namespace MyNamespace -EntityName MyEntity -EntityType Queue
```

<span data-ttu-id="5aec5-113">MyNamespace üzerindeki bir MyEntity kuyruğu için MyRule adlı yetkilendirme kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5aec5-113">Removes authorization rule called MyRule for a MyEntity Queue on MyNamespace.</span></span>

## <span data-ttu-id="5aec5-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5aec5-114">PARAMETERS</span></span>

### <span data-ttu-id="5aec5-115">-VarlıkAdı</span><span class="sxs-lookup"><span data-stu-id="5aec5-115">-EntityName</span></span>
<span data-ttu-id="5aec5-116">Kuralın uygulanacağı varlık adı.</span><span class="sxs-lookup"><span data-stu-id="5aec5-116">The entity name to apply rule at.</span></span>

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

### <span data-ttu-id="5aec5-117">-EntityType</span><span class="sxs-lookup"><span data-stu-id="5aec5-117">-EntityType</span></span>
<span data-ttu-id="5aec5-118">Varlık türü (kuyruk, konu, geçiş, NotificationHub).</span><span class="sxs-lookup"><span data-stu-id="5aec5-118">The entity type (Queue, Topic, Relay, NotificationHub).</span></span>

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

### <span data-ttu-id="5aec5-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="5aec5-119">-Name</span></span>
<span data-ttu-id="5aec5-120">Benzersiz yetkilendirme kuralı adı.</span><span class="sxs-lookup"><span data-stu-id="5aec5-120">The unique authorization rule name.</span></span>

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

### <span data-ttu-id="5aec5-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="5aec5-121">-Namespace</span></span>
<span data-ttu-id="5aec5-122">Yetkilendirme kuralını uygulamak için ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="5aec5-122">The namespace name to apply the authorization rule.</span></span>
<span data-ttu-id="5aec5-123">Hiçbir EntityName sağlanmadı kural ad alanı düzeyinde olacaktır.</span><span class="sxs-lookup"><span data-stu-id="5aec5-123">If no EntityName provided the rule will be on the namespace level.</span></span>

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

### <span data-ttu-id="5aec5-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="5aec5-124">-PassThru</span></span>
<span data-ttu-id="5aec5-125">Bu cmdlet 'in, üzerinde işlem yaptığı öğeyi temsil eden bir nesne döndürdüğü anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="5aec5-125">Indicates that this cmdlet returns an object representing the item on which it operates.</span></span>
<span data-ttu-id="5aec5-126">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="5aec5-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5aec5-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="5aec5-127">-Profile</span></span>
<span data-ttu-id="5aec5-128">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5aec5-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5aec5-129">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="5aec5-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5aec5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5aec5-130">CommonParameters</span></span>
<span data-ttu-id="5aec5-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5aec5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5aec5-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5aec5-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5aec5-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5aec5-133">INPUTS</span></span>

## <span data-ttu-id="5aec5-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5aec5-134">OUTPUTS</span></span>

## <span data-ttu-id="5aec5-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5aec5-135">NOTES</span></span>

## <span data-ttu-id="5aec5-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5aec5-136">RELATED LINKS</span></span>

[<span data-ttu-id="5aec5-137">Get-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="5aec5-137">Get-AzureSBAuthorizationRule</span></span>](./Get-AzureSBAuthorizationRule.md)

[<span data-ttu-id="5aec5-138">New-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="5aec5-138">New-AzureSBAuthorizationRule</span></span>](./New-AzureSBAuthorizationRule.md)

[<span data-ttu-id="5aec5-139">Set-AzureSBAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="5aec5-139">Set-AzureSBAuthorizationRule</span></span>](./Set-AzureSBAuthorizationRule.md)


