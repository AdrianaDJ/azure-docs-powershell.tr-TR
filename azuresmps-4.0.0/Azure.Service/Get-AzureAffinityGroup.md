---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 77B26360-F22B-457F-BDE3-9920A5736947
online version: ''
schema: 2.0.0
ms.openlocfilehash: 323b04a57cffc71059dff3f91480d54684941695
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105671"
---
# <span data-ttu-id="325fd-101">Get-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="325fd-101">Get-AzureAffinityGroup</span></span>

## <span data-ttu-id="325fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="325fd-102">SYNOPSIS</span></span>
<span data-ttu-id="325fd-103">Bir Azure benzeşim grubu nesnesi alır.</span><span class="sxs-lookup"><span data-stu-id="325fd-103">Gets an Azure affinity group object.</span></span>

## <span data-ttu-id="325fd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="325fd-104">SYNTAX</span></span>

```
Get-AzureAffinityGroup [[-Name] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="325fd-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="325fd-105">DESCRIPTION</span></span>
<span data-ttu-id="325fd-106">**Get-AzureAffinityGroup** cmdlet 'ı bir Azure benzeşim grubu alır.</span><span class="sxs-lookup"><span data-stu-id="325fd-106">The **Get-AzureAffinityGroup** cmdlet gets an Azure affinity group.</span></span>
<span data-ttu-id="325fd-107">Benzeşim grubu nesnesi, benzeşim grubunun bir parçası olan benzeşim grubu adını, konumunu, etiketini, açıklamayı ve depolama ve barındırılan hizmetleri içerir.</span><span class="sxs-lookup"><span data-stu-id="325fd-107">The affinity group object includes the affinity group name, location, label, description and the storage and hosted services that are part of the affinity group.</span></span>

## <span data-ttu-id="325fd-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="325fd-108">EXAMPLES</span></span>

### <span data-ttu-id="325fd-109">Örnek 1: benzeşim grubunun özelliklerini alma</span><span class="sxs-lookup"><span data-stu-id="325fd-109">Example 1: Get properties of an affinity group</span></span>
```
PS C:\> Get-AzureAffinityGroup -Name "South01"
```

<span data-ttu-id="325fd-110">Bu komut, South01 adlı benzeşim grubunun özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="325fd-110">This command gets the properties of the affinity group named South01.</span></span>

## <span data-ttu-id="325fd-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="325fd-111">PARAMETERS</span></span>

### <span data-ttu-id="325fd-112">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="325fd-112">-InformationAction</span></span>
<span data-ttu-id="325fd-113">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="325fd-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="325fd-114">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="325fd-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="325fd-115">'A</span><span class="sxs-lookup"><span data-stu-id="325fd-115">Continue</span></span>
- <span data-ttu-id="325fd-116">Manıza</span><span class="sxs-lookup"><span data-stu-id="325fd-116">Ignore</span></span>
- <span data-ttu-id="325fd-117">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="325fd-117">Inquire</span></span>
- <span data-ttu-id="325fd-118">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="325fd-118">SilentlyContinue</span></span>
- <span data-ttu-id="325fd-119">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="325fd-119">Stop</span></span>
- <span data-ttu-id="325fd-120">Biliriz</span><span class="sxs-lookup"><span data-stu-id="325fd-120">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="325fd-121">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="325fd-121">-InformationVariable</span></span>
<span data-ttu-id="325fd-122">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="325fd-122">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="325fd-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="325fd-123">-Name</span></span>
<span data-ttu-id="325fd-124">Bu cmdlet 'in aldığı benzeşim grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="325fd-124">Specifies the name of the affinity group that this cmdlet gets.</span></span>
<span data-ttu-id="325fd-125">Yönetim Portalı aracılığıyla oluşturulan benzeşim gruplarının adları genellikle Guid 'Ler.</span><span class="sxs-lookup"><span data-stu-id="325fd-125">Names for affinity groups created through the Management Portal are typically GUIDs.</span></span>
<span data-ttu-id="325fd-126">Yönetim bağlantı noktası, benzeşim grubu etiketini gösterir.</span><span class="sxs-lookup"><span data-stu-id="325fd-126">The Management Port shows the affinity group label.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="325fd-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="325fd-127">-Profile</span></span>
<span data-ttu-id="325fd-128">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="325fd-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="325fd-129">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="325fd-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="325fd-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="325fd-130">CommonParameters</span></span>
<span data-ttu-id="325fd-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="325fd-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="325fd-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="325fd-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="325fd-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="325fd-133">INPUTS</span></span>

## <span data-ttu-id="325fd-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="325fd-134">OUTPUTS</span></span>

### <span data-ttu-id="325fd-135">AffinityGroup</span><span class="sxs-lookup"><span data-stu-id="325fd-135">AffinityGroup</span></span>

## <span data-ttu-id="325fd-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="325fd-136">NOTES</span></span>

## <span data-ttu-id="325fd-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="325fd-137">RELATED LINKS</span></span>

[<span data-ttu-id="325fd-138">New-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="325fd-138">New-AzureAffinityGroup</span></span>](./New-AzureAffinityGroup.md)

[<span data-ttu-id="325fd-139">Remove-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="325fd-139">Remove-AzureAffinityGroup</span></span>](./Remove-AzureAffinityGroup.md)

[<span data-ttu-id="325fd-140">Set-AzureAffinityGroup</span><span class="sxs-lookup"><span data-stu-id="325fd-140">Set-AzureAffinityGroup</span></span>](./Set-AzureAffinityGroup.md)


