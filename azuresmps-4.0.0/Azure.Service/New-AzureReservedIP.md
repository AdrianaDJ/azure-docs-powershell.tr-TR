---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9C22F5D7-1FD0-4699-83D7-1D72C5234DEF
online version: ''
schema: 2.0.0
ms.openlocfilehash: d09173c43de9c01056055f714217db5eb4c58225
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105993"
---
# <span data-ttu-id="b5707-101">New-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="b5707-101">New-AzureReservedIP</span></span>

## <span data-ttu-id="b5707-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5707-102">SYNOPSIS</span></span>
<span data-ttu-id="b5707-103">Ayrılmış bir IP adresi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b5707-103">Creates a reserved IP address.</span></span>

## <span data-ttu-id="b5707-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b5707-104">SYNTAX</span></span>

### <span data-ttu-id="b5707-105">CreateNewReservedIP (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b5707-105">CreateNewReservedIP (Default)</span></span>
```
New-AzureReservedIP [-ReservedIPName] <String> [[-Label] <String>] [-Location] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="b5707-106">CreateInUseReservedIPUsingSlot</span><span class="sxs-lookup"><span data-stu-id="b5707-106">CreateInUseReservedIPUsingSlot</span></span>
```
New-AzureReservedIP [-ReservedIPName] <String> [[-Label] <String>] [-Location] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="b5707-107">CreateInUseReservedIP</span><span class="sxs-lookup"><span data-stu-id="b5707-107">CreateInUseReservedIP</span></span>
```
New-AzureReservedIP [-ReservedIPName] <String> [[-Label] <String>] [-Location] <String> [-ServiceName] <String>
 [[-VirtualIPName] <String>] [[-Slot] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b5707-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="b5707-108">DESCRIPTION</span></span>
<span data-ttu-id="b5707-109">**New-AzureReservedIP** cmdlet 'i ayrılmış bir IP adresi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b5707-109">The **New-AzureReservedIP** cmdlet creates a reserved IP address.</span></span>

## <span data-ttu-id="b5707-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b5707-110">EXAMPLES</span></span>

### <span data-ttu-id="b5707-111">Örnek 1: yeni bir ayrılmış IP oluşturma</span><span class="sxs-lookup"><span data-stu-id="b5707-111">Example 1: Create a new reserved IP</span></span>
```
PS C:\> New-AzureReservedIP -ReservedIPName $Name -Label $Label -Location $Location
```

<span data-ttu-id="b5707-112">Bu komut, abonelikte, Web, çalışan ve sanal makineleri içeren bulut hizmetleri oluşturmak için kullanılabilen yeni bir ayrılmış IP adresi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b5707-112">This command creates a new reserved IP address in the subscription, which can be used for creating cloud services that include Web, Worker, and Virtual Machines.</span></span>

### <span data-ttu-id="b5707-113">Örnek 2: var olan bir IP 'ye dayalı olarak ayrılmış bir IP oluşturma</span><span class="sxs-lookup"><span data-stu-id="b5707-113">Example 2: Create a reserved IP based on an existing IP</span></span>
```
PS C:\> New-AzureReservedIP -ReservedIPName resip14 -Location "West Europe" -ServiceName piptestwesteurope
```

<span data-ttu-id="b5707-114">Bu komut belirtilen hizmette mevcut bir VIP (sanal IP) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b5707-114">This command creates an existing VIP (Virtual IP) on the specified service.</span></span>

## <span data-ttu-id="b5707-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b5707-115">PARAMETERS</span></span>

### <span data-ttu-id="b5707-116">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="b5707-116">-InformationAction</span></span>
<span data-ttu-id="b5707-117">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5707-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b5707-118">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="b5707-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b5707-119">'A</span><span class="sxs-lookup"><span data-stu-id="b5707-119">Continue</span></span>
- <span data-ttu-id="b5707-120">Manıza</span><span class="sxs-lookup"><span data-stu-id="b5707-120">Ignore</span></span>
- <span data-ttu-id="b5707-121">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="b5707-121">Inquire</span></span>
- <span data-ttu-id="b5707-122">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="b5707-122">SilentlyContinue</span></span>
- <span data-ttu-id="b5707-123">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="b5707-123">Stop</span></span>
- <span data-ttu-id="b5707-124">Biliriz</span><span class="sxs-lookup"><span data-stu-id="b5707-124">Suspend</span></span>

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

### <span data-ttu-id="b5707-125">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="b5707-125">-InformationVariable</span></span>
<span data-ttu-id="b5707-126">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5707-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b5707-127">Etiketli</span><span class="sxs-lookup"><span data-stu-id="b5707-127">-Label</span></span>
<span data-ttu-id="b5707-128">Ayrılmış IP adresi için bir etiket belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5707-128">Specifies a label for the reserved IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5707-129">-Konum</span><span class="sxs-lookup"><span data-stu-id="b5707-129">-Location</span></span>
<span data-ttu-id="b5707-130">Ayrılmış IP adresinin oluşturulacağı konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5707-130">Specifies a location at which to create the reserved IP address.</span></span>

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

### <span data-ttu-id="b5707-131">-Profil</span><span class="sxs-lookup"><span data-stu-id="b5707-131">-Profile</span></span>
<span data-ttu-id="b5707-132">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5707-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b5707-133">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="b5707-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b5707-134">-Rezervedıpname</span><span class="sxs-lookup"><span data-stu-id="b5707-134">-ReservedIPName</span></span>
<span data-ttu-id="b5707-135">Ayrılmış IP adresi adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5707-135">Specifies the reserved IP address name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5707-136">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="b5707-136">-ServiceName</span></span>
<span data-ttu-id="b5707-137">Hizmet adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5707-137">Specifies a service name.</span></span>

```yaml
Type: String
Parameter Sets: CreateInUseReservedIP
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5707-138">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="b5707-138">-Slot</span></span>
<span data-ttu-id="b5707-139">Dağıtım yuvasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5707-139">Specifies the deployment slot.</span></span>
<span data-ttu-id="b5707-140">Bu parametre için kabul edilebilir değerler: hazırlama, üretim.</span><span class="sxs-lookup"><span data-stu-id="b5707-140">The acceptable values for this parameter are: Staging, Production.</span></span>

