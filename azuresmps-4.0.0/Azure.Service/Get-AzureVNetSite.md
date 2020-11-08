---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: CFAA371E-F320-4FC3-80E0-5C857E5C0998
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0fbb80550acb0c743a3134a315f790bc25fb793a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106527"
---
# <span data-ttu-id="a88ec-101">Get-AzureVNetSite</span><span class="sxs-lookup"><span data-stu-id="a88ec-101">Get-AzureVNetSite</span></span>

## <span data-ttu-id="a88ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a88ec-102">SYNOPSIS</span></span>
<span data-ttu-id="a88ec-103">Azure sanal ağları hakkında bilgi içeren bir liste nesnesi alır.</span><span class="sxs-lookup"><span data-stu-id="a88ec-103">Gets a list object with information about Azure virtual networks.</span></span>

## <span data-ttu-id="a88ec-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a88ec-104">SYNTAX</span></span>

```
Get-AzureVNetSite [[-VNetName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="a88ec-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a88ec-105">DESCRIPTION</span></span>
<span data-ttu-id="a88ec-106">**Get-AzureVNetSite** cmdlet 'i geçerli aboneliğin Azure sanal ağları hakkında bilgi içeren bir liste nesnesi alır.</span><span class="sxs-lookup"><span data-stu-id="a88ec-106">The **Get-AzureVNetSite** cmdlet gets a list object with information about Azure virtual networks for the current subscription.</span></span>
<span data-ttu-id="a88ec-107">Bir sanal ağ adı belirtirseniz, yalnızca o sanal ağın bilgileri döndürülür.</span><span class="sxs-lookup"><span data-stu-id="a88ec-107">If you specify a virtual network name, only information for that virtual network is returned.</span></span>

## <span data-ttu-id="a88ec-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a88ec-108">EXAMPLES</span></span>

### <span data-ttu-id="a88ec-109">Örnek 1: geçerli abonelikteki tüm sanal ağlar hakkında bilgi alın</span><span class="sxs-lookup"><span data-stu-id="a88ec-109">Example 1: Get information about all virtual networks in the current subscription</span></span>
```
PS C:\> Get-AzureVNetSite
```

<span data-ttu-id="a88ec-110">Bu komut, geçerli abonelikteki tüm sanal ağlar hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="a88ec-110">This command gets information about all the virtual networks in the current subscription.</span></span>

### <span data-ttu-id="a88ec-111">Örnek 2: geçerli abonelikteki belirli bir sanal ağ hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="a88ec-111">Example 2: Get information about a specific virtual network in the current subscription</span></span>
```
PS C:\> Get-AzureVNetSite -VNetName "MyProductionNetwork"
```

<span data-ttu-id="a88ec-112">Bu komut, yalnızca Myüretim ağı sanal ağındaki bilgileri getirir.</span><span class="sxs-lookup"><span data-stu-id="a88ec-112">This command retrieves information on the MyProductionNetwork virtual network only.</span></span>

## <span data-ttu-id="a88ec-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a88ec-113">PARAMETERS</span></span>

### <span data-ttu-id="a88ec-114">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="a88ec-114">-InformationAction</span></span>
<span data-ttu-id="a88ec-115">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a88ec-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a88ec-116">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="a88ec-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a88ec-117">'A</span><span class="sxs-lookup"><span data-stu-id="a88ec-117">Continue</span></span>
- <span data-ttu-id="a88ec-118">Manıza</span><span class="sxs-lookup"><span data-stu-id="a88ec-118">Ignore</span></span>
- <span data-ttu-id="a88ec-119">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="a88ec-119">Inquire</span></span>
- <span data-ttu-id="a88ec-120">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="a88ec-120">SilentlyContinue</span></span>
- <span data-ttu-id="a88ec-121">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="a88ec-121">Stop</span></span>
- <span data-ttu-id="a88ec-122">Biliriz</span><span class="sxs-lookup"><span data-stu-id="a88ec-122">Suspend</span></span>

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

### <span data-ttu-id="a88ec-123">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="a88ec-123">-InformationVariable</span></span>
<span data-ttu-id="a88ec-124">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="a88ec-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a88ec-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="a88ec-125">-Profile</span></span>
<span data-ttu-id="a88ec-126">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a88ec-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a88ec-127">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="a88ec-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a88ec-128">-Vağ adı</span><span class="sxs-lookup"><span data-stu-id="a88ec-128">-VNetName</span></span>
<span data-ttu-id="a88ec-129">Hakkında bilgi döndürmek için sanal ağ adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a88ec-129">Specifies a virtual network name to return information about.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a88ec-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a88ec-130">CommonParameters</span></span>
<span data-ttu-id="a88ec-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a88ec-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a88ec-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a88ec-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a88ec-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a88ec-133">INPUTS</span></span>

## <span data-ttu-id="a88ec-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a88ec-134">OUTPUTS</span></span>

## <span data-ttu-id="a88ec-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a88ec-135">NOTES</span></span>

## <span data-ttu-id="a88ec-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a88ec-136">RELATED LINKS</span></span>

[<span data-ttu-id="a88ec-137">Get-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="a88ec-137">Get-AzureVNetConfig</span></span>](./Get-AzureVNetConfig.md)

[<span data-ttu-id="a88ec-138">Remove-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="a88ec-138">Remove-AzureVNetConfig</span></span>](./Remove-AzureVNetConfig.md)

[<span data-ttu-id="a88ec-139">Set-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="a88ec-139">Set-AzureVNetConfig</span></span>](./Set-AzureVNetConfig.md)


