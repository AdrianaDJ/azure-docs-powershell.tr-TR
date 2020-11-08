---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 4E059EF1-740C-4AEB-AF41-BF6003BE15F2
online version: ''
schema: 2.0.0
ms.openlocfilehash: a52f2585771ec10d6acf52b14c88bd1ed0af0427
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105936"
---
# <span data-ttu-id="905b4-101">Test-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="905b4-101">Test-AzureStaticVNetIP</span></span>

## <span data-ttu-id="905b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="905b4-102">SYNOPSIS</span></span>
<span data-ttu-id="905b4-103">Statik sanal ağ IP adresinin kullanılabilirliğini sınar ve sorgulanan adres kullanılamıyorsa öneri listesini alır.</span><span class="sxs-lookup"><span data-stu-id="905b4-103">Tests the availability of a static virtual network IP address, and gets a list of suggestions if the queried address is not available.</span></span>

## <span data-ttu-id="905b4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="905b4-104">SYNTAX</span></span>

```
Test-AzureStaticVNetIP [-VNetName] <String> [-IPAddress] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="905b4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="905b4-105">DESCRIPTION</span></span>
<span data-ttu-id="905b4-106">**Test-AzureStaticVNetIP** cmdlet 'i statik sanal ağ IP adresinin kullanılabilirliğini sınar ve sorgulanan adres kullanılamıyorsa öneri listesini alır.</span><span class="sxs-lookup"><span data-stu-id="905b4-106">The **Test-AzureStaticVNetIP** cmdlet tests the availability of a static virtual network IP address, and gets a list of suggestions if the queried address is not available.</span></span>

## <span data-ttu-id="905b4-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="905b4-107">EXAMPLES</span></span>

### <span data-ttu-id="905b4-108">2</span><span class="sxs-lookup"><span data-stu-id="905b4-108">1:</span></span>
```

```

## <span data-ttu-id="905b4-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="905b4-109">PARAMETERS</span></span>

### <span data-ttu-id="905b4-110">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="905b4-110">-InformationAction</span></span>
<span data-ttu-id="905b4-111">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="905b4-111">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="905b4-112">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="905b4-112">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="905b4-113">'A</span><span class="sxs-lookup"><span data-stu-id="905b4-113">Continue</span></span>
- <span data-ttu-id="905b4-114">Manıza</span><span class="sxs-lookup"><span data-stu-id="905b4-114">Ignore</span></span>
- <span data-ttu-id="905b4-115">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="905b4-115">Inquire</span></span>
- <span data-ttu-id="905b4-116">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="905b4-116">SilentlyContinue</span></span>
- <span data-ttu-id="905b4-117">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="905b4-117">Stop</span></span>
- <span data-ttu-id="905b4-118">Biliriz</span><span class="sxs-lookup"><span data-stu-id="905b4-118">Suspend</span></span>

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

### <span data-ttu-id="905b4-119">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="905b4-119">-InformationVariable</span></span>
<span data-ttu-id="905b4-120">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="905b4-120">Specifies an information variable.</span></span>

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

### <span data-ttu-id="905b4-121">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="905b4-121">-IPAddress</span></span>
<span data-ttu-id="905b4-122">Sorgulanacak statik sanal ağ IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="905b4-122">Specifies the static virtual network IP address to query.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="905b4-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="905b4-123">-Profile</span></span>
<span data-ttu-id="905b4-124">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="905b4-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="905b4-125">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="905b4-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="905b4-126">-Vağ adı</span><span class="sxs-lookup"><span data-stu-id="905b4-126">-VNetName</span></span>
<span data-ttu-id="905b4-127">Sanal ağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="905b4-127">Specifies the Name of the virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="905b4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="905b4-128">CommonParameters</span></span>
<span data-ttu-id="905b4-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="905b4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="905b4-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="905b4-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="905b4-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="905b4-131">INPUTS</span></span>

## <span data-ttu-id="905b4-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="905b4-132">OUTPUTS</span></span>

## <span data-ttu-id="905b4-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="905b4-133">NOTES</span></span>

## <span data-ttu-id="905b4-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="905b4-134">RELATED LINKS</span></span>

[<span data-ttu-id="905b4-135">Get-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="905b4-135">Get-AzureStaticVNetIP</span></span>](./Get-AzureStaticVNetIP.md)

[<span data-ttu-id="905b4-136">Set-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="905b4-136">Set-AzureStaticVNetIP</span></span>](./Set-AzureStaticVNetIP.md)