```yaml
Type: String
Parameter Sets: CreateInUseReservedIP
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5707-141">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="b5707-141">-VirtualIPName</span></span>
<span data-ttu-id="b5707-142">Bu cmdlet 'in dağıtımınızdaki mevcut bir sanal IP adresini (VIP) ayırmada **Sanalıpname** parametresini kullanacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5707-142">Specifies that this cmdlet uses the **VirtualIPName** parameter to reserve an existing virtual IP address (VIP) in your deployment.</span></span>
<span data-ttu-id="b5707-143">Bu parametre belirtilmezse, bu cmdlet yeni bir VIP ayırır.</span><span class="sxs-lookup"><span data-stu-id="b5707-143">If this parameter is not specified, this cmdlet reserves a new VIP.</span></span>

```yaml
Type: String
Parameter Sets: CreateInUseReservedIP
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5707-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5707-144">CommonParameters</span></span>
<span data-ttu-id="b5707-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b5707-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5707-146">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5707-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5707-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b5707-147">INPUTS</span></span>

## <span data-ttu-id="b5707-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b5707-148">OUTPUTS</span></span>

## <span data-ttu-id="b5707-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b5707-149">NOTES</span></span>

## <span data-ttu-id="b5707-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b5707-150">RELATED LINKS</span></span>

[<span data-ttu-id="b5707-151">Get-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="b5707-151">Get-AzureReservedIP</span></span>](./Get-AzureReservedIP.md)

[<span data-ttu-id="b5707-152">Remove-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="b5707-152">Remove-AzureReservedIP</span></span>](./Remove-AzureReservedIP.md)


