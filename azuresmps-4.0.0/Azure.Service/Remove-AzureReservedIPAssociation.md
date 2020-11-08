---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A6964C80-1991-46FC-84C8-5B00616386BE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9e43f841fea77626c18edbda541fa011e95faceb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106136"
---
# <span data-ttu-id="4c73a-101">Remove-AzureReservedIPAssociation</span><span class="sxs-lookup"><span data-stu-id="4c73a-101">Remove-AzureReservedIPAssociation</span></span>

## <span data-ttu-id="4c73a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c73a-102">SYNOPSIS</span></span>
<span data-ttu-id="4c73a-103">Ayrılmış IP adresindeki ilişkiyi VM veya bulut hizmetine kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4c73a-103">Removes the association from the reserved IP address to the VM or cloud service.</span></span>

## <span data-ttu-id="4c73a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4c73a-104">SYNTAX</span></span>

```
Remove-AzureReservedIPAssociation [-ReservedIPName] <String> [-ServiceName] <String>
 [[-VirtualIPName] <String>] [[-Slot] <String>] [-Force] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="4c73a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4c73a-105">DESCRIPTION</span></span>
<span data-ttu-id="4c73a-106">**Remove-AzureReservedIPAssociation** cmdlet 'i, ayrılmış IP adresini bir sanal MAKINEDEN (VM) veya bulut hizmetinden dışarı ilişkilendirir.</span><span class="sxs-lookup"><span data-stu-id="4c73a-106">The **Remove-AzureReservedIPAssociation** cmdlet disassociates a reserved IP address from a virtual machine (VM) or Cloud Service.</span></span>
<span data-ttu-id="4c73a-107">İşlem tamamlandığında, ayrılmış IP adresi ücretsizdir ve VM/VIP, Azure envanterden dinamik bir genel IP adresi alır.</span><span class="sxs-lookup"><span data-stu-id="4c73a-107">When the operation completes, the reserved IP address is free and the VM/VIP gets a dynamic public IP Address from the Azure Inventory.</span></span>

## <span data-ttu-id="4c73a-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4c73a-108">EXAMPLES</span></span>

### <span data-ttu-id="4c73a-109">Örnek 1: ayrılmış IP ilişkisini kaldırma</span><span class="sxs-lookup"><span data-stu-id="4c73a-109">Example 1: Remove a reserved IP association</span></span>
```
PS C:\> Remove-AzureReservedIPAssociation -ReservedIPName "ResIp14" -ServiceName "PipTestWestEurope"
```

<span data-ttu-id="4c73a-110">Bu komut, ResIp14 adlı ayrılmış IP adresini PipTestWestEurope adlı hizmetten kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4c73a-110">This command disassociates the reserved IP address named ResIp14 from the service named PipTestWestEurope.</span></span>
<span data-ttu-id="4c73a-111">PipTestWestEurope yeni bir dinamik VIP atanacaktır.</span><span class="sxs-lookup"><span data-stu-id="4c73a-111">PipTestWestEurope will be assigned a new dynamic VIP.</span></span>

## <span data-ttu-id="4c73a-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4c73a-112">PARAMETERS</span></span>

### <span data-ttu-id="4c73a-113">-Force</span><span class="sxs-lookup"><span data-stu-id="4c73a-113">-Force</span></span>
<span data-ttu-id="4c73a-114">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="4c73a-114">Forces the command to run without asking for user confirmation.</span></span>

<span data-ttu-id="4c73a-115">Ayrılmış IP ilişkisini kaldırırken uyarı iletilerini atlamak için bu bayrağı kullanın.</span><span class="sxs-lookup"><span data-stu-id="4c73a-115">Use this flag to bypass warning messages when removing the reserved IP association.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c73a-116">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="4c73a-116">-InformationAction</span></span>
<span data-ttu-id="4c73a-117">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c73a-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="4c73a-118">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="4c73a-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4c73a-119">'A</span><span class="sxs-lookup"><span data-stu-id="4c73a-119">Continue</span></span>
- <span data-ttu-id="4c73a-120">Manıza</span><span class="sxs-lookup"><span data-stu-id="4c73a-120">Ignore</span></span>
- <span data-ttu-id="4c73a-121">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="4c73a-121">Inquire</span></span>
- <span data-ttu-id="4c73a-122">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="4c73a-122">SilentlyContinue</span></span>
- <span data-ttu-id="4c73a-123">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="4c73a-123">Stop</span></span>
- <span data-ttu-id="4c73a-124">Biliriz</span><span class="sxs-lookup"><span data-stu-id="4c73a-124">Suspend</span></span>

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

### <span data-ttu-id="4c73a-125">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="4c73a-125">-InformationVariable</span></span>
<span data-ttu-id="4c73a-126">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c73a-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="4c73a-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="4c73a-127">-Profile</span></span>
<span data-ttu-id="4c73a-128">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c73a-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4c73a-129">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="4c73a-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4c73a-130">-Rezervedıpname</span><span class="sxs-lookup"><span data-stu-id="4c73a-130">-ReservedIPName</span></span>
<span data-ttu-id="4c73a-131">Ayrılmış IP adresinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c73a-131">Specifies the name of the reserved IP address.</span></span>

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

### <span data-ttu-id="4c73a-132">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="4c73a-132">-ServiceName</span></span>
<span data-ttu-id="4c73a-133">Hizmetin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c73a-133">Specifies the  name of the service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c73a-134">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="4c73a-134">-Slot</span></span>
<span data-ttu-id="4c73a-135">Dağıtım ortamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c73a-135">Specifies the deployment environment.</span></span>
<span data-ttu-id="4c73a-136">Bu parametre için kabul edilebilir değerler: üretim, aşamalandırma.</span><span class="sxs-lookup"><span data-stu-id="4c73a-136">The acceptable values for this parameter are: Production, Staging.</span></span>

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

### <span data-ttu-id="4c73a-137">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="4c73a-137">-VirtualIPName</span></span>
<span data-ttu-id="4c73a-138">Bir hizmet veya VM ile ilişkilendirmenin kaldırılacağı sanal IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c73a-138">Specifies a virtual IP address from which to remove the association with a service or VM.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c73a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c73a-139">CommonParameters</span></span>
<span data-ttu-id="4c73a-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4c73a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c73a-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c73a-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c73a-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4c73a-142">INPUTS</span></span>

## <span data-ttu-id="4c73a-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4c73a-143">OUTPUTS</span></span>

### <span data-ttu-id="4c73a-144">Microsoft. Windowsazme. Commands. Utilities. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="4c73a-144">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="4c73a-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4c73a-145">NOTES</span></span>

## <span data-ttu-id="4c73a-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4c73a-146">RELATED LINKS</span></span>

[<span data-ttu-id="4c73a-147">Set-AzureReservedIPAssociation</span><span class="sxs-lookup"><span data-stu-id="4c73a-147">Set-AzureReservedIPAssociation</span></span>](./Set-AzureReservedIPAssociation.md)


