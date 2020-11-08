---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 94D20309-5F72-4BE5-A150-2D6DD754286A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7a9d793bb9bc8d96150b812474bed9f8997adbe1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106104"
---
# <span data-ttu-id="08761-101">Remove-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="08761-101">Remove-AzureStaticVNetIP</span></span>

## <span data-ttu-id="08761-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08761-102">SYNOPSIS</span></span>
<span data-ttu-id="08761-103">Varsa, bir sanal makine nesnesinden statik sanal ağ IP adresi bilgilerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="08761-103">Removes the static virtual network IP address information from a virtual machine object, if any.</span></span>

## <span data-ttu-id="08761-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="08761-104">SYNTAX</span></span>

```
Remove-AzureStaticVNetIP -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="08761-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="08761-105">DESCRIPTION</span></span>
<span data-ttu-id="08761-106">**Remove-AzureStaticVNetIP** cmdlet 'i, varsa bir sanal makine nesnesinden statik sanal ağ (VNet) IP adresi bilgilerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="08761-106">The **Remove-AzureStaticVNetIP** cmdlet removes the static virtual network (VNet) IP address information from a virtual machine object, if any.</span></span>

## <span data-ttu-id="08761-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="08761-107">EXAMPLES</span></span>

### <span data-ttu-id="08761-108">2</span><span class="sxs-lookup"><span data-stu-id="08761-108">1:</span></span>
```

```

## <span data-ttu-id="08761-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="08761-109">PARAMETERS</span></span>

### <span data-ttu-id="08761-110">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="08761-110">-InformationAction</span></span>
<span data-ttu-id="08761-111">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="08761-111">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="08761-112">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="08761-112">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="08761-113">'A</span><span class="sxs-lookup"><span data-stu-id="08761-113">Continue</span></span>
- <span data-ttu-id="08761-114">Manıza</span><span class="sxs-lookup"><span data-stu-id="08761-114">Ignore</span></span>
- <span data-ttu-id="08761-115">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="08761-115">Inquire</span></span>
- <span data-ttu-id="08761-116">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="08761-116">SilentlyContinue</span></span>
- <span data-ttu-id="08761-117">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="08761-117">Stop</span></span>
- <span data-ttu-id="08761-118">Biliriz</span><span class="sxs-lookup"><span data-stu-id="08761-118">Suspend</span></span>

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

### <span data-ttu-id="08761-119">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="08761-119">-InformationVariable</span></span>
<span data-ttu-id="08761-120">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="08761-120">Specifies an information variable.</span></span>

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

### <span data-ttu-id="08761-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="08761-121">-Profile</span></span>
<span data-ttu-id="08761-122">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="08761-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="08761-123">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="08761-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="08761-124">-VM</span><span class="sxs-lookup"><span data-stu-id="08761-124">-VM</span></span>
<span data-ttu-id="08761-125">Kalıcı bir sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="08761-125">Specifies a persistent virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="08761-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08761-126">CommonParameters</span></span>
<span data-ttu-id="08761-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="08761-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08761-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08761-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08761-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="08761-129">INPUTS</span></span>

## <span data-ttu-id="08761-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="08761-130">OUTPUTS</span></span>

## <span data-ttu-id="08761-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="08761-131">NOTES</span></span>

## <span data-ttu-id="08761-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="08761-132">RELATED LINKS</span></span>

[<span data-ttu-id="08761-133">Get-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="08761-133">Get-AzureStaticVNetIP</span></span>](./Get-AzureStaticVNetIP.md)

[<span data-ttu-id="08761-134">Set-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="08761-134">Set-AzureStaticVNetIP</span></span>](./Set-AzureStaticVNetIP.md)


