---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: C0EEC51F-F8AB-4A6C-8F99-2B2DFFE9BB26
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9b5f4d5319e705c4f0481edcb5a44a579f4ff01d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105618"
---
# <span data-ttu-id="95688-101">Get-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="95688-101">Get-AzureReservedIP</span></span>

## <span data-ttu-id="95688-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95688-102">SYNOPSIS</span></span>
<span data-ttu-id="95688-103">Ayrılmış IP adresini adıyla alır veya abonelikteki tüm ayrılmış IP adreslerini listeler.</span><span class="sxs-lookup"><span data-stu-id="95688-103">Gets a reserved IP address by its name or lists all the reserved IP addresses in the subscription.</span></span>

## <span data-ttu-id="95688-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="95688-104">SYNTAX</span></span>

```
Get-AzureReservedIP [[-ReservedIPName] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="95688-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="95688-105">DESCRIPTION</span></span>
<span data-ttu-id="95688-106">**Get-AzureReservedIP** cmdlet 'i ayrılmış bir IP adresini adıyla alır veya abonelikteki tüm ayrılmış IP adreslerini listeler.</span><span class="sxs-lookup"><span data-stu-id="95688-106">The **Get-AzureReservedIP** cmdlet gets a reserved IP address by its name or lists all of the reserved IP addresses in the subscription.</span></span>

## <span data-ttu-id="95688-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="95688-107">EXAMPLES</span></span>

### <span data-ttu-id="95688-108">Örnek 1: tüm ayrılmış IP adreslerini al</span><span class="sxs-lookup"><span data-stu-id="95688-108">Example 1: Get all reserved IP addresses</span></span>
```
PS C:\> Get-AzureReservedIP
```

<span data-ttu-id="95688-109">Bu komut, tüm ayrılmış IP adreslerini alır.</span><span class="sxs-lookup"><span data-stu-id="95688-109">This command gets all reserved IP addresses.</span></span>

### <span data-ttu-id="95688-110">Örnek 2: belirtilen ada sahip ayrılmış bir IP adresi alma</span><span class="sxs-lookup"><span data-stu-id="95688-110">Example 2: Get a reserved IP address with a specified name</span></span>
```
PS C:\> Get-AzureReservedIP -ReservedIPName $IpName
```

<span data-ttu-id="95688-111">Bu komut, $IpName değişkeni tarafından belirtilen adı içeren ayrılmış IP adresini alır.</span><span class="sxs-lookup"><span data-stu-id="95688-111">This command gets the reserved IP address that has the name specified by the $IpName variable.</span></span>

## <span data-ttu-id="95688-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="95688-112">PARAMETERS</span></span>

### <span data-ttu-id="95688-113">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="95688-113">-InformationAction</span></span>
<span data-ttu-id="95688-114">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="95688-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="95688-115">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="95688-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="95688-116">'A</span><span class="sxs-lookup"><span data-stu-id="95688-116">Continue</span></span>
- <span data-ttu-id="95688-117">Manıza</span><span class="sxs-lookup"><span data-stu-id="95688-117">Ignore</span></span>
- <span data-ttu-id="95688-118">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="95688-118">Inquire</span></span>
- <span data-ttu-id="95688-119">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="95688-119">SilentlyContinue</span></span>
- <span data-ttu-id="95688-120">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="95688-120">Stop</span></span>
- <span data-ttu-id="95688-121">Biliriz</span><span class="sxs-lookup"><span data-stu-id="95688-121">Suspend</span></span>

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

### <span data-ttu-id="95688-122">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="95688-122">-InformationVariable</span></span>
<span data-ttu-id="95688-123">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="95688-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="95688-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="95688-124">-Profile</span></span>
<span data-ttu-id="95688-125">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="95688-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="95688-126">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="95688-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="95688-127">-Rezervedıpname</span><span class="sxs-lookup"><span data-stu-id="95688-127">-ReservedIPName</span></span>
<span data-ttu-id="95688-128">Ayrılmış IP adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="95688-128">Specifies the reserved IP name.</span></span>

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

### <span data-ttu-id="95688-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95688-129">CommonParameters</span></span>
<span data-ttu-id="95688-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="95688-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95688-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95688-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95688-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="95688-132">INPUTS</span></span>

## <span data-ttu-id="95688-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="95688-133">OUTPUTS</span></span>

## <span data-ttu-id="95688-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="95688-134">NOTES</span></span>

## <span data-ttu-id="95688-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="95688-135">RELATED LINKS</span></span>

[<span data-ttu-id="95688-136">New-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="95688-136">New-AzureReservedIP</span></span>](./New-AzureReservedIP.md)

[<span data-ttu-id="95688-137">Remove-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="95688-137">Remove-AzureReservedIP</span></span>](./Remove-AzureReservedIP.md)


