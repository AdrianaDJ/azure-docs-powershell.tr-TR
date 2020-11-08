---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 14B4050D-3597-4760-A152-82617B88078D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 291ea94bbdfff1da8d658074ebfb72df8943f0e8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106053"
---
# <span data-ttu-id="9d0fe-101">Set-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="9d0fe-101">Set-AzureRemoteAppCollection</span></span>

## <span data-ttu-id="9d0fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d0fe-102">SYNOPSIS</span></span>
<span data-ttu-id="9d0fe-103">RemoteApp koleksiyonunun özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="9d0fe-103">Sets the properties of a RemoteApp collection.</span></span>

## <span data-ttu-id="9d0fe-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9d0fe-104">SYNTAX</span></span>

### <span data-ttu-id="9d0fe-105">Yalnızca Description(varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9d0fe-105">DescriptionOnly (Default)</span></span>
```
Set-AzureRemoteAppCollection [-CollectionName] <String> -Description <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="9d0fe-106">Yalnızca plan</span><span class="sxs-lookup"><span data-stu-id="9d0fe-106">PlanOnly</span></span>
```
Set-AzureRemoteAppCollection [-CollectionName] <String> -Plan <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="9d0fe-107">Etkialanıbirleştirilmiş</span><span class="sxs-lookup"><span data-stu-id="9d0fe-107">DomainJoined</span></span>
```
Set-AzureRemoteAppCollection [-CollectionName] <String> -Credential <PSCredential> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="9d0fe-108">Yalnızca rdpproperty</span><span class="sxs-lookup"><span data-stu-id="9d0fe-108">RdpPropertyOnly</span></span>
```
Set-AzureRemoteAppCollection [-CollectionName] <String> -CustomRdpProperty <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="9d0fe-109">Yalnızca acllevel</span><span class="sxs-lookup"><span data-stu-id="9d0fe-109">AclLevelOnly</span></span>
```
Set-AzureRemoteAppCollection [-CollectionName] <String> -AclLevel <CollectionAclLevel>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9d0fe-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="9d0fe-110">DESCRIPTION</span></span>
<span data-ttu-id="9d0fe-111">**Set-AzureRemoteAppCollection** cmdlet 'i, bir Azure RemoteApp koleksiyonunun özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="9d0fe-111">The **Set-AzureRemoteAppCollection** cmdlet sets the properties of an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="9d0fe-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9d0fe-112">EXAMPLES</span></span>

## <span data-ttu-id="9d0fe-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9d0fe-113">PARAMETERS</span></span>

### <span data-ttu-id="9d0fe-114">-AclLevel</span><span class="sxs-lookup"><span data-stu-id="9d0fe-114">-AclLevel</span></span>
<span data-ttu-id="9d0fe-115">Koleksiyonun erişim denetim listesi (ACL) düzeyini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9d0fe-115">Specifies the access control list (ACL) level for the collection.</span></span>
<span data-ttu-id="9d0fe-116">Bu parametre için kabul edilebilir değerler: koleksiyon ve uygulama.</span><span class="sxs-lookup"><span data-stu-id="9d0fe-116">The acceptable values for this parameter are: Collection and Application.</span></span>

```yaml
Type: CollectionAclLevel
Parameter Sets: AclLevelOnly
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d0fe-117">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="9d0fe-117">-CollectionName</span></span>
<span data-ttu-id="9d0fe-118">Azure RemoteApp koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9d0fe-118">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="9d0fe-119">-Credential</span><span class="sxs-lookup"><span data-stu-id="9d0fe-119">-Credential</span></span>
<span data-ttu-id="9d0fe-120">Azure RemoteApp sunucularına etki alanınıza katılma izni olan bir hizmet hesabının kimlik bilgilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9d0fe-120">Specifies the credentials of a service account that has permission to join the Azure RemoteApp servers to your domain.</span></span>
<span data-ttu-id="9d0fe-121">**PSCredential** nesnesi almak için **Get-Credential** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="9d0fe-121">To obtain a **PSCredential** object, use the **Get-Credential** cmdlet.</span></span>

```yaml
Type: PSCredential
Parameter Sets: DomainJoined
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d0fe-122">-Customrdpözelliği</span><span class="sxs-lookup"><span data-stu-id="9d0fe-122">-CustomRdpProperty</span></span>
<span data-ttu-id="9d0fe-123">Sürücü yeniden yönlendirmeyi ve diğer ayarları yapılandırmak için kullanılabilecek özel Uzak Masaüstü Protokolü (RDP) özelliklerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9d0fe-123">Specifies custom Remote Desktop Protocol (RDP) properties which can be used to configure drive redirection and other settings.</span></span> <span data-ttu-id="9d0fe-124">Ayrıntılar için [Windows Server 'Daki Uzak Masaüstü Hizmetleri 'Ndeki RDP ayarlarına](https://technet.microsoft.com/library/ff393699(v=ws.10).aspx) bakın `(https://technet.microsoft.com/library/ff393699(v=ws.10).aspx)` .  </span><span class="sxs-lookup"><span data-stu-id="9d0fe-124">See [RDP Settings for Remote Desktop Services in Windows Server](https://technet.microsoft.com/library/ff393699(v=ws.10).aspx)  `(https://technet.microsoft.com/library/ff393699(v=ws.10).aspx)` for details.</span></span>

```yaml
Type: String
Parameter Sets: RdpPropertyOnly
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d0fe-125">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="9d0fe-125">-Description</span></span>
<span data-ttu-id="9d0fe-126">Koleksiyon için kısa bir açıklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="9d0fe-126">Specifies a short description for the collection.</span></span>

```yaml
Type: String
Parameter Sets: DescriptionOnly
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d0fe-127">-Plan</span><span class="sxs-lookup"><span data-stu-id="9d0fe-127">-Plan</span></span>
<span data-ttu-id="9d0fe-128">Kullanım sınırlarını tanımlayan Azure RemoteApp koleksiyonu planını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9d0fe-128">Specifies the plan for the Azure RemoteApp collection, which defines the usage limits.</span></span>
<span data-ttu-id="9d0fe-129">Planları görmek için **Get-AzureRemoteAppPlan** 'ı kullanın.</span><span class="sxs-lookup"><span data-stu-id="9d0fe-129">Use **Get-AzureRemoteAppPlan** to see the plans available.</span></span>

```yaml
Type: String
Parameter Sets: PlanOnly
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d0fe-130">-Profil</span><span class="sxs-lookup"><span data-stu-id="9d0fe-130">-Profile</span></span>
<span data-ttu-id="9d0fe-131">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9d0fe-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9d0fe-132">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="9d0fe-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9d0fe-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d0fe-133">CommonParameters</span></span>
<span data-ttu-id="9d0fe-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9d0fe-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d0fe-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d0fe-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d0fe-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9d0fe-136">INPUTS</span></span>

## <span data-ttu-id="9d0fe-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9d0fe-137">OUTPUTS</span></span>

## <span data-ttu-id="9d0fe-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9d0fe-138">NOTES</span></span>

## <span data-ttu-id="9d0fe-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9d0fe-139">RELATED LINKS</span></span>

[<span data-ttu-id="9d0fe-140">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="9d0fe-140">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="9d0fe-141">New-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="9d0fe-141">New-AzureRemoteAppCollection</span></span>](./New-AzureRemoteAppCollection.md)

[<span data-ttu-id="9d0fe-142">Update-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="9d0fe-142">Update-AzureRemoteAppCollection</span></span>](./Update-AzureRemoteAppCollection.md)


