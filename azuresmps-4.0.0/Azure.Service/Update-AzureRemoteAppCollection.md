---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 67890A2A-7922-4E4A-96B4-B58CF532D2DE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 75a949128309e2777984be0dac33f27b0bc53aab
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105737"
---
# <span data-ttu-id="17fac-101">Update-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="17fac-101">Update-AzureRemoteAppCollection</span></span>

## <span data-ttu-id="17fac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17fac-102">SYNOPSIS</span></span>
<span data-ttu-id="17fac-103">Bir Azure RemoteApp koleksiyonunu yeni bir şablon görüntüsüyle güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="17fac-103">Updates an Azure RemoteApp collection with a new template image.</span></span>

## <span data-ttu-id="17fac-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="17fac-104">SYNTAX</span></span>

```
Update-AzureRemoteAppCollection [-CollectionName] <String> [-ImageName] <String> [[-SubnetName] <String>]
 [-ForceLogoffWhenUpdateComplete] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17fac-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="17fac-105">DESCRIPTION</span></span>
<span data-ttu-id="17fac-106">**Update-AzureRemoteAppCollection** cmdlet 'i, bir Azure RemoteApp koleksiyonunu yeni bir şablon resmiyle güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="17fac-106">The **Update-AzureRemoteAppCollection** cmdlet updates an Azure RemoteApp collection with a new template image.</span></span>
<span data-ttu-id="17fac-107">Güncelleştirme tamamlandıktan sonra, oturumları otomatik olarak oturumu kapatmadan önce oturumu açmak için bir saat daha var. Yeniden oturum açtıklarında, yeni güncelleştirilmiş koleksiyona bağlanırlar.</span><span class="sxs-lookup"><span data-stu-id="17fac-107">After the update completes, users with existing sessions have one hour to sign out before they are automatically signed out. When they sign in again, they connect to the newly updated collection.</span></span>
<span data-ttu-id="17fac-108">Koleksiyon güncelleştirildiğinde kullanıcıları hemen oturumu açmaya zorlamak için *Forcelogoffwhenupdatecomplete* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="17fac-108">To force users to be immediately signed out as soon as the collection is updated, specify the *ForceLogoffWhenUpdateComplete* parameter.</span></span>

## <span data-ttu-id="17fac-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="17fac-109">EXAMPLES</span></span>

## <span data-ttu-id="17fac-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="17fac-110">PARAMETERS</span></span>

### <span data-ttu-id="17fac-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="17fac-111">-CollectionName</span></span>
<span data-ttu-id="17fac-112">Azure RemoteApp koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="17fac-112">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17fac-113">-ForceLogoffWhenUpdateComplete</span><span class="sxs-lookup"><span data-stu-id="17fac-113">-ForceLogoffWhenUpdateComplete</span></span>
<span data-ttu-id="17fac-114">Güncelleştirme tamamlandığında bu cmdlet 'in kullanıcıları var olan oturumlarından işaretdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="17fac-114">Indicates that this cmdlet signs users out of their existing sessions as soon as the update is complete.</span></span>
<span data-ttu-id="17fac-115">Kullanıcılar yeniden oturum açtığında, yeni güncelleştirilmiş koleksiyona bağlanırlar.</span><span class="sxs-lookup"><span data-stu-id="17fac-115">When users sign in again, they connect to the newly updated collection.</span></span>

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

### <span data-ttu-id="17fac-116">-GörüntüAdı</span><span class="sxs-lookup"><span data-stu-id="17fac-116">-ImageName</span></span>
<span data-ttu-id="17fac-117">Azure RemoteApp şablonu görüntüsünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="17fac-117">Specifies the name of an Azure RemoteApp template image.</span></span>

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

### <span data-ttu-id="17fac-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="17fac-118">-Profile</span></span>
<span data-ttu-id="17fac-119">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="17fac-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="17fac-120">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="17fac-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="17fac-121">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="17fac-121">-SubnetName</span></span>
<span data-ttu-id="17fac-122">Koleksiyonun taşınacağı alt ağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="17fac-122">Specifies the name of the subnet into which to move the collection.</span></span>

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

### <span data-ttu-id="17fac-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="17fac-123">-Confirm</span></span>
<span data-ttu-id="17fac-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="17fac-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17fac-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17fac-125">-WhatIf</span></span>
<span data-ttu-id="17fac-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="17fac-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17fac-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="17fac-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17fac-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17fac-128">CommonParameters</span></span>
<span data-ttu-id="17fac-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="17fac-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17fac-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17fac-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17fac-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="17fac-131">INPUTS</span></span>

## <span data-ttu-id="17fac-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="17fac-132">OUTPUTS</span></span>

## <span data-ttu-id="17fac-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="17fac-133">NOTES</span></span>

## <span data-ttu-id="17fac-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="17fac-134">RELATED LINKS</span></span>

[<span data-ttu-id="17fac-135">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="17fac-135">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="17fac-136">New-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="17fac-136">New-AzureRemoteAppCollection</span></span>](./New-AzureRemoteAppCollection.md)

[<span data-ttu-id="17fac-137">Set-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="17fac-137">Set-AzureRemoteAppCollection</span></span>](./Set-AzureRemoteAppCollection.md)


