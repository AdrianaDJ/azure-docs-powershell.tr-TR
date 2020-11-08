---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 3249E908-B1D9-4707-844D-168274F1A466
online version: ''
schema: 2.0.0
ms.openlocfilehash: ae16609adf70b2e5a0edcd05c36b30860a3920cf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105825"
---
# <span data-ttu-id="bac45-101">Set-AzureReservedIPAssociation</span><span class="sxs-lookup"><span data-stu-id="bac45-101">Set-AzureReservedIPAssociation</span></span>

## <span data-ttu-id="bac45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bac45-102">SYNOPSIS</span></span>
<span data-ttu-id="bac45-103">Ayrılmış bir IP adresini mevcut bir sanal makineyle veya bulut hizmetiyle ilişkilendirir.</span><span class="sxs-lookup"><span data-stu-id="bac45-103">Associates a reserved IP address with an existing virtual machine or cloud service.</span></span>

## <span data-ttu-id="bac45-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bac45-104">SYNTAX</span></span>

```
Set-AzureReservedIPAssociation [-ReservedIPName] <String> [-ServiceName] <String> [[-VirtualIPName] <String>]
 [[-Slot] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="bac45-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bac45-105">DESCRIPTION</span></span>
<span data-ttu-id="bac45-106">**Set-AzureReservedIPAssociation** cmdlet 'i, ayrılmış bir IP adresini çalışan bir sanal makinenin veya bulut HIZMETININ sanal IP ADRESIYLE (VIP) ilişkilendirir.</span><span class="sxs-lookup"><span data-stu-id="bac45-106">The **Set-AzureReservedIPAssociation** cmdlet associates a reserved IP address with the Virtual IP address (VIP) of a running virtual machine or cloud service.</span></span>
<span data-ttu-id="bac45-107">Ayrılmış IP adresi bu cmdlet 'in başlatılması sırasında kullanımda olmamalıdır ve sanal makine veya bulut hizmetiyle aynı bölgede olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="bac45-107">The reserved IP address must not be in use at the time of invocation of this cmdlet, and must be in the same region as the virtual machine or cloud service.</span></span>

<span data-ttu-id="bac45-108">İşlemin tamamlanması yaklaşık 30 saniye sürer ve bu da ayrılmış IP adresi kullanılarak sanal makine veya hizmetin erişilebilir olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="bac45-108">The operation takes about 30 seconds to complete, after which the virtual machine or service is accessible using the reserved IP address.</span></span>

## <span data-ttu-id="bac45-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bac45-109">EXAMPLES</span></span>

### <span data-ttu-id="bac45-110">Örnek 1: ayrılmış IP ilişkilendirmesi ayarlama</span><span class="sxs-lookup"><span data-stu-id="bac45-110">Example 1: Set a reserved IP association</span></span>
```
PS C:\> Set-AzureReservedIPAssociation -ReservedIPName "ResIp14" -ServiceName "PipTestWestEurope"
```

<span data-ttu-id="bac45-111">Bu komut, ResIp14 adlı ayrılmış IP adresini hizmet PipTestWestEurope olarak atar.</span><span class="sxs-lookup"><span data-stu-id="bac45-111">This command assigns the reserved IP address named ResIp14 to the service PipTestWestEurope.</span></span>
<span data-ttu-id="bac45-112">ResIp14, Batı Avrupa bölgesinde ayrılmış bir IP.</span><span class="sxs-lookup"><span data-stu-id="bac45-112">ResIp14 is a reserved IP in the West Europe region.</span></span>

## <span data-ttu-id="bac45-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bac45-113">PARAMETERS</span></span>

### <span data-ttu-id="bac45-114">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="bac45-114">-InformationAction</span></span>
<span data-ttu-id="bac45-115">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bac45-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="bac45-116">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="bac45-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bac45-117">'A</span><span class="sxs-lookup"><span data-stu-id="bac45-117">Continue</span></span>
- <span data-ttu-id="bac45-118">Manıza</span><span class="sxs-lookup"><span data-stu-id="bac45-118">Ignore</span></span>
- <span data-ttu-id="bac45-119">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="bac45-119">Inquire</span></span>
- <span data-ttu-id="bac45-120">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="bac45-120">SilentlyContinue</span></span>
- <span data-ttu-id="bac45-121">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="bac45-121">Stop</span></span>
- <span data-ttu-id="bac45-122">Biliriz</span><span class="sxs-lookup"><span data-stu-id="bac45-122">Suspend</span></span>

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

### <span data-ttu-id="bac45-123">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="bac45-123">-InformationVariable</span></span>
<span data-ttu-id="bac45-124">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="bac45-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="bac45-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="bac45-125">-Profile</span></span>
<span data-ttu-id="bac45-126">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bac45-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="bac45-127">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="bac45-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bac45-128">-Rezervedıpname</span><span class="sxs-lookup"><span data-stu-id="bac45-128">-ReservedIPName</span></span>
<span data-ttu-id="bac45-129">Sanal makine veya hizmetle ilişkilendirilecek ayrılmış IP adresinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bac45-129">Specifies the name of the reserved IP address to associate with a virtual machine or service.</span></span>

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

### <span data-ttu-id="bac45-130">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="bac45-130">-ServiceName</span></span>
<span data-ttu-id="bac45-131">Ayrılmış IP adresiyle ilişkilendirilecek dağıtımın bulunduğu hizmetin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bac45-131">Specifies the name of the service that has the deployment with which to associate the reserved IP address.</span></span>

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

### <span data-ttu-id="bac45-132">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="bac45-132">-Slot</span></span>
<span data-ttu-id="bac45-133">Dağıtım yuvasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bac45-133">Specifies the deployment slot.</span></span>
<span data-ttu-id="bac45-134">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="bac45-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bac45-135">Geçici saklama</span><span class="sxs-lookup"><span data-stu-id="bac45-135">Staging</span></span>
- <span data-ttu-id="bac45-136">Üretim</span><span class="sxs-lookup"><span data-stu-id="bac45-136">Production</span></span>

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

### <span data-ttu-id="bac45-137">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="bac45-137">-VirtualIPName</span></span>
<span data-ttu-id="bac45-138">Ayrılmış bir IP ile ilişkilendirilecek mevcut bir VIP 'in adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bac45-138">Specifies the name of an existing VIP to associate with a reserved IP.</span></span>
<span data-ttu-id="bac45-139">Bulut hizmetinize VIP eklemek için Add-AzureVirtualIP bakın.</span><span class="sxs-lookup"><span data-stu-id="bac45-139">See Add-AzureVirtualIP to add VIPs to your cloud service.</span></span>

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

### <span data-ttu-id="bac45-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bac45-140">CommonParameters</span></span>
<span data-ttu-id="bac45-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bac45-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bac45-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bac45-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bac45-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bac45-143">INPUTS</span></span>

## <span data-ttu-id="bac45-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bac45-144">OUTPUTS</span></span>

### <span data-ttu-id="bac45-145">Microsoft. Windowsazme. Commands. Utilities. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="bac45-145">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="bac45-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bac45-146">NOTES</span></span>

## <span data-ttu-id="bac45-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bac45-147">RELATED LINKS</span></span>

[<span data-ttu-id="bac45-148">Remove-AzureReservedIPAssociation</span><span class="sxs-lookup"><span data-stu-id="bac45-148">Remove-AzureReservedIPAssociation</span></span>](./Remove-AzureReservedIPAssociation.md)


